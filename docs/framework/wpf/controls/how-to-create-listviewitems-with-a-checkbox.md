---
title: '방법: CheckBox를 사용하여 ListViewItems 만들기'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: 1ed623495529609c83c0ced68bfc1696c29d4570
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54682244"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a><span data-ttu-id="a01d1-102">방법: CheckBox를 사용하여 ListViewItems 만들기</span><span class="sxs-lookup"><span data-stu-id="a01d1-102">How to: Create ListViewItems with a CheckBox</span></span>
<span data-ttu-id="a01d1-103">이 예제에서는 열을 표시 하는 방법을 보여 줍니다 <xref:System.Windows.Controls.CheckBox> 컨트롤을 <xref:System.Windows.Controls.ListView> 사용 하는 컨트롤을 <xref:System.Windows.Controls.GridView>입니다.</span><span class="sxs-lookup"><span data-stu-id="a01d1-103">This example shows how to display a column of <xref:System.Windows.Controls.CheckBox> controls in a <xref:System.Windows.Controls.ListView> control that uses a <xref:System.Windows.Controls.GridView>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a01d1-104">예제</span><span class="sxs-lookup"><span data-stu-id="a01d1-104">Example</span></span>  
 <span data-ttu-id="a01d1-105">포함 된 열을 만들려면 <xref:System.Windows.Controls.CheckBox> 컨트롤을 <xref:System.Windows.Controls.ListView>, 만들기를 <xref:System.Windows.DataTemplate> 포함 하는 <xref:System.Windows.Controls.CheckBox>합니다.</span><span class="sxs-lookup"><span data-stu-id="a01d1-105">To create a column that contains <xref:System.Windows.Controls.CheckBox> controls in a <xref:System.Windows.Controls.ListView>, create a <xref:System.Windows.DataTemplate> that contains a <xref:System.Windows.Controls.CheckBox>.</span></span> <span data-ttu-id="a01d1-106">설정한 합니다 <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> 의 <xref:System.Windows.Controls.GridViewColumn> 에 <xref:System.Windows.DataTemplate>합니다.</span><span class="sxs-lookup"><span data-stu-id="a01d1-106">Then set the <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> of a <xref:System.Windows.Controls.GridViewColumn> to the <xref:System.Windows.DataTemplate>.</span></span>  
  
 <span data-ttu-id="a01d1-107">다음 예제와 <xref:System.Windows.DataTemplate> 를 포함 하는 <xref:System.Windows.Controls.CheckBox>합니다.</span><span class="sxs-lookup"><span data-stu-id="a01d1-107">The following example shows a <xref:System.Windows.DataTemplate> that contains a <xref:System.Windows.Controls.CheckBox>.</span></span> <span data-ttu-id="a01d1-108">예제를 <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> 의 속성을 <xref:System.Windows.Controls.CheckBox> 에 <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> 속성 값을 <xref:System.Windows.Controls.ListViewItem> 포함 된.</span><span class="sxs-lookup"><span data-stu-id="a01d1-108">The example binds the <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> property of the <xref:System.Windows.Controls.CheckBox> to the <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> property value of the <xref:System.Windows.Controls.ListViewItem> that contains it.</span></span> <span data-ttu-id="a01d1-109">따라서 경우는 <xref:System.Windows.Controls.ListViewItem> 포함 하는 합니다 <xref:System.Windows.Controls.CheckBox> 을 선택 하면를 <xref:System.Windows.Controls.CheckBox> 확인란이 선택 되어 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01d1-109">Therefore, when the <xref:System.Windows.Controls.ListViewItem> that contains the <xref:System.Windows.Controls.CheckBox> is selected, the <xref:System.Windows.Controls.CheckBox> is checked.</span></span>  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 <span data-ttu-id="a01d1-110">다음 예제에는 열을 만드는 방법을 보여 줍니다 <xref:System.Windows.Controls.CheckBox> 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="a01d1-110">The following example shows how to create a column of <xref:System.Windows.Controls.CheckBox> controls.</span></span> <span data-ttu-id="a01d1-111">예제에서는 열 수 있도록를 <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> 의 속성을 <xref:System.Windows.Controls.GridViewColumn> 에 <xref:System.Windows.DataTemplate>.</span><span class="sxs-lookup"><span data-stu-id="a01d1-111">To make the column, the example sets the <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> property of the <xref:System.Windows.Controls.GridViewColumn> to the <xref:System.Windows.DataTemplate>.</span></span>  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a><span data-ttu-id="a01d1-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="a01d1-112">See also</span></span>
- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="a01d1-113">ListView 개요</span><span class="sxs-lookup"><span data-stu-id="a01d1-113">ListView Overview</span></span>](../../../../docs/framework/wpf/controls/listview-overview.md)
- [<span data-ttu-id="a01d1-114">방법 항목</span><span class="sxs-lookup"><span data-stu-id="a01d1-114">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [<span data-ttu-id="a01d1-115">GridView 개요</span><span class="sxs-lookup"><span data-stu-id="a01d1-115">GridView Overview</span></span>](../../../../docs/framework/wpf/controls/gridview-overview.md)
