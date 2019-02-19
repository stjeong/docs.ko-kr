---
title: '>> 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 809cd2cab29d3378892ea224cf846e9d0909b073
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219726"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="ed0f8-102">>> 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="ed0f8-102">>> operator (C# Reference)</span></span>

<span data-ttu-id="ed0f8-103">오른쪽 시프트 연산자 `>>`는 첫 번째 피연산자를 두 번째 피연산자로 정의된 비트 수만큼 오른쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-103">The right-shift operator `>>` shifts its first operand right by the number of bits defined by its second operand.</span></span> <span data-ttu-id="ed0f8-104">모든 정수 형식은 `>>` 연산자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-104">All integer types support the `>>` operator.</span></span> <span data-ttu-id="ed0f8-105">그러나 두 번째 피연산자의 형식은 [int](../keywords/int.md) 또는 `int`로의 [미리 정의된 암시적 숫자 변환](../keywords/implicit-numeric-conversions-table.md)이 있는 형식이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-105">However, the type of the second operand must be [int](../keywords/int.md) or a type that has a [predefined implicit numeric conversion](../keywords/implicit-numeric-conversions-table.md) to `int`.</span></span>

<span data-ttu-id="ed0f8-106">오른쪽 시프트 연산은 하위 비트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-106">The right-shift operation discards the low-order bits.</span></span> <span data-ttu-id="ed0f8-107">빈 상위 공백 비트 위치는 다음과 같이 첫 번째 피연산자 형식에 따라 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-107">The high-order empty bit positions are set based on the type of the first operand as follows:</span></span>

- <span data-ttu-id="ed0f8-108">첫 번째 피연산자가 [int](../keywords/int.md) 또는 [long](../keywords/long.md) 형식인 경우 오른쪽 시프트 연산자는 **산술** 시프트를 수행합니다. 첫 번째 피연산자의 최상위 비트(부호 비트) 값이 빈 상위 비트 위치로 전파됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-108">If the first operand is of type [int](../keywords/int.md) or [long](../keywords/long.md), the right-shift operator performs an **arithmetic** shift: the value of the most significant bit (the sign bit) of the first operand is propagated to the high-order empty bit positions.</span></span> <span data-ttu-id="ed0f8-109">즉, 빈 상위 비트 위치는 첫 번째 피연산자가 음수가 아닌 경우 0으로 설정되고, 음수인 경우 1로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-109">That is, the high-order empty bit positions are set to zero if the first operand is non-negative and set to one if it's negative.</span></span>

- <span data-ttu-id="ed0f8-110">첫 번째 피연산자가 [uint](../keywords/uint.md) 또는 [ulong](../keywords/ulong.md) 형식이면 오른쪽 시프트 피연산자는 **논리적** 시프트를 수행합니다. 빈 상위 비트 위치가 항상 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-110">If the first operand is of type [uint](../keywords/uint.md) or [ulong](../keywords/ulong.md), the right-shift operator performs a **logical** shift: the high-order empty bit positions are always set to zero.</span></span>

<span data-ttu-id="ed0f8-111">다음 예제에서는 해당 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-111">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[right shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShift)]

## <a name="shift-count"></a><span data-ttu-id="ed0f8-112">시프트 수</span><span class="sxs-lookup"><span data-stu-id="ed0f8-112">Shift count</span></span>

<span data-ttu-id="ed0f8-113">`x >> count` 식의 경우 실제 시프트 수는 다음과 같이 `x` 형식에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-113">For the expression `x >> count`, the actual shift count depends on the type of `x` as follows:</span></span>

- <span data-ttu-id="ed0f8-114">`x` 형식이 [int](../keywords/int.md) 또는 [uint](../keywords/uint.md)이면 두 번째 피연산자의 하위 *5*비트로 시프트 수가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-114">If the type of `x` is [int](../keywords/int.md) or [uint](../keywords/uint.md), the shift count is given by the low-order *five* bits of the second operand.</span></span> <span data-ttu-id="ed0f8-115">즉, 시프트 수는 `count & 0x1F`(또는 `count & 0b_1_1111`)에서 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-115">That is, the shift count is computed from `count & 0x1F` (or `count & 0b_1_1111`).</span></span>

- <span data-ttu-id="ed0f8-116">`x` 형식이 [long](../keywords/long.md) 또는 [ulong](../keywords/ulong.md)이면 두 번째 피연산자의 하위 *6*비트로 시프트 수가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-116">If the type of `x` is [long](../keywords/long.md) or [ulong](../keywords/ulong.md), the shift count is given by the low-order *six* bits of the second operand.</span></span> <span data-ttu-id="ed0f8-117">즉, 시프트 수는 `count & 0x3F`(또는 `count & 0b_11_1111`)에서 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-117">That is, the shift count is computed from `count & 0x3F` (or `count & 0b_11_1111`).</span></span>

<span data-ttu-id="ed0f8-118">다음 예제에서는 해당 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-118">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftByLargeCount)]

## <a name="remarks"></a><span data-ttu-id="ed0f8-119">주의</span><span class="sxs-lookup"><span data-stu-id="ed0f8-119">Remarks</span></span>

<span data-ttu-id="ed0f8-120">시프트 작업으로 인해 오버플로가 발생하지 않고 [Checked 및 Unchecked](../keywords/checked-and-unchecked.md) 컨텍스트에서 동일한 결과가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-120">Shift operations never cause overflows and produce the same results in [checked and unchecked](../keywords/checked-and-unchecked.md) contexts.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="ed0f8-121">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="ed0f8-121">Operator overloadability</span></span>

<span data-ttu-id="ed0f8-122">사용자 정의 형식은 `>>` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-122">User-defined types can [overload](../keywords/operator.md) the `>>` operator.</span></span> <span data-ttu-id="ed0f8-123">사용자 정의 형식 `T`가 `>>` 연산자를 오버로드하는 경우 첫 번째 피연산자의 형식은 `T`여야 하고, 두 번째 피연산자의 형식은 `int`여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-123">If a user-defined type `T` overloads the `>>` operator, the type of the first operand must be `T` and the type of the second operand must be `int`.</span></span> <span data-ttu-id="ed0f8-124">`>>` 연산자가 오버로드되면 [오른쪽 시프트 대입 연산자](right-shift-assignment-operator.md) `>>=`도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-124">When the `>>` operator is overloaded, the [right-shift assignment operator](right-shift-assignment-operator.md) `>>=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="ed0f8-125">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="ed0f8-125">C# language specification</span></span>

<span data-ttu-id="ed0f8-126">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [시프트 연산자](~/_csharplang/spec/expressions.md#shift-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-126">For more information, see the [Shift operators](~/_csharplang/spec/expressions.md#shift-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed0f8-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ed0f8-127">See also</span></span>

- [<span data-ttu-id="ed0f8-128">C# 참조</span><span class="sxs-lookup"><span data-stu-id="ed0f8-128">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="ed0f8-129">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="ed0f8-129">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="ed0f8-130">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="ed0f8-130">C# operators</span></span>](index.md)
- [<span data-ttu-id="ed0f8-131"><< 연산자</span><span class="sxs-lookup"><span data-stu-id="ed0f8-131"><< operator</span></span>](left-shift-operator.md)