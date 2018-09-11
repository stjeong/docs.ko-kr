---
title: 유연한 형식(F#)
description: '지정 된 형식과 호환 되는 형식 매개 변수, 변수 또는 값 수 있음을 나타냅니다는 F # 유연한 형식 주석은 사용 하는 방법에 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: b6c97c3cc19f15b2c8db74b2c55660a16b2858f7
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44270947"
---
# <a name="flexible-types"></a><span data-ttu-id="f9c91-103">유연한 형식</span><span class="sxs-lookup"><span data-stu-id="f9c91-103">Flexible Types</span></span>

<span data-ttu-id="f9c91-104">A *유연한 형식 주석은* 은 클래스 또는 인터페이스의 개체 지향 계층 구조의 위치 호환성을 결정 하는 경우 지정 된 형식과 호환 되는 형식 매개 변수, 변수 또는 값 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-104">A *flexible type annotation* indicates that a parameter, variable, or value has a type that is compatible with a specified type, where compatibility is determined by position in an object-oriented hierarchy of classes or interfaces.</span></span> <span data-ttu-id="f9c91-105">유연한 형식 형식 계층에서 더 높은 형식으로 자동 변환이 발생 하지 않습니다 하지만 여전히 계층 구조의 모든 형식 또는 인터페이스를 구현 하는 형식을 사용 하 여 기능을 사용 하도록 설정 하려는 경우에 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-105">Flexible types are useful specifically when the automatic conversion to types higher in the type hierarchy does not occur but you still want to enable your functionality to work with any type in the hierarchy or any type that implements an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c91-106">구문</span><span class="sxs-lookup"><span data-stu-id="f9c91-106">Syntax</span></span>

```fsharp
#type
```

## <a name="remarks"></a><span data-ttu-id="f9c91-107">설명</span><span class="sxs-lookup"><span data-stu-id="f9c91-107">Remarks</span></span>

<span data-ttu-id="f9c91-108">이전 구문에서 *형식* 기본 형식 또는 인터페이스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-108">In the previous syntax, *type* represents a base type or an interface.</span></span>

<span data-ttu-id="f9c91-109">유연한 형식 제한 기본 또는 인터페이스 형식와 호환 되는 형식에 허용 되는 형식 제약 조건이 있는 제네릭 형식에는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-109">A flexible type is equivalent to a generic type that has a constraint that limits the allowed types to types that are compatible with the base or interface type.</span></span> <span data-ttu-id="f9c91-110">즉, 다음 두 줄의 코드는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-110">That is, the following two lines of code are equivalent.</span></span>

```fsharp
#SomeType

'T when 'T :> SomeType
```

<span data-ttu-id="f9c91-111">유연한 형식은 여러 가지 상황에서에서 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-111">Flexible types are useful in several types of situations.</span></span> <span data-ttu-id="f9c91-112">예를 들어, 고차 함수 (인수로 서 함수를 사용 하는 함수)에 있는 경우 유용 융통성 있는 형식을 반환 하는 함수를 포함 하려면.</span><span class="sxs-lookup"><span data-stu-id="f9c91-112">For example, when you have a higher order function (a function that takes a function as an argument), it is often useful to have the function return a flexible type.</span></span> <span data-ttu-id="f9c91-113">다음 예제에서는 시퀀스 인수를 사용 하 여 유연한 형식의 사용 `iterate2` 시퀀스, 배열, 목록 및 기타 열거 가능한 형식을 생성 하는 함수를 사용 하는 고차 함수를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-113">In the following example, the use of a flexible type with a sequence argument in `iterate2` enables the higher order function to work with functions that generate sequences, arrays, lists, and any other enumerable type.</span></span>

<span data-ttu-id="f9c91-114">유연한 형식 반환, 다른 하나는 시퀀스를 반환 하는의 하나는 다음 두 함수를 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-114">Consider the following two functions, one of which returns a sequence, the other of which returns a flexible type.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4101.fs)]

<span data-ttu-id="f9c91-115">다른 예로, 합니다 [Seq.concat](https://msdn.microsoft.com/library/2eeb69a9-fc2f-4b7d-8dee-101fa2b00712) 라이브러리 함수:</span><span class="sxs-lookup"><span data-stu-id="f9c91-115">As another example, consider the [Seq.concat](https://msdn.microsoft.com/library/2eeb69a9-fc2f-4b7d-8dee-101fa2b00712) library function:</span></span>

```fsharp
val concat: sequences:seq<#seq<'T>> -> seq<'T>
```

<span data-ttu-id="f9c91-116">이 함수에 있는 다음 열거 가능한 시퀀스를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-116">You can pass any of the following enumerable sequences to this function:</span></span>

- <span data-ttu-id="f9c91-117">목록의 목록</span><span class="sxs-lookup"><span data-stu-id="f9c91-117">A list of lists</span></span>
- <span data-ttu-id="f9c91-118">배열 목록</span><span class="sxs-lookup"><span data-stu-id="f9c91-118">A list of arrays</span></span>
- <span data-ttu-id="f9c91-119">목록의 배열</span><span class="sxs-lookup"><span data-stu-id="f9c91-119">An array of lists</span></span>
- <span data-ttu-id="f9c91-120">시퀀스의 배열</span><span class="sxs-lookup"><span data-stu-id="f9c91-120">An array of sequences</span></span>
- <span data-ttu-id="f9c91-121">열거 가능한 시퀀스의 다른 조합</span><span class="sxs-lookup"><span data-stu-id="f9c91-121">Any other combination of enumerable sequences</span></span>

<span data-ttu-id="f9c91-122">다음 코드에서는 `Seq.concat` 유연한 형식을 사용 하 여 지원할 수 있는 시나리오를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-122">The following code uses `Seq.concat` to demonstrate the scenarios that you can support by using flexible types.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4102.fs)]

<span data-ttu-id="f9c91-123">출력은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-123">The output is as follows.</span></span>

```
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
```

<span data-ttu-id="f9c91-124">F #에서는 다른 개체 지향 언어와 마찬가지로 가지 컨텍스트는 파생된 형식 또는 인터페이스를 구현 하는 형식으로 자동 변환 됩니다 기본 형식 또는 인터페이스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-124">In F#, as in other object-oriented languages, there are contexts in which derived types or types that implement interfaces are automatically converted to a base type or interface type.</span></span> <span data-ttu-id="f9c91-125">이러한 자동 변환 형식은 형식 인수 또는 함수 형식 반환 형식과 같은 보다 복잡 한 형식의 일부로 종속 된 위치에 때가 아니라 하지만 직접 인수를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-125">These automatic conversions occur in direct arguments, but not when the type is in a subordinate position, as part of a more complex type such as a return type of a function type, or as a type argument.</span></span> <span data-ttu-id="f9c91-126">따라서 되도록 적용 하는 형식이 더 복잡 한 형식의 일부가 유연한 형식 표기법은 주로 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9c91-126">Thus, the flexible type notation is primarily useful when the type you are applying it to is part of a more complex type.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9c91-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="f9c91-127">See also</span></span>

- [<span data-ttu-id="f9c91-128">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="f9c91-128">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="f9c91-129">제네릭</span><span class="sxs-lookup"><span data-stu-id="f9c91-129">Generics</span></span>](generics/index.md)
