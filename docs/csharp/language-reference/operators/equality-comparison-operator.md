---
title: == 연산자 - C# 참조
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- ==_CSharpKeyword
helpviewer_keywords:
- == operator [C#]
- equality operator [C#]
ms.assetid: 34c6b597-caa2-4855-a7cd-38ecdd11bd07
ms.openlocfilehash: 6d86348eefc87e847267f262141ff49e5d51faae
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53655961"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="ecff4-102">== 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="ecff4-102">== Operator (C# Reference)</span></span>

<span data-ttu-id="ecff4-103">같음 연산자 `==`는 피연산자가 같으면 `true`를 반환하고, 그렇지 않으면 `false`를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-103">The equality operator `==` returns `true` if its operands are equal, `false` otherwise.</span></span>

## <a name="value-types-equality"></a><span data-ttu-id="ecff4-104">값 형식 같음</span><span class="sxs-lookup"><span data-stu-id="ecff4-104">Value types equality</span></span>

<span data-ttu-id="ecff4-105">[기본 제공 값 형식](../keywords/value-types-table.md)의 피연산자는 해당 값이 같은 경우 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-105">Operands of the [built-in value types](../keywords/value-types-table.md) are equal if their values are equal:</span></span>

[!code-csharp-interactive[value types equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ValueTypesEquality)]

> [!NOTE]
> <span data-ttu-id="ecff4-106">관계형 연산자 `==`, `>`, `<`, `>=` 및 `<=`의 경우 피연산자 중 하나가 숫자(<xref:System.Double.NaN?displayProperty=nameWithType> 또는 <xref:System.Single.NaN?displayProperty=nameWithType>)가 아니s며 연산의 결과는 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="ecff4-107">이는 `NaN` 값이 다른 `double`(또는 `float`) 값보다 크거나, 작거나, 같지 않음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="ecff4-108">자세한 내용과 예제는 <xref:System.Double.NaN?displayProperty=nameWithType> 또는 <xref:System.Single.NaN?displayProperty=nameWithType> 참조 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecff4-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="ecff4-109">기본 정수 형식의 해당 값이 같은 경우 동일한 [열거형](../keywords/enum.md) 형식의 피연산자가 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-109">Two operands of the same [enum](../keywords/enum.md) type are equal if the corresponding values of the underlying integral type are equal.</span></span>

<span data-ttu-id="ecff4-110">기본적으로 `==` 연산자는 사용자 정의 [구조체](../keywords/struct.md) 형식에 대해 정의되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-110">By default, the `==` operator is not defined for a user-defined [struct](../keywords/struct.md) type.</span></span> <span data-ttu-id="ecff4-111">사용자 정의 형식은 `==` 연산자를 [오버로드](#operator-overloadability)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-111">A user-defined type can [overload](#operator-overloadability) the `==` operator.</span></span>

<span data-ttu-id="ecff4-112">C# 7.3부터는 `==` 및 [`!=`](not-equal-operator.md) 연산자가 C# [튜플](../../tuples.md)에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-112">Beginning with C# 7.3, the `==` and [`!=`](not-equal-operator.md) operators are supported by C# [tuples](../../tuples.md).</span></span> <span data-ttu-id="ecff4-113">자세한 내용은 [C# 튜플 형식](../../tuples.md) 문서의 [같음 및 튜플](../../tuples.md#equality-and-tuples) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecff4-113">For more information, see the [Equality and tuples](../../tuples.md#equality-and-tuples) section of the [C# tuple types](../../tuples.md) article.</span></span>

## <a name="string-equality"></a><span data-ttu-id="ecff4-114">문자열 같음</span><span class="sxs-lookup"><span data-stu-id="ecff4-114">String equality</span></span>

<span data-ttu-id="ecff4-115">두 개의 [문자열](../keywords/string.md) 피연산자가 모두 `null`이거나 두 문자열 인스턴스가 같은 길이고 각 문자 위치에 동일한 문자가 있을 때 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-115">Two [string](../keywords/string.md) operands are equal when both of them are `null` or both string instances are of the same length and have identical characters in each character position:</span></span>

[!code-csharp-interactive[string equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#StringEquality)]

<span data-ttu-id="ecff4-116">대/소문자 구분 서수 비교입니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-116">That is case-sensitive ordinal comparison.</span></span> <span data-ttu-id="ecff4-117">문자열을 비교하는 방법에 대한 자세한 내용은 [C#에서 문자열을 비교하는 방법](../../how-to/compare-strings.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecff4-117">For more information about how to compare strings, see [How to compare strings in C#](../../how-to/compare-strings.md).</span></span>

## <a name="reference-types-equality"></a><span data-ttu-id="ecff4-118">참조 형식 같음</span><span class="sxs-lookup"><span data-stu-id="ecff4-118">Reference types equality</span></span>

<span data-ttu-id="ecff4-119">동일한 개체를 참조하는 경우 `string` 참조 형식 피연산자가 아닌 두 개의 피연산자가 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-119">Two other than `string` reference type operands are equal when they refer to the same object:</span></span>

[!code-csharp-interactive[reference type equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ReferenceTypesEquality)]

<span data-ttu-id="ecff4-120">이 예제에서는 `==` 연산자가 사용자 정의 참조 형식에서 지원됨을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-120">The example shows that the `==` operator is supported by user-defined reference types.</span></span> <span data-ttu-id="ecff4-121">그러나 사용자 정의 참조 형식은 `==` 연산자를 오버로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-121">However, a user-defined reference type can overload the `==` operator.</span></span> <span data-ttu-id="ecff4-122">참조 형식이 `==` 연산자를 오버로드하는 경우 <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> 메서드를 사용하여 해당 형식의 두 참조가 동일한 개체를 참조하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-122">If a reference type overloads the `==` operator, use the <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> method to check if two references of that type refer to the same object.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="ecff4-123">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="ecff4-123">Operator overloadability</span></span>

<span data-ttu-id="ecff4-124">사용자 정의 형식은 `==` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-124">User-defined types can [overload](../keywords/operator.md) the `==` operator.</span></span> <span data-ttu-id="ecff4-125">형식이 같음 연산자 `==`를 오버로드하는 경우 [같지 않음 연산자](not-equal-operator.md) `!=`도 오버로드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecff4-125">If a type overloads the equality operator `==`, it must also overload the [inequality operator](not-equal-operator.md) `!=`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="ecff4-126">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="ecff4-126">C# language specification</span></span>

<span data-ttu-id="ecff4-127">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [관계형 및 형식 테스트 연산자](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecff4-127">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ecff4-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ecff4-128">See also</span></span>

- [<span data-ttu-id="ecff4-129">C# 참조</span><span class="sxs-lookup"><span data-stu-id="ecff4-129">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="ecff4-130">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="ecff4-130">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="ecff4-131">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="ecff4-131">C# Operators</span></span>](index.md)
- [<span data-ttu-id="ecff4-132">같음 비교</span><span class="sxs-lookup"><span data-stu-id="ecff4-132">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
