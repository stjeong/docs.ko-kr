---
title: '방법: 사각형에 애니메이션 효과 주기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], rectangles
- rectangles [WPF], animating
ms.assetid: 572ffb95-790d-4ace-adbf-b2ea8a90e75b
ms.openlocfilehash: dbff015bdc5f9ce56d2c366e0d348429efb7f4b5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305157"
---
# <a name="how-to-animate-a-rectangle"></a><span data-ttu-id="b7045-102">방법: 사각형에 애니메이션 효과 주기</span><span class="sxs-lookup"><span data-stu-id="b7045-102">How to: Animate a Rectangle</span></span>
<span data-ttu-id="b7045-103">이 예제에서는 사각형의 위치 및 크기 변화에 애니메이션 효과를 주는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7045-103">This example shows how to animate changes to the size and position of a rectangle.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7045-104">예제</span><span class="sxs-lookup"><span data-stu-id="b7045-104">Example</span></span>  
 <span data-ttu-id="b7045-105">인스턴스를 사용 하 여 다음 예제에서는 <xref:System.Windows.Media.Animation.RectAnimation> 클래스에 애니메이션 효과를 <xref:System.Windows.Media.RectangleGeometry.Rect%2A> 의 속성은 <xref:System.Windows.Media.RectangleGeometry>, 크기 및 사각형의 위치 변경 애니메이션 효과 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7045-105">The following example uses an instance of the <xref:System.Windows.Media.Animation.RectAnimation> class to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry>, which animates changes to the size and position of the rectangle.</span></span>  
  
 [!code-csharp[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/RectAnimationExample.cs#rectanimationwholepage)]
 [!code-vb[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/RectAnimationExample.vb#rectanimationwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="b7045-106">참고자료</span><span class="sxs-lookup"><span data-stu-id="b7045-106">See also</span></span>
- <xref:System.Windows.Media.Animation.RectAnimation>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.RectangleGeometry>
- [<span data-ttu-id="b7045-107">애니메이션 개요</span><span class="sxs-lookup"><span data-stu-id="b7045-107">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [<span data-ttu-id="b7045-108">그래픽 및 멀티미디어</span><span class="sxs-lookup"><span data-stu-id="b7045-108">Graphics and Multimedia</span></span>](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [<span data-ttu-id="b7045-109">그래픽 방법 항목</span><span class="sxs-lookup"><span data-stu-id="b7045-109">Graphics How-to Topics</span></span>](graphics-how-to-topics.md)
- [<span data-ttu-id="b7045-110">애니메이션 및 타이밍 방법 항목</span><span class="sxs-lookup"><span data-stu-id="b7045-110">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
