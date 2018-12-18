---
title: continue 문 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- continue_CSharpKeyword
- continue
helpviewer_keywords:
- continue keyword [C#]
ms.assetid: 8a5ac96f-f98a-4519-b32d-345847ed7be0
ms.openlocfilehash: fbb5d170f10c0a4b6c6edeae6c3f4a549de65525
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243903"
---
# <a name="continue-c-reference"></a><span data-ttu-id="4a08e-102">continue(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="4a08e-102">continue (C# Reference)</span></span>

<span data-ttu-id="4a08e-103">`continue` 문은 자신이 나타나는 바깥쪽 [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md) 또는 [foreach](../../../csharp/language-reference/keywords/foreach-in.md) 문의 다음 반복으로 제어를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="4a08e-103">The `continue` statement passes control to the next iteration of the enclosing [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md), or [foreach](../../../csharp/language-reference/keywords/foreach-in.md) statement in which it appears.</span></span>

## <a name="example"></a><span data-ttu-id="4a08e-104">예제</span><span class="sxs-lookup"><span data-stu-id="4a08e-104">Example</span></span>

<span data-ttu-id="4a08e-105">이 예제에서 카운터는 1에서 10까지 계산하도록 초기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a08e-105">In this example, a counter is initialized to count from 1 to 10.</span></span> <span data-ttu-id="4a08e-106">`continue` 문을 `(i < 9)` 식과 함께 사용하면 `continue`와 `for` 본문의 끝 사이에 있는 문을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="4a08e-106">By using the `continue` statement in conjunction with the expression `(i < 9)`, the statements between `continue` and the end of the `for` body are skipped.</span></span>

[!code-csharp[csrefKeywordsJump#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#3)]

## <a name="c-language-specification"></a><span data-ttu-id="4a08e-107">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="4a08e-107">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="4a08e-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4a08e-108">See also</span></span>

- [<span data-ttu-id="4a08e-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="4a08e-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4a08e-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="4a08e-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4a08e-111">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="4a08e-111">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="4a08e-112">break 문</span><span class="sxs-lookup"><span data-stu-id="4a08e-112">break Statement</span></span>](/cpp/cpp/break-statement-cpp)  
- [<span data-ttu-id="4a08e-113">점프 문</span><span class="sxs-lookup"><span data-stu-id="4a08e-113">Jump Statements</span></span>](../../../csharp/language-reference/keywords/jump-statements.md)