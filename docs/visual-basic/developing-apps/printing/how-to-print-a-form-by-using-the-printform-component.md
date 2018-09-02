---
title: '방법: PrintForm 구성 요소를 사용하여 폼 인쇄(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Form [Visual Basic], printing
ms.assetid: df963bf6-3ee1-49f4-8b2e-1d95d1beb0be
ms.openlocfilehash: 723524c7c9876d353624ad47d504ea2528a31cfe
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43422729"
---
# <a name="how-to-print-a-form-by-using-the-printform-component-visual-basic"></a><span data-ttu-id="226e5-102">방법: PrintForm 구성 요소를 사용하여 폼 인쇄(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="226e5-102">How to: Print a Form by Using the PrintForm Component (Visual Basic)</span></span>
<span data-ttu-id="226e5-103"><xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 사용하면 <xref:System.Drawing.Printing.PrintDocument> 구성 요소를 사용하지 않고 화면에 표시된 대로 정확히 폼 이미지를 빠르게 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-103">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component enables you to quickly print an image of a form exactly as it appears on screen without using a <xref:System.Drawing.Printing.PrintDocument> component.</span></span> <span data-ttu-id="226e5-104">다음 절차에서는 프린터, 인쇄 미리 보기 창, Encapsulated PostScript 파일 등으로 폼을 인쇄하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-104">The following procedures show how to print a form to a printer, to a print preview window, and to an Encapsulated PostScript file.</span></span>  
  
 <span data-ttu-id="226e5-105">PowerPack 컨트롤은 더 이상 Visual Studio에 포함 되었지만 이러한에서 다운로드할 수 없습니다 합니다 [다운로드 센터](https://www.microsoft.com/en-us/download/details.aspx?id=25169)합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-105">The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span></span>  
  
### <a name="to-print-a-form-to-the-default-printer"></a><span data-ttu-id="226e5-106">폼을 기본 프린터로 인쇄하려면</span><span class="sxs-lookup"><span data-stu-id="226e5-106">To print a form to the default printer</span></span>  
  
1.  <span data-ttu-id="226e5-107">**도구 상자**에서 **Visual Basic PowerPacks** 탭을 클릭하고 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 폼으로 끕니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-107">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="226e5-108"><xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 구성 요소 트레이에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-108">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="226e5-109">**속성** 창에서 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> 속성을 <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-109">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span></span>  
  
3.  <span data-ttu-id="226e5-110">`Click` 인쇄 **용**`Button`이벤트 처리기와 같은 적절한 이벤트 처리기에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-110">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print()  
    ```  
  
### <a name="to-display-a-form-in-a-print-preview-window"></a><span data-ttu-id="226e5-111">폼을 인쇄 미리 보기 창에 표시하려면</span><span class="sxs-lookup"><span data-stu-id="226e5-111">To display a form in a print preview window</span></span>  
  
1.  <span data-ttu-id="226e5-112">**도구 상자**에서 **Visual Basic PowerPacks** 탭을 클릭하고 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 폼으로 끕니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-112">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="226e5-113"><xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 구성 요소 트레이에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-113">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="226e5-114">**속성** 창에서 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> 속성을 <xref:System.Drawing.Printing.PrintAction.PrintToPreview>로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-114">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPreview>.</span></span>  
  
3.  <span data-ttu-id="226e5-115">`Click` 인쇄 **용**`Button`이벤트 처리기와 같은 적절한 이벤트 처리기에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-115">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print()  
    ```  
  
### <a name="to-print-a-form-to-a-file"></a><span data-ttu-id="226e5-116">폼을 파일로 출력하려면</span><span class="sxs-lookup"><span data-stu-id="226e5-116">To print a form to a file</span></span>  
  
1.  <span data-ttu-id="226e5-117">**도구 상자**에서 **Visual Basic PowerPacks** 탭을 클릭하고 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 폼으로 끕니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-117">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="226e5-118"><xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 구성 요소 트레이에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-118">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="226e5-119">**속성** 창에서 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> 속성을 <xref:System.Drawing.Printing.PrintAction.PrintToFile>로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-119">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToFile>.</span></span>  
  
3.  <span data-ttu-id="226e5-120">선택적으로 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A> 속성을 선택하고 대상 파일의 전체 경로 및 파일 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-120">Optionally, select the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A> property and type the full path and file name for the destination file.</span></span>  
  
     <span data-ttu-id="226e5-121">이 단계를 건너뛰면 런타임에 파일 이름을 묻는 메시지가 사용자에게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-121">If you skip this step, the user will be prompted for a file name at run time.</span></span>  
  
4.  <span data-ttu-id="226e5-122">`Click` 인쇄 **용**`Button`이벤트 처리기와 같은 적절한 이벤트 처리기에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="226e5-122">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).</span></span>  
  
    ```  
    PrintForm1.Print()  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="226e5-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="226e5-123">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintFileName%2A>  
 [<span data-ttu-id="226e5-124">방법: 폼의 클라이언트 영역 인쇄</span><span class="sxs-lookup"><span data-stu-id="226e5-124">How to: Print the Client Area of a Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-the-client-area-of-a-form.md)  
 [<span data-ttu-id="226e5-125">방법: 폼의 클라이언트 영역 및 비클라이언트 영역 인쇄</span><span class="sxs-lookup"><span data-stu-id="226e5-125">How to: Print Client and Non-Client Areas of a Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)  
 [<span data-ttu-id="226e5-126">방법: 스크롤 가능 폼 인쇄</span><span class="sxs-lookup"><span data-stu-id="226e5-126">How to: Print a Scrollable Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-a-scrollable-form.md)  
 [<span data-ttu-id="226e5-127">PrintForm 구성 요소</span><span class="sxs-lookup"><span data-stu-id="226e5-127">PrintForm Component</span></span>](../../../visual-basic/developing-apps/printing/printform-component.md)
