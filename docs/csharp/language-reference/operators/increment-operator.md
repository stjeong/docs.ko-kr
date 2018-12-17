---
title: ++ 연산자(C# 참조)
ms.date: 11/26/2018
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: b29f4f1ab00c0f8026f118cb72b090e3b728bfc5
ms.sourcegitcommit: 6ae7cdd0437a32884556dd4826ca90e957b7a4e3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/06/2018
ms.locfileid: "48030472"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="4ce1a-102">++ 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="4ce1a-102">++ Operator (C# Reference)</span></span>

<span data-ttu-id="4ce1a-103">단항 증가 연산자(`++`)는 피연산자를 1씩 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-103">The unary increment operator `++` increments its operand by 1.</span></span> <span data-ttu-id="4ce1a-104">후위 증가 연산자 `x++` 및 전위 증가 연산자 `++x`의 두 가지 형태로 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-104">It's supported in two forms: the postfix increment operator, `x++`, and the prefix increment operator, `++x`.</span></span>

## <a name="postfix-increment-operator"></a><span data-ttu-id="4ce1a-105">후위 증가 연산자</span><span class="sxs-lookup"><span data-stu-id="4ce1a-105">Postfix increment operator</span></span>

<span data-ttu-id="4ce1a-106">`x++`의 결과는 다음 예제와 같이 연산 ‘전’ `x`의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-106">The result of `x++` is the value of `x` *before* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[postfix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixIncrement)]

## <a name="prefix-increment-operator"></a><span data-ttu-id="4ce1a-107">후위 증가 연산자</span><span class="sxs-lookup"><span data-stu-id="4ce1a-107">Prefix increment operator</span></span>

<span data-ttu-id="4ce1a-108">`++x`의 결과는 다음 예제와 같이 연산 ‘후’ `x`의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-108">The result of `++x` is the value of `x` *after* the operation, as the following example shows:</span></span>

[!code-csharp-interactive[prefix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixIncrement)]

## <a name="remarks"></a><span data-ttu-id="4ce1a-109">설명</span><span class="sxs-lookup"><span data-stu-id="4ce1a-109">Remarks</span></span>

<span data-ttu-id="4ce1a-110">증가 연산자는 모든 [정수 형식](../keywords/integral-types-table.md)([char](../keywords/char.md) 형식 포함), [부동 소수점 형식](../keywords/floating-point-types-table.md) 및 모든 [열거형](../keywords/enum.md) 형식에 대해 미리 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-110">The increment operator is predefined for all [integral types](../keywords/integral-types-table.md) (including the [char](../keywords/char.md) type), [floating-point types](../keywords/floating-point-types-table.md), and any [enum](../keywords/enum.md) type.</span></span>

<span data-ttu-id="4ce1a-111">증가 연산자의 피연산자는 변수, [속성](../../programming-guide/classes-and-structs/properties.md) 액세스 또는 [인덱서](../../../csharp/programming-guide/indexers/index.md) 액세스여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-111">An operand of the increment operator must be a variable, a [property](../../programming-guide/classes-and-structs/properties.md) access, or an [indexer](../../../csharp/programming-guide/indexers/index.md) access.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="4ce1a-112">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="4ce1a-112">Operator overloadability</span></span>

<span data-ttu-id="4ce1a-113">사용자 정의 형식은 `++` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-113">User-defined types can [overload](../keywords/operator.md) the `++` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="4ce1a-114">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="4ce1a-114">C# language specification</span></span>

<span data-ttu-id="4ce1a-115">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [후위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) 및 [전위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-115">For more information, see the [Postfix increment and decrement operators](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) and [Prefix increment and decrement operators](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4ce1a-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4ce1a-116">See also</span></span>

- [<span data-ttu-id="4ce1a-117">C# 참조</span><span class="sxs-lookup"><span data-stu-id="4ce1a-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="4ce1a-118">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="4ce1a-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4ce1a-119">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="4ce1a-119">C# Operators</span></span>](index.md)
- [<span data-ttu-id="4ce1a-120">-- 연산자</span><span class="sxs-lookup"><span data-stu-id="4ce1a-120">-- Operator</span></span>](decrement-operator.md)
- [<span data-ttu-id="4ce1a-121">방법: 포인터 증가 및 감소</span><span class="sxs-lookup"><span data-stu-id="4ce1a-121">How to: increment and decrement pointers</span></span>](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
