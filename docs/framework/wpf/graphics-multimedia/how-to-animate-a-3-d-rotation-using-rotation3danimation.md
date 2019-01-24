---
title: '방법: Rotation3DAnimation을 사용하여 3차원 회전에 애니메이션 효과 주기'
ms.date: 03/30/2017
helpviewer_keywords:
- 3-D translations [WPF], animating [WPF], with Rotation3DAnimation
- Rotation3DAnimation [WPF]
- animation [WPF], 3-D translations [WPF], with Rotation3DAnimation
ms.assetid: a92223ec-b634-4f5e-8e79-d33bc43ecfb3
ms.openlocfilehash: 32977235477737d95948bba89734905d35af4baf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564788"
---
# <a name="how-to-animate-a-3-d-rotation-using-rotation3danimation"></a><span data-ttu-id="d6ee7-102">방법: Rotation3DAnimation을 사용하여 3차원 회전에 애니메이션 효과 주기</span><span class="sxs-lookup"><span data-stu-id="d6ee7-102">How to: Animate a 3-D Rotation Using Rotation3DAnimation</span></span>
<span data-ttu-id="d6ee7-103">다음 예제에서는 비틀 회전 ""를 사용 하 여 3D 개체를 확인 하는 방법을 보여 줍니다 <xref:System.Windows.Media.Animation.Rotation3DAnimation> 애니메이션 효과를 <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> 의 속성을 <xref:System.Windows.Media.Media3D.RotateTransform3D> 3D 개체에 적용 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-103">The following example shows how to make a 3D object rotate while it "wobbles" by using <xref:System.Windows.Media.Animation.Rotation3DAnimation> to animate the <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> property of the <xref:System.Windows.Media.Media3D.RotateTransform3D> object applied to the 3D object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d6ee7-104">예제</span><span class="sxs-lookup"><span data-stu-id="d6ee7-104">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#Rotation3DAnimationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotation3DAnimationExample.xaml#rotation3danimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="d6ee7-105">참고자료</span><span class="sxs-lookup"><span data-stu-id="d6ee7-105">See also</span></span>
- [<span data-ttu-id="d6ee7-106">3차원 그래픽 개요</span><span class="sxs-lookup"><span data-stu-id="d6ee7-106">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
- [<span data-ttu-id="d6ee7-107">키 프레임을 사용하여 3차원 회전에 애니메이션 효과 주기(Rotation3DAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="d6ee7-107">Animate a 3-D Rotation Using Key Frames (Rotation3DAnimationUsingKeyFrames)</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-key-frames.md)
- [<span data-ttu-id="d6ee7-108">Storyboard를 사용하여 3차원 회전에 애니메이션 효과 주기</span><span class="sxs-lookup"><span data-stu-id="d6ee7-108">Animate a 3-D Rotation Using Storyboards</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="d6ee7-109">4원수를 사용하여 3차원 회전에 애니메이션 효과 주기</span><span class="sxs-lookup"><span data-stu-id="d6ee7-109">Animate a 3-D Rotation Using Quaternions</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-quaternions.md)
- [<span data-ttu-id="d6ee7-110">애니메이션 개요</span><span class="sxs-lookup"><span data-stu-id="d6ee7-110">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
