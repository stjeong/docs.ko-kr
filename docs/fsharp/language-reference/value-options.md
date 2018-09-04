---
title: '값 옵션 (F #)'
description: '옵션 종류의 구조체 버전인는 F # 값 옵션 형식에 대해 알아봅니다.'
ms.date: 06/16/2018
ms.openlocfilehash: 4c255cbbcfd9cb480230de09cd370a401c87343a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43527585"
---
# <a name="value-options"></a><span data-ttu-id="d35bc-103">값 옵션</span><span class="sxs-lookup"><span data-stu-id="d35bc-103">Value Options</span></span>

<span data-ttu-id="d35bc-104">F # 값 옵션 종류는 다음과 같은 두 가지 경우를 저장할 때 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-104">The Value Option type in F# is used when the following two circumstances hold:</span></span>

1. <span data-ttu-id="d35bc-105">시나리오에 적합 한 [F # 옵션](options.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-105">A scenario is appropriate for an [F# Option](options.md).</span></span>
2. <span data-ttu-id="d35bc-106">구조체를 사용 하는 시나리오의 성능 이점을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-106">Using a struct provides a performance benefit in your scenario.</span></span>

<span data-ttu-id="d35bc-107">일부 성능에 민감한 시나리오는 "해결" 구조체를 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-107">Not all performance-sensitive scenarios are "solved" by using structs.</span></span> <span data-ttu-id="d35bc-108">참조 형식 대신 사용 하는 경우 복사 하는 추가 비용을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-108">You must consider the additional cost of copying when using them instead of reference types.</span></span> <span data-ttu-id="d35bc-109">그러나 큰 F # 프로그램 일반적으로 인스턴스화할 실행 부하 과다 경로 통해 이동 하는 많은 선택적 형식 구조체 때로는 프로그램의 수명 동안 전반적인 성능 향상을 위해을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-109">However, large F# programs commonly instantiate many optional types that flow through hot paths, because structs can sometimes yield better overall performance over the lifetime of a program.</span></span>

## <a name="definition"></a><span data-ttu-id="d35bc-110">정의</span><span class="sxs-lookup"><span data-stu-id="d35bc-110">Definition</span></span>

<span data-ttu-id="d35bc-111">값 옵션으로 정의 됩니다는 [구조체 구분 된 공용 구조체](discriminated-unions.md#struct-discriminated-unions) 참조 옵션 형식과 비슷한입니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-111">Value Option is defined as a [struct discriminated union](discriminated-unions.md#struct-discriminated-unions) that is similar to the reference option type:</span></span>

```fsharp
[<StructuralEquality; StructuralComparison>]
[<CompiledName("FSharpValueOption`1")>]
[<Struct>]
type ValueOption<'T> =
    | ValueNone: 'T voption
    | ValueSome: 'T -> 'T voption

    member Value : 'T

and 'T voption = ValueOption<'T>
```

<span data-ttu-id="d35bc-112">구조적 같음 및 비교 값 옵션이 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-112">Value Option conforms to structural equality and comparison.</span></span> <span data-ttu-id="d35bc-113">주요 차이점은는 컴파일된 이름, 형식 이름 및 경우 대/소문자가 모든 이라는 것을 나타내는 값 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-113">The main difference is that the compiled name, type name, and case names all indicate that it is a value type.</span></span>

## <a name="using-value-options"></a><span data-ttu-id="d35bc-114">값 옵션을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="d35bc-114">Using Value Options</span></span>

<span data-ttu-id="d35bc-115">값 옵션 처럼 사용 됩니다 [옵션](options.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-115">Value Options are used just like [Options](options.md).</span></span> <span data-ttu-id="d35bc-116">`ValueSome` 값이 있는지를 나타내는 데 사용 되 고 `ValueNone` 값 없을 때 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-116">`ValueSome` is used to indicate that a value is present, and `ValueNone` is used when a value is not present:</span></span>

```fsharp
let tryParseDateTime (s: string) =
    match System.DateTime.TryParse(s) with
    | (true, dt) -> ValueSome dt
    | (false, _) -> ValueNone

let possibleDateString1 = "1990-12-25"
let possibleDateString2 = "This is not a date"

let result1 = tryParseDateTime possibleDateString1
let result2 = tryParseDateTime possibleDateString2

match (result1, result2) with
| ValueSome d1, ValueSome d2 -> printfn "Both are dates!"
| ValueSome d1, ValueNone -> printfn "Only the first is a date!"
| ValueNone, ValueSome d2 -> printfn "Only the second is a date!"
| ValueNone, ValueNone -> printfn "None of them are dates!"
```

<span data-ttu-id="d35bc-117">와 마찬가지로 [옵션](options.md)를 반환 하는 함수에 대 한 명명 규칙 `ValueOption` 사용 하 여 접두사를 지정 하는 `try`합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-117">As with [Options](options.md), the naming convention for a function that returns `ValueOption` is to prefix it with `try`.</span></span>

## <a name="value-option-properties-and-methods"></a><span data-ttu-id="d35bc-118">값 옵션 속성 및 메서드</span><span class="sxs-lookup"><span data-stu-id="d35bc-118">Value Option properties and methods</span></span>

<span data-ttu-id="d35bc-119">지금은 값 옵션에 대 한 하나의 속성은: `Value`합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-119">There is one property for Value Options at this time: `Value`.</span></span> <span data-ttu-id="d35bc-120"><xref:System.InvalidOperationException> 값이 현재가이 속성을 호출할 때 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-120">An <xref:System.InvalidOperationException> is raised if no value is present when this property is invoked.</span></span>

## <a name="value-option-functions"></a><span data-ttu-id="d35bc-121">값 옵션 함수</span><span class="sxs-lookup"><span data-stu-id="d35bc-121">Value Option functions</span></span>

<span data-ttu-id="d35bc-122">값 옵션에 대 한 하나의 모듈 바인딩된 함수는 현재 `defaultValueArg`:</span><span class="sxs-lookup"><span data-stu-id="d35bc-122">There is currently one module-bound function for Value Options, `defaultValueArg`:</span></span>

```fsharp
val defaultValueArg : arg:'T voption -> defaultValue:'T -> 'T 
```

<span data-ttu-id="d35bc-123">와 마찬가지로 합니다 `defaultArg` 함수를 `defaultValueArg` 경우 지정 된 값 옵션의 기본 값을 반환 존재 않으면 그렇지 않은 경우 지정된 된 기본값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-123">As with the `defaultArg` function, `defaultValueArg` returns the underlying value of the given Value Option if it exists; otherwise, it returns the specified default value.</span></span>

<span data-ttu-id="d35bc-124">이때 값 옵션에 대 한 다른 모듈 바인딩된 함수가 없는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d35bc-124">At this time, there are no other module-bound functions for Value Options.</span></span>

## <a name="see-also"></a><span data-ttu-id="d35bc-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="d35bc-125">See also</span></span>

[<span data-ttu-id="d35bc-126">옵션</span><span class="sxs-lookup"><span data-stu-id="d35bc-126">Options</span></span>](options.md)