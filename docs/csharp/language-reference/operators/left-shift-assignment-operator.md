---
title: <<= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: d2105fbee4ddfe1b2cb3325d82b0f2f8c5559297
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219453"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="93cbe-102">\<\<= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="93cbe-102">\<\<= operator (C# Reference)</span></span>

<span data-ttu-id="93cbe-103">왼쪽 시프트 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-103">The left-shift assignment operator.</span></span>

<span data-ttu-id="93cbe-104">다음과 같은 `<<=` 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="93cbe-104">An expression using the `<<=` operator, such as</span></span>

```csharp
x <<= y
```

<span data-ttu-id="93cbe-105">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-105">is equivalent to</span></span>

```csharp
x = x << y
```

<span data-ttu-id="93cbe-106">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="93cbe-107">[`<<` 연산자](left-shift-operator.md)는 첫 번째 피연산자를 두 번째 피연산자로 정의된 비트 수만큼 왼쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-107">The [`<<` operator](left-shift-operator.md) shifts its first operand left by the number of bits defined by its second operand.</span></span>

<span data-ttu-id="93cbe-108">다음 예제에서는 `<<=` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-108">The following example demonstrates the usage of the `<<=` operator:</span></span>

[!code-csharp-interactive[left shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="93cbe-109">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="93cbe-109">Operator overloadability</span></span>

<span data-ttu-id="93cbe-110">사용자 정의 형식으로 [`<<` 연산자](left-shift-operator.md)를 [오버로드](../keywords/operator.md)하면 왼쪽 시프트 대입 연산자`<<=`는 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-110">If a user-defined type [overloads](../keywords/operator.md) the [`<<` operator](left-shift-operator.md), the left-shift assignment operator `<<=` is implicitly overloaded.</span></span> <span data-ttu-id="93cbe-111">사용자 정의 형식에는 왼쪽 시프트 대입 연산자를 명시적으로 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="93cbe-111">A user-defined type cannot explicitly overload the left-shift assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="93cbe-112">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="93cbe-112">C# language specification</span></span>

<span data-ttu-id="93cbe-113">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [복합 할당](~/_csharplang/spec/expressions.md#compound-assignment) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93cbe-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="93cbe-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="93cbe-114">See also</span></span>

- [<span data-ttu-id="93cbe-115">C# 참조</span><span class="sxs-lookup"><span data-stu-id="93cbe-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="93cbe-116">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="93cbe-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="93cbe-117">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="93cbe-117">C# Operators</span></span>](index.md)
