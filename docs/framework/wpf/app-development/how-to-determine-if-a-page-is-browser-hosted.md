---
title: '방법: 브라우저에서 호스팅되는 페이지 인지 확인 합니다.'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosted pages in browser [WPF]
- pages [WPF], hosted in browser
ms.assetid: 737e0f26-8371-49b4-9579-70879e51e1aa
ms.openlocfilehash: aa2aa36e4f887c4fa02314f7834e2a46268c8ff9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54661297"
---
# <a name="how-to-determine-if-a-page-is-browser-hosted"></a><span data-ttu-id="3d601-102">방법: 브라우저에서 호스팅되는 페이지 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d601-102">How to: Determine If a Page is Browser Hosted</span></span>
<span data-ttu-id="3d601-103">확인 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Controls.Page> 브라우저에서 호스팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d601-103">This example demonstrates how to determine if a <xref:System.Windows.Controls.Page> is hosted in a browser.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d601-104">예제</span><span class="sxs-lookup"><span data-stu-id="3d601-104">Example</span></span>  
 <span data-ttu-id="3d601-105"><xref:System.Windows.Controls.Page> 알 수 없는 호스트 수 및 결과적으로 호스트를 비롯 한 여러 가지 형식으로 로드할 수는 <xref:System.Windows.Controls.Frame>, <xref:System.Windows.Navigation.NavigationWindow>, 또는 브라우저.</span><span class="sxs-lookup"><span data-stu-id="3d601-105">A <xref:System.Windows.Controls.Page> can be host agnostic and, consequently, can be loaded into several different types of hosts, including a <xref:System.Windows.Controls.Frame>, a <xref:System.Windows.Navigation.NavigationWindow>, or a browser.</span></span> <span data-ttu-id="3d601-106">라이브러리 어셈블리를 하나 이상의 페이지를 포함 하 고는 참조 되는 여러 독립 실행형으로 탐색할 수 있는 경우 발생할 수 있습니다 ([!INCLUDE[TLA#tla_xbap](../../../../includes/tlasharptla-xbap-md.md)]) 애플리케이션을 호스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d601-106">This can happen when you have a library assembly that contains one or more pages, and which is referenced by multiple standalone and browsable ([!INCLUDE[TLA#tla_xbap](../../../../includes/tlasharptla-xbap-md.md)]) host applications.</span></span>  
  
 <span data-ttu-id="3d601-107">다음 예제에 사용 하는 방법을 보여 줍니다. <xref:System.Windows.Interop.BrowserInteropHelper.IsBrowserHosted%2A?displayProperty=nameWithType> 여부를 확인 하는 <xref:System.Windows.Controls.Page> 브라우저에서 호스팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d601-107">The following example demonstrates how to use <xref:System.Windows.Interop.BrowserInteropHelper.IsBrowserHosted%2A?displayProperty=nameWithType> to determine if a <xref:System.Windows.Controls.Page> is hosted in a browser.</span></span>  
  
 [!code-csharp[HOWTOBrowserInteropHelperSnippets#IsBrowserHostedCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOBrowserInteropHelperSnippets/CSharp/Page1.xaml.cs#isbrowserhostedcode)]
 [!code-vb[HOWTOBrowserInteropHelperSnippets#IsBrowserHostedCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOBrowserInteropHelperSnippets/visualbasic/page1.xaml.vb#isbrowserhostedcode)]  
  
## <a name="see-also"></a><span data-ttu-id="3d601-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="3d601-108">See also</span></span>
- <xref:System.Windows.Controls.Frame>
- <xref:System.Windows.Controls.Page>
