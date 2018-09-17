---
title: do(C# 참조)
ms.date: 05/28/2018
f1_keywords:
- do_CSharpKeyword
- do
helpviewer_keywords:
- do keyword [C#]
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
ms.openlocfilehash: 89c13f5b547c13052e229ff6eb3a39ae5babce41
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45591006"
---
# <a name="do-c-reference"></a><span data-ttu-id="3b1f2-102">do(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="3b1f2-102">do (C# Reference)</span></span>

<span data-ttu-id="3b1f2-103">`do` 문은 지정된 부울 식이 `true`로 평가되는 동안 명령문 또는 명령문 블록을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-103">The `do` statement executes a statement or a block of statements while a specified boolean expression evaluates to `true`.</span></span> <span data-ttu-id="3b1f2-104">이 식은 각 루프 실행 후 평가되기 때문에 `do-while` 루프가 한 번 이상 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-104">Because that expression is evaluated after each execution of the loop, a `do-while` loop executes one or more times.</span></span> <span data-ttu-id="3b1f2-105">이는 0번 이상 실행되는 [while](while.md) 루프와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-105">This differs from the [while](while.md) loop, which executes zero or more times.</span></span>

<span data-ttu-id="3b1f2-106">`do` 문 블록 내의 어느 지점에서나 [break](break.md) 문을 사용하여 루프를 중단할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-106">At any point within the `do` statement block, you can break out of the loop by using the [break](break.md) statement.</span></span>

<span data-ttu-id="3b1f2-107">[continue](continue.md) 문을 사용하여 `while` 식의 계산을 직접 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-107">You can step directly to the evaluation of the `while` expression by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="3b1f2-108">식이 `true`로 계산될 경우 루프의 첫 번째 문에서 계속 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-108">If the expression evaluates to `true`, execution continues at the first statement in the loop.</span></span> <span data-ttu-id="3b1f2-109">그렇지 않으면 실행은 루프 뒤에 나오는 첫 번째 문에서 계속됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-109">Otherwise, execution continues at the first statement after the loop.</span></span>

<span data-ttu-id="3b1f2-110">[goto](goto.md), [return](return.md) 또는 [throw](throw.md) 문으로 `do-while` 루프를 종료할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-110">You also can exit a `do-while` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="example"></a><span data-ttu-id="3b1f2-111">예</span><span class="sxs-lookup"><span data-stu-id="3b1f2-111">Example</span></span>

<span data-ttu-id="3b1f2-112">다음 예제에서는 `do` 문의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-112">The following example shows the usage of the `do` statement.</span></span> <span data-ttu-id="3b1f2-113">**Run**을 선택하여 예제 코드를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-113">Select **Run** to run the example code.</span></span> <span data-ttu-id="3b1f2-114">그런 다음, 코드를 수정하고 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b1f2-114">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[do loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="3b1f2-115">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="3b1f2-115">C# language specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="3b1f2-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3b1f2-116">See also</span></span>

- [<span data-ttu-id="3b1f2-117">C# 참조</span><span class="sxs-lookup"><span data-stu-id="3b1f2-117">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="3b1f2-118">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="3b1f2-118">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="3b1f2-119">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="3b1f2-119">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="3b1f2-120">do-while 문(C++)</span><span class="sxs-lookup"><span data-stu-id="3b1f2-120">do-while Statement (C++)</span></span>](/cpp/cpp/do-while-statement-cpp)  
- [<span data-ttu-id="3b1f2-121">반복 문</span><span class="sxs-lookup"><span data-stu-id="3b1f2-121">Iteration Statements</span></span>](iteration-statements.md)  
- [<span data-ttu-id="3b1f2-122">while 문</span><span class="sxs-lookup"><span data-stu-id="3b1f2-122">while statement</span></span>](while.md)  
