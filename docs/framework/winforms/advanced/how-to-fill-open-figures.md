---
title: '방법: 열린 그림 채우기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- open figures [Windows Forms], filling
- figures [Windows Forms], filling
ms.assetid: 5a36b0e4-f1f4-46c0-a85a-22ae98491950
ms.openlocfilehash: b4dd37decd86d625a9cdf8a6b4027dfaec0c0ff1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730752"
---
# <a name="how-to-fill-open-figures"></a>방법: 열린 그림 채우기
전달 하 여 경로 채울 수는 <xref:System.Drawing.Drawing2D.GraphicsPath> 개체는 <xref:System.Drawing.Graphics.FillPath%2A> 메서드. <xref:System.Drawing.Graphics.FillPath%2A> 메서드는 현재 경로 대해 설정 된 채우기 모드 (대체 또는 감기)에 따라 경로 입력 합니다. 경로 모든 열린 그림 그림이 닫혀 있는 것 처럼 경로가 채워집니다. [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 시작 지점으로 해당 끝점에서 직선 그리기 하 여 그림을 닫습니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 하나의 열린 그림 (호) 및 닫힌된 그림 하나 (타원)에 포함 된 경로 만듭니다. 합니다 <xref:System.Drawing.Graphics.FillPath%2A> 메서드는 기본 채우기 모드에 따라 경로 채우는 <xref:System.Drawing.Drawing2D.FillMode.Alternate>합니다.  
  
 다음 그림에서는 예제 코드의 출력을 보여줍니다. 경로 채워지는지 확인 (에 따라 <xref:System.Drawing.Drawing2D.FillMode.Alternate>)를 시작 점으로 끝 지점에서 직선으로 열린 그림 닫힌 경우.  
  
 ![열린 경로 채우기](../../../../docs/framework/winforms/advanced/media/fillopenpath.png "FillOpenPath")  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>코드 컴파일  
 앞의 예제는 Windows forms에서 사용하도록 설계되었으며 <xref:System.Windows.Forms.Control.Paint> 이벤트 처리기의 매개 변수인 <xref:System.Windows.Forms.PaintEventArgs> `e`가 필요합니다.  
  
## <a name="see-also"></a>참고자료
- <xref:System.Drawing.Drawing2D.GraphicsPath>
- [GDI+의 그래픽 경로](../../../../docs/framework/winforms/advanced/graphics-paths-in-gdi.md)
