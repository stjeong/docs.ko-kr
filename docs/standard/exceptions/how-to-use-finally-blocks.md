---
title: '방법: Finally 블록 사용'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- exceptions, try/catch blocks
- exceptions, finally blocks
- try/catch blocks
- finally blocks
- ArgumentOutOfRangeException class
ms.assetid: 4b9c0137-04af-4468-91d1-b9014df8ddd2
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 213ab53c68a37ac0ba5f337a1d6fc32bfe6f8989
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44190217"
---
# <a name="how-to-use-finally-blocks"></a><span data-ttu-id="7d802-102">Finally 블록을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="7d802-102">How to use finally blocks</span></span>

<span data-ttu-id="7d802-103">예외가 발생하면 실행이 중단되고 해당 예외 처리기에 제어가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-103">When an exception occurs, execution stops and control is given to the appropriate exception handler.</span></span> <span data-ttu-id="7d802-104">이 경우 대체로 실행될 것으로 예상한 코드 줄을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-104">This often means that lines of code you expect to be executed are bypassed.</span></span> <span data-ttu-id="7d802-105">파일 닫기와 같은 일부 리소스 정리 작업은 예외가 throw된 경우에도 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-105">Some resource cleanup, such as closing a file, needs to be done even if an exception is thrown.</span></span> <span data-ttu-id="7d802-106">이 작업을 위해 `finally` 블록을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-106">To do this, you can use a `finally` block.</span></span> <span data-ttu-id="7d802-107">`finally` 블록은 예외가 throw되었는지 여부에 관계없이 항상 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-107">A `finally` block always executes, regardless of whether an exception is thrown.</span></span>

<span data-ttu-id="7d802-108">다음 코드 예제에서는 `try`/`catch` 블록을 사용하여 <xref:System.ArgumentOutOfRangeException>을 catch합니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-108">The following code example uses a `try`/`catch` block to catch an <xref:System.ArgumentOutOfRangeException>.</span></span> <span data-ttu-id="7d802-109">`Main` 메서드는 두 개의 배열을 만들고 한 배열을 다른 배열에 복사하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-109">The `Main` method creates two arrays and attempts to copy one to the other.</span></span> <span data-ttu-id="7d802-110">작업에서 <xref:System.ArgumentOutOfRangeException>이 발생하고 콘솔에 오류가 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-110">The action generates an <xref:System.ArgumentOutOfRangeException> and the error is written to the console.</span></span> <span data-ttu-id="7d802-111">`finally` 블록은 복사 작업의 결과에 관계없이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d802-111">The `finally` block executes regardless of the outcome of the copy action.</span></span>

[!code-cpp[CodeTryCatchFinallyExample#3](../../../samples/snippets/cpp/VS_Snippets_CLR/CodeTryCatchFinallyExample/CPP/source2.cpp#3)]
[!code-csharp[CodeTryCatchFinallyExample#3](../../../samples/snippets/csharp/VS_Snippets_CLR/CodeTryCatchFinallyExample/CS/source2.cs#3)]
[!code-vb[CodeTryCatchFinallyExample#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/CodeTryCatchFinallyExample/VB/source2.vb#3)]  

## <a name="see-also"></a><span data-ttu-id="7d802-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7d802-112">See also</span></span>

- [<span data-ttu-id="7d802-113">예외</span><span class="sxs-lookup"><span data-stu-id="7d802-113">Exceptions</span></span>](index.md)
