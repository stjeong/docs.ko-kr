---
title: '방법: 백그라운드 작업을 사용하는 폼 구현'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [Windows Forms], forms
- BackgroundWorker component
- background tasks
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- background threads
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9f483f93-1613-4be1-a021-b4934e9c78f3
ms.openlocfilehash: 8f348097223d2db4c54d9ecbba89eb8d179b6680
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43404538"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a><span data-ttu-id="20865-102">방법: 백그라운드 작업을 사용하는 폼 구현</span><span class="sxs-lookup"><span data-stu-id="20865-102">How to: Implement a Form That Uses a Background Operation</span></span>
<span data-ttu-id="20865-103">다음 예제 프로그램은 피보나치 숫자를 계산하는 폼을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20865-103">The following example program creates a form that calculates Fibonacci numbers.</span></span> <span data-ttu-id="20865-104">계산은 사용자 인터페이스 스레드와 별개인 스레드에서 실행되므로 계산이 진행될 때 사용자 인터페이스가 지연 없이 계속 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="20865-104">The calculation runs on a thread that is separate from the user interface thread, so the user interface continues to run without delays as the calculation proceeds.</span></span>  
  
 <span data-ttu-id="20865-105">Visual Studio에서는 이 작업이 광범위하게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="20865-105">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="20865-106">또한 [연습: 백그라운드 작업을 사용하는 양식 구현](https://msdn.microsoft.com/library/b2zk6580\(v=vs.110\))을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20865-106">Also see [Walkthrough: Implementing a Form That Uses a Background Operation](https://msdn.microsoft.com/library/b2zk6580\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="20865-107">예제</span><span class="sxs-lookup"><span data-stu-id="20865-107">Example</span></span>  
 [!code-cpp[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="20865-108">코드 컴파일</span><span class="sxs-lookup"><span data-stu-id="20865-108">Compiling the Code</span></span>  
 <span data-ttu-id="20865-109">이 예제에는 다음 사항이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="20865-109">This example requires:</span></span>  
  
-   <span data-ttu-id="20865-110">System, System.Drawing 및 System.Windows.Forms 어셈블리에 대한 참조</span><span class="sxs-lookup"><span data-stu-id="20865-110">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="20865-111">Visual Basic 또는 Visual C#에 대 한 명령줄에서이 예제를 빌드하는 방법에 대 한 내용은 [명령줄에서 빌드](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) 하거나 [csc.exe를 사용한 명령줄 빌드](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="20865-111">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="20865-112">또한 새 프로젝트에 코드를 붙여 넣어 Visual Studio에서이 예제를 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20865-112">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="20865-113">[방법: Visual Studio를 사용하여 전체 Windows Forms 코드 예제 컴파일 및 실행](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20865-113">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="20865-114">강력한 프로그래밍</span><span class="sxs-lookup"><span data-stu-id="20865-114">Robust Programming</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="20865-115">모든 종류의 다중 스레딩을 사용할 때는 매우 심각하고 복잡한 버그에 잠재적으로 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="20865-115">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="20865-116">다중 스레딩을 사용하는 솔루션을 구현하기 전에 [관리되는 스레딩을 구현하는 최선의 방법](../../../../docs/standard/threading/managed-threading-best-practices.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20865-116">Consult the [Managed Threading Best Practices](../../../../docs/standard/threading/managed-threading-best-practices.md) before implementing any solution that uses multithreading.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20865-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="20865-117">See Also</span></span>  
 <xref:System.ComponentModel.BackgroundWorker>  
 <xref:System.ComponentModel.DoWorkEventArgs>  
 [<span data-ttu-id="20865-118">이벤트 기반 비동기 패턴 개요</span><span class="sxs-lookup"><span data-stu-id="20865-118">Event-based Asynchronous Pattern Overview</span></span>](../../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)  
 [<span data-ttu-id="20865-119">관리되는 스레딩을 구현하는 최선의 방법</span><span class="sxs-lookup"><span data-stu-id="20865-119">Managed Threading Best Practices</span></span>](../../../../docs/standard/threading/managed-threading-best-practices.md)
