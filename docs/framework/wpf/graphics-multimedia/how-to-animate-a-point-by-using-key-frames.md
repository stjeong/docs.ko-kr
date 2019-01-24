---
title: '방법: 키 프레임을 사용하여 포인트에 애니메이션 효과 주기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating Points with
- Points [WPF], animating with key frames
- animation [WPF], Points with key frames
ms.assetid: d2e2ef10-0773-4133-856e-d41c09f60ded
ms.openlocfilehash: 9d976bca77629b85226da3d4e018a35cb522afef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738341"
---
# <a name="how-to-animate-a-point-by-using-key-frames"></a><span data-ttu-id="dc0fb-102">방법: 키 프레임을 사용하여 포인트에 애니메이션 효과 주기</span><span class="sxs-lookup"><span data-stu-id="dc0fb-102">How to: Animate a Point by Using Key Frames</span></span>
<span data-ttu-id="dc0fb-103">사용 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> 애니메이션 효과를 주는 클래스를 <xref:System.Windows.Point>입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-103">This example shows how to use the <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> class to animate a <xref:System.Windows.Point>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc0fb-104">예제</span><span class="sxs-lookup"><span data-stu-id="dc0fb-104">Example</span></span>  
 <span data-ttu-id="dc0fb-105">다음 예제에서는 삼각형 경로를 따라 타원을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-105">The following example moves an ellipse along a triangular path.</span></span> <span data-ttu-id="dc0fb-106">예제에서는 <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> 클래스에 애니메이션 효과를 <xref:System.Windows.Media.EllipseGeometry.Center%2A> 의 속성을 <xref:System.Windows.Media.EllipseGeometry>입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-106">The example uses the <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.EllipseGeometry.Center%2A> property of an <xref:System.Windows.Media.EllipseGeometry>.</span></span> <span data-ttu-id="dc0fb-107">이 애니메이션은 다음과 같은 방식으로 세 가지 키 프레임을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-107">This animation uses three key frames in the following manner:</span></span>  
  
1.  <span data-ttu-id="dc0fb-108">처음 1/2 초 동안의 인스턴스를 사용 하 여는 <xref:System.Windows.Media.Animation.LinearPointKeyFrame> 시작 위치부터 일정 한 속도로 경로 따라 타원을 이동 하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-108">During the first half second, uses an instance of the <xref:System.Windows.Media.Animation.LinearPointKeyFrame> class to move the ellipse along a path at a steady rate from its starting position.</span></span> <span data-ttu-id="dc0fb-109">과 같은 선형 키 프레임 <xref:System.Windows.Media.Animation.LinearPointKeyFrame> 값 사이 매끄러운 선형 보간을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-109">Linear key frames like <xref:System.Windows.Media.Animation.LinearPointKeyFrame> create a smooth linear interpolation between values.</span></span>  
  
2.  <span data-ttu-id="dc0fb-110">0.5 초가 고 다음의 끝 중의 인스턴스를 사용 하 여 <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> 갑자기 다음 위치로 경로 따라 타원을 이동 하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-110">During the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> class to suddenly move the ellipse along the path to the next position.</span></span> <span data-ttu-id="dc0fb-111">과 같은 불연속 키 프레임 <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> 값 간에 갑작스러운 이동을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-111">Discrete key frames like <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> create sudden jumps between values.</span></span>  
  
3.  <span data-ttu-id="dc0fb-112">마지막 2 초 동안의 인스턴스를 사용 하 여는 <xref:System.Windows.Media.Animation.SplinePointKeyFrame> 클래스 타원을 다시 시작 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-112">During the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplinePointKeyFrame> class to move the ellipse back to its starting position.</span></span> <span data-ttu-id="dc0fb-113">과 같은 스플라인 키 프레임 <xref:System.Windows.Media.Animation.SplinePointKeyFrame> 의 값에 따라 값 사이 가변 전환을 만듭니다는 <xref:System.Windows.Media.Animation.SplinePointKeyFrame.KeySpline%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-113">Spline key frames like <xref:System.Windows.Media.Animation.SplinePointKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplinePointKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="dc0fb-114">이 예제에서 애니메이션은 느리게 시작하다가 시간 세그먼트의 끝에 다가가면 기하급수적으로 빨라집니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-114">In this example, the animation begins slowly and speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-csharp[keyframes_snip#PointAnimationUsingKeyFramesWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/PointAnimationUsingKeyFramesExample.cs#pointanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#PointAnimationUsingKeyFramesWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/pointanimationusingkeyframesexample.vb#pointanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#PointAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/PointAnimationUsingKeyFramesExample.xaml#pointanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="dc0fb-115">전체 샘플을 보려면 [키 프레임 애니메이션 샘플](https://go.microsoft.com/fwlink/?LinkID=160012)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-115">For the complete sample, see [KeyFrame Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
 <span data-ttu-id="dc0fb-116">다른 애니메이션 예제를 사용 하 여 일관성을 위해이 예제의 코드 버전 사용을 <xref:System.Windows.Media.Animation.Storyboard> 적용할 개체는 <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames>합니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-116">For consistency with other animation examples, the code versions of this example use a <xref:System.Windows.Media.Animation.Storyboard> object to apply the <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames>.</span></span> <span data-ttu-id="dc0fb-117">그러나 코드에서 단일 애니메이션을 적용할 때 간단 하 게 사용 합니다 <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> 사용 하는 대신 메서드를 <xref:System.Windows.Media.Animation.Storyboard>입니다.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-117">However, when applying a single animation in code, it's simpler to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method instead of using a <xref:System.Windows.Media.Animation.Storyboard>.</span></span> <span data-ttu-id="dc0fb-118">예제를 보려면 [Storyboard를 사용하지 않고 속성에 애니메이션 효과 주기](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-without-using-a-storyboard.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dc0fb-118">For an example, see [Animate a Property Without Using a Storyboard](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-without-using-a-storyboard.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc0fb-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="dc0fb-119">See also</span></span>
- <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A?displayProperty=nameWithType>
- <xref:System.Windows.Media.EllipseGeometry>
- [<span data-ttu-id="dc0fb-120">키 프레임 애니메이션 개요</span><span class="sxs-lookup"><span data-stu-id="dc0fb-120">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
- [<span data-ttu-id="dc0fb-121">키 프레임 방법 항목</span><span class="sxs-lookup"><span data-stu-id="dc0fb-121">Key-Frame How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
