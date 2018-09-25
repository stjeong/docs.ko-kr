---
title: TreeWalker를 사용하여 UI 자동화 요소 간 탐색
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- classes, TreeWalker
- TreeWalker class
- elements, navigating among
- UI Automation, navigating among elements
ms.assetid: afcd21dc-2ffa-48c9-9332-51269f44b7e9
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: f2f7c140211e558677ce90fcc3ef138a2022881f
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47077995"
---
# <a name="navigate-among-ui-automation-elements-with-treewalker"></a><span data-ttu-id="7e788-102">TreeWalker를 사용하여 UI 자동화 요소 간 탐색</span><span class="sxs-lookup"><span data-stu-id="7e788-102">Navigate Among UI Automation Elements with TreeWalker</span></span>
> [!NOTE]
>  <span data-ttu-id="7e788-103">이 설명서는 <xref:System.Windows.Automation> 네임스페이스에 정의된 관리되는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 클래스를 사용하려는 .NET Framework 개발자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7e788-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="7e788-104">에 대 한 최신 정보에 대 한 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]를 참조 하세요 [Windows Automation API: UI 자동화](https://go.microsoft.com/fwlink/?LinkID=156746)합니다.</span><span class="sxs-lookup"><span data-stu-id="7e788-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="7e788-105">이 항목 간에 이동 하는 방법을 보여 주는 예제 코드가 포함 되어 있습니다 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] 를 사용 하 여 요소를 <xref:System.Windows.Automation.TreeWalker> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="7e788-105">This topic contains example code that shows how to navigate among [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] elements by using the <xref:System.Windows.Automation.TreeWalker> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e788-106">예제</span><span class="sxs-lookup"><span data-stu-id="7e788-106">Example</span></span>  
 <span data-ttu-id="7e788-107">다음 예제에서는 <xref:System.Windows.Automation.TreeWalker.GetParent%2A> 를 탐색 하려면는 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] 트리 루트 요소 또는 데스크톱을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7e788-107">The following example uses <xref:System.Windows.Automation.TreeWalker.GetParent%2A> to walk up the [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] tree until it finds the root element, or desktop.</span></span> <span data-ttu-id="7e788-108">바로 아래에 있는 요소에 지정 된 요소의 부모 창입니다.</span><span class="sxs-lookup"><span data-stu-id="7e788-108">The element just below that is the parent window of the specified element.</span></span>  
  
 [!code-csharp[UIAFocusTracker_snip#102](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFocusTracker_snip/CSharp/FocusTracker.cs#102)]
 [!code-vb[UIAFocusTracker_snip#102](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFocusTracker_snip/VisualBasic/FocusTracker.vb#102)]  
  
## <a name="example"></a><span data-ttu-id="7e788-109">예제</span><span class="sxs-lookup"><span data-stu-id="7e788-109">Example</span></span>  
 <span data-ttu-id="7e788-110">다음 예제에서는 <xref:System.Windows.Automation.TreeWalker.GetFirstChild%2A> 하 고 <xref:System.Windows.Automation.TreeWalker.GetNextSibling%2A> 만들려면를 <xref:System.Windows.Forms.TreeView> 의 전체 하위 트리를 보여 주는 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] 컨트롤 보기에 있는 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="7e788-110">The following example uses <xref:System.Windows.Automation.TreeWalker.GetFirstChild%2A> and <xref:System.Windows.Automation.TreeWalker.GetNextSibling%2A> to create a <xref:System.Windows.Forms.TreeView> that shows an entire subtree of [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] elements that are in the control view and that are enabled.</span></span>  
  
 [!code-csharp[UIAClient_snip#174](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#174)]
 [!code-vb[UIAClient_snip#174](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#174)]  
  
## <a name="see-also"></a><span data-ttu-id="7e788-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7e788-111">See Also</span></span>  
 [<span data-ttu-id="7e788-112">UI 자동화 요소 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e788-112">Obtaining UI Automation Elements</span></span>](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)
