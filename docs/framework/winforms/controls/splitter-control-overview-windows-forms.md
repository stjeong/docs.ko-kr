---
title: Splitter 컨트롤 개요(Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Splitter
helpviewer_keywords:
- Splitter control [Windows Forms], about Splitter control
ms.assetid: e2b6ab83-dfdd-40ec-9762-850702c82dcb
ms.openlocfilehash: 583596ec44dd5318c199d6cfc33901dbd952b115
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54522611"
---
# <a name="splitter-control-overview-windows-forms"></a><span data-ttu-id="c4ed4-102">Splitter 컨트롤 개요(Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="c4ed4-102">Splitter Control Overview (Windows Forms)</span></span>
> [!IMPORTANT]
>  <span data-ttu-id="c4ed4-103"><xref:System.Windows.Forms.SplitContainer>은 이전 버전의 <xref:System.Windows.Forms.Splitter> 컨트롤을 대체하고 확장한 컨트롤이지만 이전 버전과의 호환성 및 앞으로의 사용 가능성을 고려하여 <xref:System.Windows.Forms.Splitter>를 유지하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4ed4-103">Although <xref:System.Windows.Forms.SplitContainer> replaces and adds functionality to the <xref:System.Windows.Forms.Splitter> control of previous versions, <xref:System.Windows.Forms.Splitter> is retained for both backward compatibility and future use if you choose.</span></span>  
  
 <span data-ttu-id="c4ed4-104">Windows Forms <xref:System.Windows.Forms.Splitter> 컨트롤은 런타임에 도킹 된 컨트롤의 크기를 조정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4ed4-104">Windows Forms <xref:System.Windows.Forms.Splitter> controls are used to resize docked controls at run time.</span></span> <span data-ttu-id="c4ed4-105"><xref:System.Windows.Forms.Splitter> 컨트롤은 Windows 탐색기와 데이터 창에는 서로 다른 시간에 다양 한 너비의 정보가 포함 되어 있는 데이터의 길이 다양 한 컨트롤과 폼에 자주 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4ed4-105">The <xref:System.Windows.Forms.Splitter> control is often used on forms with controls that have varying lengths of data to present, like Windows Explorer, whose data panes contain information of varying widths at different times.</span></span>  
  
## <a name="working-with-the-splitter-control"></a><span data-ttu-id="c4ed4-106">Splitter 컨트롤 사용</span><span class="sxs-lookup"><span data-stu-id="c4ed4-106">Working with the Splitter Control</span></span>  
 <span data-ttu-id="c4ed4-107">Splitter 컨트롤을 크기를 조정할 수 있는 컨트롤의 도킹 되지 않은 가장자리 마우스 포인터를 가리키는 사용자, 포인터를 컨트롤의 크기를 조정할 수 있음을 나타내는 모양이 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ed4-107">When the user points the mouse pointer at the undocked edge of a control that can be resized by a splitter control, the pointer changes its appearance to indicate that the control can be resized.</span></span> <span data-ttu-id="c4ed4-108">Splitter 컨트롤을 사용 하 여 사용자의 크기를 바로 앞에 있는 도킹된 된 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ed4-108">With the splitter control, the user can resize the docked control that is immediately before it.</span></span> <span data-ttu-id="c4ed4-109">따라서 런타임에 도킹된 된 컨트롤 크기를 조정 하려면 사용자를 사용 하려면 컨트롤 컨테이너의 가장자리에 도킹 하 고 해당 컨테이너의 같은 쪽에 splitter 컨트롤을 도킹 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ed4-109">Therefore, to enable the user to resize a docked control at run time, dock the control to be resized to an edge of a container, and then dock a splitter control to the same side of that container.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4ed4-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="c4ed4-110">See also</span></span>
- <xref:System.Windows.Forms.SplitContainer>
- [<span data-ttu-id="c4ed4-111">방법: Windows Forms에 컨트롤 도킹</span><span class="sxs-lookup"><span data-stu-id="c4ed4-111">How to: Dock Controls on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-dock-controls-on-windows-forms.md)
- [<span data-ttu-id="c4ed4-112">Windows Forms에 사용할 수 있는 컨트롤</span><span class="sxs-lookup"><span data-stu-id="c4ed4-112">Controls to Use on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
