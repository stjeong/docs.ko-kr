---
title: '! 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 02/14/2019
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 464bd658c9bf430191d84d3d5ad8d57173ab87c5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303714"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="976a2-103">!</span><span class="sxs-lookup"><span data-stu-id="976a2-103">!</span></span> <span data-ttu-id="976a2-104">연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="976a2-104">operator (C# Reference)</span></span>

<span data-ttu-id="976a2-105">논리적 부정 연산자 `!`는 해당 [bool](../keywords/bool.md) 피연산자의 논리적 부정을 계산하는 단항 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="976a2-105">The logical negation operator `!` is a unary operator that computes logical negation of its [bool](../keywords/bool.md) operand.</span></span> <span data-ttu-id="976a2-106">즉, 피연산자가 `false`인 경우 `true`를 생성하고, 피연산자가 `true`인 경우 `false`를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="976a2-106">That is, it produces `true`, if the operand is `false`, and `false`, if the operand is `true`:</span></span>

[!code-csharp-interactive[logical negation](~/samples/snippets/csharp/language-reference/operators/LogicalNegationExamples.cs#Example)]

## <a name="operator-overloadability"></a><span data-ttu-id="976a2-107">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="976a2-107">Operator overloadability</span></span>

<span data-ttu-id="976a2-108">사용자 정의 형식은 `!` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="976a2-108">User-defined types can [overload](../keywords/operator.md) the `!` operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="976a2-109">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="976a2-109">C# language specification</span></span>

<span data-ttu-id="976a2-110">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [논리적 부정 연산자](~/_csharplang/spec/expressions.md#logical-negation-operator) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="976a2-110">For more information, see the [Logical negation operator](~/_csharplang/spec/expressions.md#logical-negation-operator) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="976a2-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="976a2-111">See also</span></span>

- [<span data-ttu-id="976a2-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="976a2-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="976a2-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="976a2-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="976a2-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="976a2-114">C# Operators</span></span>](index.md)