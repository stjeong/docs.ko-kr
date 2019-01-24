---
title: '방법: 폼에 표준 메뉴 항목 제공'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- menu items [Windows Forms], standard
- ToolStrip control [Windows Forms]
ms.assetid: 75db9126-e70c-4e81-921d-b83c0a4a9f50
ms.openlocfilehash: befff7b2eceb37b49c4d1263f46bf93775d432c5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564018"
---
# <a name="how-to-provide-standard-menu-items-to-a-form"></a><span data-ttu-id="ed3b2-102">방법: 폼에 표준 메뉴 항목 제공</span><span class="sxs-lookup"><span data-stu-id="ed3b2-102">How to: Provide Standard Menu Items to a Form</span></span>
<span data-ttu-id="ed3b2-103"><xref:System.Windows.Forms.MenuStrip> 컨트롤을 사용하여 폼에 표준 메뉴를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-103">You can provide a standard menu for your forms with the <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
 <span data-ttu-id="ed3b2-104">Visual Studio에서이 기능에 대해 폭넓게 지원이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-104">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="ed3b2-105">또한 참조 [연습: 폼에 표준 메뉴 항목 제공](walkthrough-providing-standard-menu-items-to-a-form.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-105">Also see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed3b2-106">예제</span><span class="sxs-lookup"><span data-stu-id="ed3b2-106">Example</span></span>  
 <span data-ttu-id="ed3b2-107">다음 코드 예제에서는 <xref:System.Windows.Forms.MenuStrip> 컨트롤을 사용하여 표준 메뉴가 있는 폼을 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-107">The following code example demonstrates how to use a <xref:System.Windows.Forms.MenuStrip> control to create a form with a standard menu.</span></span> <span data-ttu-id="ed3b2-108">메뉴 항목 선택이 <xref:System.Windows.Forms.StatusStrip> 컨트롤에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-108">Menu item selections are displayed in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ed3b2-109">코드 컴파일</span><span class="sxs-lookup"><span data-stu-id="ed3b2-109">Compiling the Code</span></span>  
 <span data-ttu-id="ed3b2-110">이 예제에는 다음 사항이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-110">This example requires:</span></span>  
  
-   <span data-ttu-id="ed3b2-111">System, System.Drawing 및 System.Windows.Forms 어셈블리에 대한 참조</span><span class="sxs-lookup"><span data-stu-id="ed3b2-111">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="ed3b2-112">Visual Basic 또는 Visual C#에 대 한 명령줄에서이 예제를 빌드하는 방법에 대 한 내용은 [명령줄에서 빌드](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) 하거나 [csc.exe를 사용한 명령줄 빌드](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="ed3b2-113">또한 새 프로젝트에 코드를 붙여 넣어 Visual Studio에서이 예제를 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="ed3b2-114">또한 참조 [방법: 컴파일 및 Visual Studio를 사용 하 여 전체 Windows Forms 코드 예제를 실행](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))합니다.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-114">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed3b2-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="ed3b2-115">See also</span></span>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="ed3b2-116">MenuStrip 컨트롤</span><span class="sxs-lookup"><span data-stu-id="ed3b2-116">MenuStrip Control</span></span>](../../../../docs/framework/winforms/controls/menustrip-control-windows-forms.md)
