---
title: '방법: 사용자 지정 패널 요소 만들기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Panel control [WPF]
- custom Panel elements [WPF]
ms.assetid: e0df4f1e-8c07-4e86-89a3-e22acfffdc2a
ms.openlocfilehash: bca8900ccb3c31a78066a43709a5e9334bc09eab
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43531786"
---
# <a name="how-to-create-a-custom-panel-element"></a>방법: 사용자 지정 패널 요소 만들기
## <a name="example"></a>예제  
 기본 레이아웃 동작을 재정의 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Controls.Panel> 요소에서 파생 되는 사용자 지정 레이아웃 요소를 만들고 <xref:System.Windows.Controls.Panel>합니다.  
  
 이 예제에서는 간단한 사용자 지정 정의 <xref:System.Windows.Controls.Panel> 라는 요소가 `PlotPanel`, 자식 요소에 따라 두 하드 코드 된 x 및 y 좌표를 배치 하는 합니다. 이 예에서 `x` 및 `y` 로 설정 됩니다 `50`하므로 x 및 y에 해당 위치에 배치 됩니다 모든 자식 요소 축.  
  
 사용자 지정 구현 <xref:System.Windows.Controls.Panel> 동작을 사용 하 여 합니다 <xref:System.Windows.FrameworkElement.MeasureOverride%2A> 및 <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> 메서드. 각 메서드는 반환 된 <xref:System.Windows.Size> 배치 하 고 자식 요소를 렌더링 하는 데 필요한 데이터입니다.  
  
 [!code-cpp[PlotPanel#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Windows.Controls.Panel>  
 [패널 개요](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [사용자 지정 콘텐츠 줄 바꿈 패널 샘플 만들기](https://go.microsoft.com/fwlink/?LinkID=159979)
