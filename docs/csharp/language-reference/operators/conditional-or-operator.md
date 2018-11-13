---
title: '|| 연산자(C# 참조)'
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: a391078372e4ec0a3882bed4515733adedffb547
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "42925542"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="6f6ff-102">|| 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="6f6ff-102">|| Operator (C# Reference)</span></span>

<span data-ttu-id="6f6ff-103">"단락(short-circuiting)" 논리 OR 연산자로도 알려져 있는 조건부 논리 OR 연산자 `||`는 [bool](../keywords/bool.md) 피연산자의 논리 OR을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-103">The conditional logical OR operator `||`, also known as the "short-circuiting" logical OR operator, computes the logical OR of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="6f6ff-104">`x` 또는 `y`가 `true`로 평가되면 `x || y`의 결과는 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-104">The result of `x || y` is `true` if either `x` or `y` evaluates to `true`.</span></span> <span data-ttu-id="6f6ff-105">그렇지 않으면 결과는 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="6f6ff-106">첫 번째 피연산자가 `true`로 평가되면 두 번째 피연산자는 평가되지 않고 작업 결과는 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-106">If the first operand evaluates to `true`, the second operand is not evaluated and the result of operation is `true`.</span></span> <span data-ttu-id="6f6ff-107">다음 예제에서는 해당 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

<span data-ttu-id="6f6ff-108">[논리 OR 연산자](or-operator.md) `|`도 해당 `bool` 피연산자의 논리 OR을 계산하지만 항상 두 피연산자를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-108">The [logical OR operator](or-operator.md) `|` also computes the logical OR of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="6f6ff-109">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="6f6ff-109">Operator overloadability</span></span>

<span data-ttu-id="6f6ff-110">사용자 정의 형식으로 조건부 논리 OR 연산자를 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-110">A user-defined type cannot overload the conditional logical OR operator.</span></span> <span data-ttu-id="6f6ff-111">그러나 사용자 정의 형식이 특정 방식으로 [논리 OR](or-operator.md), [true](../keywords/true-operator.md) 및 [false](../keywords/false-operator.md) 연산자를 오버로드하는 경우 `||` 작업은 해당 형식의 피연산자에 대해 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-111">However, if a user-defined type overloads the [logical OR](or-operator.md), [true](../keywords/true-operator.md), and [false](../keywords/false-operator.md) operators in a certain way, the `||` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="6f6ff-112">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [사용자 정의 조건부 논리 연산자](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="6f6ff-113">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="6f6ff-113">C# language specification</span></span>

<span data-ttu-id="6f6ff-114">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [조건부 논리 연산자](~/_csharplang/spec/expressions.md#conditional-logical-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6f6ff-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6f6ff-115">See also</span></span>

- [<span data-ttu-id="6f6ff-116">C# 참조</span><span class="sxs-lookup"><span data-stu-id="6f6ff-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="6f6ff-117">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="6f6ff-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="6f6ff-118">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="6f6ff-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="6f6ff-119">&& 연산자</span><span class="sxs-lookup"><span data-stu-id="6f6ff-119">&& operator</span></span>](conditional-and-operator.md)
- [! 연산자]<span data-ttu-id="6f6ff-120">(logical-negation-operator.md)</span><span class="sxs-lookup"><span data-stu-id="6f6ff-120">(logical-negation-operator.md)</span></span>
- [<span data-ttu-id="6f6ff-121">| 연산자</span><span class="sxs-lookup"><span data-stu-id="6f6ff-121">| operator</span></span>](or-operator.md)
