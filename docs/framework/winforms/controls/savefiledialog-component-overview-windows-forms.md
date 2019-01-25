---
title: SaveFileDialog 구성 요소 개요(Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- SaveFileDialog
helpviewer_keywords:
- Save File dialog box [Windows Forms], displaying
- SaveFileDialog component [Windows Forms], about SaveFileDialog
ms.assetid: be7a625f-46fd-4d06-9985-b613dcbf9bd2
ms.openlocfilehash: ab8eb5409d017c6ea73a44e4e57ccec9cece4824
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631063"
---
# <a name="savefiledialog-component-overview-windows-forms"></a>SaveFileDialog 구성 요소 개요(Windows Forms)
Windows Forms <xref:System.Windows.Forms.SaveFileDialog> 구성 요소는 미리 구성된 대화 상자입니다. 표준으로 동일 **파일 저장** Windows에서 사용 하는 대화 상자. <xref:System.Windows.Forms.CommonDialog> 클래스에서 상속됩니다.  
  
## <a name="working-with-the-savefiledialog-component"></a>SaveFileDialog 구성 요소를 사용 하 여 작업  
 사용자가 직접 대화 상자를 구성 하는 대신 파일을 저장할 수 있도록 간단한 솔루션으로 사용 합니다. 표준 Windows 대화 상자에 의존 하 여 만든 응용 프로그램의 기본 기능을 사용자에 게 친숙 한 경우 그러나 때 사용 하는 <xref:System.Windows.Forms.SaveFileDialog> 구성 요소를 사용자 고유의 파일 저장 논리를 작성 해야 합니다.  
  
 사용할 수는 <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> 런타임에 대화 상자를 표시 하는 방법입니다. 사용 하 여 읽기/쓰기 모드에서 파일을 열 수는 <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> 메서드.  
  
 폼에 추가 될 때를 <xref:System.Windows.Forms.SaveFileDialog> 구성 요소가 Windows Forms 디자이너 아래쪽에 있는 트레이에 나타납니다.  
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Forms.SaveFileDialog>
- [SaveFileDialog 구성 요소](../../../../docs/framework/winforms/controls/savefiledialog-component-windows-forms.md)
