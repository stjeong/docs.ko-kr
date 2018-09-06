---
title: UI 자동화를 사용하여 텍스트 찾기 및 강조
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text, highlighting
- finding text
- text, finding
- UI automation, highlighting text
- UI automation, finding text
- highlighting text
ms.assetid: b77693f5-87bb-4b29-a297-05ff882e2044
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 7229c9468948061726e81e3c79d2ab56e7497fa4
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858231"
---
# <a name="find-and-highlight-text-using-ui-automation"></a><span data-ttu-id="a3cc3-102">UI 자동화를 사용하여 텍스트 찾기 및 강조</span><span class="sxs-lookup"><span data-stu-id="a3cc3-102">Find and Highlight Text Using UI Automation</span></span>
> [!NOTE]
>  <span data-ttu-id="a3cc3-103">이 설명서는 <xref:System.Windows.Automation> 네임스페이스에 정의된 관리되는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 클래스를 사용하려는 .NET Framework 개발자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="a3cc3-104">에 대 한 최신 정보에 대 한 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]를 참조 하세요 [Windows Automation API: UI 자동화](https://go.microsoft.com/fwlink/?LinkID=156746)합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="a3cc3-105">이 항목에는 순차적으로 검색 하 고 사용 하 여 텍스트 컨트롤의 콘텐츠 내에 있는 문자열의 각 항목을 강조 표시 하는 방법을 보여 줍니다. [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-105">This topic demonstrates how to sequentially search for and highlight each occurrence of a string within the content of a text control using [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3cc3-106">예제</span><span class="sxs-lookup"><span data-stu-id="a3cc3-106">Example</span></span>  
 <span data-ttu-id="a3cc3-107">다음 예에서는 한 <xref:System.Windows.Automation.TextPattern> 텍스트 컨트롤 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-107">The following example obtains a <xref:System.Windows.Automation.TextPattern> object from a text control.</span></span> <span data-ttu-id="a3cc3-108">A <xref:System.Windows.Automation.Text.TextPatternRange> 전체 문서의 텍스트 내용을 나타내는 개체를 사용 하 여 만든은 <xref:System.Windows.Automation.TextPattern.DocumentRange%2A> 속성 <xref:System.Windows.Automation.TextPattern>합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-108">A <xref:System.Windows.Automation.Text.TextPatternRange> object, representing the textual content of the entire document, is then created using the <xref:System.Windows.Automation.TextPattern.DocumentRange%2A> property of this <xref:System.Windows.Automation.TextPattern>.</span></span> <span data-ttu-id="a3cc3-109">두 개의 추가 <xref:System.Windows.Automation.Text.TextPatternRange> 개체는 만들어진 다음에 대해 순차적 검색 및 기능을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cc3-109">Two additional <xref:System.Windows.Automation.Text.TextPatternRange> objects are then created for the sequential search and highlight functionality.</span></span>  
  
 [!code-csharp[FindText#StartApp](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#startapp)]
 [!code-vb[FindText#StartApp](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#startapp)]  
[!code-csharp[FindText#FindTextProvider](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#findtextprovider)]
[!code-vb[FindText#FindTextProvider](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#findtextprovider)]  
[!code-csharp[FindText#SearchTarget](../../../samples/snippets/csharp/VS_Snippets_Wpf/FindText/CSharp/SearchWindow.cs#searchtarget)]
[!code-vb[FindText#SearchTarget](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindText/VisualBasic/SearchWindow.vb#searchtarget)]  
  
## <a name="see-also"></a><span data-ttu-id="a3cc3-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a3cc3-110">See Also</span></span>  
 [<span data-ttu-id="a3cc3-111">UI 자동화를 사용하여 텍스트 찾기 및 강조</span><span class="sxs-lookup"><span data-stu-id="a3cc3-111">Find and Highlight Text Using UI Automation</span></span>](../../../docs/framework/ui-automation/find-and-highlight-text-using-ui-automation.md)
