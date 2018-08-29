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
ms.openlocfilehash: c3ddb5171ca8ded053d56fde26ab86ebc4ae5cb2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552846"
---
# <a name="how-to-create-and-use-a-canvas"></a><span data-ttu-id="9a90d-102">방법: 캔버스 만들기 및 사용</span><span class="sxs-lookup"><span data-stu-id="9a90d-102">How to: Create and Use a Canvas</span></span>
<span data-ttu-id="9a90d-103">다음 예제는 <xref:System.Windows.Controls.Canvas> 컨트롤 클래스 인스턴스의 생성 및 사용법에 관한 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="9a90d-103">This example shows how to create and use an instance of <xref:System.Windows.Controls.Canvas>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a90d-104">예제</span><span class="sxs-lookup"><span data-stu-id="9a90d-104">Example</span></span>  
 <span data-ttu-id="9a90d-105">다음 예제에서는 명시적으로 두 개의 배치 <xref:System.Windows.Controls.TextBlock> 요소를 사용 하 여는 <xref:System.Windows.Controls.Canvas.SetTop%2A> 및 <xref:System.Windows.Controls.Canvas.SetLeft%2A> 방식의 <xref:System.Windows.Controls.Canvas>합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90d-105">The following example explicitly positions two <xref:System.Windows.Controls.TextBlock> elements by using the <xref:System.Windows.Controls.Canvas.SetTop%2A> and <xref:System.Windows.Controls.Canvas.SetLeft%2A> methods of <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="9a90d-106">이 예에서는 또한 할당 한 <xref:System.Windows.Controls.Control.Background%2A> 의 색 `LightSteelBlue` 에 <xref:System.Windows.Controls.Canvas>합니다.</span><span class="sxs-lookup"><span data-stu-id="9a90d-106">The example also assigns a <xref:System.Windows.Controls.Control.Background%2A> color of `LightSteelBlue` to the <xref:System.Windows.Controls.Canvas>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9a90d-107">[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]를 이용하여 <xref:System.Windows.Controls.TextBlock> 엘리먼트들을 배치하는 경우 <xref:System.Windows.Controls.Canvas.Top%2A> 속성과 <xref:System.Windows.Controls.Canvas.Left%2A> 속성을 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a90d-107">When you use [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to position <xref:System.Windows.Controls.TextBlock> elements, use the <xref:System.Windows.Controls.Canvas.Top%2A> and <xref:System.Windows.Controls.Canvas.Left%2A> properties.</span></span>  
  
 [!code-csharp[CanvasCode#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasCode/CSharp/Canvas_Code.cs#1)]
 [!code-vb[CanvasCode#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasCode/VisualBasic/canvas_vb.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="9a90d-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9a90d-108">See Also</span></span>  
 <xref:System.Windows.Controls.Canvas>  
 <xref:System.Windows.Controls.TextBlock>  
 <xref:System.Windows.Controls.Canvas.SetTop%2A>  
 <xref:System.Windows.Controls.Canvas.SetLeft%2A>  
 <xref:System.Windows.Controls.Canvas.Top%2A>  
 <xref:System.Windows.Controls.Canvas.Left%2A>  
 [<span data-ttu-id="9a90d-109">패널 개요</span><span class="sxs-lookup"><span data-stu-id="9a90d-109">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [<span data-ttu-id="9a90d-110">방법 항목</span><span class="sxs-lookup"><span data-stu-id="9a90d-110">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/canvas-how-to-topics.md)
