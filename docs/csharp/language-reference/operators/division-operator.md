---
title: / 연산자 - C# 참조
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: 45bcd64b60e7d13f389064faefeda815ea1f32c9
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286535"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="bc90a-102">/ 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="bc90a-102">/ Operator (C# Reference)</span></span>

<span data-ttu-id="bc90a-103">나누기 연산자 `/`는 두 번째 피연산자로 첫 번째 피연산자를 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-103">The division operator `/` divides its first operand by its second operand.</span></span> <span data-ttu-id="bc90a-104">모든 숫자 형식은 나누기 연산자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-104">All numeric types support the division operator.</span></span>

## <a name="integer-division"></a><span data-ttu-id="bc90a-105">정수 나누기</span><span class="sxs-lookup"><span data-stu-id="bc90a-105">Integer division</span></span>

<span data-ttu-id="bc90a-106">정수 형식의 피연산자의 경우 `/` 연산자의 결과는 정수 형식이고 두 피연산자의 몫과 동일한 값은 0으로 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-106">For the operands of integer types, the result of the `/` operator is of an integer type and equals the quotient of the two operands rounded towards zero:</span></span>

[!code-csharp-interactive[integer division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#Integer)]

<span data-ttu-id="bc90a-107">두 피연산자의 몫을 부동 소수점 숫자로 가져오려면 `float`, `double` 또는 `decimal` 형식을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="bc90a-107">To obtain the quotient of the two operands as a floating-point number, use the `float`, `double`, or `decimal` type:</span></span>

[!code-csharp-interactive[integer as floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#IntegerAsFloatingPoint)]

## <a name="floating-point-division"></a><span data-ttu-id="bc90a-108">부동 소수점 나누기</span><span class="sxs-lookup"><span data-stu-id="bc90a-108">Floating-point division</span></span>

<span data-ttu-id="bc90a-109">`float`, `double` 및 `decimal` 형식의 경우 `/` 연산자의 결과는 두 피연산자의 몫입니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-109">For the `float`, `double`, and `decimal` types, the result of the `/` operator is the quotient of the two operands:</span></span>

[!code-csharp-interactive[floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#FloatingPoint)]

<span data-ttu-id="bc90a-110">피연산자 중 하나가 `decimal`이면 `float` 또는 `double` 모두 `decimal`로 암시적으로 변환할 수 없기 때문에 나머지 피연산자는 `float` 또는 `double`일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-110">If one of the operands is `decimal`, another operand can be neither `float` nor `double`, because neither `float` nor `double` is implicitly convertible to `decimal`.</span></span> <span data-ttu-id="bc90a-111">`float` 또는 `double` 피연산자를 `decimal` 형식으로 암시적으로 변환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-111">You must explicitly convert the `float` or `double` operand to the `decimal` type.</span></span> <span data-ttu-id="bc90a-112">숫자 형식 간의 암시적 변환에 대한 자세한 내용은 [암시적 숫자 변환 표](../keywords/implicit-numeric-conversions-table.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc90a-112">For more information about implicit conversions between numeric types, see [Implicit numeric conversions table](../keywords/implicit-numeric-conversions-table.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="bc90a-113">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="bc90a-113">Operator overloadability</span></span>

<span data-ttu-id="bc90a-114">사용자 정의 형식은 `/` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-114">User-defined types can [overload](../keywords/operator.md) the `/` operator.</span></span> <span data-ttu-id="bc90a-115">`/` 연산자가 오버로드되면 [나누기 대입 연산자](division-assignment-operator.md) `/=`도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc90a-115">When the `/` operator is overloaded, the [division assignment operator](division-assignment-operator.md) `/=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="bc90a-116">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="bc90a-116">C# language specification</span></span>

<span data-ttu-id="bc90a-117">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [나누기 연산자](~/_csharplang/spec/expressions.md#division-operator) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc90a-117">For more information, see the [Division operator](~/_csharplang/spec/expressions.md#division-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bc90a-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bc90a-118">See also</span></span>

- [<span data-ttu-id="bc90a-119">C# 참조</span><span class="sxs-lookup"><span data-stu-id="bc90a-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="bc90a-120">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="bc90a-120">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="bc90a-121">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="bc90a-121">C# Operators</span></span>](index.md)
- [<span data-ttu-id="bc90a-122">% 연산자</span><span class="sxs-lookup"><span data-stu-id="bc90a-122">% Operator</span></span>](remainder-operator.md)
