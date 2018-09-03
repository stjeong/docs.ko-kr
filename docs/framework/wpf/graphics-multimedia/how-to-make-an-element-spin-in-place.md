---
title: '방법: 현재 위치에서 요소가 회전하도록 만들기'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], spinning elements
- spinning elements [WPF]
ms.assetid: 1f011976-8b07-4c31-9faf-019e0ddaa24c
ms.openlocfilehash: 56385d7c31465e25f19486ea5cdaa8876cdb30ff
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43461633"
---
# <a name="how-to-make-an-element-spin-in-place"></a>방법: 현재 위치에서 요소가 회전하도록 만들기
이 예제에서는 요소를 사용 하 여 회전 하는 <xref:System.Windows.Media.RotateTransform> 및 <xref:System.Windows.Media.Animation.DoubleAnimation>합니다.  
  
 다음 예제에서는 합니다 <xref:System.Windows.Media.RotateTransform> 에 <xref:System.Windows.UIElement.RenderTransform%2A> 요소의 속성입니다. 예제에서는 <xref:System.Windows.Media.Animation.DoubleAnimation> 애니메이션 효과를 주는 합니다 <xref:System.Windows.Media.RotateTransform.Angle%2A> 의 <xref:System.Windows.Media.RotateTransform>합니다. 이 예제에서는 요소 위치에 실행 되도록 설정 된 <xref:System.Windows.UIElement.RenderTransformOrigin%2A> 점 (0.5, 0.5) 요소의 속성입니다.  
  
## <a name="example"></a>예제  
 [!code-xaml[transformanimations_snip#11](../../../../samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/RotateAboutCenterExample.xaml#11)]  
  
 추가 변환 예제를 포함 하는 전체 샘플을 참조 하세요 [2 차원 변환 샘플](https://go.microsoft.com/fwlink/?LinkID=158252)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [애니메이션 개요](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Transform 개요](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
