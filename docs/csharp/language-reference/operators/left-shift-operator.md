---
title: << 연산자 - C# 참조
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: deea2d0f720ba7f096e65c67378586bc88f24673
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219439"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="2ec22-102">\<\< 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="2ec22-102">\<\< operator (C# Reference)</span></span>

<span data-ttu-id="2ec22-103">왼쪽 시프트 연산자 `<<`는 첫 번째 피연산자를 두 번째 피연산자로 정의된 비트 수만큼 왼쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-103">The left-shift operator `<<` shifts its first operand left by the number of bits defined by its second operand.</span></span> <span data-ttu-id="2ec22-104">모든 정수 형식은 `<<` 연산자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-104">All integer types support the `<<` operator.</span></span> <span data-ttu-id="2ec22-105">그러나 두 번째 피연산자의 형식은 [int](../keywords/int.md) 또는 `int`로의 [미리 정의된 암시적 숫자 변환](../keywords/implicit-numeric-conversions-table.md)이 있는 형식이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-105">However, the type of the second operand must be [int](../keywords/int.md) or a type that has a [predefined implicit numeric conversion](../keywords/implicit-numeric-conversions-table.md) to `int`.</span></span>

<span data-ttu-id="2ec22-106">다음 예제와 같이 결과 형식 범위를 벗어나는 상위 비트는 삭제되고, 빈 하위 비트 위치는 0으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-106">The high-order bits that are outside the range of the result type are discarded, and the low-order empty bit positions are set to zero, as the following example shows:</span></span>

[!code-csharp-interactive[left shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShift)]

## <a name="shift-count"></a><span data-ttu-id="2ec22-107">시프트 수</span><span class="sxs-lookup"><span data-stu-id="2ec22-107">Shift count</span></span>

<span data-ttu-id="2ec22-108">`x << count` 식의 경우 실제 시프트 수는 다음과 같이 `x` 형식에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-108">For the expression `x << count`, the actual shift count depends on the type of `x` as follows:</span></span>

- <span data-ttu-id="2ec22-109">`x` 형식이 [int](../keywords/int.md) 또는 [uint](../keywords/uint.md)이면 두 번째 피연산자의 하위 *5*비트로 시프트 수가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-109">If the type of `x` is [int](../keywords/int.md) or [uint](../keywords/uint.md), the shift count is given by the low-order *five* bits of the second operand.</span></span> <span data-ttu-id="2ec22-110">즉, 시프트 수는 `count & 0x1F`(또는 `count & 0b_1_1111`)에서 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-110">That is, the shift count is computed from `count & 0x1F` (or `count & 0b_1_1111`).</span></span>

- <span data-ttu-id="2ec22-111">`x` 형식이 [long](../keywords/long.md) 또는 [ulong](../keywords/ulong.md)이면 두 번째 피연산자의 하위 *6*비트로 시프트 수가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-111">If the type of `x` is [long](../keywords/long.md) or [ulong](../keywords/ulong.md), the shift count is given by the low-order *six* bits of the second operand.</span></span> <span data-ttu-id="2ec22-112">즉, 시프트 수는 `count & 0x3F`(또는 `count & 0b_11_1111`)에서 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-112">That is, the shift count is computed from `count & 0x3F` (or `count & 0b_11_1111`).</span></span>

<span data-ttu-id="2ec22-113">다음 예제에서는 해당 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-113">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftByLargeCount)]

## <a name="remarks"></a><span data-ttu-id="2ec22-114">주의</span><span class="sxs-lookup"><span data-stu-id="2ec22-114">Remarks</span></span>

<span data-ttu-id="2ec22-115">시프트 작업으로 인해 오버플로가 발생하지 않고 [Checked 및 Unchecked](../keywords/checked-and-unchecked.md) 컨텍스트에서 동일한 결과가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-115">Shift operations never cause overflows and produce the same results in [checked and unchecked](../keywords/checked-and-unchecked.md) contexts.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="2ec22-116">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="2ec22-116">Operator overloadability</span></span>

<span data-ttu-id="2ec22-117">사용자 정의 형식은 `<<` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-117">User-defined types can [overload](../keywords/operator.md) the `<<` operator.</span></span> <span data-ttu-id="2ec22-118">사용자 정의 형식 `T`가 `<<` 연산자를 오버로드하는 경우 첫 번째 피연산자의 형식은 `T`여야 하고, 두 번째 피연산자의 형식은 `int`여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-118">If a user-defined type `T` overloads the `<<` operator, the type of the first operand must be `T` and the type of the second operand must be `int`.</span></span> <span data-ttu-id="2ec22-119">`<<` 연산자가 오버로드되면 [왼쪽 시프트 대입 연산자](left-shift-assignment-operator.md) `<<=`도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ec22-119">When the `<<` operator is overloaded, the [left-shift assignment operator](left-shift-assignment-operator.md) `<<=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="2ec22-120">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="2ec22-120">C# language specification</span></span>

<span data-ttu-id="2ec22-121">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [시프트 연산자](~/_csharplang/spec/expressions.md#shift-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2ec22-121">For more information, see the [Shift operators](~/_csharplang/spec/expressions.md#shift-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2ec22-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2ec22-122">See also</span></span>

- [<span data-ttu-id="2ec22-123">C# 참조</span><span class="sxs-lookup"><span data-stu-id="2ec22-123">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="2ec22-124">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="2ec22-124">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="2ec22-125">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="2ec22-125">C# Operators</span></span>](index.md)
- [<span data-ttu-id="2ec22-126">>> 연산자</span><span class="sxs-lookup"><span data-stu-id="2ec22-126">>> operator</span></span>](right-shift-operator.md)
