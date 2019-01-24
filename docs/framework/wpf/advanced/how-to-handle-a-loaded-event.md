---
title: '방법: Loaded 이벤트 처리'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- XAML [WPF], Loaded events
- events [WPF], Loaded
- Loaded events [WPF]
ms.assetid: 0cf8d003-8441-4df4-807a-6db09347e829
ms.openlocfilehash: 187d75c436913140855f4d860eb3b6ad4656f309
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54682945"
---
# <a name="how-to-handle-a-loaded-event"></a><span data-ttu-id="0478f-102">방법: Loaded 이벤트 처리</span><span class="sxs-lookup"><span data-stu-id="0478f-102">How to: Handle a Loaded Event</span></span>
<span data-ttu-id="0478f-103">처리 하는 방법을 보여 주는이 예제는 <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> 이벤트 및 해당 이벤트를 처리 하기 위한 적절 한 시나리오가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0478f-103">This example shows how to handle the <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> event, and an appropriate scenario for handling that event.</span></span> <span data-ttu-id="0478f-104">처리기를 만듭니다를 <xref:System.Windows.Controls.Button> 페이지가 로드 되는 경우.</span><span class="sxs-lookup"><span data-stu-id="0478f-104">The handler  creates a <xref:System.Windows.Controls.Button> when the page loads.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0478f-105">예제</span><span class="sxs-lookup"><span data-stu-id="0478f-105">Example</span></span>  
 <span data-ttu-id="0478f-106">다음 예제에서는 [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] 코드 숨김 파일을 함께 합니다.</span><span class="sxs-lookup"><span data-stu-id="0478f-106">The following example uses [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] together with a code-behind file.</span></span>  
  
 [!code-xaml[FELoaded#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FELoaded#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml.cs#handler)]
 [!code-vb[FELoaded#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FELoaded/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a><span data-ttu-id="0478f-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="0478f-107">See also</span></span>
- <xref:System.Windows.FrameworkElement>
- [<span data-ttu-id="0478f-108">개체 수명 이벤트</span><span class="sxs-lookup"><span data-stu-id="0478f-108">Object Lifetime Events</span></span>](../../../../docs/framework/wpf/advanced/object-lifetime-events.md)
- [<span data-ttu-id="0478f-109">라우트된 이벤트 개요</span><span class="sxs-lookup"><span data-stu-id="0478f-109">Routed Events Overview</span></span>](../../../../docs/framework/wpf/advanced/routed-events-overview.md)
- [<span data-ttu-id="0478f-110">방법 항목</span><span class="sxs-lookup"><span data-stu-id="0478f-110">How-to Topics</span></span>](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
