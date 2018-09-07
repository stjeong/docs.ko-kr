---
title: 클래스와 구조체 간의 선택
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- class library design guidelines [.NET Framework], classes
- structures [.NET Framework], vs. classes
- classes [.NET Framework], design guidelines
- type design guidelines, structures
- structures [.NET Framework], design guidelines
- classes [.NET Framework], vs. structures
- type design guidelines, classes
ms.assetid: f8b8ec9b-0ba7-4dea-aadf-a93395cd804f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06661cb2c34d1da9085fa2129cb0c3307b99097e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43865555"
---
# <a name="choosing-between-class-and-struct"></a><span data-ttu-id="0e7b5-102">클래스와 구조체 간의 선택</span><span class="sxs-lookup"><span data-stu-id="0e7b5-102">Choosing Between Class and Struct</span></span>
<span data-ttu-id="0e7b5-103">모든 프레임 워크 디자이너 얼굴 기본 디자인 결정 사항 중 하나 (참조 형식) 클래스 또는 구조체 (값 형식) 형식이 디자인 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-103">One of the basic design decisions every framework designer faces is whether to design a type as a class (a reference type) or as a struct (a value type).</span></span> <span data-ttu-id="0e7b5-104">값 형식과 참조 동작의 차이점 이해 하는 것은이 선택 하는 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-104">Good understanding of the differences in the behavior of reference types and value types is crucial in making this choice.</span></span>  
  
 <span data-ttu-id="0e7b5-105">첫 번째 스택의 반면 스택에 하거나 값 형식 할당 된 또는 포함 하는 인라인 형식 및 할당 취소 될 때 참조 형식 힙에 할당 되 고 가비지가 수집은 생각 값 형식과 참조 형식 간의 차이점 해제 또는 포함 하는 형식 가져옵니다 할당 취소 된 경우.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-105">The first difference between reference types and value types we will consider is that reference types are allocated on the heap and garbage-collected, whereas value types are allocated either on the stack or inline in containing types and deallocated when the stack unwinds or when their containing type gets deallocated.</span></span> <span data-ttu-id="0e7b5-106">따라서 할당 및 할당 취소 값 형식의 일반 할당 및 할당 취소 참조 형식의 보다 저렴 한에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-106">Therefore, allocations and deallocations of value types are in general cheaper than allocations and deallocations of reference types.</span></span>  
  
 <span data-ttu-id="0e7b5-107">다음으로, 형식은 참조의 배열 힙에 있는 참조 형식의 인스턴스에 대 한만 참조 아웃 아웃오브 라인, 배열 요소를 의미를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-107">Next, arrays of reference types are allocated out-of-line, meaning the array elements are just references to instances of the reference type residing on the heap.</span></span> <span data-ttu-id="0e7b5-108">값 형식 배열의 배열 요소 값 형식의 실제 인스턴스 즉 인라인으로 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-108">Value type arrays are allocated inline, meaning that the array elements are the actual instances of the value type.</span></span> <span data-ttu-id="0e7b5-109">따라서, 할당 및 할당 취소 값 형식 배열의 할당 및 할당 취소는 참조 형식 배열 보다 훨씬 저렴 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-109">Therefore, allocations and deallocations of value type arrays are much cheaper than allocations and deallocations of reference type arrays.</span></span> <span data-ttu-id="0e7b5-110">또한은 대부분의 경우 값 형식 배열 참조의 효율이 훨씬을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-110">In addition, in a majority of cases value type arrays exhibit much better locality of reference.</span></span>  
  
 <span data-ttu-id="0e7b5-111">다음 차이점 메모리 사용량 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-111">The next difference is related to memory usage.</span></span> <span data-ttu-id="0e7b5-112">값 형식은 참조 형식 또는 구현 하는 인터페이스 중 하나를 변환할 때는 boxed 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-112">Value types get boxed when cast to a reference type or one of the interfaces they implement.</span></span> <span data-ttu-id="0e7b5-113">Unboxed 받게 경우 값 형식으로 다시 캐스팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-113">They get unboxed when cast back to the value type.</span></span> <span data-ttu-id="0e7b5-114">상자 개체 힙에 할당 되는 가비지 수집, 너무 boxing 및 unboxing 되는 힙, 가비지 수집기 및 궁극적으로 응용 프로그램의 성능에 부정적인 영향을 줄을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-114">Because boxes are objects that are allocated on the heap and are garbage-collected, too much boxing and unboxing can have a negative impact on the heap, the garbage collector, and ultimately the performance of the application.</span></span>  <span data-ttu-id="0e7b5-115">반면, 참조 형식 캐스팅 하는 이러한 boxing 되지 않습니다 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-115">In contrast, no such boxing occurs as reference types are cast.</span></span>  
  
 <span data-ttu-id="0e7b5-116">다음으로, 참조 형식 할당 값 형식 할당 전체 값을 복사 하는 반면 참조를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-116">Next, reference type assignments copy the reference, whereas value type assignments copy the entire value.</span></span> <span data-ttu-id="0e7b5-117">따라서 큰 참조 형식의 할당은 큰 값 형식 할당 보다 저렴 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-117">Therefore, assignments of large reference types are cheaper than assignments of large value types.</span></span>  
  
 <span data-ttu-id="0e7b5-118">마지막으로, 참조 형식은 값 형식이 값으로 전달 되는 반면 참조로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-118">Finally, reference types are passed by reference, whereas value types are passed by value.</span></span> <span data-ttu-id="0e7b5-119">참조 형식의 인스턴스에 대 한 변경 내용을 인스턴스를 가리키는 모든 참조를 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-119">Changes to an instance of a reference type affect all references pointing to the instance.</span></span> <span data-ttu-id="0e7b5-120">값 형식 인스턴스 값으로 전달 될 때 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-120">Value type instances are copied when they are passed by value.</span></span> <span data-ttu-id="0e7b5-121">값 형식 인스턴스의 변경 되 면 물론 바뀌지 않습니다 복사본 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-121">When an instance of a value type is changed, it of course does not affect any of its copies.</span></span> <span data-ttu-id="0e7b5-122">복사본을 사용자에 의해 명시적으로 생성 하지는 인수는 전달 또는 반환 값이 반환 됩니다 때 암시적으로 만들어지는 하지만 때문에 값 형식을 변경할 수 있는 많은 사용자에 게 혼동을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-122">Because the copies are not created explicitly by the user but are implicitly created when arguments are passed or return values are returned, value types that can be changed can be confusing to many users.</span></span> <span data-ttu-id="0e7b5-123">따라서 값 형식을 변경할 수 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-123">Therefore, value types should be immutable.</span></span>  
  
 <span data-ttu-id="0e7b5-124">일반적으로 대부분의 프레임 워크에서 형식 클래스 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-124">As a rule of thumb, the majority of types in a framework should be classes.</span></span> <span data-ttu-id="0e7b5-125">그러나 경우도, 있는 값 형식의 특성 있도록 구조체를 사용 하는 것이 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-125">There are, however, some situations in which the characteristics of a value type make it more appropriate to use structs.</span></span>  
  
 <span data-ttu-id="0e7b5-126">**✓ CONSIDER** 형식 인스턴스의 작고 일반적으로 수명이 또는 일반적으로 다른 개체에 포함 된 경우 클래스 대신 구조체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-126">**✓ CONSIDER** defining a struct instead of a class if instances of the type are small and commonly short-lived or are commonly embedded in other objects.</span></span>  
  
 <span data-ttu-id="0e7b5-127">**X AVOID** 형식에는 다음과 같은 특성을 모두 하지 않으면 구조체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-127">**X AVOID** defining a struct unless the type has all of the following characteristics:</span></span>  
  
