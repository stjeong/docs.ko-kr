---
title: '방법: Panel의 OnRender 메서드 재정의'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- overriding OnRender method
- Panel control, overriding OnRender method
- OnRender method
- controls, Panel, overriding OnRender method
helpviewer_keywords:
- overriding OnRender method of Panel control [WPF]
- OnRender method [WPF], overriding
- Panel control [WPF], overriding OnRender method
ms.assetid: 57397834-a085-4e36-90ab-416fad98f341
ms.openlocfilehash: 8f3b65bdfe96efdc57c6b8d30991439d3bdb0bc5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43404438"
---
# <a name="how-to-override-the-panel-onrender-method"></a><span data-ttu-id="ca078-102">방법: Panel의 OnRender 메서드 재정의</span><span class="sxs-lookup"><span data-stu-id="ca078-102">How to: Override the Panel OnRender Method</span></span>
<span data-ttu-id="ca078-103">재정의 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Controls.Panel.OnRender%2A> 메서드의 <xref:System.Windows.Controls.Panel> 레이아웃 요소를 사용자 지정 그래픽 효과 추가 하려면.</span><span class="sxs-lookup"><span data-stu-id="ca078-103">This example shows how to override the <xref:System.Windows.Controls.Panel.OnRender%2A> method of <xref:System.Windows.Controls.Panel> in order to add custom graphical effects to a layout element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ca078-104">예제</span><span class="sxs-lookup"><span data-stu-id="ca078-104">Example</span></span>  
 <span data-ttu-id="ca078-105">사용 된 <xref:System.Windows.Controls.Panel.OnRender%2A> 그래픽 효과 렌더링된 panel 요소를 추가 하기 위해 메서드.</span><span class="sxs-lookup"><span data-stu-id="ca078-105">Use the <xref:System.Windows.Controls.Panel.OnRender%2A> method in order to add graphical effects to a rendered panel element.</span></span> <span data-ttu-id="ca078-106">예를 들어, 사용자 지정 테두리 또는 배경 효과 추가 하려면이 메서드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca078-106">For example, you can use this method to add custom border or background effects.</span></span> <span data-ttu-id="ca078-107"><xref:System.Windows.Media.DrawingContext> 개체는 도형, 텍스트, 이미지 또는 비디오를 그리기 위한 메서드를 제공 하는 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca078-107">A <xref:System.Windows.Media.DrawingContext> object is passed as an argument, which provides methods for drawing shapes, text, images, or videos.</span></span> <span data-ttu-id="ca078-108">결과적으로,이 메서드는 패널 개체의 사용자 지정에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca078-108">As a result, this method is useful for customization of a panel object.</span></span>  
  
 [!code-csharp[LightWeightCustomPanel#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LightWeightCustomPanel/CSharp/OffsetPanel.cs#1)]
 [!code-vb[LightWeightCustomPanel#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/LightWeightCustomPanel/visualbasic/offsetpanel.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="ca078-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ca078-109">See Also</span></span>  
 <xref:System.Windows.Controls.Panel>  
 [<span data-ttu-id="ca078-110">패널 개요</span><span class="sxs-lookup"><span data-stu-id="ca078-110">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [<span data-ttu-id="ca078-111">사용자 지정 방사형 패널 샘플</span><span class="sxs-lookup"><span data-stu-id="ca078-111">Custom Radial Panel Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159982)  
 [<span data-ttu-id="ca078-112">방법 항목</span><span class="sxs-lookup"><span data-stu-id="ca078-112">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/panel-how-to-topics.md)
