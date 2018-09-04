---
title: UI 자동화 공급자에서 속성 반환
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- providers, UI Automation, returning properties
- properties, returned by UI Automation providers
- UI Automation, providers returning properties
ms.assetid: 5eba950e-b9e1-48eb-ab8e-b69db76bf589
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 3e24d9bebc891ecdae9d3a68d700d053194374ce
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43527069"
---
# <a name="return-properties-from-a-ui-automation-provider"></a>UI 자동화 공급자에서 속성 반환
> [!NOTE]
>  이 설명서는 <xref:System.Windows.Automation> 네임스페이스에 정의된 관리되는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 클래스를 사용하려는 .NET Framework 개발자를 위한 것입니다. 에 대 한 최신 정보에 대 한 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]를 참조 하세요 [Windows Automation API: UI 자동화](https://go.microsoft.com/fwlink/?LinkID=156746)합니다.  
  
 이 항목에는 UI 자동화 공급자가 클라이언트 응용 프로그램에 요소의 속성을 반환할 수 있는 방법을 보여주는 샘플 코드가 있습니다.  
  
 명시적으로 지원되지 않는 모든 속성의 경우 공급자는 `null` 을 반환해야 합니다(Visual Basic의 경우`Nothing` ). 이렇게 하면 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 이 호스트 창 공급자와 같은 다른 소스에서 속성을 가져올 수 있습니다.  
  
## <a name="example"></a>예제  
 [!code-csharp[UIAFragmentProvider_snip#117](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFragmentProvider_snip/CSharp/ListFragment.cs#117)]
 [!code-vb[UIAFragmentProvider_snip#117](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFragmentProvider_snip/VisualBasic/ListFragment.vb#117)]  
  
## <a name="see-also"></a>참고 항목  
 [UI 자동화 공급자 개요](../../../docs/framework/ui-automation/ui-automation-providers-overview.md)  
 [서버 쪽 UI 자동화 공급자 구현](../../../docs/framework/ui-automation/server-side-ui-automation-provider-implementation.md)
