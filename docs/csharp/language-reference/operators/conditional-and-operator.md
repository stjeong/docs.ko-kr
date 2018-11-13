---
title: '&amp;&amp; 연산자(C# 참조)'
ms.date: 11/06/2018
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: d0e6d9a5aedc7dc87393e3dea070bf442b3268dc
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "43529237"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="a247f-102">&amp;&amp; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="a247f-102">&amp;&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="a247f-103">"단락(short-circuiting)" 논리 AND 연산자로도 알려져 있는 조건부 논리 AND 연산자 `&&`는 [bool](../keywords/bool.md) 피연산자의 논리 AND를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-103">The conditional logical AND operator `&&`, also known as the "short-circuiting" logical AND operator, computes the logical AND of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="a247f-104">`x` 및 `y`가 모두 `true`로 평가되면 `x && y`의 결과는 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-104">The result of `x && y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="a247f-105">그렇지 않으면 결과는 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="a247f-106">첫 번째 피연산자가 `false`로 평가되면 두 번째 피연산자는 평가되지 않고 작업 결과는 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-106">If the first operand evaluates to `false`, the second operand is not evaluated and the result of operation is `false`.</span></span> <span data-ttu-id="a247f-107">다음 예제에서는 해당 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#And)]

<span data-ttu-id="a247f-108">[논리 AND 연산자](and-operator.md) `&`도 해당 `bool` 피연산자의 논리 AND를 계산하지만 항상 두 피연산자를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-108">The [logical AND operator](and-operator.md) `&` also computes the logical AND of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="a247f-109">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="a247f-109">Operator overloadability</span></span>

<span data-ttu-id="a247f-110">사용자 정의 형식에는 조건부 논리 AND 연산자를 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-110">A user-defined type cannot overload the conditional logical AND operator.</span></span> <span data-ttu-id="a247f-111">그러나 사용자 정의 형식이 특정 방식으로 [논리 AND](and-operator.md), [true](../keywords/true-operator.md) 및 [false](../keywords/false-operator.md) 연산자를 오버로드하는 경우 `&&` 작업은 해당 형식의 피연산자에 대해 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a247f-111">However, if a user-defined type overloads the [logical AND](and-operator.md), [true](../keywords/true-operator.md), and [false](../keywords/false-operator.md) operators in a certain way, the `&&` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="a247f-112">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [사용자 정의 조건부 논리 연산자](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a247f-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="a247f-113">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="a247f-113">C# language specification</span></span>

<span data-ttu-id="a247f-114">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [조건부 논리 연산자](~/_csharplang/spec/expressions.md#conditional-logical-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a247f-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a247f-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a247f-115">See also</span></span>

- [<span data-ttu-id="a247f-116">C# 참조</span><span class="sxs-lookup"><span data-stu-id="a247f-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a247f-117">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="a247f-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a247f-118">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="a247f-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="a247f-119">|| 연산자</span><span class="sxs-lookup"><span data-stu-id="a247f-119">|| operator</span></span>](conditional-or-operator.md)
- [! 연산자]<span data-ttu-id="a247f-120">(logical-negation-operator.md)</span><span class="sxs-lookup"><span data-stu-id="a247f-120">(logical-negation-operator.md)</span></span>
- [<span data-ttu-id="a247f-121">& 연산자</span><span class="sxs-lookup"><span data-stu-id="a247f-121">& operator</span></span>](and-operator.md)
