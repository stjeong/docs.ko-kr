---
title: '% 연산자(C# 참조)'
ms.date: 09/04/2018
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
ms.openlocfilehash: 9cd2f7ad3856feb34667686979c942ecb21887c2
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44266698"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="79d04-102">% 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="79d04-102">% Operator (C# Reference)</span></span>

<span data-ttu-id="79d04-103">나머지 연산자 `%`는 첫 번째 피연산자를 두 번째 피연산자로 나눈 후 나머지를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-103">The remainder operator `%` computes the remainder after dividing its first operand by its second operand.</span></span> <span data-ttu-id="79d04-104">사용자 정의 형식은 `%` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-104">User-defined types can [overload](../keywords/operator.md) the `%` operator.</span></span> <span data-ttu-id="79d04-105">`%`가 오버로드되면 [나머지 할당 연산자](remainder-assignment-operator.md) `%=`도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-105">When the `%` is overloaded, the [remainder assignment operator](remainder-assignment-operator.md) `%=` is also implicitly overloaded.</span></span>

<span data-ttu-id="79d04-106">모든 숫자 형식은 나머지 연산자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-106">All numeric types support the remainder operator.</span></span>

## <a name="integer-remainder"></a><span data-ttu-id="79d04-107">정수 나머지</span><span class="sxs-lookup"><span data-stu-id="79d04-107">Integer remainder</span></span>
  
<span data-ttu-id="79d04-108">정수 피연산자의 경우 `a % b`의 결과가 `a - (a / b) * b`에서 생성된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-108">For the integer operands, the result of `a % b` is the value produced by `a - (a / b) * b`.</span></span> <span data-ttu-id="79d04-109">다음 예와 같이 0이 아닌 나머지의 부호는 첫 번째 피연산자와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-109">The sign of the non-zero remainder is the same as that of the first operand, as the following example shows:</span></span>

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a><span data-ttu-id="79d04-110">부동 소수점 나머지</span><span class="sxs-lookup"><span data-stu-id="79d04-110">Floating-point remainder</span></span>

<span data-ttu-id="79d04-111">[float](../keywords/float.md) 및 [double](../keywords/double.md) 피연산자의 경우, 유한 `x` 및 `y`에 대한 `x % y`의 결과는 다음과 같은 `z` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-111">For the [float](../keywords/float.md) and [double](../keywords/double.md) operands, the result of `x % y` for the finite `x` and `y` is the value `z` such that</span></span>

- <span data-ttu-id="79d04-112">0이 아닌 경우 `z`의 부호는 `x`의 부호와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-112">the sign of `z`, if non-zero, is the same as the sign of `x`;</span></span>
- <span data-ttu-id="79d04-113">`z`의 절대 값은 `|x| - n * |y|`에서 생성된 값입니다. 여기서 `n`은 `|x| / |y|`보다 작거나 같은 최대 가능한 정수이고 `|x|` 및 `|y|`는 각각 `x` 및 `y`의 절대 값입니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-113">the absolute value of `z` is the value produced by `|x| - n * |y|` where `n` is the largest possible integer that is less than or equal to `|x| / |y|` and `|x|` and `|y|` are the absolute values of `x` and `y`, respectively.</span></span>

<span data-ttu-id="79d04-114">무한 피연산자의 경우 `%` 연산자의 동작에 대한 자세한 내용은 [C# 언어 사양](/dotnet/csharp/language-reference/language-specification/index)의 [나머지 연산자](/dotnet/csharp/language-reference/language-specification/expressions#remainder-operator) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="79d04-114">For information about behavior of the `%` operator in case of non-finite operands, see the [Remainder operator](/dotnet/csharp/language-reference/language-specification/expressions#remainder-operator) section of the [C# language specification](/dotnet/csharp/language-reference/language-specification/index).</span></span>

> [!NOTE]
> <span data-ttu-id="79d04-115">나머지 계산 방법은 정수 피연산자에 사용되는 것과 유사하지만 IEEE 754와는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-115">This method of computing the remainder is analogous to that used for integer operands, but differs from the IEEE 754.</span></span> <span data-ttu-id="79d04-116">IEEE 754를 준수하는 나머지 작업이 필요한 경우 <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> 메서드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-116">If you need the remainder operation that complies with the IEEE 754, use the <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="79d04-117">다음 예제에서는 `float` 및 `double` 피연산자에 대한 나머지 연산자의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-117">The following example demonstrates the behavior of the remainder operator for `float` and `double` operands:</span></span>

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

<span data-ttu-id="79d04-118">부동 소수점 형식과 연결될 수 있는 반올림 오류를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-118">Note the round-off errors that can be associated with the floating-point types.</span></span>

<span data-ttu-id="79d04-119">[10진수](../keywords/decimal.md) 피연산자의 경우 나머지 연산자 `%`는 <xref:System.Decimal?displayProperty=nameWithType> 형식의 [나머지 연산자](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>)와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="79d04-119">For the [decimal](../keywords/decimal.md) operands, the remainder operator `%` is equivalent to the [remainder operator](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>) of the <xref:System.Decimal?displayProperty=nameWithType> type.</span></span>

## <a name="see-also"></a><span data-ttu-id="79d04-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="79d04-120">See also</span></span>

- [<span data-ttu-id="79d04-121">C# 참조</span><span class="sxs-lookup"><span data-stu-id="79d04-121">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="79d04-122">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="79d04-122">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="79d04-123">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="79d04-123">C# Operators</span></span>](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
