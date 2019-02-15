---
title: '방법: 애니메이션 시작 값에 애니메이션 출력 값 추가'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF]
ms.assetid: b89a82be-b03d-481e-a8d3-cc513d09ca00
ms.openlocfilehash: 3f1110880b7a8d4bcef40bcb66bcade6597a15dc
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303363"
---
# <a name="how-to-add-an-animation-output-value-to-an-animation-starting-value"></a>방법: 애니메이션 시작 값에 애니메이션 출력 값 추가
이 예제에서는 애니메이션 시작 값에 애니메이션 출력 값을 추가 하는 방법을 보여 줍니다.  
  
## <a name="example"></a>예제  
 <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> 속성 애니메이션된 속성의 시작 값 (기본값)에 추가 하는 애니메이션의 출력 값 여부를 지정 합니다. 사용할 수는 <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> 가장 기본적인 애니메이션 및 대부분의 키 프레임 애니메이션을 사용 하 여 속성입니다. 자세한 내용은 [애니메이션 개요](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md) 하 고 [키 프레임 애니메이션 개요](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)합니다.  
  
 다음 예제를 사용 하 여 결과 보여 줍니다.는 <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A?displayProperty=nameWithType> 속성을 <xref:System.Windows.Media.Animation.DoubleAnimation> 하 고 사용 하는 <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsAdditive%2A?displayProperty=nameWithType> 속성과 <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>합니다.  
  
 [!code-xaml[timingbehaviors_snip#IsAdditiveWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsAdditiveExample.xaml#isadditivewholepage)]  
  
## <a name="see-also"></a>참고자료
- [주기가 반복되는 동안 애니메이션 값 누적](../../../../docs/framework/wpf/graphics-multimedia/how-to-accumulate-animation-values-during-repeat-cycles.md)
- [애니메이션 개요](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [키 프레임 애니메이션 개요](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
- [애니메이션 및 타이밍 방법 항목](animation-and-timing-how-to-topics.md)
