---
title: '방법: 캔버스 만들기 및 사용'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Canvas
- Canvas control [WPF], creating
- Canvas control [WPF], using
ms.assetid: 420b9487-9a15-477c-9489-a22a4dec7779
ms.openlocfilehash: d2d56851de2444ce246750688df67ed5ba9adb9a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687481"
---
# <a name="how-to-create-and-use-a-canvas"></a>방법: 캔버스 만들기 및 사용
다음 예제는 <xref:System.Windows.Controls.Canvas> 컨트롤 클래스 인스턴스의 생성 및 사용법에 관한 예제입니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 명시적으로 두 개의 배치 <xref:System.Windows.Controls.TextBlock> 를 사용 하 여 요소를 <xref:System.Windows.Controls.Canvas.SetTop%2A> 및 <xref:System.Windows.Controls.Canvas.SetLeft%2A> 의 메서드 <xref:System.Windows.Controls.Canvas>. 할당 예제를 <xref:System.Windows.Controls.Control.Background%2A> 의 색 `LightSteelBlue` 에 <xref:System.Windows.Controls.Canvas>합니다.  
  
> [!NOTE]
>  [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]를 이용하여 <xref:System.Windows.Controls.TextBlock> 엘리먼트들을 배치하는 경우 <xref:System.Windows.Controls.Canvas.Top%2A> 속성과 <xref:System.Windows.Controls.Canvas.Left%2A> 속성을 사용하면 됩니다.  
  
 [!code-csharp[CanvasCode#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasCode/CSharp/Canvas_Code.cs#1)]
 [!code-vb[CanvasCode#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasCode/VisualBasic/canvas_vb.vb#1)]  
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.TextBlock>
- <xref:System.Windows.Controls.Canvas.SetTop%2A>
- <xref:System.Windows.Controls.Canvas.SetLeft%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- [패널 개요](../../../../docs/framework/wpf/controls/panels-overview.md)
- [방법 항목](../../../../docs/framework/wpf/controls/canvas-how-to-topics.md)
