---
title: '방법: 스크롤 가능 폼 인쇄(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- entire form [Visual Basic], printing
- scrollable form [Visual Basic], printing
ms.assetid: 1196e1cf-b77f-4928-a3e4-85b51ba3787d
ms.openlocfilehash: 4a509b7c48f2bff705bc95e58fb88252cb8ca4b9
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43779421"
---
# <a name="how-to-print-a-scrollable-form-visual-basic"></a>방법: 스크롤 가능 폼 인쇄(Visual Basic)
<xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 사용하면 <xref:System.Drawing.Printing.PrintDocument> 구성 요소를 사용하지 않고 폼 이미지를 빠르게 인쇄할 수 있습니다. 기본적으로 폼의 현재 표시되는 부분만 인쇄되고, 사용자가 런타임에 폼 크기를 변경하면 이미지가 의도대로 인쇄되지 않을 수 있습니다. 다음 절차에서는 폼 크기가 조정되었더라도 스크롤 가능한 폼의 전체 클라이언트 영역을 인쇄하는 방법을 보여 줍니다.  
  
 PowerPack 컨트롤은 더 이상 Visual Studio에 포함 되었지만 이러한에서 다운로드할 수 없습니다 합니다 [다운로드 센터](https://www.microsoft.com/en-us/download/details.aspx?id=25169)합니다.  
  
### <a name="to-print-the-complete-client-area-of-a-scrollable-form"></a>스크롤 가능한 폼의 전체 클라이언트 영역을 인쇄하려면  
  
1.  **도구 상자**에서 **Visual Basic PowerPacks** 탭을 클릭하고 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 폼으로 끕니다.  
  
     <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 구성 요소 트레이에 추가됩니다.  
  
2.  **속성** 창에서 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> 속성을 <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>로 설정합니다.  
  
3.  `Click` 인쇄 **용**`Button`이벤트 처리기와 같은 적절한 이벤트 처리기에 다음 코드를 추가합니다.  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.Scrollable)  
    ```  
  
    > [!NOTE]
    >  일부 운영 체제에서는 <xref:System.Drawing.Graphics> 메서드로 그려진 텍스트나 그래픽이 제대로 인쇄되지 않을 수 있습니다. 이 경우 `Scrollable` 매개 변수를 사용해서 인쇄할 수 없습니다.  
  
## <a name="see-also"></a>참고 항목  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print%2A>  
 [PrintForm 구성 요소](../../../visual-basic/developing-apps/printing/printform-component.md)  
 [방법: 폼의 클라이언트 영역 인쇄](../../../visual-basic/developing-apps/printing/how-to-print-the-client-area-of-a-form.md)  
 [방법: 폼의 클라이언트 영역 및 비클라이언트 영역 인쇄](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)
