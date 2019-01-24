---
title: 조각 (F#)
description: 기존 분할 영역을 사용 하는 방법에 알아봅니다 F# 데이터 형식 및 다른 데이터 형식에 대 한 사용자 고유의 조각을 정의 하는 방법입니다.
ms.date: 01/22/2019
ms.openlocfilehash: c204c6cbb195b33998b92dd940313a132ecc321d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54746714"
---
# <a name="slices"></a><span data-ttu-id="9c7b6-103">조각</span><span class="sxs-lookup"><span data-stu-id="9c7b6-103">Slices</span></span>

<span data-ttu-id="9c7b6-104">F#, 조각은 데이터 형식의 하위 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-104">In F#, a slice is a subset of a data type.</span></span> <span data-ttu-id="9c7b6-105">하거나 정의 해야 데이터 형식을 데이터 형식에서 조각을 가져올 수는 `GetSlice` 메서드 또는 [확장명을 입력](type-extensions.md) 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-105">To be able to take a slice from a data type, the data type must either define a `GetSlice` method or in a [type extension](type-extensions.md) that is in scope.</span></span> <span data-ttu-id="9c7b6-106">이 문서에서는 기존 분할 영역을 사용 하는 방법을 설명 F# 형식 및 사용자 지정 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-106">This article explains how to take slices from existing F# types and how to define your own.</span></span>

<span data-ttu-id="9c7b6-107">조각이 비슷합니다 [인덱서](members/indexed-properties.md), 하지만 여러 세션 대신 기본 데이터 구조에서 단일 값이 구해지 기를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-107">Slices are similar to [indexers](members/indexed-properties.md), but instead of yielding a single value from the underlying data structure, they yield multiple ones.</span></span>

<span data-ttu-id="9c7b6-108">F#현재는 문자열, 목록, 배열 및 2D 배열 조각화에 대 한 내장 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-108">F# currently has intrinsic support for slicing strings, lists, arrays, and 2D arrays.</span></span>

## <a name="basic-slicing-with-f-lists-and-arrays"></a><span data-ttu-id="9c7b6-109">사용 하 여 기본 조각화 F# 목록 및 배열</span><span class="sxs-lookup"><span data-stu-id="9c7b6-109">Basic slicing with F# lists and arrays</span></span>

<span data-ttu-id="9c7b6-110">분할 되는 가장 일반적인 데이터 형식은 F# 목록과 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-110">The most common data types that are sliced are F# lists and arrays.</span></span> <span data-ttu-id="9c7b6-111">다음 예제에서는 목록을 사용 하 여이 작업을 수행 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-111">The following example demonstrates how to do this with lists:</span></span>

```fsharp
// Generate a list of 100 integers
let fullList = [ 1 .. 100 ]

// Create a slice from indices 1-5 (inclusive)
let smallSlice = fullList.[1..5]
printfn "Small slice: %A" smallSlice

// Create a slice from the beginning to index 5 (inclusive)
let unboundedBeginning = fullList.[..5]
printfn "Unbounded beginning slice: %A" unboundedBeginning

// Create a slice from an index to the end of the list
let unboundedEnd = fullList.[94..]
printfn "Unbounded end slice: %A" unboundedEnd
```

<span data-ttu-id="9c7b6-112">배열 조각화 같으며 목록 조각화:</span><span class="sxs-lookup"><span data-stu-id="9c7b6-112">Slicing arrays is just like slicing lists:</span></span>

```fsharp
// Generate an array of 100 integers
let fullArray = [| 1 .. 100 |]

// Create a slice from indices 1-5 (inclusive)
let smallSlice = fullArray.[1..5]
printfn "Small slice: %A" smallSlice

// Create a slice from the beginning to index 5 (inclusive)
let unboundedBeginning = fullArray.[..5]
printfn "Unbounded beginning slice: %A" unboundedBeginning

// Create a slice from an index to the end of the list
let unboundedEnd = fullArray.[94..]
printfn "Unbounded end slice: %A" unboundedEnd
```

## <a name="slicing-multidimensional-arrays"></a><span data-ttu-id="9c7b6-113">다차원 배열 조각화</span><span class="sxs-lookup"><span data-stu-id="9c7b6-113">Slicing multidimensional arrays</span></span>

<span data-ttu-id="9c7b6-114">F#다차원 배열을 지원 합니다 F# 핵심 라이브러리입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-114">F# supports multidimensional arrays in the F# core library.</span></span> <span data-ttu-id="9c7b6-115">1 차원 배열과 마찬가지로 다차원 배열 조각도 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-115">As with one-dimensional arrays, slices of multidimensional arrays can also be useful.</span></span> <span data-ttu-id="9c7b6-116">그러나 특정 행과 열에 대 한 부분을 수행할 수 있도록 추가 차원이 미치는 구문은 약간 다릅니다 한다고 규정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-116">However, the introduction of additional dimensions mandates a slightly different syntax so that you can take slices of specific rows and columns.</span></span>

<span data-ttu-id="9c7b6-117">다음 예제에서는 2 차원 배열 조각화 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-117">The following examples demonstrate how to slice a 2D array:</span></span>

```fsharp
// Generate a 3x3 2D matrix
let A = array2D [[1;2;3];[4;5;6];[7;8;9]]
printfn "Full matrix:\n %A" A

// Take the first row
let row0 = A.[0,*]
printfn "Row 0: %A" row0

// Take the first column
let col0 = A.[*,0]
printfn "Column 0: %A" col0

// Take all rows but only two columns
let subA = A.[*,0..1]
printfn "%A" subA

// Take two rows and all columns
let subA' = A.[0..1,*]
printfn "%A" subA'

// Slice a 2x2 matrix out of the full 3x3 matrix
let twoByTwo = A.[0..1,0..1]
printfn "%A" twobyTwo
```

<span data-ttu-id="9c7b6-118">F# 핵심 라이브러리를 정의 하지 않습니다 `GetSlice`3D 배열에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-118">The F# core library does not define `GetSlice`for 3D arrays.</span></span> <span data-ttu-id="9c7b6-119">정의 해야 합니다 또는 다른 배열을 한 차원 조각화 하려는 경우는 `GetSlice` 멤버 직접.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-119">If you wish to slice those or other arrays of more dimensions, you must define the `GetSlice` member yourself.</span></span>

## <a name="defining-slices-for-other-data-structures"></a><span data-ttu-id="9c7b6-120">기타 데이터 구조에 대 한 슬라이스를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-120">Defining slices for other data structures</span></span>

<span data-ttu-id="9c7b6-121">F# 핵심 라이브러리는 형식의 제한 된 집합에 대 한 슬라이스를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-121">The F# core library defines slices for a limited set of types.</span></span> <span data-ttu-id="9c7b6-122">자세한 데이터 형식에 대 한 조각을 정의 하려는 경우 형식 정의 자체 또는 형식 확장에서이 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-122">If you wish to define slices for more data types, you can do so either in the type definition itself or in a type extension.</span></span>

<span data-ttu-id="9c7b6-123">예를 들어 다음과 같습니다 하는 방법에 대 한 슬라이스를 정의할 수 있습니다는 <xref:System.ArraySegment`1> 편리한 데이터 조작을 위한 클래스:</span><span class="sxs-lookup"><span data-stu-id="9c7b6-123">For example, here's how you might define slices for the <xref:System.ArraySegment`1> class to allow for convenient data manipulation:</span></span>

```fsharp
open System

type ArraySegment<'TItem> with
    member segment.GetSlice(?start, ?finish) =
        let start = defaultArg start 0
        let finish = defaultArg finish segment.Count
        ArraySegment(segment.Array, segment.Offset + start, finish - start)

let arr = ArraySegment [| 1 .. 10 |]
let slice = arr.[2..5] //[ 3; 4; 5]
```

### <a name="use-inlining-to-avoid-boxing-if-it-is-necessary"></a><span data-ttu-id="9c7b6-124">필요한 경우 boxing을 방지 하려면 인라인 처리 사용</span><span class="sxs-lookup"><span data-stu-id="9c7b6-124">Use inlining to avoid boxing if it is necessary</span></span>

<span data-ttu-id="9c7b6-125">좋습니다 구조체 실제로 된 형식에 대 한 조각을 정의 하는 경우 있습니다 `inline` 는 `GetSlice` 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-125">If you are defining slices for a type that is actually a struct, we recommend that you `inline` the `GetSlice` member.</span></span> <span data-ttu-id="9c7b6-126">F# 컴파일러 조각화의 결과로 모든 힙 할당을 방지 하는 선택적 인수를 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-126">The F# compiler optimizes away the optional arguments, avoiding any heap allocations as a result of slicing.</span></span> <span data-ttu-id="9c7b6-127">이 같은 구문을 조각화 하는 데 매우 중요 <xref:System.Span`1> 는 힙에 할당 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7b6-127">This is critically important for slicing constructs such as <xref:System.Span`1> that cannot be be allocated on the heap.</span></span>

```fsharp
open System

type Span<'T> with
    // Note the 'inline' in the member definition
    member inline sp.GetSlice(startIdx, endIdx) =
        let s = defaultArg startIdx 0
        let e = defaultArg endIdx sp.Length
        sp.Slice(s, e)

let printSpan (sp: Span<int>) =
    let arr = sp.ToArray()
    printfn "%A" arr

let sp = [| 1; 2; 3; 4; 5 |].AsSpan()
printSpan sp.[0..] // [|1; 2; 3; 4; 5|]
printSpan sp.[..5] // [|1; 2; 3; 4; 5|]
printSpan sp.[0..3] // [|1; 2; 3|]
printSpan sp.[1..2] // |2; 3|]
```

## <a name="see-also"></a><span data-ttu-id="9c7b6-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="9c7b6-128">See also</span></span>

- [<span data-ttu-id="9c7b6-129">인덱싱된 속성</span><span class="sxs-lookup"><span data-stu-id="9c7b6-129">Indexed properties</span></span>](members/indexed-properties.md)