---
title: 형식 디자인 지침
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7fb9964d0e542c0937c55ae65bd88b3f7149fa8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44187941"
---
# <a name="type-design-guidelines"></a><span data-ttu-id="56f19-102">형식 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="56f19-102">Type Design Guidelines</span></span>
<span data-ttu-id="56f19-103">CLR 관점에서 보면는 두 가지 범주의 형식-참조 형식과 값 형식-있지만 프레임 워크 디자인에 대 한 토론을 하기 위해 고유한 특정 디자인 규칙을 사용 하 여 각 논리적인 그룹으로 형식 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-103">From the CLR perspective, there are only two categories of types—reference types and value types—but for the purpose of a discussion about framework design, we divide types into more logical groups, each with its own specific design rules.</span></span>  
  
 <span data-ttu-id="56f19-104">클래스는 참조 형식의 일반적인 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-104">Classes are the general case of reference types.</span></span> <span data-ttu-id="56f19-105">이러한 대부분의 프레임 워크에서 형식의 대량 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-105">They make up the bulk of types in the majority of frameworks.</span></span> <span data-ttu-id="56f19-106">클래스 일반 적용 가능성을 다양 한 지 원하는 개체 지향 기능 집합을 해당 인기도 미납 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-106">Classes owe their popularity to the rich set of object-oriented features they support and to their general applicability.</span></span> <span data-ttu-id="56f19-107">기본 클래스가 추상 클래스와 확장성 관련 된 특별 한 논리 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-107">Base classes and abstract classes are special logical groups related to extensibility.</span></span>  
  
 <span data-ttu-id="56f19-108">인터페이스는 형식을 구현할 수 있는 참조 형식과 값 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-108">Interfaces are types that can be implemented by both reference types and value types.</span></span> <span data-ttu-id="56f19-109">따라서 참조 형식과 값 형식의 다형 계층의 루트로 사용 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-109">They can thus serve as roots of polymorphic hierarchies of reference types and value types.</span></span> <span data-ttu-id="56f19-110">또한 기본적으로 CLR에서 지원 되지 않는 여러 상속을 시뮬레이트하려 인터페이스를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-110">In addition, interfaces can be used to simulate multiple inheritance, which is not natively supported by the CLR.</span></span>  
  
 <span data-ttu-id="56f19-111">구조체 값 형식의 일반적인 경우는 및 언어 기본 형식에 유사한 간단한 형식에 대 한 예약 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-111">Structs are the general case of value types and should be reserved for small, simple types, similar to language primitives.</span></span>  
  
 <span data-ttu-id="56f19-112">열거형은 특수 한 일의 주, 콘솔 색 등과 같은 값의 간단한 집합을 정의 하는 데 사용 되는 값 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-112">Enums are a special case of value types used to define short sets of values, such as days of the week, console colors, and so on.</span></span>  
  
 <span data-ttu-id="56f19-113">정적 클래스는 정적 멤버에 대 한 컨테이너를 사용 하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-113">Static classes are types intended to be containers for static members.</span></span> <span data-ttu-id="56f19-114">일반적으로 다른 작업에 대 한 바로 가기를 제공에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-114">They are commonly used to provide shortcuts to other operations.</span></span>  
  
 <span data-ttu-id="56f19-115">대리자, 예외, 특성, 배열 및 컬렉션은 특정 용도 위한 참조 형식의 모든 특별 한 경우 및 해당 디자인 및 사용에 대 한 지침은이 가이드의 다른 곳에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-115">Delegates, exceptions, attributes, arrays, and collections are all special cases of reference types intended for specific uses, and guidelines for their design and usage are discussed elsewhere in this book.</span></span>  
  
 <span data-ttu-id="56f19-116">**✓ DO** 각 형식이 관련 되지 않은 기능의 임의 컬렉션 뿐 아니라 관련된 멤버의 잘 정의 된 집합 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f19-116">**✓ DO** ensure that each type is a well-defined set of related members, not just a random collection of unrelated functionality.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="56f19-117">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="56f19-117">In This Section</span></span>  
 [<span data-ttu-id="56f19-118">클래스와 구조체 간의 선택</span><span class="sxs-lookup"><span data-stu-id="56f19-118">Choosing Between Class and Struct</span></span>](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)  
 [<span data-ttu-id="56f19-119">추상 클래스 디자인</span><span class="sxs-lookup"><span data-stu-id="56f19-119">Abstract Class Design</span></span>](../../../docs/standard/design-guidelines/abstract-class.md)  
 [<span data-ttu-id="56f19-120">정적 클래스 디자인</span><span class="sxs-lookup"><span data-stu-id="56f19-120">Static Class Design</span></span>](../../../docs/standard/design-guidelines/static-class.md)  
 [<span data-ttu-id="56f19-121">인터페이스 디자인</span><span class="sxs-lookup"><span data-stu-id="56f19-121">Interface Design</span></span>](../../../docs/standard/design-guidelines/interface.md)  
 [<span data-ttu-id="56f19-122">구조체 디자인</span><span class="sxs-lookup"><span data-stu-id="56f19-122">Struct Design</span></span>](../../../docs/standard/design-guidelines/struct.md)  
 [<span data-ttu-id="56f19-123">열거형 디자인</span><span class="sxs-lookup"><span data-stu-id="56f19-123">Enum Design</span></span>](../../../docs/standard/design-guidelines/enum.md)  
 [<span data-ttu-id="56f19-124">중첩 형식</span><span class="sxs-lookup"><span data-stu-id="56f19-124">Nested Types</span></span>](../../../docs/standard/design-guidelines/nested-types.md)  
 <span data-ttu-id="56f19-125">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="56f19-125">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="56f19-126">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="56f19-126">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56f19-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="56f19-127">See also</span></span>

- [<span data-ttu-id="56f19-128">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="56f19-128">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
