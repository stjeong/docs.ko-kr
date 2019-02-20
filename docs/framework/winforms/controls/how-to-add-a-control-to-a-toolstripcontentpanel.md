---
title: '방법: ToolStripContentPanel에 컨트롤 추가'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripContentPanel [Windows Forms], adding controls
ms.assetid: fa410960-bf1a-42fc-80e8-f2e27fb3dbb8
ms.openlocfilehash: 193ad1e8c85e0b8830eb4f6efcb87a154b82949f
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56442453"
---
# <a name="how-to-add-a-control-to-a-toolstripcontentpanel"></a>방법: ToolStripContentPanel에 컨트롤 추가
컨트롤 하나 이상을 프로그래밍 방식으로 <xref:System.Windows.Forms.ToolStripContentPanel>에 추가할 수 있습니다.  
  
## <a name="example"></a>예제  
 다음 코드 예제에서는 <xref:System.Windows.Forms.RichTextBox>를 <xref:System.Windows.Forms.ToolStripContentPanel>에 추가하는 방법을 보여 줍니다.  
  
 [!code-csharp[System.Windows.Forms.ToolStripContainer#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStripContainer/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStripContainer#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStripContainer/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>코드 컴파일  
 이 코드 예제에는 다음이 필요합니다.  
  
-   System, System.Data 및 System.Windows.Forms 어셈블리에 대한 참조  
  
 Visual Basic 또는 Visual C#에 대 한 명령줄에서이 예제를 빌드하는 방법에 대 한 내용은 [명령줄에서 빌드](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) 하거나 [csc.exe를 사용한 명령줄 빌드](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)합니다. 또한 새 프로젝트에 코드를 붙여 넣어 Visual Studio에서이 예제를 빌드할 수 있습니다.
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Forms.ToolStripContentPanel>
- <xref:System.Windows.Forms.ToolStripContainer>
- [ToolStripContainer 컨트롤](../../../../docs/framework/winforms/controls/toolstripcontainer-control.md)
- [ToolStrip 컨트롤](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
