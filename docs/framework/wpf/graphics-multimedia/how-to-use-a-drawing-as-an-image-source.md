---
title: '방법: 그림을 이미지 소스로 사용'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], drawings [WPF], as image sources
- image sources [WPF], drawings
- drawings [WPF], as image sources
ms.assetid: dcf71c7b-9e86-4b8e-8e39-0d0ce0389ef4
ms.openlocfilehash: 01c8cd65128ce4e78dcbf9e38519091767b7ba2f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499277"
---
# <a name="how-to-use-a-drawing-as-an-image-source"></a><span data-ttu-id="e8d69-102">방법: 그림을 이미지 소스로 사용</span><span class="sxs-lookup"><span data-stu-id="e8d69-102">How to: Use a Drawing as an Image Source</span></span>
<span data-ttu-id="e8d69-103">사용 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Media.Drawing> 으로 <xref:System.Windows.Controls.Image.Source%2A> 에 대 한는 <xref:System.Windows.Controls.Image> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d69-103">This example shows how to use a <xref:System.Windows.Media.Drawing> as the <xref:System.Windows.Controls.Image.Source%2A> for an <xref:System.Windows.Controls.Image> control.</span></span> <span data-ttu-id="e8d69-104">표시할를 <xref:System.Windows.Media.Drawing> 사용 하 여는 <xref:System.Windows.Controls.Image> 컨트롤을 사용 하 여를 <xref:System.Windows.Media.DrawingImage> 으로 <xref:System.Windows.Controls.Image> 컨트롤의 <xref:System.Windows.Controls.Image.Source%2A> 설정 합니다 <xref:System.Windows.Media.DrawingImage> 개체의 <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> 속성을 표시 하려는 그리기.</span><span class="sxs-lookup"><span data-stu-id="e8d69-104">To display a <xref:System.Windows.Media.Drawing> with an <xref:System.Windows.Controls.Image> control, use a <xref:System.Windows.Media.DrawingImage> as the <xref:System.Windows.Controls.Image> control's <xref:System.Windows.Controls.Image.Source%2A> and set the <xref:System.Windows.Media.DrawingImage> object's <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> property to the drawing you want to display.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e8d69-105">예제</span><span class="sxs-lookup"><span data-stu-id="e8d69-105">Example</span></span>  
 <span data-ttu-id="e8d69-106">다음 예제에서는 <xref:System.Windows.Media.DrawingImage> 와 <xref:System.Windows.Controls.Image> 표시할 컨트롤을 <xref:System.Windows.Media.GeometryDrawing>입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d69-106">The following example uses a <xref:System.Windows.Media.DrawingImage> and an <xref:System.Windows.Controls.Image> control to display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="e8d69-107">이 예제는 다음과 같은 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d69-107">This example produces the following output:</span></span>  
  
 <span data-ttu-id="e8d69-108">![타원 두 개의 GeometryDrawing](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="e8d69-108">![A GeometryDrawing of two ellipses](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
<span data-ttu-id="e8d69-109">DrawingImage</span><span class="sxs-lookup"><span data-stu-id="e8d69-109">A DrawingImage</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingImageExample.cs#drawingimageexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingImageExample.xaml#drawingimageexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e8d69-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="e8d69-110">See also</span></span>
- <xref:System.Windows.Freezable.Freeze%2A>
- [<span data-ttu-id="e8d69-111">ImageDrawing을 사용하여 이미지 그리기</span><span class="sxs-lookup"><span data-stu-id="e8d69-111">Draw an Image Using ImageDrawing</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-draw-an-image-using-imagedrawing.md)
- [<span data-ttu-id="e8d69-112">Drawing 개체 개요</span><span class="sxs-lookup"><span data-stu-id="e8d69-112">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [<span data-ttu-id="e8d69-113">Freezable 개체 개요</span><span class="sxs-lookup"><span data-stu-id="e8d69-113">Freezable Objects Overview</span></span>](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)
- [<span data-ttu-id="e8d69-114">PresentationOptions:Freeze 특성</span><span class="sxs-lookup"><span data-stu-id="e8d69-114">PresentationOptions:Freeze Attribute</span></span>](../../../../docs/framework/wpf/advanced/presentationoptions-freeze-attribute.md)
