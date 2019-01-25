---
title: '방법: 캐시 된 요소를 브러시로 사용'
ms.date: 03/30/2017
helpviewer_keywords:
- BitmapCache [WPF], using
- cached element [WPF], use as a brush
- BitmapCacheBrush [WPF], using
- CacheMode [WPF], using
ms.assetid: d36e944a-866e-4baf-98c4-fd6a75f6fdd0
ms.openlocfilehash: 7ff0e9eb131faaed3874995ee137126eac31f43d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597933"
---
# <a name="how-to-use-a-cached-element-as-a-brush"></a><span data-ttu-id="b3d84-102">방법: 캐시 된 요소를 브러시로 사용</span><span class="sxs-lookup"><span data-stu-id="b3d84-102">How to: Use a Cached Element as a Brush</span></span>
<span data-ttu-id="b3d84-103">사용 하 여는 <xref:System.Windows.Media.BitmapCacheBrush> 클래스를 효율적으로 캐시 된 요소를 다시 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3d84-103">Use the <xref:System.Windows.Media.BitmapCacheBrush> class to reuse a cached element efficiently.</span></span> <span data-ttu-id="b3d84-104">새 인스턴스를 만들고 요소를 캐시 하려면 합니다 <xref:System.Windows.Media.BitmapCache> 클래스 및 요소에 할당할 <xref:System.Windows.UIElement.CacheMode%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d84-104">To cache an element, create a new instance of the <xref:System.Windows.Media.BitmapCache> class and assign it to the element's <xref:System.Windows.UIElement.CacheMode%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b3d84-105">예제</span><span class="sxs-lookup"><span data-stu-id="b3d84-105">Example</span></span>  
 <span data-ttu-id="b3d84-106">다음 코드 예제에서는 캐시 된 요소를 다시 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3d84-106">The following code example shows how to reuse a cached element.</span></span> <span data-ttu-id="b3d84-107">캐시 된 요소는 <xref:System.Windows.Controls.Image> 큰 이미지를 표시 하는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d84-107">The cached element is an <xref:System.Windows.Controls.Image> control that displays a large image.</span></span> <span data-ttu-id="b3d84-108"><xref:System.Windows.Controls.Image> 컨트롤이 사용 하 여 비트맵으로 캐시 되는 <xref:System.Windows.Media.BitmapCache> 할당 하 여 클래스 및 캐시를 다시 사용을 <xref:System.Windows.Media.BitmapCacheBrush>입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d84-108">The <xref:System.Windows.Controls.Image> control is cached as a bitmap by using the <xref:System.Windows.Media.BitmapCache> class, and the cache is reused by assigning it to a <xref:System.Windows.Media.BitmapCacheBrush>.</span></span> <span data-ttu-id="b3d84-109">브러시는 효율적인 재사용을 표시할 25 단추의 배경을에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3d84-109">The brush is assigned to the background of twenty-five buttons to show efficient reuse.</span></span>  
  
 [!code-xaml[System.Windows.Media.BitmapCacheBrush#_BitmapCacheBrushXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcachebrush/cs/window1.xaml#_bitmapcachebrushxaml)]  
  
## <a name="see-also"></a><span data-ttu-id="b3d84-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="b3d84-110">See also</span></span>
- <xref:System.Windows.Media.BitmapCache>
- <xref:System.Windows.Media.BitmapCacheBrush>
- <xref:System.Windows.UIElement.CacheMode%2A>
- [<span data-ttu-id="b3d84-111">방법: 요소를 캐시 하 여 렌더링 성능 향상</span><span class="sxs-lookup"><span data-stu-id="b3d84-111">How to: Improve Rendering Performance by Caching an Element</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-improve-rendering-performance-by-caching-an-element.md)
