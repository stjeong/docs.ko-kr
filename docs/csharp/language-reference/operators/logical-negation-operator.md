---
title: '! 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 6b6d1796032f536aac0be49d4f101c1380b4e98f
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333228"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="3e72c-103">!</span><span class="sxs-lookup"><span data-stu-id="3e72c-103">!</span></span> <span data-ttu-id="3e72c-104">연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="3e72c-104">operator (C# Reference)</span></span>

<span data-ttu-id="3e72c-105">논리적 부정 연산자(`!`)는 해당 피연산자를 부정하는 단항 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="3e72c-105">The logical negation operator (`!`) is a unary operator that negates its operand.</span></span> <span data-ttu-id="3e72c-106">`bool`에 대해 정의되며, 해당 피연산자가 `false`인 경우에만 `true`를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3e72c-106">It is defined for `bool` and returns `true` if and only if its operand is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e72c-107">주의</span><span class="sxs-lookup"><span data-stu-id="3e72c-107">Remarks</span></span>

<span data-ttu-id="3e72c-108">사용자 정의 형식은 `!` 연산자를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="3e72c-108">User-defined types can overload the `!` operator (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="3e72c-109">예제</span><span class="sxs-lookup"><span data-stu-id="3e72c-109">Example</span></span>

[!code-csharp[csRefOperators#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#7)]

## <a name="see-also"></a><span data-ttu-id="3e72c-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3e72c-110">See also</span></span>

- [<span data-ttu-id="3e72c-111">C# 참조</span><span class="sxs-lookup"><span data-stu-id="3e72c-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3e72c-112">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="3e72c-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3e72c-113">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="3e72c-113">C# Operators</span></span>](index.md)