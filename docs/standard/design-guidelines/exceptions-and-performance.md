---
title: 예외 및 성능
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- tester-doer pattern
- TryParse pattern
- exceptions, throwing
- exceptions, performance
- throwing exceptions, performance
ms.assetid: 3ad6aad9-08e6-4232-b336-0e301f2493e6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d664b7b61394bd9bfe6d0abd7130f9f0191e7a03
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083548"
---
# <a name="exceptions-and-performance"></a><span data-ttu-id="823bb-102">예외 및 성능</span><span class="sxs-lookup"><span data-stu-id="823bb-102">Exceptions and Performance</span></span>
<span data-ttu-id="823bb-103">예외와 관련 된 한 가지 일반적인 문제는 예외를 지속적으로 실패 하는 코드를 사용 하는 경우 구현의 성능은 허용 되지 경우</span><span class="sxs-lookup"><span data-stu-id="823bb-103">One common concern related to exceptions is that if exceptions are used for code that routinely fails, the performance of the implementation will be unacceptable.</span></span> <span data-ttu-id="823bb-104">이 맞는 말입니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-104">This is a valid concern.</span></span> <span data-ttu-id="823bb-105">멤버에서 예외를 throw 하는 경우 해당 성능이 크기가 커져 느린 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-105">When a member throws an exception, its performance can be orders of magnitude slower.</span></span> <span data-ttu-id="823bb-106">그러나 오류 코드를 사용 하 여 허용 하지 않는 예외 지침을 준수할 엄격 하 게 하는 동안 적절 한 성능을 달성 하는 것이 같습니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-106">However, it is possible to achieve good performance while strictly adhering to the exception guidelines that disallow using error codes.</span></span> <span data-ttu-id="823bb-107">이 섹션에서 설명 하는 두 가지 패턴에는이 작업을 수행 하는 방법을 제안 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-107">Two patterns described in this section suggest ways to do this.</span></span>  
  
 <span data-ttu-id="823bb-108">**X DO NOT** 있는지 예외 영향을 줄 수 성능 저하 문제 때문에 오류 코드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-108">**X DO NOT** use error codes because of concerns that exceptions might affect performance negatively.</span></span>  
  
 <span data-ttu-id="823bb-109">성능 향상을 위해 Tester-doer 패턴 또는 다음 두 섹션에 설명 된 구문 분석 시도 패턴을 사용 하는 것이 같습니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-109">To improve performance, it is possible to use either the Tester-Doer Pattern or the Try-Parse Pattern, described in the next two sections.</span></span>  
  
## <a name="tester-doer-pattern"></a><span data-ttu-id="823bb-110">Tester-doer 패턴</span><span class="sxs-lookup"><span data-stu-id="823bb-110">Tester-Doer Pattern</span></span>  
 <span data-ttu-id="823bb-111">경우에 따라 성능 예외를 throw 할 멤버의 멤버를 두 개로 분할 하 여 개선할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-111">Sometimes performance of an exception-throwing member can be improved by breaking the member into two.</span></span> <span data-ttu-id="823bb-112">살펴보겠습니다 합니다 <xref:System.Collections.Generic.ICollection%601.Add%2A> 메서드는 <xref:System.Collections.Generic.ICollection%601> 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-112">Let’s look at the <xref:System.Collections.Generic.ICollection%601.Add%2A> method of the <xref:System.Collections.Generic.ICollection%601> interface.</span></span>  
  
```  
ICollection<int> numbers = ...   
numbers.Add(1);  
```  
  
 <span data-ttu-id="823bb-113">메서드가 `Add` 컬렉션이 읽기 전용 이면 throw 됩니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-113">The method `Add` throws if the collection is read-only.</span></span> <span data-ttu-id="823bb-114">이 종종 실패 메서드 호출이 필요한 시나리오에서 성능 문제를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-114">This can be a performance problem in scenarios where the method call is expected to fail often.</span></span> <span data-ttu-id="823bb-115">문제를 완화 하는 방법 중 하나는 값을 추가 하기 전에 컬렉션에 쓸 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-115">One of the ways to mitigate the problem is to test whether the collection is writable before trying to add a value.</span></span>  
  