-   <span data-ttu-id="0e7b5-128">단일 값을 기본 형식과 비슷한를 논리적으로 나타내는 (`int`, `double`등.).</span><span class="sxs-lookup"><span data-stu-id="0e7b5-128">It logically represents a single value, similar to primitive types (`int`, `double`, etc.).</span></span>  
  
-   <span data-ttu-id="0e7b5-129">인스턴스 크기를 16 바이트를 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-129">It has an instance size under 16 bytes.</span></span>  
  
-   <span data-ttu-id="0e7b5-130">변경할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-130">It is immutable.</span></span>  
  
-   <span data-ttu-id="0e7b5-131">자주 넣을 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-131">It will not have to be boxed frequently.</span></span>  
  
 <span data-ttu-id="0e7b5-132">다른 모든 경우에 클래스 형식을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7b5-132">In all other cases, you should define your types as classes.</span></span>  
  
 <span data-ttu-id="0e7b5-133">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="0e7b5-133">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="0e7b5-134">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="0e7b5-134">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e7b5-135">참고자료</span><span class="sxs-lookup"><span data-stu-id="0e7b5-135">See also</span></span>

- [<span data-ttu-id="0e7b5-136">형식 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="0e7b5-136">Type Design Guidelines</span></span>](../../../docs/standard/design-guidelines/type.md)  
- [<span data-ttu-id="0e7b5-137">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="0e7b5-137">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
