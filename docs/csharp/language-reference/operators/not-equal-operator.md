---
title: '!= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- '!=_CSharpKeyword'
helpviewer_keywords:
- inequality operator (!=) [C#]
- not equals operator (!=) [C#]
- '!= operator [C#]'
ms.assetid: eeff7a4e-ad6f-462d-9f8d-49e9b91c6c97
ms.openlocfilehash: 939b5664dba4345e62a43fb2f8d4d5379659d6aa
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610179"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="59364-102">!= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="59364-102">!= Operator (C# Reference)</span></span>

<span data-ttu-id="59364-103">같지 않음 연산자 `!=`는 피연산자가 같지 않으면 `true`를 반환하고, 그렇지 않으면 `false`를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="59364-103">The inequality operator `!=` returns `true` if its operands are not equal, `false` otherwise.</span></span> <span data-ttu-id="59364-104">[기본 제공 형식](../keywords/built-in-types-table.md)의 피연산자의 경우 식 `x != y`는 식 `!(x == y)`와 동일한 결과를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="59364-104">For the operands of the [built-in types](../keywords/built-in-types-table.md), the expression `x != y` produces the same result as the expression `!(x == y)`.</span></span> <span data-ttu-id="59364-105">자세한 내용은 [== 연산자](equality-comparison-operator.md) 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59364-105">For more information, see the [== Operator](equality-comparison-operator.md) article.</span></span>

<span data-ttu-id="59364-106">다음 예제에서는 `!=` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59364-106">The following example demonstrates the usage of the `!=` operator:</span></span>

[!code-csharp-interactive[non-equality examples](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#NonEquality)]

## <a name="operator-overloadability"></a><span data-ttu-id="59364-107">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="59364-107">Operator overloadability</span></span>

<span data-ttu-id="59364-108">사용자 정의 형식은 `!=` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59364-108">User-defined types can [overload](../keywords/operator.md) the `!=` operator.</span></span> <span data-ttu-id="59364-109">형식이 같지 않음 연산자 `!=`를 오버로드하는 경우 [같음 연산자](equality-comparison-operator.md) `==`도 오버로드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59364-109">If a type overloads the inequality operator `!=`, it must also overload the [equality operator](equality-comparison-operator.md) `==`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="59364-110">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="59364-110">C# language specification</span></span>

<span data-ttu-id="59364-111">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [관계형 및 형식 테스트 연산자](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59364-111">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="59364-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="59364-112">See also</span></span>

- [<span data-ttu-id="59364-113">C# 참조</span><span class="sxs-lookup"><span data-stu-id="59364-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="59364-114">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="59364-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="59364-115">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="59364-115">C# Operators</span></span>](index.md)
- [<span data-ttu-id="59364-116">같음 비교</span><span class="sxs-lookup"><span data-stu-id="59364-116">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
