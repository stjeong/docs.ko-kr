---
title: '방법: 하이퍼링크에 밑줄이 그어지는지 여부 지정'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Hyperlink control type [WPF]
ms.assetid: 3996cfe6-1dac-4835-aeb3-c719ce9cfee5
ms.openlocfilehash: 3199bce25d49bb471fe21735ebb919bbb7f5132c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54576959"
---
# <a name="how-to-specify-whether-a-hyperlink-is-underlined"></a><span data-ttu-id="54617-102">방법: 하이퍼링크에 밑줄이 그어지는지 여부 지정</span><span class="sxs-lookup"><span data-stu-id="54617-102">How to: Specify Whether a Hyperlink is Underlined</span></span>
<span data-ttu-id="54617-103"><xref:System.Windows.Documents.Hyperlink> 개체는 유동 콘텐츠 내에서 하이퍼링크를 호스트할 수 있는 인라인 수준의 유동 콘텐츠 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="54617-103">The <xref:System.Windows.Documents.Hyperlink> object is an inline-level flow content element that allows you to host hyperlinks within the flow content.</span></span> <span data-ttu-id="54617-104">기본적으로 <xref:System.Windows.Documents.Hyperlink> 사용을 <xref:System.Windows.TextDecoration> 밑줄을 표시 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="54617-104">By default, <xref:System.Windows.Documents.Hyperlink> uses a <xref:System.Windows.TextDecoration> object to display an underline.</span></span> <span data-ttu-id="54617-105"><xref:System.Windows.TextDecoration> 많을 경우에 특히 개체를 인스턴스화할 때 성능이 저하 될 수 있습니다 <xref:System.Windows.Documents.Hyperlink> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="54617-105"><xref:System.Windows.TextDecoration> objects can be performance intensive to instantiate, particularly if you have many <xref:System.Windows.Documents.Hyperlink> objects.</span></span> <span data-ttu-id="54617-106">광범위 하 게 사용 한다면 <xref:System.Windows.Documents.Hyperlink> 와 같은 경우 트리거될 때만 밑줄이 표시 하려는 요소를 <xref:System.Windows.ContentElement.MouseEnter> 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="54617-106">If you make extensive use of <xref:System.Windows.Documents.Hyperlink> elements, you may want to consider showing an underline only when triggering an event, such as the <xref:System.Windows.ContentElement.MouseEnter> event.</span></span>  
  
 <span data-ttu-id="54617-107">다음 예제에서는 "My MSN" 링크 밑줄은 동적-만 표시 될 때를 <xref:System.Windows.ContentElement.MouseEnter> 이벤트가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="54617-107">In the following example, the underline for the "My MSN" link is dynamic—it only appears when the <xref:System.Windows.ContentElement.MouseEnter> event is triggered.</span></span>  
  
 <span data-ttu-id="54617-108">![Textdecoration을 표시 하는 하이퍼링크](../../../../docs/framework/wpf/advanced/media/textdecoration03.png "TextDecoration03")</span><span class="sxs-lookup"><span data-stu-id="54617-108">![Hyperlinks displaying TextDecorations](../../../../docs/framework/wpf/advanced/media/textdecoration03.png "TextDecoration03")</span></span>  
<span data-ttu-id="54617-109">Textdecoration을 사용 하 여 정의 하는 하이퍼링크</span><span class="sxs-lookup"><span data-stu-id="54617-109">Hyperlinks defined with TextDecorations</span></span>  
  
## <a name="example"></a><span data-ttu-id="54617-110">예제</span><span class="sxs-lookup"><span data-stu-id="54617-110">Example</span></span>  
 <span data-ttu-id="54617-111">다음 태그 샘플은 <xref:System.Windows.Documents.Hyperlink> 와 밑줄 없이 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="54617-111">The following markup sample shows a <xref:System.Windows.Documents.Hyperlink> defined with and without an underline:</span></span>  
  
 [!code-xaml[Performance#PerformanceSnippet11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml#performancesnippet11)]  
  
 <span data-ttu-id="54617-112">다음 코드 샘플에는 밑줄을 만드는 방법을 보여 줍니다 합니다 <xref:System.Windows.Documents.Hyperlink> 에 <xref:System.Windows.ContentElement.MouseEnter> 이벤트에서 제거 하 고는 <xref:System.Windows.ContentElement.MouseLeave> 이벤트.</span><span class="sxs-lookup"><span data-stu-id="54617-112">The following code sample shows how to create an underline for the <xref:System.Windows.Documents.Hyperlink> on the <xref:System.Windows.ContentElement.MouseEnter> event, and remove it on the <xref:System.Windows.ContentElement.MouseLeave> event.</span></span>  
  
 [!code-csharp[Performance#PerformanceSnippet15](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml.cs#performancesnippet15)]
 [!code-vb[Performance#PerformanceSnippet15](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Performance/visualbasic/hyperlink.xaml.vb#performancesnippet15)]  
  
## <a name="see-also"></a><span data-ttu-id="54617-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="54617-113">See also</span></span>
- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [<span data-ttu-id="54617-114">WPF 응용 프로그램 성능 최적화</span><span class="sxs-lookup"><span data-stu-id="54617-114">Optimizing WPF Application Performance</span></span>](../../../../docs/framework/wpf/advanced/optimizing-wpf-application-performance.md)
- [<span data-ttu-id="54617-115">텍스트 장식 만들기</span><span class="sxs-lookup"><span data-stu-id="54617-115">Create a Text Decoration</span></span>](../../../../docs/framework/wpf/advanced/how-to-create-a-text-decoration.md)
