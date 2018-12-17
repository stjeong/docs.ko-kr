---
title: ~ 연산자(C# 참조)
ms.date: 11/05/2018
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 1bcb07c5639a098e3a8c566e92083ca0d48efb81
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153217"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="e526c-102">~ 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="e526c-102">~ Operator (C# Reference)</span></span>

<span data-ttu-id="e526c-103">비트 보수 연산자 `~`는 각 비트를 반대로 하여 피연산자의 비트 단위 보수를 생성하는 단항 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="e526c-103">The bitwise complement operator `~` is a unary operator that produces a bitwise complement of its operand by reversing each bit.</span></span> <span data-ttu-id="e526c-104">모든 정수 형식은 `~` 연산자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e526c-104">All integer types support the `~` operator.</span></span>

> [!NOTE]
> <span data-ttu-id="e526c-105">또한 `~` 기호는 종료자를 선언하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e526c-105">The `~` symbol is also used to declare finalizers.</span></span> <span data-ttu-id="e526c-106">자세한 내용은 [종료자](../../programming-guide/classes-and-structs/destructors.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e526c-106">For more information, see [Finalizers](../../programming-guide/classes-and-structs/destructors.md).</span></span>

<span data-ttu-id="e526c-107">다음 예제에서는 `~` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e526c-107">The following example demonstrates the usage of the `~` operator:</span></span>

[!code-csharp-interactive[bitwise NOT](~/samples/snippets/csharp/language-reference/operators/BitwiseComplementExamples.cs#Example)]

> [!NOTE]
> <span data-ttu-id="e526c-108">앞의 예제에서는 [C# 7.0에서 도입](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements)되고 [C# 7.2에서 향상](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals)된 이진 리터럴을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e526c-108">The preceding example uses the binary literals [introduced in C# 7.0](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements) and [enhanced  in C# 7.2](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="e526c-109">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="e526c-109">Operator overloadability</span></span>

<span data-ttu-id="e526c-110">사용자 정의 형식은 `~` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e526c-110">User-defined types can [overload](../keywords/operator.md) the `~` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="e526c-111">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="e526c-111">C# language specification</span></span>

<span data-ttu-id="e526c-112">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [비트 보수 연산자](~/_csharplang/spec/expressions.md#bitwise-complement-operator) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e526c-112">For more information, see the [Bitwise complement operator](~/_csharplang/spec/expressions.md#bitwise-complement-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e526c-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e526c-113">See also</span></span>

- [<span data-ttu-id="e526c-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="e526c-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="e526c-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="e526c-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="e526c-116">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="e526c-116">C# Operators</span></span>](index.md)
- [<span data-ttu-id="e526c-117">종료자</span><span class="sxs-lookup"><span data-stu-id="e526c-117">Finalizers</span></span>](../../programming-guide/classes-and-structs/destructors.md)
- [<span data-ttu-id="e526c-118">& 연산자</span><span class="sxs-lookup"><span data-stu-id="e526c-118">& operator</span></span>](and-operator.md)
- [<span data-ttu-id="e526c-119">| 연산자</span><span class="sxs-lookup"><span data-stu-id="e526c-119">| operator</span></span>](or-operator.md)
- [<span data-ttu-id="e526c-120">^ 연산자</span><span class="sxs-lookup"><span data-stu-id="e526c-120">^ operator</span></span>](xor-operator.md)
