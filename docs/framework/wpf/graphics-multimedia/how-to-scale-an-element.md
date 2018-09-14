---
title: '방법: 요소 배율 조정'
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], elements
- graphics [WPF], scaling elements
ms.assetid: 18158d94-bbe7-4f6a-814e-84d27fa748bf
ms.openlocfilehash: 44c638b58d828e5beb0b9de5c7bb0b67c8e82d87
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45609124"
---
# <a name="how-to-scale-an-element"></a><span data-ttu-id="d55c5-102">방법: 요소 배율 조정</span><span class="sxs-lookup"><span data-stu-id="d55c5-102">How to: Scale an Element</span></span>
<span data-ttu-id="d55c5-103">사용 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Media.ScaleTransform> 요소 배율을 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-103">This example shows how to use a <xref:System.Windows.Media.ScaleTransform> to scale an element.</span></span>  
  
 <span data-ttu-id="d55c5-104">사용 된 <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> 및 <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> 요소의 크기를 조정 하 여 지정한 배율로 속성.</span><span class="sxs-lookup"><span data-stu-id="d55c5-104">Use the <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> and <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> properties to resize the element by the factor you specify.</span></span> <span data-ttu-id="d55c5-105">예를 들어, 한 <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> 원래 너비의 150%로 요소를 확장 하는 값이 1.5 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-105">For example, a <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> value of 1.5 stretches the element to 150 percent of its original width.</span></span> <span data-ttu-id="d55c5-106"><xref:System.Windows.Media.ScaleTransform.ScaleY%2A> 0.5의 50%가 요소의 높이 축소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-106">A <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> value of 0.5 shrinks the height of an element by 50 percent.</span></span>  
  
 <span data-ttu-id="d55c5-107">사용 된 <xref:System.Windows.Media.ScaleTransform.CenterX%2A> 및 <xref:System.Windows.Media.ScaleTransform.CenterY%2A> 크기 조정 작업의 중심 지점을 지정 하는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-107">Use the <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A> properties to specify the point that is the center of the scale operation.</span></span> <span data-ttu-id="d55c5-108">기본적으로 <xref:System.Windows.Media.ScaleTransform> 의 중심은 사각형의 왼쪽 위 모퉁이에 해당 하는 점 (0, 0).</span><span class="sxs-lookup"><span data-stu-id="d55c5-108">By default, a <xref:System.Windows.Media.ScaleTransform> is centered at the point (0,0), which corresponds to the upper-left corner of the rectangle.</span></span> <span data-ttu-id="d55c5-109">이 설정은 요소를 이동 하는 고 적용 하는 경우 더 크게 표시 되 게 적용을 <xref:System.Windows.Media.Transform>는 개체가 있는 좌표 공간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-109">This has the effect of moving the element and also of making it appear larger, because when you apply a <xref:System.Windows.Media.Transform>, you change the coordinate space in which the object resides.</span></span>  
  
 <span data-ttu-id="d55c5-110">다음 예제에서는 한 <xref:System.Windows.Media.ScaleTransform> 50-에서-50의 크기를 두 배로 <xref:System.Windows.Shapes.Rectangle>합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-110">The following example uses a <xref:System.Windows.Media.ScaleTransform> to double the size of a 50-by-50 <xref:System.Windows.Shapes.Rectangle>.</span></span> <span data-ttu-id="d55c5-111">합니다 <xref:System.Windows.Media.ScaleTransform> 값이 0 (기본값)를 둘 다에 <xref:System.Windows.Media.ScaleTransform.CenterX%2A> 고 <xref:System.Windows.Media.ScaleTransform.CenterY%2A>합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-111">The <xref:System.Windows.Media.ScaleTransform> has a value of 0 (the default) for both <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d55c5-112">예제</span><span class="sxs-lookup"><span data-stu-id="d55c5-112">Example</span></span>  
 [!code-xaml[transformsSample#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#21)]  
  
 <span data-ttu-id="d55c5-113">일반적으로 설정한 <xref:System.Windows.Media.ScaleTransform.CenterX%2A> 하 고 <xref:System.Windows.Media.ScaleTransform.CenterY%2A> 크기가 조정 되는 개체의 가운데에: (<xref:System.Windows.FrameworkElement.Width%2A>/2,  <xref:System.Windows.FrameworkElement.Height%2A> /2).</span><span class="sxs-lookup"><span data-stu-id="d55c5-113">Typically, you set <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A> to the center of the object that is scaled: (<xref:System.Windows.FrameworkElement.Width%2A>/2, <xref:System.Windows.FrameworkElement.Height%2A>/2).</span></span>  
  
 <span data-ttu-id="d55c5-114">다음 예제에서는 다른 <xref:System.Windows.Shapes.Rectangle> 크기의 두 배로 증가 하는 단,이 <xref:System.Windows.Media.ScaleTransform> 값이 25 둘 다에 <xref:System.Windows.Media.ScaleTransform.CenterX%2A> 및 <xref:System.Windows.Media.ScaleTransform.CenterY%2A>, 사각형의 중심에 해당 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-114">The following example shows another <xref:System.Windows.Shapes.Rectangle> that is doubled in size; however, this <xref:System.Windows.Media.ScaleTransform> has a value of 25 for both <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A>, which corresponds to the center of the rectangle.</span></span>  
  
 [!code-xaml[transformsSample#22](../../../../samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#22)]  
  
 <span data-ttu-id="d55c5-115">다음 그림에서는 둘 사이의 차이 보여 줍니다. <xref:System.Windows.Media.ScaleTransform> 작업 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-115">The following illustration shows the difference between the two <xref:System.Windows.Media.ScaleTransform> operations.</span></span> <span data-ttu-id="d55c5-116">점선은 크기 조정 전의 사각형 크기 및 위치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d55c5-116">The dotted line shows the size and position of the rectangle before scaling.</span></span>  
  
 <span data-ttu-id="d55c5-117">![여러 중심점을 사용한 2x 배율 조정](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-scalecenter.gif "wcpsdk_graphicsmm_scalecenter")</span><span class="sxs-lookup"><span data-stu-id="d55c5-117">![2x scales with different center points](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-scalecenter.gif "wcpsdk_graphicsmm_scalecenter")</span></span>  
<span data-ttu-id="d55c5-118">ScaleX 및 ScaleY 값은 같지만 중심은 다른 두 개의 ScaleTransform 작업</span><span class="sxs-lookup"><span data-stu-id="d55c5-118">Two ScaleTransform operations with identical ScaleX and ScaleY values but different centers</span></span>  
  
 <span data-ttu-id="d55c5-119">전체 샘플을 보려면 [2차원 변환 샘플](https://go.microsoft.com/fwlink/?LinkID=158252)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d55c5-119">For the complete sample, see [2-D Transforms Sample](https://go.microsoft.com/fwlink/?LinkID=158252).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d55c5-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d55c5-120">See Also</span></span>  
 <xref:System.Windows.Media.Transform>  
 <xref:System.Windows.Media.ScaleTransform>  
 [<span data-ttu-id="d55c5-121">Transform 개요</span><span class="sxs-lookup"><span data-stu-id="d55c5-121">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)  
 [<span data-ttu-id="d55c5-122">방법 항목</span><span class="sxs-lookup"><span data-stu-id="d55c5-122">How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transformations-how-to-topics.md)
