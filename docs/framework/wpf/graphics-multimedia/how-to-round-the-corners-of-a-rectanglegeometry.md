---
title: '방법: 사각형 기하 도형의 모퉁이 둥글게 하기'
ms.date: 03/30/2017
helpviewer_keywords:
- corners [WPF], rounding
- RectangleGeometry class [WPF], rounding corners
- graphics [WPF], rounding corners of RectangleGeometry objects [WPF]
- rounding corners of RectangleGeometry objects [WPF]
ms.assetid: 926644bc-1357-4c0b-ac81-694bd090ae87
ms.openlocfilehash: 1a3ea08e4f54af117474cee23e6ac1041a1ed72b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648377"
---
# <a name="how-to-round-the-corners-of-a-rectanglegeometry"></a><span data-ttu-id="e3e19-102">방법: 사각형 기하 도형의 모퉁이 둥글게 하기</span><span class="sxs-lookup"><span data-stu-id="e3e19-102">How to: Round the Corners of a RectangleGeometry</span></span>
<span data-ttu-id="e3e19-103">모퉁이 둥글게 하는 <xref:System.Windows.Media.RectangleGeometry>설정, 해당 <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> 및 <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> 0 보다 큰 값으로 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e19-103">To round the corners of a <xref:System.Windows.Media.RectangleGeometry>, set its <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> properties to a value greater than zero.</span></span> <span data-ttu-id="e3e19-104">이 값이 클수록 더 둥글게 사각형의 모퉁이입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e19-104">The larger the values, the rounder the rectangle's corners.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e3e19-105">예제</span><span class="sxs-lookup"><span data-stu-id="e3e19-105">Example</span></span>  
 <span data-ttu-id="e3e19-106">다음 예제에서는 몇 가지 <xref:System.Windows.Media.RectangleGeometry> 다른 개체 <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> 고 <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e19-106">The following example shows several <xref:System.Windows.Media.RectangleGeometry> objects with different <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> settings.</span></span> <span data-ttu-id="e3e19-107">합니다 <xref:System.Windows.Media.RectangleGeometry> 개체를 사용 하 여 표시 됩니다 <xref:System.Windows.Shapes.Path> 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e19-107">The <xref:System.Windows.Media.RectangleGeometry> objects are displayed using <xref:System.Windows.Shapes.Path> elements.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRoundedRectangleGeometryExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/RectangleGeometryRoundedCornerExample.xaml#graphicsmmroundedrectanglegeometryexamplewholepage)]  
  
 <span data-ttu-id="e3e19-108">![여러 RadiusX 사각형&#47;RadiusY 설정을](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-rounded.png "graphicsmm_rounded")</span><span class="sxs-lookup"><span data-stu-id="e3e19-108">![Rectangles with different RadiusX&#47;RadiusY settings](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-rounded.png "graphicsmm_rounded")</span></span>  
<span data-ttu-id="e3e19-109">모퉁이가 둥근 사각형</span><span class="sxs-lookup"><span data-stu-id="e3e19-109">Rectangles with Rounded Corners</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3e19-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="e3e19-110">See also</span></span>
- [<span data-ttu-id="e3e19-111">Geometry 개요</span><span class="sxs-lookup"><span data-stu-id="e3e19-111">Geometry Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
- [<span data-ttu-id="e3e19-112">복합 도형 만들기</span><span class="sxs-lookup"><span data-stu-id="e3e19-112">Create a Composite Shape</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-composite-shape.md)
- [<span data-ttu-id="e3e19-113">PathGeometry를 사용하여 도형 만들기</span><span class="sxs-lookup"><span data-stu-id="e3e19-113">Create a Shape by Using a PathGeometry</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md)
