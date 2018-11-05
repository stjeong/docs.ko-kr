---
title: + 연산자(C# 참조)
ms.date: 10/22/2018
f1_keywords:
- +_CSharpKeyword
helpviewer_keywords:
- + operator [C#]
- concatenation operator [C#]
- addition operator [C#]
ms.assetid: 93e56486-bb42-43c1-bd43-60af11e64e67
ms.openlocfilehash: ae2774d96bc50afa271fffdea445e640e68c3647
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192306"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="97b8a-102">+ 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="97b8a-102">+ Operator (C# Reference)</span></span>

<span data-ttu-id="97b8a-103">`+` 연산자는 두 개의 형식인 단항 더하기 연산자 또는 이항 더하기 연산자에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-103">The `+` operator is supported in two forms: a unary plus operator or a binary addition operator.</span></span>

<span data-ttu-id="97b8a-104">사용자 정의 형식은 단항 및 이항 `+` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-104">User-defined types can [overload](../keywords/operator.md) the unary and binary `+` operators.</span></span> <span data-ttu-id="97b8a-105">이항 `+` 연산자가 오버로드되면 [더하기 대입 연산자](addition-assignment-operator.md) `+=`도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-105">When a binary `+` operator is overloaded, the [addition assignment operator](addition-assignment-operator.md) `+=` is also implicitly overloaded.</span></span>

## <a name="unary-plus-operator"></a><span data-ttu-id="97b8a-106">단항 더하기 연산자</span><span class="sxs-lookup"><span data-stu-id="97b8a-106">Unary plus operator</span></span>

<span data-ttu-id="97b8a-107">단항 `+` 연산자는 피연산자의 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-107">The unary `+` operator returns the value of its operand.</span></span> <span data-ttu-id="97b8a-108">모든 숫자 형식에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-108">It's supported by all numeric types.</span></span>

## <a name="numeric-addition"></a><span data-ttu-id="97b8a-109">숫자 더하기</span><span class="sxs-lookup"><span data-stu-id="97b8a-109">Numeric addition</span></span>

<span data-ttu-id="97b8a-110">숫자 형식의 경우 `+` 연산자는 해당 피연산자의 합계를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-110">For numeric types, the `+` operator computes the sum of its operands:</span></span>

[!code-csharp-interactive[numeric addition](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddNumerics)]

## <a name="string-concatenation"></a><span data-ttu-id="97b8a-111">문자열 연결</span><span class="sxs-lookup"><span data-stu-id="97b8a-111">String concatenation</span></span>

<span data-ttu-id="97b8a-112">피연산자 중 하나 또는 둘 다가 [문자열](../keywords/string.md) 형식이면 `+` 연산자는 피연산자의 문자열 표현을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-112">When one or both operands are of type [string](../keywords/string.md), the `+` operator concatenates the string representations of its operands:</span></span>

[!code-csharp-interactive[string concatenation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddStrings)]

<span data-ttu-id="97b8a-113">C# 6부터 [문자열 보간](../tokens/interpolated.md)은 문자열 형식을 지정하는 더욱 편리한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-113">Starting with C# 6, [string interpolation](../tokens/interpolated.md) provides a more convenient way to format strings:</span></span>

[!code-csharp-interactive[string interpolation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#UseStringInterpolation)]

## <a name="delegate-combination"></a><span data-ttu-id="97b8a-114">대리자 조합</span><span class="sxs-lookup"><span data-stu-id="97b8a-114">Delegate combination</span></span>

<span data-ttu-id="97b8a-115">[대리자](../keywords/delegate.md) 형식의 경우 `+` 연산자는 호출될 때 첫 번째 피연산자를 호출한 후 두 번째 피연산자를 호출하는 새 대리자 인스턴스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-115">For [delegate](../keywords/delegate.md) types, the `+` operator returns a new delegate instance that, when invoked, invokes the first operand and then invokes the second operand.</span></span> <span data-ttu-id="97b8a-116">피연산자 중 하나라도 `null`이면 `+` 연산자는 다른 피연산자(`null`일 수도 있음)의 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-116">If any of the operands is `null`, the `+` operator returns the value of another operand (which also might be `null`).</span></span> <span data-ttu-id="97b8a-117">다음 예제는 `+` 연산자를 사용하여 대리자를 결합하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="97b8a-117">The following example shows how delegates can be combined with the `+` operator:</span></span>

[!code-csharp-interactive[delegate combination](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddDelegates)]

<span data-ttu-id="97b8a-118">대리자 형식에 대한 자세한 내용은 [대리자](../../programming-guide/delegates/index.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="97b8a-118">For more information about delegate types, see [Delegates](../../programming-guide/delegates/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="97b8a-119">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="97b8a-119">C# language specification</span></span>

<span data-ttu-id="97b8a-120">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [단항 더하기 연산자](~/_csharplang/spec/expressions.md#unary-plus-operator) 및 [더하기 연산자](~/_csharplang/spec/expressions.md#addition-operator) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="97b8a-120">For more information, see the [Unary plus operator](~/_csharplang/spec/expressions.md#unary-plus-operator) and [Addition operator](~/_csharplang/spec/expressions.md#addition-operator) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="97b8a-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="97b8a-121">See also</span></span>

- [<span data-ttu-id="97b8a-122">C# 참조</span><span class="sxs-lookup"><span data-stu-id="97b8a-122">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="97b8a-123">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="97b8a-123">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="97b8a-124">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="97b8a-124">C# Operators</span></span>](index.md)
- [<span data-ttu-id="97b8a-125">문자열 보간</span><span class="sxs-lookup"><span data-stu-id="97b8a-125">String interpolation</span></span>](../tokens/interpolated.md)
- [<span data-ttu-id="97b8a-126">방법: 여러 문자열 연결</span><span class="sxs-lookup"><span data-stu-id="97b8a-126">How to: Concatenate Multiple Strings</span></span>](../../how-to/concatenate-multiple-strings.md)
- [<span data-ttu-id="97b8a-127">대리자</span><span class="sxs-lookup"><span data-stu-id="97b8a-127">Delegates</span></span>](../../programming-guide/delegates/index.md)
- [<span data-ttu-id="97b8a-128">Checked 및 Unchecked</span><span class="sxs-lookup"><span data-stu-id="97b8a-128">Checked and unchecked</span></span>](../keywords/checked-and-unchecked.md)
