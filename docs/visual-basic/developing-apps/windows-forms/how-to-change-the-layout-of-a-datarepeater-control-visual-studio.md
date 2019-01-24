---
title: '방법: DataRepeater 컨트롤 (Visual Studio)의 레이아웃 변경'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, changing layout style
- DataRepeater, changing orientation
ms.assetid: 33aa8fd5-ac63-4bd0-ba13-8c2ab17e7824
ms.openlocfilehash: 3389daa6383444b48faab4c5383b281e44349bce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625603"
---
# <a name="how-to-change-the-layout-of-a-datarepeater-control-visual-studio"></a>방법: DataRepeater 컨트롤 (Visual Studio)의 레이아웃 변경
<xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤 (가로 스크롤 항목)는 가로 또는 세로 방향 (세로 스크롤 항목)에 표시할 수 있습니다 방향입니다. 디자인 타임 또는 런타임에 방향을 변경 하 여 변경할 수 있습니다는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> 속성입니다. 변경 하는 경우는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> 런타임에 속성을 수도 있습니다 크기를 조정 하는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 자식 컨트롤의 위치 및 합니다.  
  
> [!NOTE]
>  컨트롤의 위치를 변경 하는 경우는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 런타임에 호출 해야 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A> 및 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A> 컨트롤의 위치를 변경 하는 코드 블록의 시작과 끝에서 메서드.  
  
### <a name="to-change-the-layout-at-design-time"></a>디자인 타임 레이아웃을 변경 하려면  
  
1.  Windows Forms 디자이너에서 선택 된 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 제어 합니다.  
  
    > [!NOTE]
    >  바깥쪽 테두리를 선택 해야 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 위에 없는 컨트롤의 아래쪽 영역에서을 클릭 하 여 컨트롤 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 지역.  
  
2.  속성 창에서 설정 된 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A> 속성을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical> 또는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal>합니다.  
  
### <a name="to-change-the-layout-at-run-time"></a>런타임에 레이아웃을 변경 하려면  
  
1.  단추 또는 메뉴에 다음 코드를 추가 `Click` 이벤트 처리기:  
  
     [!code-csharp[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterLayout#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_1.vb)]  
  
2.  크기를 조정 하려면 예제 단원에 나와 있는 다음과 같은 코드를 추가 하려고 대부분의 경우에는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 새 방향에 맞게 컨트롤을 다시 정렬 합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 응답 하는 방법의 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyleChanged> 이벤트 처리기에서 이벤트입니다. 이 예제를 실행 하려면를 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 라는 컨트롤 `DataRepeater1` 폼에서 해당 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 두 포함 <xref:System.Windows.Forms.TextBox> 라는 컨트롤 `TextBox1` 및 `TextBox2`합니다.  
  
 [!code-csharp[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.cs)]
 [!code-vb[VbPowerPacksDataRepeaterLayout#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-layout-of-a-datarepeater-control-visual-studio_2.vb)]  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A>
- [DataRepeater 컨트롤 소개](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [DataRepeater 컨트롤 문제 해결](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [방법: DataRepeater 컨트롤의 모양 변경](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
