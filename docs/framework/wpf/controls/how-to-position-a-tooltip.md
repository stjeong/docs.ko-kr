---
title: '방법: 도구 설명 배치'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolTip control [WPF], positioning
- positioning ToolTip controls [WPF]
ms.assetid: cddf3757-9e5f-4ce3-a6eb-44489cf3804a
ms.openlocfilehash: 403b070e782a6f243fd5a420e569daa02044dbb1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54727705"
---
# <a name="how-to-position-a-tooltip"></a>방법: 도구 설명 배치
이 예제에는 화면의 도구 설명의 위치를 지정 하는 방법을 보여 줍니다.  
  
## <a name="example"></a>예제  
 둘 다에 정의 된 5 가지 속성 집합을 사용 하 여 도구 설명을 배치할 수 있습니다 합니다 <xref:System.Windows.Controls.ToolTip> 및 <xref:System.Windows.Controls.ToolTipService> 클래스입니다. 다음 표에서 이러한 두 속성을 5 개를 표시 하 고 클래스에 따라 해당 참조 설명서에 대 한 링크를 제공 합니다.  
  
### <a name="corresponding-tooltip-properties-according-to-class"></a>클래스에 따라 해당 도구 설명 속성  
  
|<xref:System.Windows.Controls.ToolTip?displayProperty=nameWithType> 클래스 속성|<xref:System.Windows.Controls.ToolTipService?displayProperty=nameWithType> 클래스 속성|  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Windows.Controls.ToolTip.Placement%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.Placement%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementTarget%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementTarget%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementRectangle%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementRectangle%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.HorizontalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.HorizontalOffset%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.VerticalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.VerticalOffset%2A?displayProperty=nameWithType>|  
  
 사용 하 여 도구 설명의 내용을 정의 하는 경우는 <xref:System.Windows.Controls.ToolTip> 개체 클래스의 속성을 사용할 수 있지만 <xref:System.Windows.Controls.ToolTipService> 속성 보다 우선적으로 적용 합니다. 사용 된 <xref:System.Windows.Controls.ToolTipService> 속성으로 정의 되어 있지 않은 도구 설명에 <xref:System.Windows.Controls.ToolTip> 개체입니다.  
  
 다음 그림은 이러한 속성을 사용 하 여 도구 설명을 배치 하는 방법을 보여 줍니다. 하지만, [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] 이러한 그림과 예제에 정의 된 속성을 설정 하는 방법을 보여 줍니다는 <xref:System.Windows.Controls.ToolTip> 클래스의 해당 속성을 <xref:System.Windows.Controls.ToolTipService> 클래스 동일한 레이아웃 규칙에 따라 합니다. 배치 속성에 대 한 가능한 값에 대 한 자세한 내용은 참조 하세요. [Popup 배치 동작](../../../../docs/framework/wpf/controls/popup-placement-behavior.md)합니다.  
  
 ![ToolTip 배치](../../../../docs/framework/wpf/controls/media/tooltipplacement.png "ToolTipPlacement")  
배치 속성을 사용 하 여 ToolTip 배치  
  
 ![배치 사각형을 사용 하 여 ToolTip 배치](../../../../docs/framework/wpf/controls/media/tooltipplacementrectangle.png "ToolTipPlacementRectangle")  
배치 및 PlacementRectangle 속성을 사용 하 여 ToolTip 배치  
  
 ![ToolTip 배치 다이어그램](../../../../docs/framework/wpf/controls/media/tooltipplacementprhv.png "ToolTipPlacementPRHV")  
Placement, PlacementRectangle, 및 오프셋 속성을 사용 하 여 ToolTip 배치  
  
 다음 예제에서는 사용 하는 방법을 보여 줍니다 합니다 <xref:System.Windows.Controls.ToolTip> 내용이 도구 설명의 위치를 지정 하는 속성을 <xref:System.Windows.Controls.ToolTip> 개체입니다.  
  
 [!code-xaml[ToolTipService#ToolTip](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
  
 [!code-csharp[ToolTipService#ToolTipCode](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#tooltipcode)]
 [!code-vb[ToolTipService#ToolTipCode](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#tooltipcode)]  
  
 다음 예제에서는 사용 하는 방법을 보여 줍니다 합니다 <xref:System.Windows.Controls.ToolTipService> 내용이 아닙니다. 도구 설명의 위치를 지정 하는 속성을 <xref:System.Windows.Controls.ToolTip> 개체입니다.  
  
 [!code-xaml[ToolTipService#NoToolTip](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
 [!code-csharp[ToolTipService#NoToolTipCode](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#notooltipcode)]
 [!code-vb[ToolTipService#NoToolTipCode](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#notooltipcode)]  
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [방법 항목](../../../../docs/framework/wpf/controls/tooltip-how-to-topics.md)
- [도구 설명 개요](../../../../docs/framework/wpf/controls/tooltip-overview.md)
- [ContextMenuService 및 ToolTipService를 사용 하 여](https://msdn.microsoft.com/library/809b0e9c-d612-4cda-b8af-1a698c68f4d1)
