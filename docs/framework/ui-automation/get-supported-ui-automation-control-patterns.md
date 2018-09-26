---
title: 지원되는 UI 자동화 컨트롤 패턴 가져오기
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- control patterns, getting
- UI Automation, getting control patterns
- getting, control patterns
ms.assetid: 006c54c9-50bf-48d9-a855-9d62eb95603a
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: d948ff2f71ff7d4335cacc0fa3815dd75af4ad45
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47231383"
---
# <a name="get-supported-ui-automation-control-patterns"></a>지원되는 UI 자동화 컨트롤 패턴 가져오기
> [!NOTE]
>  이 설명서는 <xref:System.Windows.Automation> 네임스페이스에 정의된 관리되는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 클래스를 사용하려는 .NET Framework 개발자를 위한 것입니다. 에 대 한 최신 정보에 대 한 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]를 참조 하세요 [Windows Automation API: UI 자동화](https://go.microsoft.com/fwlink/?LinkID=156746)합니다.  
  
 이 항목에서는에서 컨트롤 패턴 개체를 검색 하는 방법을 보여 줍니다. [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 요소입니다.  
  
### <a name="obtain-all-control-patterns"></a>모든 컨트롤 패턴 가져오기  
  
1.  가져오기는 <xref:System.Windows.Automation.AutomationElement> 관심 있는 해당 컨트롤 패턴이 있습니다.  
  
2.  호출 <xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A> 요소에서 모든 컨트롤 패턴을 가져오려고 합니다.  
  
> [!CAUTION]
>  클라이언트를 사용 하지 않도록이 가장 좋습니다 <xref:System.Windows.Automation.AutomationElement.GetSupportedPatterns%2A>합니다. 이 메서드를 호출 하는 대로 성능이 심각 하 게 저하 될 수 있습니다 <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> 기존의 각 컨트롤 패턴에 대해 내부적으로 합니다. 가능한 경우 클라이언트를 호출 해야 <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> 키 패턴에 대 한 합니다.  
  
### <a name="obtain-a-specific-control-pattern"></a>특정 컨트롤 패턴 가져오기  
  
1.  가져오기는 <xref:System.Windows.Automation.AutomationElement> 관심 있는 해당 컨트롤 패턴이 있습니다.  
  
2.  호출 <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> 또는 <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> 특정 패턴에 대 한 쿼리 합니다. 이러한 메서드는 비슷하지만, 패턴이 없으면 하지만 <xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A> 예외를 발생 시키고 및 <xref:System.Windows.Automation.AutomationElement.TryGetCurrentPattern%2A> 반환 `false`합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 검색을 <xref:System.Windows.Automation.AutomationElement> 목록 항목에 대 한 가져옵니다는 <xref:System.Windows.Automation.SelectionItemPattern> 해당 요소에서 합니다.  
  
 [!code-csharp[UIAClient_snip#103](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#103)]
 [!code-vb[UIAClient_snip#103](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#103)]  
  
## <a name="see-also"></a>참고 항목  
 [클라이언트용 UI 자동화 컨트롤 패턴](../../../docs/framework/ui-automation/ui-automation-control-patterns-for-clients.md)
