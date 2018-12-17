---
title: -- 연산자(C# 참조)
ms.date: 11/26/2018
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 0858321d6fe192a55bc548f169c558542238a981
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153341"
---
# <a name="---operator-c-reference"></a><span data-ttu-id="b2454-102">-- 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="b2454-102">-- Operator (C# Reference)</span></span>

<span data-ttu-id="b2454-103">단항 감소 연산자(`--`)는 피연산자를 1씩 감소합니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-103">The unary decrement operator `--` decrements its operand by 1.</span></span> <span data-ttu-id="b2454-104">후위 감소 연산자 `x--` 및 전위 감소 연산자 `--x`의 두 가지 형태로 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-104">It's supported in two forms: the postfix decrement operator, `x--`, and the prefix decrement operator, `--x`.</span></span>

## <a name="postfix-decrement-operator"></a><span data-ttu-id="b2454-105">후위 감소 연산자</span><span class="sxs-lookup"><span data-stu-id="b2454-105">Postfix decrement operator</span></span>

<span data-ttu-id="b2454-106">`x--`의 결과는 다음 예제와 같이 연산 ‘전’ `x`의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-106">The result of `x--` is the value of `x` *before* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[postfix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixDecrement)]

## <a name="prefix-decrement-operator"></a><span data-ttu-id="b2454-107">후위 감소 연산자</span><span class="sxs-lookup"><span data-stu-id="b2454-107">Prefix decrement operator</span></span>

<span data-ttu-id="b2454-108">`--x`의 결과는 다음 예제와 같이 연산 ‘후’ `x`의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-108">The result of `--x` is the value of `x` *after* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[prefix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixDecrement)]

## <a name="remarks"></a><span data-ttu-id="b2454-109">설명</span><span class="sxs-lookup"><span data-stu-id="b2454-109">Remarks</span></span>

<span data-ttu-id="b2454-110">감소 연산자는 모든 [정수 형식](../keywords/integral-types-table.md)([char](../keywords/char.md) 형식 포함), [부동 소수점 형식](../keywords/floating-point-types-table.md) 및 모든 [열거형](../keywords/enum.md) 형식에 대해 미리 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-110">The decrement operator is predefined for all [integral types](../keywords/integral-types-table.md) (including the [char](../keywords/char.md) type), [floating-point types](../keywords/floating-point-types-table.md), and any [enum](../keywords/enum.md) type.</span></span>

<span data-ttu-id="b2454-111">감소 연산자의 피연산자는 변수, [속성](../../programming-guide/classes-and-structs/properties.md) 액세스 또는 [인덱서](../../../csharp/programming-guide/indexers/index.md) 액세스여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-111">An operand of the decrement operator must be a variable, a [property](../../programming-guide/classes-and-structs/properties.md) access, or an [indexer](../../../csharp/programming-guide/indexers/index.md) access.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="b2454-112">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="b2454-112">Operator overloadability</span></span>

<span data-ttu-id="b2454-113">사용자 정의 형식은 `--` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2454-113">User-defined types can [overload](../keywords/operator.md) the `--` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b2454-114">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="b2454-114">C# language specification</span></span>

<span data-ttu-id="b2454-115">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [후위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) 및 [전위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b2454-115">For more information, see the [Postfix increment and decrement operators](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) and [Prefix increment and decrement operators](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b2454-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b2454-116">See also</span></span>

- [<span data-ttu-id="b2454-117">C# 참조</span><span class="sxs-lookup"><span data-stu-id="b2454-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b2454-118">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="b2454-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b2454-119">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="b2454-119">C# Operators</span></span>](index.md)
- [<span data-ttu-id="b2454-120">++ 연산자</span><span class="sxs-lookup"><span data-stu-id="b2454-120">++ Operator</span></span>](increment-operator.md)
- [<span data-ttu-id="b2454-121">방법: 포인터 증가 및 감소</span><span class="sxs-lookup"><span data-stu-id="b2454-121">How to: increment and decrement pointers</span></span>](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
