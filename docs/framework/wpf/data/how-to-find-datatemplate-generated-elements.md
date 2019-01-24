---
title: '방법: DataTemplate에서 생성된 요소 찾기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- finding DataTemplate elements [WPF]
- DataTemplate [WPF]
ms.assetid: bfcd564e-5e9e-451e-8641-a9b5c3cfac90
ms.openlocfilehash: d271a3d53a0e102f8f969fd0751e15b470a52862
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511568"
---
# <a name="how-to-find-datatemplate-generated-elements"></a>방법: DataTemplate에서 생성된 요소 찾기
이 예제에 의해 생성 된 요소를 찾는 방법을 보여 줍니다는 <xref:System.Windows.DataTemplate>합니다.  
  
## <a name="example"></a>예제  
 이 예에는 <xref:System.Windows.Controls.ListBox> 일부에 바인딩된 [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] 데이터:  
  
 [!code-xaml[FindGeneratedItems#LB](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#lb)]  
  
 합니다 <xref:System.Windows.Controls.ListBox> 다음을 사용 하 여 <xref:System.Windows.DataTemplate>:  
  
 [!code-xaml[FindGeneratedItems#DT](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#dt)]  
  
 검색 하려는 경우는 <xref:System.Windows.Controls.TextBlock> 의해 생성 된 요소를 <xref:System.Windows.DataTemplate> 특정 <xref:System.Windows.Controls.ListBoxItem>, 가져올 필요가 <xref:System.Windows.Controls.ListBoxItem>, 찾을 <xref:System.Windows.Controls.ContentPresenter> 내 <xref:System.Windows.Controls.ListBoxItem>, 호출 <xref:System.Windows.FrameworkTemplate.FindName%2A> 에 <xref:System.Windows.DataTemplate> 에 설정 된 <xref:System.Windows.Controls.ContentPresenter>합니다. 다음 예제에서는 이러한 단계를 수행 하는 방법을 보여 줍니다. 데모용으로이 상자를 만드는이 예제 메시지 텍스트를 보여 주는의 콘텐츠는 <xref:System.Windows.DataTemplate>-텍스트 블록을 생성 합니다.  
  
 [!code-csharp[FindGeneratedItems#DTFindElement](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#dtfindelement)]
 [!code-vb[FindGeneratedItems#DTFindElement](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#dtfindelement)]  
  
 다음은 구현의 `FindVisualChild`를 사용 하는 <xref:System.Windows.Media.VisualTreeHelper> 메서드:  
  
 [!code-csharp[FindGeneratedItems#FVC](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#fvc)]
 [!code-vb[FindGeneratedItems#FVC](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#fvc)]  
  
## <a name="see-also"></a>참고자료
- [방법: ControlTemplate에서 생성 된 요소 찾기](../../../../docs/framework/wpf/controls/how-to-find-controltemplate-generated-elements.md)
- [데이터 바인딩 개요](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [방법 항목](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
- [스타일 지정 및 템플릿](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [WPF XAML 이름 범위](../../../../docs/framework/wpf/advanced/wpf-xaml-namescopes.md)
- [WPF의 트리](../../../../docs/framework/wpf/advanced/trees-in-wpf.md)
