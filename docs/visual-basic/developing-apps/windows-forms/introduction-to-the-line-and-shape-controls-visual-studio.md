---
title: Line 및 Shape 컨트롤 소개(Visual Studio)
ms.date: 07/20/2015
helpviewer_keywords:
- Line control [Visual Basic], overview
- Shape control [Visual Basic], overview
- lines, drawing
- shapes, drawing
ms.assetid: 5c4e8b1a-0733-4020-af6c-f582f4026728
ms.openlocfilehash: 3623c2363f39150fd4bb202ba61ebd51df383ca8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54699924"
---
# <a name="introduction-to-the-line-and-shape-controls-visual-studio"></a>Line 및 Shape 컨트롤 소개(Visual Studio)
Visual Basic Power Packs Line 및 Shape 컨트롤은 폼과 컨테이너에서 줄 및 도형을 그리는 데 사용할 수 있는 세 개의 그래픽 컨트롤의 집합입니다. <xref:Microsoft.VisualBasic.PowerPacks.LineShape> 컨트롤은 가로, 세로 및 대각선 선을 그리는 데 사용 합니다. <xref:Microsoft.VisualBasic.PowerPacks.OvalShape> 컨트롤은 원 및 타원을 그리는 데 및 <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> 컨트롤은 사각형 및 정사각형을 그리는 데 합니다.  
  
## <a name="line-and-shape-controls"></a>Line 및 Shape 컨트롤  
 Line 및 Shape 컨트롤에 포함 된 그래픽이 많은 캡슐화 된 <xref:System.Drawing> 네임 스페이스입니다. 그러면 그래픽 개체, 펜 및 브러시를 만들지 않고도 한 번에 선과 셰이프를 그릴 수 있습니다. 그라데이션 채우기와 같은 고급 그래픽 기술은 몇 가지 속성을 설정 하 여 수행할 수 있습니다.  
  
 그래픽 메서드를 사용 하 여 선과 도형 그리기 수 이기도 하지만 여러 가지 이점이 있습니다 Line 및 Shape 컨트롤을 사용 해야 합니다.  
  
-   런타임 시에만 그래픽 메서드를 호출할 수 있습니다. Line 및 Shape 컨트롤 디자인 타임에 폼에 추가할 수 있습니다. 이렇게 하면 모양을 확인 하 고 정확 하 게; 배치할 수 있습니다. 또한 런타임에 추가할 수 있습니다.  
  
-   Line 및 Shape 컨트롤은 선택할 수 있는 런타임 시와 같은 이벤트를 제공 <xref:Microsoft.VisualBasic.PowerPacks.Shape.Click> 고 <xref:Microsoft.VisualBasic.PowerPacks.Shape.OnDoubleClick%2A>입니다. 그래픽 방법 중 선택할 수 없는 출력과 이벤트를 제공 하지 않습니다.  
  
-   Line 및 Shape 컨트롤을 제공 <xref:Microsoft.VisualBasic.PowerPacks.Shape.BringToFront%2A> 고 <xref:Microsoft.VisualBasic.PowerPacks.Shape.SendToBack%2A> 디자인 타임 및 런타임에 z 순서를 제어할 수 있도록 하는 메서드. 런타임 시 실행 순서를 변경한 경우에 그래픽이의 z 순서를 제어할 수 있습니다.  
  
-   Line 및 Shape 컨트롤은 창 없는 컨트롤; 창 핸들이 없는지를 보유 하 고 따라서 적은 시스템 리소스를 사용 합니다.  
  
### <a name="object-model"></a>개체 모델  
 Line 및 Shape 컨트롤을 기본에서 파생 <xref:Microsoft.VisualBasic.PowerPacks.Shape> 해당 공유 속성, 메서드 및 이벤트를 정의 하는 클래스입니다.  
  
 다음 그림에서는 Line 및 Shape 개체 계층 구조를 보여 줍니다.  
  
 ![Line 및 Shape 개체 계층 구조 다이어그램](../../../visual-basic/developing-apps/windows-forms/media/lineshapeobject.png "LineShapeObject")  
Line 및 Shape 개체 계층 구조  
  
 파생 된 <xref:Microsoft.VisualBasic.PowerPacks.LineShape> 클래스 속성, 메서드 및 줄에 고유한 이벤트를 포함 합니다. 파생 <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape> 클래스에 대 한 기본 클래스인 <xref:Microsoft.VisualBasic.PowerPacks.OvalShape> 및 <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>; 속성, 메서드 및 모든 셰이프에 공통 이벤트를 포함 합니다. 파생할 수 있습니다 <xref:Microsoft.VisualBasic.PowerPacks.SimpleShape> 하 여 직접 만들 `Shape` 컨트롤입니다.  
  
 합니다 <xref:Microsoft.VisualBasic.PowerPacks.OvalShape> 고 <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> 클래스 원, 타원, 사각형 및 모서리가 둥근 사각형을 그리는 데 사용할 수 있습니다.  
  
 선 또는 모양 컨트롤이 면 보이지 않는 폼 또는 컨테이너를 추가 되는 경우 <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer> 개체가 만들어집니다. 합니다 <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer> 각 컨테이너 컨트롤 내 셰이프에 대 한 캔버스의 역할도; 각 <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer> 에 해당 <xref:Microsoft.VisualBasic.PowerPacks.ShapeCollection> Line 및 Shape 컨트롤을 반복할 수 있도록 합니다. 끌어서 놓는 방법 또는 잘라내기 및 붙여넣기를 사용 하 여 다른 하나의 컨테이너에서 셰이프를 이동할 수 있습니다. 마지막 셰이프를 컨테이너에서 제거 되 면는 <xref:Microsoft.VisualBasic.PowerPacks.ShapeContainer> 도 제거 됩니다.  
  
> [!NOTE]
>  일부 컨테이너 컨트롤 Line 및 Shape 컨트롤을 지원합니다. 선 또는 모양 컨트롤에서 호스트할 수 없습니다는 <xref:System.Windows.Forms.TableLayoutPanel> 또는 <xref:System.Windows.Forms.FlowLayoutPanel>합니다.  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.PowerPacks>
- [방법: LineShape 컨트롤로 선 그리기](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
- [방법: OvalShape 및 RectangleShape 컨트롤을 사용 하 여 도형 그리기](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
- [방법: 도형 간 탭 이동 사용](../../../visual-basic/developing-apps/windows-forms/how-to-enable-tabbing-between-shapes-visual-studio.md)
