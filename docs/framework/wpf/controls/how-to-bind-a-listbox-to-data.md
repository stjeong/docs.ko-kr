---
title: '방법: 데이터에 ListBox 바인딩'
ms.date: 03/30/2017
helpviewer_keywords:
- ListBox controls [WPF], binding data to
- data binding [WPF], ListBox control
- binding data [WPF], to ListBox control
ms.assetid: de93a907-709a-44a7-84bf-578b846a3d8b
ms.openlocfilehash: 6d37cda057ea1e7ca6761363857a2647da37afee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650654"
---
# <a name="how-to-bind-a-listbox-to-data"></a>방법: 데이터에 ListBox 바인딩
응용 프로그램 개발자가 만들 수 있습니다 <xref:System.Windows.Controls.ListBox> 각각의 내용을 지정 하지 않고 컨트롤 <xref:System.Windows.Controls.ListBoxItem> 개별적으로 합니다. 개별 항목에 데이터를 바인딩할 데이터 바인딩을 사용할 수 있습니다.  
  
 다음 예제에서는 만드는 방법을 보여 줍니다.는 <xref:System.Windows.Controls.ListBox> 채우는 합니다 <xref:System.Windows.Controls.ListBoxItem> 라는 데이터 원본에 데이터 바인딩하여 요소 *색*합니다. 사용 하 여 필요 없는 경우 <xref:System.Windows.Controls.ListBoxItem> 각 항목의 내용을 지정 하는 태그입니다.  
  
## <a name="example"></a>예제  
 [!code-xaml[ListBoxEvent#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#7)]  
[!code-xaml[ListBoxEvent#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#3)]  
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.Controls.ListBoxItem>
- [컨트롤](../../../../docs/framework/wpf/advanced/optimizing-performance-controls.md)
