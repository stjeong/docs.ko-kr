---
title: '방법: 선형 그라데이션으로 영역 그리기'
ms.date: 03/30/2017
helpviewer_keywords:
- linear gradients [WPF], painting with
- brushes [WPF], painting with linear gradients
- painting [WPF], with linear gradients
ms.assetid: 00e0cd04-48c0-4ec5-850e-d321beb37a34
ms.openlocfilehash: aee9931fc366131ae492891cc4d0fff70b4a4441
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43779999"
---
# <a name="how-to-paint-an-area-with-a-linear-gradient"></a><span data-ttu-id="5f517-102">방법: 선형 그라데이션으로 영역 그리기</span><span class="sxs-lookup"><span data-stu-id="5f517-102">How to: Paint an Area with a Linear Gradient</span></span>
<span data-ttu-id="5f517-103">사용 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Media.LinearGradientBrush> 선형 그라데이션으로 영역 그리기 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-103">This example shows how to use the <xref:System.Windows.Media.LinearGradientBrush> class to paint an area with a linear gradient.</span></span> <span data-ttu-id="5f517-104">다음 예제에서는 <xref:System.Windows.Shapes.Shape.Fill%2A> 의 <xref:System.Windows.Shapes.Rectangle> 노란색에서 빨간색에서 파란색 라임 녹색으로 전환 하는 대각선 선형 그라데이션을 사용 하 여 그려집니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-104">In the following example, the <xref:System.Windows.Shapes.Shape.Fill%2A> of a <xref:System.Windows.Shapes.Rectangle> is painted with a diagonal linear gradient that transitions from yellow to red to blue to lime green.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f517-105">예제</span><span class="sxs-lookup"><span data-stu-id="5f517-105">Example</span></span>  
 [!code-xaml[GradientBrushExamples_snip#DiagonalGradient1XAML](../../../../samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#diagonalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#DiagonalGradient1CSharp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#diagonalgradient1csharp)]  
  
 <span data-ttu-id="5f517-106">다음 그림에서는 이전 예제에서 만든 그라데이션을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-106">The following illustration shows the gradient created by the previous example.</span></span>  
  
 <span data-ttu-id="5f517-107">![대각선 선형 그라데이션](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-diagonallgb.jpg "graphicsmm_DiagonalLGB")</span><span class="sxs-lookup"><span data-stu-id="5f517-107">![Diagonal linear gradient](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-diagonallgb.jpg "graphicsmm_DiagonalLGB")</span></span>  
  
 <span data-ttu-id="5f517-108">가로 선형 그라데이션 만들기, 변경 된 <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> 및 <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> 의 <xref:System.Windows.Media.LinearGradientBrush> (0, 0.5)에 (1, 0.5) 및 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-108">To create a horizontal linear gradient, change the <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> and <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> of the <xref:System.Windows.Media.LinearGradientBrush> to (0,0.5) and (1,0.5).</span></span> <span data-ttu-id="5f517-109">다음 예제에서는 <xref:System.Windows.Shapes.Rectangle> 가로 선형 그라데이션을 사용 하 여 그려집니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-109">In the following example, a <xref:System.Windows.Shapes.Rectangle> is painted with a horizontal linear gradient.</span></span>  
  
 [!code-xaml[GradientBrushExamples_snip#HorizontalGradient1XAML](../../../../samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#horizontalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#HorizontalGradient1CSharp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#horizontalgradient1csharp)]  
  
 <span data-ttu-id="5f517-110">다음 그림에서는 이전 예제에서 만든 그라데이션을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-110">The following illustration shows the gradient created by the previous example.</span></span>  
  
 <span data-ttu-id="5f517-111">![가로 선형 그라데이션의](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-horizontallgb.jpg "graphicsmm_HorizontalLGB")</span><span class="sxs-lookup"><span data-stu-id="5f517-111">![A horizontal linear gradient](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-horizontallgb.jpg "graphicsmm_HorizontalLGB")</span></span>  
  
 <span data-ttu-id="5f517-112">세로 선형 그라데이션 만들기, 변경 된 <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> 및 <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> 의 <xref:System.Windows.Media.LinearGradientBrush> (0.5, 0)을 (0.5, 1) 및 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-112">To create a vertical linear gradient, change the <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> and <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> of the <xref:System.Windows.Media.LinearGradientBrush> to (0.5,0) and (0.5,1).</span></span> <span data-ttu-id="5f517-113">다음 예제에서는 <xref:System.Windows.Shapes.Rectangle> 세로 선형 그라데이션을 사용 하 여 그려집니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-113">In the following example, a <xref:System.Windows.Shapes.Rectangle> is painted with a vertical linear gradient.</span></span>  
  
 [!code-xaml[GradientBrushExamples_snip#VerticalGradient1XAML](../../../../samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#verticalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#VerticalGradient1CSharp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#verticalgradient1csharp)]  
  
 <span data-ttu-id="5f517-114">다음 그림에서는 이전 예제에서 만든 그라데이션을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-114">The following illustration shows the gradient created by the previous example.</span></span>  
  
 <span data-ttu-id="5f517-115">![세로 선형 그라데이션](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-verticallgb.jpg "graphicsmm_VerticalLGB")</span><span class="sxs-lookup"><span data-stu-id="5f517-115">![Vertical linear gradient](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-verticallgb.jpg "graphicsmm_VerticalLGB")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5f517-116">이 항목의 예제는 시작점 및 끝점 설정에 대 한 기본 좌표계를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-116">The examples in this topic use the default coordinate system for setting start points and end points.</span></span> <span data-ttu-id="5f517-117">기본 좌표계가 경계 상자를 기준으로 합니다. 0은 경계 상자의 0 %1은 경계 상자의 100%를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-117">The default coordinate system is relative to a bounding box: 0 indicates 0 percent of the bounding box, and 1 indicates 100 percent of the bounding box.</span></span> <span data-ttu-id="5f517-118">설정 하 여이 좌표계를 변경할 수 있습니다 합니다 <xref:System.Windows.Media.GradientBrush.MappingMode%2A> 속성 값을 <xref:System.Windows.Media.BrushMappingMode.Absolute?displayProperty=nameWithType>입니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-118">You can change this coordinate system by setting the <xref:System.Windows.Media.GradientBrush.MappingMode%2A> property to the value <xref:System.Windows.Media.BrushMappingMode.Absolute?displayProperty=nameWithType>.</span></span> <span data-ttu-id="5f517-119">절대 좌표계는 경계 상자를 기준으로 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-119">An absolute coordinate system is not relative to a bounding box.</span></span> <span data-ttu-id="5f517-120">값은 로컬 공간에서 직접 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-120">Values are interpreted directly in local space.</span></span>  
  
 <span data-ttu-id="5f517-121">추가 예제를 보려면 [브러시 샘플](https://go.microsoft.com/fwlink/?LinkID=159973)합니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-121">For additional examples, see [Brushes Sample](https://go.microsoft.com/fwlink/?LinkID=159973).</span></span> <span data-ttu-id="5f517-122">그라데이션 및 브러시의 다른 형식에 대 한 자세한 내용은 참조 하세요. [단색 및 그라데이션 개요 그리기](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="5f517-122">For more information about gradients and other types of brushes, see [Painting with Solid Colors and Gradients Overview](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md).</span></span>
