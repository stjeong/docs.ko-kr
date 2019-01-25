---
title: '방법: 컨트롤을 폼의 가장자리에 맞춤'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dock property [Windows Forms], aligning controls (using code)
- forms [Windows Forms], aligning controls
- controls [Windows Forms], aligning on forms
- custom controls [Windows Forms], docking using code
ms.assetid: 5994cb59-242b-4e75-bd0e-62879c34d702
ms.openlocfilehash: ba5e9fc92f2805206f6c3796689898f3ff845896
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610411"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms"></a><span data-ttu-id="a1d39-102">방법: 컨트롤을 폼의 가장자리에 맞춤</span><span class="sxs-lookup"><span data-stu-id="a1d39-102">How to: Align a Control to the Edges of Forms</span></span>
<span data-ttu-id="a1d39-103"><xref:System.Windows.Forms.Control.Dock%2A> 속성을 설정하여 양식 가장자리에 맞춰서 컨트롤을 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-103">You can make your control align to the edge of your forms by setting the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span> <span data-ttu-id="a1d39-104">이 속성은 양식에서 컨트롤의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-104">This property designates where your control resides in the form.</span></span> <span data-ttu-id="a1d39-105"><xref:System.Windows.Forms.Control.Dock%2A> 속성은 다음 값으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-105">The <xref:System.Windows.Forms.Control.Dock%2A> property can be set to the following values:</span></span>  
  
|<span data-ttu-id="a1d39-106">설정</span><span class="sxs-lookup"><span data-stu-id="a1d39-106">Setting</span></span>|<span data-ttu-id="a1d39-107">컨트롤에 대한 영향</span><span class="sxs-lookup"><span data-stu-id="a1d39-107">Effect on your control</span></span>|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|<span data-ttu-id="a1d39-108">양식의 아래쪽에 도킹합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-108">Docks to the bottom of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Fill>|<span data-ttu-id="a1d39-109">양식의 나머지 공간을 모두 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-109">Fills all remaining space in the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Left>|<span data-ttu-id="a1d39-110">양식의 왼쪽에 도킹합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-110">Docks to the left side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.None>|<span data-ttu-id="a1d39-111">도킹하지 않고 <xref:System.Windows.Forms.Control.Location%2A> 속성으로 지정된 위치에 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-111">Does not dock anywhere, and it appears at the location specified by its <xref:System.Windows.Forms.Control.Location%2A> property.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Right>|<span data-ttu-id="a1d39-112">컨트롤을 양식의 오른쪽에 도킹합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-112">Docks to the right side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Top>|<span data-ttu-id="a1d39-113">양식의 위쪽에 도킹합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-113">Docks to the top of the form.</span></span>|  
  
 <span data-ttu-id="a1d39-114">Visual Studio에서는 디자인 타임에 이 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-114">There is design-time support for this feature in Visual Studio.</span></span>  
  
### <a name="to-set-the-dock-property-for-your-control-at-run-time"></a><span data-ttu-id="a1d39-115">런타임에 컨트롤에 대한 Dock 속성을 설정하려면</span><span class="sxs-lookup"><span data-stu-id="a1d39-115">To set the Dock property for your control at run time</span></span>  
  
1.  <span data-ttu-id="a1d39-116">코드에서 <xref:System.Windows.Forms.Control.Dock%2A> 속성을 적절한 값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1d39-116">Set the <xref:System.Windows.Forms.Control.Dock%2A> property to the appropriate value in code.</span></span>  
  
    ```vb  
    ' To set the Dock property internally.  
    Me.Dock = DockStyle.Top  
    ' To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top  
    ```  
  
    ```csharp  
    // To set the Dock property internally.  
    this.Dock = DockStyle.Top;  
    // To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="a1d39-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="a1d39-117">See also</span></span>
- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [<span data-ttu-id="a1d39-118">.NET Framework에서 사용자 지정 Windows Forms 컨트롤 개발</span><span class="sxs-lookup"><span data-stu-id="a1d39-118">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="a1d39-119">방법: FlowLayoutPanel 컨트롤의 자식 컨트롤 고정 및 도킹</span><span class="sxs-lookup"><span data-stu-id="a1d39-119">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="a1d39-120">방법: TableLayoutPanel 컨트롤의 자식 컨트롤 고정 및 도킹</span><span class="sxs-lookup"><span data-stu-id="a1d39-120">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="a1d39-121">AutoSize 속성 개요</span><span class="sxs-lookup"><span data-stu-id="a1d39-121">AutoSize Property Overview</span></span>](../../../../docs/framework/winforms/controls/autosize-property-overview.md)
