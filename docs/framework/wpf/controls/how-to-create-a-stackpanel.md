---
title: '방법: StackPanel 만들기'
ms.date: 03/30/2017
helpviewer_keywords:
- StackPanel control [WPF], creating
ms.assetid: e7ce65cb-720a-4bb6-95b6-286b74488a58
ms.openlocfilehash: 20e2b21b10129c096398606501768a7ace0617fa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674234"
---
# <a name="how-to-create-a-stackpanel"></a><span data-ttu-id="42ecd-102">방법: StackPanel 만들기</span><span class="sxs-lookup"><span data-stu-id="42ecd-102">How to: Create a StackPanel</span></span>
<span data-ttu-id="42ecd-103">만드는 방법을 보여 주는이 예제는 <xref:System.Windows.Controls.StackPanel>합니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-103">This example shows how to create a <xref:System.Windows.Controls.StackPanel>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="42ecd-104">예제</span><span class="sxs-lookup"><span data-stu-id="42ecd-104">Example</span></span>  
 <span data-ttu-id="42ecd-105"><xref:System.Windows.Controls.StackPanel> 를 요소를 지정 된 방향에서 쌓을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-105">A <xref:System.Windows.Controls.StackPanel> allows you to stack elements in a specified direction.</span></span> <span data-ttu-id="42ecd-106">에 정의 된 속성을 사용 하 여 <xref:System.Windows.Controls.StackPanel>, 콘텐츠가 흐를 수 모두 세로 방향으로, 기본 설정 또는 가로로 합니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-106">By using properties that are defined on <xref:System.Windows.Controls.StackPanel>, content can flow both vertically, which is the default setting, or horizontally.</span></span>  
  
 <span data-ttu-id="42ecd-107">5는 다음 예제에서는 수직으로 쌓습니다 <xref:System.Windows.Controls.TextBlock> 컨트롤을 다른 각 <xref:System.Windows.Controls.Border> 하 고 <xref:System.Windows.Controls.Border.Background%2A>를 사용 하 여 <xref:System.Windows.Controls.StackPanel>입니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-107">The following example vertically stacks five <xref:System.Windows.Controls.TextBlock> controls, each with a different <xref:System.Windows.Controls.Border> and <xref:System.Windows.Controls.Border.Background%2A>, by using <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="42ecd-108">지정 되지 않은 자식 요소를 <xref:System.Windows.FrameworkElement.Width%2A> 부모 창에 맞게 늘이기; 하지만 자식 요소에 있는 지정 된 <xref:System.Windows.FrameworkElement.Width%2A>, 창의 가운데에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-108">The child elements that have no specified <xref:System.Windows.FrameworkElement.Width%2A> stretch to fill the parent window; however, the child elements that have a specified <xref:System.Windows.FrameworkElement.Width%2A>, are centered within the window.</span></span>  
  
 <span data-ttu-id="42ecd-109">기본 스택 방향을 <xref:System.Windows.Controls.StackPanel> 는 세로입니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-109">The default stack direction in a <xref:System.Windows.Controls.StackPanel> is vertical.</span></span> <span data-ttu-id="42ecd-110">컨트롤 콘텐츠 흐름에 <xref:System.Windows.Controls.StackPanel>를 사용 하 여는 <xref:System.Windows.Controls.StackPanel.Orientation%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-110">To control content flow in a <xref:System.Windows.Controls.StackPanel>, use the <xref:System.Windows.Controls.StackPanel.Orientation%2A> property.</span></span> <span data-ttu-id="42ecd-111">사용 하 여 가로 맞춤을 제어할 수 있습니다는 <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="42ecd-111">You can control horizontal alignment by using the <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> property.</span></span>  
  
```xaml  
<Page xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" WindowTitle="StackPanel Sample">  
  <StackPanel>  
    <Border Background="SkyBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="12">Stacked Item #1</TextBlock>  
    </Border>  
    <Border Width="400" Background="CadetBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="14">Stacked Item #2</TextBlock>  
    </Border>  
    <Border Background="LightGoldenRodYellow" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="16">Stacked Item #3</TextBlock>  
    </Border>  
    <Border Width="200" Background="PaleGreen" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="18">Stacked Item #4</TextBlock>  
    </Border>  
    <Border Background="White" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="20">Stacked Item #5</TextBlock>  
    </Border>  
  </StackPanel>  
</Page>  
```  
  
## <a name="see-also"></a><span data-ttu-id="42ecd-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="42ecd-112">See also</span></span>
- <xref:System.Windows.Controls.StackPanel>
- [<span data-ttu-id="42ecd-113">패널 개요</span><span class="sxs-lookup"><span data-stu-id="42ecd-113">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
- [<span data-ttu-id="42ecd-114">방법 항목</span><span class="sxs-lookup"><span data-stu-id="42ecd-114">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/stackpanel-how-to-topics.md)
