---
title: '방법: 선 그리기'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], lines
- graphics [WPF], lines
- lines [WPF], drawing
ms.assetid: 0513ee01-6b27-4bb3-85f3-3a3e6710d80e
ms.openlocfilehash: 54152b6b68dd453c565afa2ffb23edfe8132a441
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629022"
---
# <a name="how-to-draw-a-line"></a><span data-ttu-id="b5932-102">방법: 선 그리기</span><span class="sxs-lookup"><span data-stu-id="b5932-102">How to: Draw a Line</span></span>
<span data-ttu-id="b5932-103">이 예제에서는 사용 하 여 선을 그리는 방법을 보여 줍니다.는 <xref:System.Windows.Shapes.Line> 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5932-103">This example shows you how to draw lines by using the <xref:System.Windows.Shapes.Line> element.</span></span>  
  
 <span data-ttu-id="b5932-104">선을 그리는 만들려면는 <xref:System.Windows.Shapes.Line> 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5932-104">To draw a line, create a <xref:System.Windows.Shapes.Line> element.</span></span> <span data-ttu-id="b5932-105">사용 하 여 해당 <xref:System.Windows.Shapes.Line.X1%2A> 하 고 <xref:System.Windows.Shapes.Line.Y1%2A> 시작점;를 사용 하 여 속성 해당 <xref:System.Windows.Shapes.Line.X2%2A> 및 <xref:System.Windows.Shapes.Line.Y2%2A> 끝점을 설정 하는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5932-105">Use its <xref:System.Windows.Shapes.Line.X1%2A> and <xref:System.Windows.Shapes.Line.Y1%2A> properties to set its start point; and use its <xref:System.Windows.Shapes.Line.X2%2A> and <xref:System.Windows.Shapes.Line.Y2%2A> properties to set its end point.</span></span> <span data-ttu-id="b5932-106">마지막으로 설정 하는 <xref:System.Windows.Shapes.Shape.Stroke%2A> 및 <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> 스트로크 없는 줄에 표시 되지 않으므로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5932-106">Finally, set its <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> because a line without a stroke is invisible.</span></span>  
  
 <span data-ttu-id="b5932-107">설정 된 <xref:System.Windows.Shapes.Shape.Fill%2A> 요소 줄에 대 한 영향을 주지 않습니다, 줄 없는 내부에 있으므로.</span><span class="sxs-lookup"><span data-stu-id="b5932-107">Setting the <xref:System.Windows.Shapes.Shape.Fill%2A> element for a line has no effect, because a line has no interior.</span></span>  
  
 <span data-ttu-id="b5932-108">다음 예제에서는 세 줄을 그립니다는 <xref:System.Windows.Controls.Canvas> 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5932-108">The following example draws three lines inside a <xref:System.Windows.Controls.Canvas> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b5932-109">예제</span><span class="sxs-lookup"><span data-stu-id="b5932-109">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#LineExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/lineexample.xaml#lineexample1)]  
  
 <span data-ttu-id="b5932-110">이 예제는 더 큰 샘플;의 일부 전체 샘플을 참조 하세요 [도형 요소 샘플](https://go.microsoft.com/fwlink/?LinkID=160037)합니다.</span><span class="sxs-lookup"><span data-stu-id="b5932-110">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5932-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="b5932-111">See also</span></span>
- <xref:System.Windows.Shapes.Line>
- [<span data-ttu-id="b5932-112">도형 요소 샘플</span><span class="sxs-lookup"><span data-stu-id="b5932-112">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
