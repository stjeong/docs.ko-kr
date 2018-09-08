---
title: '방법: 탐색 기록을 뒤로 탐색'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating back
- navigation [WPF], through navigation history (back)
ms.assetid: 9343234b-d864-441d-b8a7-d895cba80a87
ms.openlocfilehash: 7266c9486524e962a859c34c9be5ab8f6d7bf7d5
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44206025"
---
# <a name="how-to-navigate-back-through-navigation-history"></a>방법: 탐색 기록을 뒤로 탐색
이 예제에서는 탐색 기록에서 항목을 탐색 하는 방법을 보여 줍니다.  
  
## <a name="example"></a>예제  
 호스트 되는 내용에서 실행 되는 코드를 <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame> 사용 하 여 <xref:System.Windows.Navigation.NavigationService>, 또는 [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)] 탐색 기록에서 한 번에 하나의 항목을 통해 다시 이동할 수 있습니다.  
  
 탐색 한 항목이 먼저 검사 하 여 후방 탐색 기록에 항목이 있는지를 확인 해야 합니다 **CanGoBack** 속성을 호출 하 여 하나의 항목을 다시 이동 하기 전에 **GoBack** 메서드입니다. 이 다음 예제에 나와 있습니다.  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoBack** 하 고 **GoBack** 하 여 구현 됩니다 <xref:System.Windows.Navigation.NavigationWindow>를 <xref:System.Windows.Controls.Frame>, 및 <xref:System.Windows.Navigation.NavigationService>합니다.  
  
> [!NOTE]
>  호출 하는 경우 **GoBack**, 후방 탐색 기록에 항목이 없음 및는 <xref:System.InvalidOperationException> 발생 합니다.
