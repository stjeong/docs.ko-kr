---
title: 같음 연산자
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], Equals method
- class library design guidelines [.NET Framework], equality operator
- equality operator (==) [.NET Framework]
- Equals method
- == operator (equality) [.NET Framework]
ms.assetid: bc496a91-fefb-4ce0-ab4c-61f09964119a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27550a8fd8292029cad9c2e699374a190b1a532e
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45521390"
---
# <a name="equality-operators"></a><span data-ttu-id="01ffa-102">같음 연산자</span><span class="sxs-lookup"><span data-stu-id="01ffa-102">Equality Operators</span></span>
<span data-ttu-id="01ffa-103">이 섹션에서는 같음 연산자를 오버 로드에 대해 설명 하 고 가리킵니다 `operator==` 고 `operator!=` 같음 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-103">This section discusses overloading equality operators and refers to `operator==` and `operator!=` as equality operators.</span></span>  
  
 <span data-ttu-id="01ffa-104">**X DO NOT** 같음 연산자 있고 다른 선언 중 하나를 오버 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-104">**X DO NOT** overload one of the equality operators and not the other.</span></span>  
  
 <span data-ttu-id="01ffa-105">**✓ DO** 되도록 <xref:System.Object.Equals%2A?displayProperty=nameWithType> 및 같음 연산자는 정확히 동일한 의미 체계와 비슷한 성능 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-105">**✓ DO** ensure that <xref:System.Object.Equals%2A?displayProperty=nameWithType> and the equality operators have exactly the same semantics and similar performance characteristics.</span></span>  
  
 <span data-ttu-id="01ffa-106">자주 따라서 `Object.Equals` 같음 연산자를 오버 로드 하는 경우 재정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-106">This often means that `Object.Equals` needs to be overridden when the equality operators are overloaded.</span></span>  
  
 <span data-ttu-id="01ffa-107">**X AVOID** 같음 연산자에서 예외를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-107">**X AVOID** throwing exceptions from equality operators.</span></span>  
  
 <span data-ttu-id="01ffa-108">예를 들어 인수 중 하나를 throw 하지 않고 null 이면 false를 반환 `NullReferenceException`합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-108">For example, return false if one of the arguments is null instead of throwing `NullReferenceException`.</span></span>  
  
## <a name="equality-operators-on-value-types"></a><span data-ttu-id="01ffa-109">값 형식에 같음 연산자</span><span class="sxs-lookup"><span data-stu-id="01ffa-109">Equality Operators on Value Types</span></span>  
 <span data-ttu-id="01ffa-110">**✓ DO** 같음이 의미가 있을 경우에 값 형식에 같음 연산자를 오버 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-110">**✓ DO** overload the equality operators on value types, if equality is meaningful.</span></span>  
  
 <span data-ttu-id="01ffa-111">대부분의 프로그래밍 언어에서은의 기본 구현이 없는 `operator==` 값 형식에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-111">In most programming languages, there is no default implementation of `operator==` for value types.</span></span>  
  
## <a name="equality-operators-on-reference-types"></a><span data-ttu-id="01ffa-112">참조 형식에 같음 연산자</span><span class="sxs-lookup"><span data-stu-id="01ffa-112">Equality Operators on Reference Types</span></span>  
 <span data-ttu-id="01ffa-113">**X AVOID** 변경 가능한 참조 형식에 같음 연산자를 오버 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-113">**X AVOID** overloading equality operators on mutable reference types.</span></span>  
  
 <span data-ttu-id="01ffa-114">다양 한 언어 참조 형식에 대 한 기본 같음 연산자가 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="01ffa-114">Many languages have built-in equality operators for reference types.</span></span> <span data-ttu-id="01ffa-115">기본 제공 연산자에는 일반적으로 참조 같음 구현 하 고 값이 같은지를 기본 동작이 변경 될 때 많은 개발자가 알고 계십니까 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-115">The built-in operators usually implement the reference equality, and many developers are surprised when the default behavior is changed to the value equality.</span></span>  
  
 <span data-ttu-id="01ffa-116">이 문제는 불변성을 사용 하면 값이 같은지 참조 같음 사이의 차이점을 확인 하기가 훨씬 변경할 수 없는 참조 형식에 대 한 완화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-116">This problem is mitigated for immutable reference types because immutability makes it much harder to notice the difference between reference equality and value equality.</span></span>  
  
 <span data-ttu-id="01ffa-117">**X AVOID** 참조 일치 하는 것 보다 크게 느려지지 구현 되는 경우에 참조 형식에 같음 연산자를 오버 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffa-117">**X AVOID** overloading equality operators on reference types if the implementation would be significantly slower than that of reference equality.</span></span>  
  
 <span data-ttu-id="01ffa-118">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="01ffa-118">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="01ffa-119">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="01ffa-119">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01ffa-120">참고자료</span><span class="sxs-lookup"><span data-stu-id="01ffa-120">See also</span></span>

- [<span data-ttu-id="01ffa-121">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="01ffa-121">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="01ffa-122">사용 지침</span><span class="sxs-lookup"><span data-stu-id="01ffa-122">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)
