---
title: 단위 형식(F#)
description: 위치 값이 필요한 언어 구문을 사용 하 여 필요한 되었거나 필요한 값이 없는 경우 위치를 포함 하는 데 자주 사용 하는 F# 'unit' 형식 하는 방법에 대해 알아봅니다.
ms.date: 05/16/2016
ms.openlocfilehash: c3dfa5f63c25a1e8abc0f75b905c129b311479af
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "44204658"
---
# <a name="unit-type"></a><span data-ttu-id="671c8-103">단위 형식</span><span class="sxs-lookup"><span data-stu-id="671c8-103">Unit Type</span></span>

<span data-ttu-id="671c8-104">합니다 `unit` 의 특정 값이 없음을 나타내는 형식인 형식은 `unit` 형식은 다른 값이 없으므로 있거나 필요한 경우 자리 표시자로 역할을 하는 단일 값만 합니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-104">The `unit` type is a type that indicates the absence of a specific value; the `unit` type has only a single value, which acts as a placeholder when no other value exists or is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="671c8-105">구문</span><span class="sxs-lookup"><span data-stu-id="671c8-105">Syntax</span></span>

```fsharp
// The value of the unit type.
()
```

## <a name="remarks"></a><span data-ttu-id="671c8-106">설명</span><span class="sxs-lookup"><span data-stu-id="671c8-106">Remarks</span></span>

<span data-ttu-id="671c8-107">모든 F# 식은 값으로 계산 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-107">Every F# expression must evaluate to a value.</span></span> <span data-ttu-id="671c8-108">형식의 값을 원하는 값을 생성 하지 않습니다 하는 식에 대 한 `unit` 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-108">For expressions that do not generate a value that is of interest, the value of type `unit` is used.</span></span> <span data-ttu-id="671c8-109">합니다 `unit` 종류와 비슷합니다는 `void` C# 및 c + +와 같은 언어를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-109">The `unit` type resembles the `void` type in languages such as C# and C++.</span></span>

<span data-ttu-id="671c8-110">합니다 `unit` 형식은 단일 값 및 해당 값은 토큰에 나타난 `()`합니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-110">The `unit` type has a single value, and that value is indicated by the token `()`.</span></span>

<span data-ttu-id="671c8-111">값을 `unit` 유형은 F# 프로그래밍 언어 구문을 사용 하 여 값이 필요한 경우 하지만 필요한 되었거나 필요한 값이 없는 경우에서 자리를 자주 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-111">The value of the `unit` type is often used in F# programming to hold the place where a value is required by the language syntax, but when no value is needed or desired.</span></span> <span data-ttu-id="671c8-112">반환 값을 예로 들 수 있습니다는 `printf` 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-112">An example might be the return value of a `printf` function.</span></span> <span data-ttu-id="671c8-113">있으므로의 중요 한 작업을 `printf` 작업 함수에서 발생이 함수는 실제 값을 반환할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-113">Because the important actions of the `printf` operation occur in the function, the function does not have to return an actual value.</span></span> <span data-ttu-id="671c8-114">형식의 반환 값은 따라서 `unit`합니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-114">Therefore, the return value is of type `unit`.</span></span>

<span data-ttu-id="671c8-115">일부 구문은 예상을 `unit` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-115">Some constructs expect a `unit` value.</span></span> <span data-ttu-id="671c8-116">예를 들어, 한 `do` 바인딩 또는 코드 모듈의 최상위 수준에서 평가 되어야 하는 `unit` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-116">For example, a `do` binding or any code at the top level of a module is expected to evaluate to a `unit` value.</span></span> <span data-ttu-id="671c8-117">컴파일러 경고를 보고 경우는 `do` 바인딩 또는 코드 모듈의 최상위 수준에서 결과 이외의 `unit` 다음 예와에서 같이 사용 되지 않는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-117">The compiler reports a warning when a `do` binding or code at the top level of a module produces a result other than the `unit` value that is not used, as shown in the following example.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet901.fs)]

<span data-ttu-id="671c8-118">이 경고는 함수형 프로그래밍;의 특징 다른.NET 프로그래밍 언어에에서는 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-118">This warning is a characteristic of functional programming; it does not appear in other .NET programming languages.</span></span> <span data-ttu-id="671c8-119">함수 없는 부작용을 순수 함수형 프로그램에서 최종 반환 값은 함수 호출의 유일한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-119">In a purely functional program, in which functions do not have any side effects, the final return value is the only result of a function call.</span></span> <span data-ttu-id="671c8-120">따라서 결과 무시 하는 경우 가능한 프로그래밍 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-120">Therefore, when the result is ignored, it is a possible programming error.</span></span> <span data-ttu-id="671c8-121">F#은 순수 함수형 프로그래밍 언어, 이지만 가능 하면 함수형 프로그래밍 스타일을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="671c8-121">Although F# is not a purely functional programming language, it is a good practice to follow functional programming style whenever possible.</span></span>

## <a name="see-also"></a><span data-ttu-id="671c8-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="671c8-122">See also</span></span>

- [<span data-ttu-id="671c8-123">기본</span><span class="sxs-lookup"><span data-stu-id="671c8-123">Primitive</span></span>](primitive-types.md)
- [<span data-ttu-id="671c8-124">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="671c8-124">F# Language Reference</span></span>](index.md)
