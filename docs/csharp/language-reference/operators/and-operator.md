---
title: '&amp; 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
ms.openlocfilehash: a799c0e37d6607e8ff72ab984ff5e540a4e11063
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236377"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="37118-102">&amp; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="37118-102">&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="37118-103">`&` 연산자는 단항 주소 연산자 또는 이진 논리 연산자의 두 가지 형식으로 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="37118-103">The `&` operator is supported in two forms: a unary address-of operator or a binary logical operator.</span></span>

## <a name="unary-address-of-operator"></a><span data-ttu-id="37118-104">단항 주소 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-104">Unary address-of operator</span></span>

<span data-ttu-id="37118-105">단항 `&` 연산자는 해당 피연산자의 주소를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-105">The unary `&` operator returns the address of its operand.</span></span> <span data-ttu-id="37118-106">자세한 내용은 [방법: 변수의 주소 가져오기](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-address-of-a-variable.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37118-106">For more information, see [How to: obtain the address of a variable](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-address-of-a-variable.md).</span></span>

<span data-ttu-id="37118-107">주소 연산자 `&`에 [안전하지 않은](../keywords/unsafe.md) 컨텍스트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-107">The address-of operator `&` requires [unsafe](../keywords/unsafe.md) context.</span></span>

## <a name="integer-logical-bitwise-and-operator"></a><span data-ttu-id="37118-108">정수 논리적 비트 AND 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-108">Integer logical bitwise AND operator</span></span>

<span data-ttu-id="37118-109">정수 형식의 경우 `&` 연산자는 해당 피연산자의 논리적 비트 AND를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-109">For integer types, the `&` operator computes the logical bitwise AND of its operands:</span></span>

[!code-csharp-interactive[integer logical bitwise AND](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#IntegerOperands)]

> [!NOTE]
> <span data-ttu-id="37118-110">앞의 예제에서는 [C# 7.0에서 도입](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements)되고 [C# 7.2에서 향상](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals)된 이진 리터럴을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-110">The preceding example uses the binary literals [introduced in C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) and [enhanced in C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span></span>

<span data-ttu-id="37118-111">정수 형식에 대한 작업은 일반적으로 열거형 형식에서 허용되므로 `&` 연산자는 [enum](../keywords/enum.md) 피연산자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-111">Because operations on integer types are generally allowed on enumeration types, the `&` operator also supports [enum](../keywords/enum.md) operands.</span></span>

## <a name="boolean-logical-and-operator"></a><span data-ttu-id="37118-112">부울 논리 AND 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-112">Boolean logical AND operator</span></span>

<span data-ttu-id="37118-113">[bool](../keywords/bool.md) 피연산자의 경우 `&` 연산자는 피 연산자의 논리 AND를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-113">For [bool](../keywords/bool.md) operands, the `&` operator computes the logical AND of its operands.</span></span> <span data-ttu-id="37118-114">`x` 및 `y`가 모두 `true`인 경우 `x & y`의 결과는 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="37118-114">The result of `x & y` is `true` if both `x` and `y` are `true`.</span></span> <span data-ttu-id="37118-115">그렇지 않으면 결과는 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="37118-115">Otherwise, the result is `false`.</span></span>

<span data-ttu-id="37118-116">첫 번째 피연산자가 `false`로 평가되더라도 `&` 연산자는 두 피연산자를 평가하여 두 번째 피연산자의 값에 관계없이 `false`이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-116">The `&` operator evaluates both operands even if the first operand evaluates to `false`, so that the result must be `false` regardless of the value of the second operand.</span></span> <span data-ttu-id="37118-117">다음 예제에서는 해당 동작을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="37118-117">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[bool logical AND](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#BooleanOperands)]

<span data-ttu-id="37118-118">[조건부 AND 연산자](conditional-and-operator.md) `&&`도 해당 피연산자의 논리 AND를 계산하지만, 첫 번째 피연산자가 `true`로 평가되는 경우에만 두 번째 피연산자를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-118">The [conditional AND operator](conditional-and-operator.md) `&&` also computes the logical AND of its operands, but evaluates the second operand only if the first operand evaluates to `true`.</span></span>

<span data-ttu-id="37118-119">nullable bool 피연산자의 경우 `&` 연산자는 동작은 SQL의 값이 세 개인 논리와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="37118-119">For nullable bool operands, the behavior of the `&` operator is consistent with SQL's three-valued logic.</span></span> <span data-ttu-id="37118-120">자세한 내용은 [nullable 형식 사용](../../programming-guide/nullable-types/using-nullable-types.md)의 [bool? 형식](../../programming-guide/nullable-types/using-nullable-types.md#the-bool-type)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37118-120">For more information, see the [The bool? type](../../programming-guide/nullable-types/using-nullable-types.md#the-bool-type) section of the [Using nullable types](../../programming-guide/nullable-types/using-nullable-types.md) article.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="37118-121">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="37118-121">Operator overloadability</span></span>

<span data-ttu-id="37118-122">사용자 정의 형식에는 이진 `&` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37118-122">User-defined types can [overload](../keywords/operator.md) the binary `&` operator.</span></span> <span data-ttu-id="37118-123">이진 `&` 연산자가 오버로드되면 [AND 할당 연산자](and-assignment-operator.md) `&=`도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="37118-123">When a binary `&` operator is overloaded, the [AND assignment operator](and-assignment-operator.md) `&=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="37118-124">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="37118-124">C# language specification</span></span>

<span data-ttu-id="37118-125">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [주소 연산자](~/_csharplang/spec/unsafe-code.md#the-address-of-operator) 및 [논리 연산자](~/_csharplang/spec/expressions.md#logical-operators) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37118-125">For more information, see [The address-of operator](~/_csharplang/spec/unsafe-code.md#the-address-of-operator) and [Logical operators](~/_csharplang/spec/expressions.md#logical-operators) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="37118-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="37118-126">See also</span></span>

- [<span data-ttu-id="37118-127">C# 참조</span><span class="sxs-lookup"><span data-stu-id="37118-127">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="37118-128">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="37118-128">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="37118-129">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-129">C# Operators</span></span>](index.md)
- [<span data-ttu-id="37118-130">포인터 형식</span><span class="sxs-lookup"><span data-stu-id="37118-130">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="37118-131">| 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-131">| operator</span></span>](or-operator.md)
- [<span data-ttu-id="37118-132">^ 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-132">^ operator</span></span>](xor-operator.md)
- [<span data-ttu-id="37118-133">~ 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-133">~ operator</span></span>](bitwise-complement-operator.md)
- [<span data-ttu-id="37118-134">&& 연산자</span><span class="sxs-lookup"><span data-stu-id="37118-134">&& operator</span></span>](conditional-and-operator.md)