```  
ICollection<int> numbers = ...   
...  
if(!numbers.IsReadOnly){  
    numbers.Add(1);  
}  
```  
  
 <span data-ttu-id="823bb-116">예에서 속성인는 조건을 테스트 하는 데 사용 하는 멤버 `IsReadOnly`, 테스터가 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-116">The member used to test a condition, which in our example is the property `IsReadOnly`, is referred to as the tester.</span></span> <span data-ttu-id="823bb-117">잠재적으로 throwing 작업을 수행 하는 데 사용 된 멤버는 `Add` 예제의 메서드를 벗어났을 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-117">The member used to perform a potentially throwing operation, the `Add` method in our example, is referred to as the doer.</span></span>  
  
 <span data-ttu-id="823bb-118">**✓ CONSIDER** Tester-doer 패턴 예외를 throw 할 수 있는 멤버에 대 한 공통 성능 문제를 방지 하는 시나리오와 관련 된 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-118">**✓ CONSIDER** the Tester-Doer Pattern for members that might throw exceptions in common scenarios to avoid performance problems related to exceptions.</span></span>  
  
## <a name="try-parse-pattern"></a><span data-ttu-id="823bb-119">구문 분석 시도 패턴</span><span class="sxs-lookup"><span data-stu-id="823bb-119">Try-Parse Pattern</span></span>  
 <span data-ttu-id="823bb-120">성능이 매우 중요 한 Api에 대 한 이전 섹션에서 설명한 Tester-doer 패턴 보다는 훨씬 빠른 패턴을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-120">For extremely performance-sensitive APIs, an even faster pattern than the Tester-Doer Pattern described in the previous section should be used.</span></span> <span data-ttu-id="823bb-121">멤버 의미 체계의 일부 경우 잘 정의 된 테스트 하기 위해 멤버 이름의 조정에 대 한 패턴을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-121">The pattern calls for adjusting the member name to make a well-defined test case a part of the member semantics.</span></span> <span data-ttu-id="823bb-122">예를 들어 <xref:System.DateTime> 정의 <xref:System.DateTime.Parse%2A> 문자열의 구문 분석 하지 못하면 예외가 throw 되는 메서드.</span><span class="sxs-lookup"><span data-stu-id="823bb-122">For example, <xref:System.DateTime> defines a <xref:System.DateTime.Parse%2A> method that throws an exception if parsing of a string fails.</span></span> <span data-ttu-id="823bb-123">또한 해당 정의 <xref:System.DateTime.TryParse%2A> 메서드를 구문 분석 하려고 하지만 false를 반환 합니다 구문 분석 실패 하 고 사용 하 여 성공적으로 구문 분석 결과 반환 하는 경우는 `out` 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-123">It also defines a corresponding <xref:System.DateTime.TryParse%2A> method that attempts to parse, but returns false if parsing is unsuccessful and returns the result of a successful parsing using an `out` parameter.</span></span>  
  
```  
public struct DateTime {  
    public static DateTime Parse(string dateTime){   
        ...   
    }  
    public static bool TryParse(string dateTime, out DateTime result){  
        ...  
    }  
}  
```  
  
 <span data-ttu-id="823bb-124">이 패턴을 사용 하는 경우에 엄격한 용어로 시도 기능을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-124">When using this pattern, it is important to define the try functionality in strict terms.</span></span> <span data-ttu-id="823bb-125">잘 정의 된 try 이외의 어떤 이유로 든 실패 하면 멤버 멤버는 해당 하는 예외가 계속 throw 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-125">If the member fails for any reason other than the well-defined try, the member must still throw a corresponding exception.</span></span>  
  
 <span data-ttu-id="823bb-126">**✓ CONSIDER** Try 구문 분석 패턴 예외를 throw 할 수 있는 멤버에 대 한 공통 성능 문제를 방지 하는 시나리오와 관련 된 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-126">**✓ CONSIDER** the Try-Parse Pattern for members that might throw exceptions in common scenarios to avoid performance problems related to exceptions.</span></span>  
  
 <span data-ttu-id="823bb-127">**✓ DO** 이 패턴을 구현 하는 방법에 대 한 접두사 "Try" 및 Boolean 반환 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-127">**✓ DO** use the prefix "Try" and Boolean return type for methods implementing this pattern.</span></span>  
  
 <span data-ttu-id="823bb-128">**✓ DO** Try 구문 분석 패턴을 사용 하 여 각 멤버에 대 한 예외 throw 멤버를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="823bb-128">**✓ DO** provide an exception-throwing member for each member using the Try-Parse Pattern.</span></span>  
  
 <span data-ttu-id="823bb-129">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="823bb-129">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="823bb-130">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="823bb-130">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="823bb-131">참고자료</span><span class="sxs-lookup"><span data-stu-id="823bb-131">See also</span></span>

- [<span data-ttu-id="823bb-132">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="823bb-132">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="823bb-133">예외 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="823bb-133">Design Guidelines for Exceptions</span></span>](../../../docs/standard/design-guidelines/exceptions.md)
