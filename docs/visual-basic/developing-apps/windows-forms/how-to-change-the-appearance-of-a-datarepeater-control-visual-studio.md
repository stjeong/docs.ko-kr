---
title: '방법: DataRepeater 컨트롤 (Visual Studio)의 모양 변경'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, customizing
- DataRepeater, changing run time appearance
ms.assetid: 2af6dfce-760b-489e-b863-8da967f315c3
ms.openlocfilehash: e5508329ba716b53eff0c9e1bfe13e190fa1fd85
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716637"
---
# <a name="how-to-change-the-appearance-of-a-datarepeater-control-visual-studio"></a>방법: DataRepeater 컨트롤 (Visual Studio)의 모양 변경
모양을 변경할 수 있습니다는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 속성을 설정 하 여 디자인 타임 또는 런타임에 처리 하 여 컨트롤을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> 이벤트입니다.  
  
 컨트롤의 항목 템플릿 섹션을 선택한 경우 디자인 타임에 설정 하는 속성 각각에 대해 반복 됩니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> 런타임 시. 모양과 관련 된 속성을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 런타임 시 컨테이너의 일부가 되는 경우에만 그대로 살펴보기 컨트롤 자체는 표시 됩니다 (경우에 예를 들어를 <xref:System.Windows.Forms.Control.Padding%2A> 큰 값으로 설정).  
  
 런타임 시 모양 관련 속성을 설정할 수 있습니다 기반 조건에. 예를 들어, 일정 관리 응용 프로그램에서 사용자에 게 경고할 기한 항목은 항목의 배경색을 변경할 수 있습니다. 에 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> 같은 조건문에서 속성을 설정 하는 경우 이벤트 처리기 `If…Then`을 사용 해야는 `Else` 절 조건에 맞지 않을 때 모양을 지정할 수.  
  
### <a name="to-change-the-appearance-at-design-time"></a>디자인 타임 모양을 변경 하려면  
  
1.  Windows Forms 디자이너에서의 항목 템플릿 (위) 영역을 선택 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 제어 합니다.  
  
2.  속성 창에서 속성을 선택 하 고 값을 변경 합니다. 모양에 영향을 주는 공용 속성에 포함 <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.BackgroundImage%2A>를 <xref:System.Windows.Forms.Panel.BorderStyle%2A>, 및 <xref:System.Windows.Forms.Control.ForeColor%2A>합니다.  
  
### <a name="to-change-the-appearance-at-run-time"></a>런타임 시 모양을 변경 하려면  
  
1.  코드 편집기의 이벤트 드롭다운 목록에서 **DrawItem**을 클릭합니다.  
  
2.  에 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> 이벤트 처리기 속성을 설정 하는 코드를 추가 합니다.  
  
     [!code-csharp[VbPowerPacksDataRepeaterAppearance#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterAppearance#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_1.vb)]  
  
## <a name="example"></a>예제  
 에 대 한 일부 일반적인 사용자 지정을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤 포함의 색을 교대로 반복 되는 조건에 따라 필드의 색을 변경 하는 행을 표시 합니다. 다음 예제에서는 이러한 사용자 지정을 수행 하는 방법을 보여 줍니다. 이 예에서는 있다고 가정 된 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> Northwind 데이터베이스의 Products 테이블에 바인딩된 컨트롤입니다.  
  
 [!code-vb[VbPowerPacksDataRepeaterAlternateBackColor#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_2.vb)]
 [!code-csharp[VbPowerPacksDataRepeaterAlternateBackColor#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_2.cs)]  
  
 이러한 사용자 지정 둘 다 제공 해야 하는 조건의 양쪽 모두에 대 한 속성을 설정 하는 코드를 참고 합니다. 지정 하지 않으면 경우는 `Else` 조건 런타임에 예기치 않은 결과가 표시 됩니다.  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>
- [DataRepeater 컨트롤 소개](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [DataRepeater 컨트롤 문제 해결](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [방법: DataRepeater 컨트롤의 바인딩된 데이터 표시](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)
- [방법: DataRepeater 컨트롤의 바인딩되지 않은 컨트롤 표시](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)
- [방법: DataRepeater 컨트롤의 항목 머리글 표시](../../../visual-basic/developing-apps/windows-forms/how-to-display-item-headers-in-a-datarepeater-control-visual-studio.md)
