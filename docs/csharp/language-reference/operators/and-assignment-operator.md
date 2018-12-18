---
title: '&amp;= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 10/29/2018
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: 223d2f30ee77457e1f9d5304ec299517932499d0
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237027"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="f6cbc-102">&amp;= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="f6cbc-102">&amp;= Operator (C# Reference)</span></span>

<span data-ttu-id="f6cbc-103">AND 대입 연산자.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-103">The AND assignment operator.</span></span>

<span data-ttu-id="f6cbc-104">다음과 같은 `&=` 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="f6cbc-104">An expression using the `&=` operator, such as</span></span>

```csharp
x &= y
```

<span data-ttu-id="f6cbc-105">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-105">is equivalent to</span></span>

```csharp
x = x & y
```

<span data-ttu-id="f6cbc-106">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="f6cbc-107">정수 피연산자의 경우 [`&` 연산자](and-operator.md)는 피연산자의 비트 논리 AND를 계산합니다. [bool](../keywords/bool.md) 피연산자의 경우 피연산자의 논리 AND를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-107">For integer operands, the [`&` operator](and-operator.md) computes the bitwise logical AND of its operands; for [bool](../keywords/bool.md) operands, it computes the logical AND of its operands.</span></span>

<span data-ttu-id="f6cbc-108">다음 예제에서는 `&=` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-108">The following example demonstrates the usage of the `&=` operator:</span></span>

[!code-csharp-interactive[AND assignment example](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#AndAssignmentExample)]

## <a name="operator-overloadability"></a><span data-ttu-id="f6cbc-109">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="f6cbc-109">Operator overloadability</span></span>

<span data-ttu-id="f6cbc-110">사용자 정의 형식으로 [`&` 연산자 ](and-operator.md)를 [오버로드](../keywords/operator.md)하면 AND 대입 연산자 `&=`는 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-110">If a user-defined type [overloads](../keywords/operator.md) the [`&` operator](and-operator.md), the AND assignment operator `&=` is implicitly overloaded.</span></span> <span data-ttu-id="f6cbc-111">사용자 정의 형식에는 AND 대입 연산자를 명시적으로 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-111">A user-defined type cannot explicitly overload the AND assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="f6cbc-112">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="f6cbc-112">C# language specification</span></span>

<span data-ttu-id="f6cbc-113">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [복합 할당](~/_csharplang/spec/expressions.md#compound-assignment) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f6cbc-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f6cbc-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f6cbc-114">See also</span></span>

- [<span data-ttu-id="f6cbc-115">C# 참조</span><span class="sxs-lookup"><span data-stu-id="f6cbc-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="f6cbc-116">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="f6cbc-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="f6cbc-117">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="f6cbc-117">C# Operators</span></span>](index.md)
