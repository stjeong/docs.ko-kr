---
title: /= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: ed4dd6c0c944b77543aae4de8d51534b4df4f4ef
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286522"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="e24be-102">/= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="e24be-102">/= Operator (C# Reference)</span></span>

<span data-ttu-id="e24be-103">나누기 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-103">The division assignment operator.</span></span>

<span data-ttu-id="e24be-104">다음과 같은 `/=` 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="e24be-104">An expression using the `/=` operator, such as</span></span>

```csharp
x /= y
```

<span data-ttu-id="e24be-105">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-105">is equivalent to</span></span>

```csharp
x = x / y
```

<span data-ttu-id="e24be-106">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="e24be-107">[나누기 연산자](division-operator.md) `/`는 두 번째 피연산자로 첫 번째 피연산자를 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-107">The [division operator](division-operator.md) `/` divides its first operand by its second operand.</span></span> <span data-ttu-id="e24be-108">모든 숫자 형식에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="e24be-109">다음 예제에서는 `/=` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-109">The following example demonstrates the usage of the `/=` operator:</span></span>

[!code-csharp-interactive[divide and assign](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#DivisionAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="e24be-110">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="e24be-110">Operator overloadability</span></span>

<span data-ttu-id="e24be-111">사용자 정의 형식이 [나누기 연산자](division-operator.md) `/`를 [오버로드](../keywords/operator.md)하면 나누기 대입 연산자 `/=`는 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-111">If a user-defined type [overloads](../keywords/operator.md) the [division operator](division-operator.md) `/`, the division assignment operator `/=` is implicitly overloaded.</span></span> <span data-ttu-id="e24be-112">사용자 정의 형식에는 나누기 대입 연산자를 명시적으로 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e24be-112">A user-defined type cannot explicitly overload the division assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="e24be-113">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="e24be-113">C# language specification</span></span>

<span data-ttu-id="e24be-114">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [복합 할당](~/_csharplang/spec/expressions.md#compound-assignment) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e24be-114">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e24be-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e24be-115">See also</span></span>

- [<span data-ttu-id="e24be-116">C# 참조</span><span class="sxs-lookup"><span data-stu-id="e24be-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="e24be-117">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="e24be-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="e24be-118">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="e24be-118">C# Operators</span></span>](index.md)
