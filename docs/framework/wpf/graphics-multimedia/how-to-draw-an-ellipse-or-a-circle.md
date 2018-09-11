---
title: '방법: 타원 또는 원 그리기'
ms.date: 03/30/2017
helpviewer_keywords:
- ellipses [WPF], drawing
- circles [WPF], drawing
- drawing circles [WPF]
- drawing ellipses [WPF]
- graphics [WPF], drawing circles
- graphics [WPF], drawing ellipses
ms.assetid: 99763b8c-bfc8-44be-8231-8a70daf5481a
ms.openlocfilehash: ddeada8619d1b6c8970f1efb7cca1bc98773d0c5
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44262076"
---
# <a name="how-to-draw-an-ellipse-or-a-circle"></a><span data-ttu-id="22270-102">방법: 타원 또는 원 그리기</span><span class="sxs-lookup"><span data-stu-id="22270-102">How to: Draw an Ellipse or a Circle</span></span>
<span data-ttu-id="22270-103">사용 하 여 타원과 원을 그리는 방법을 보여 주는이 예제는 <xref:System.Windows.Shapes.Ellipse> 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="22270-103">This example shows how to draw ellipses and circles by using the <xref:System.Windows.Shapes.Ellipse> element.</span></span> <span data-ttu-id="22270-104">타원을 그릴 만들기는 <xref:System.Windows.Shapes.Ellipse> 요소를 지정 하 고 해당 <xref:System.Windows.FrameworkElement.Width%2A> 및 <xref:System.Windows.FrameworkElement.Height%2A>합니다.</span><span class="sxs-lookup"><span data-stu-id="22270-104">To draw an ellipse, create an <xref:System.Windows.Shapes.Ellipse> element and specify its <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A>.</span></span> <span data-ttu-id="22270-105">사용 하 여 해당 <xref:System.Windows.Shapes.Shape.Fill%2A> 속성을 지정 합니다 <xref:System.Windows.Media.Brush> 타원의 내부를 그리는 데 사용 되는 합니다.</span><span class="sxs-lookup"><span data-stu-id="22270-105">Use its <xref:System.Windows.Shapes.Shape.Fill%2A> property to specify the <xref:System.Windows.Media.Brush> that is used to paint the interior of the ellipse.</span></span> <span data-ttu-id="22270-106">사용 하 여 해당 <xref:System.Windows.Shapes.Shape.Stroke%2A> 속성을 지정 합니다 <xref:System.Windows.Media.Brush> 타원 윤곽선을 그리는 데 사용 되는 합니다.</span><span class="sxs-lookup"><span data-stu-id="22270-106">Use its <xref:System.Windows.Shapes.Shape.Stroke%2A> property to specify the <xref:System.Windows.Media.Brush> that is used to paint the outline of the ellipse.</span></span> <span data-ttu-id="22270-107"><xref:System.Windows.Shapes.Shape.StrokeThickness%2A> 속성 타원 윤곽선의 두께 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22270-107">The <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> property specifies the thickness of the ellipse outline.</span></span>  
  
 <span data-ttu-id="22270-108">원을 그리려면 합니다 <xref:System.Windows.FrameworkElement.Width%2A> 및 <xref:System.Windows.FrameworkElement.Height%2A> 의 <xref:System.Windows.Shapes.Ellipse> 서로 다른 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="22270-108">To draw a circle, make the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> of the <xref:System.Windows.Shapes.Ellipse> element equal to each other.</span></span>  
  
 <span data-ttu-id="22270-109">다음 예제에서는 네 개의 <xref:System.Windows.Shapes.Ellipse> 내에서 요소를 <xref:System.Windows.Controls.Canvas>입니다.</span><span class="sxs-lookup"><span data-stu-id="22270-109">The following example draws four <xref:System.Windows.Shapes.Ellipse> elements within a <xref:System.Windows.Controls.Canvas>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="22270-110">예제</span><span class="sxs-lookup"><span data-stu-id="22270-110">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#EllipseExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/ellipseexample.xaml#ellipseexample1)]  
  
 <span data-ttu-id="22270-111">이 예제에서는 한 <xref:System.Windows.Controls.Canvas> 줄임표 들어 사용할 수 있습니다 ellipse 요소 (및 다른 모든 도형 요소)와 <xref:System.Windows.Controls.Panel> 또는 <xref:System.Windows.Controls.Control> 텍스트가 아닌 콘텐츠를 지 원하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="22270-111">Although this example uses a <xref:System.Windows.Controls.Canvas> to contain the ellipses, you can use ellipse elements (and all the other shape elements) with any <xref:System.Windows.Controls.Panel> or <xref:System.Windows.Controls.Control> that supports non-text content.</span></span>  
  
 <span data-ttu-id="22270-112">이 예제는 더 큰 샘플;의 일부 전체 샘플을 참조 하세요 [도형 요소 샘플](https://go.microsoft.com/fwlink/?LinkID=160037)합니다.</span><span class="sxs-lookup"><span data-stu-id="22270-112">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22270-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="22270-113">See Also</span></span>  
 <xref:System.Windows.Shapes.Ellipse>  
 <xref:System.Windows.Shapes.Shape>  
 [<span data-ttu-id="22270-114">도형 요소 샘플</span><span class="sxs-lookup"><span data-stu-id="22270-114">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
