---
title: '방법: LineShape 컨트롤로 선 그리기 (Visual Studio)를 사용 하 여 선 그리기'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- LineShape control [Visual Basic]
- lines, drawing
ms.assetid: 83e71b4e-aa76-4f9b-b547-8704309fd1e5
ms.openlocfilehash: 46360c01dfaf2c6fe199725a9ecfba2248c72d6d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596230"
---
# <a name="how-to-draw-lines-with-the-lineshape-control-visual-studio"></a>방법: LineShape 컨트롤로 선 그리기 (Visual Studio)를 사용 하 여 선 그리기
사용할 수는 <xref:Microsoft.VisualBasic.PowerPacks.LineShape> 디자인 타임 및 런타임에 폼 이나 컨테이너에서 가로, 세로 또는 대각선 그릴 컨트롤입니다.  
  
 **참고** 컴퓨터에서에서 표시할 수 있습니다 다른 이름이 나 위치 일부 Visual Studio 사용자 인터페이스 요소 다음 지침을 합니다. 이러한 요소는 사용하는 Visual Studio 버전 및 설정에 따라 결정됩니다. 자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.  
  
### <a name="to-draw-a-line-at-design-time"></a>디자인 타임에 선 그리기  
  
1.  끌어를 <xref:Microsoft.VisualBasic.PowerPacks.LineShape> 에서 제어를 **Visual Basic PowerPacks** 탭에 **도구 상자** 을 폼 이나 컨테이너 컨트롤로 끌어 놓습니다.  
  
2.  크기 조정 끌어서 크기 및 줄 위치에 대 한 핸들을 이동 합니다.  
  
     크기 및 위치를 변경 하 여 줄 수도 있습니다는 `X1`, `X2`를 `Y1`, 및 `Y2` 속성에는 **속성** 창입니다.  
  
3.  에 **속성** 창에서 필요에 따라 추가 속성을 설정할와 같은 `BorderStyle` 또는 `BorderColor` 줄의 모양을 변경 하려면.  
  
### <a name="to-draw-a-line-at-run-time"></a>런타임에 선을 그리려면  
  
1.  **프로젝트** 메뉴에서 **참조 추가**를 클릭합니다.  
  
2.  에 **참조 추가** 대화 상자에서 **Microsoft.VisualBasic.PowerPacks.VS**를 클릭 하 고 **확인**합니다.  
  
3.  에 **코드 편집기**에 추가 `Imports` 또는 `using` 모듈의 맨 위에 있는 문을:  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  
  
4.  `Event` 프로시저에 다음 코드를 추가합니다.  
  
     [!code-csharp[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.vb)]  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.PowerPacks.LineShape>
- [Line 및 Shape 컨트롤 소개](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
- [방법: OvalShape 및 RectangleShape 컨트롤을 사용 하 여 도형 그리기](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
