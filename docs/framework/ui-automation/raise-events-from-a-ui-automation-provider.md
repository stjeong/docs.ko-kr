---
title: UI 자동화 공급자에서 이벤트 발생
ms.date: 03/30/2017
helpviewer_keywords:
- UI Automation, raising events
- raising UI Automation events
ms.assetid: 9fe2f01b-f7d8-49a8-a185-d4472b9976c0
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: d8c65be9135049be81694c3aa375df0b27641bf2
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47398971"
---
# <a name="raise-events-from-a-ui-automation-provider"></a><span data-ttu-id="85ee9-102">UI 자동화 공급자에서 이벤트 발생</span><span class="sxs-lookup"><span data-stu-id="85ee9-102">Raise Events from a UI Automation Provider</span></span>
> [!NOTE]
>  <span data-ttu-id="85ee9-103">이 설명서는 <xref:System.Windows.Automation> 네임스페이스에 정의된 관리되는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 클래스를 사용하려는 .NET Framework 개발자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="85ee9-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="85ee9-104">에 대 한 최신 정보에 대 한 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]를 참조 하세요 [Windows Automation API: UI 자동화](https://go.microsoft.com/fwlink/?LinkID=156746)합니다.</span><span class="sxs-lookup"><span data-stu-id="85ee9-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="85ee9-105">이 항목에는 UI 자동화 공급자에서 이벤트를 발생시키는 방법을 보여주는 예제 코드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85ee9-105">This topic contains example code that shows how to raise an event from a UI Automation provider.</span></span>  
  
## <a name="example"></a><span data-ttu-id="85ee9-106">예제</span><span class="sxs-lookup"><span data-stu-id="85ee9-106">Example</span></span>  
 <span data-ttu-id="85ee9-107">다음 예제에서는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 이벤트가 사용자 지정 단추 컨트롤의 구현에서 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="85ee9-107">In the following example, a [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] event is raised in the implementation of a custom button control.</span></span> <span data-ttu-id="85ee9-108">이 구현을 통해 UI 자동화 클라이언트 응용 프로그램이 단추 클릭을 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85ee9-108">The implementation enables a UI Automation client application to simulate a button click.</span></span>  
  
 <span data-ttu-id="85ee9-109">불필요한 프로세스를 방지하기 위해, 이 예제에서는 <xref:System.Windows.Automation.Provider.AutomationInteropProvider.ClientsAreListening%2A> 을 검사하여 이벤트 발생 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="85ee9-109">To avoid unnecessary processing, the example checks <xref:System.Windows.Automation.Provider.AutomationInteropProvider.ClientsAreListening%2A> to see whether events should be raised.</span></span>  
  
 [!code-csharp[UIAProvider_snip#150](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAProvider_snip/CSharp/FragmentRoot.cs#150)]  
  
## <a name="see-also"></a><span data-ttu-id="85ee9-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="85ee9-110">See Also</span></span>  
 [<span data-ttu-id="85ee9-111">UI 자동화 공급자 개요</span><span class="sxs-lookup"><span data-stu-id="85ee9-111">UI Automation Providers Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-providers-overview.md)
