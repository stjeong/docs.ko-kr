---
title: ToolStripProgressBar 컨트롤 개요
ms.date: 03/30/2017
f1_keywords:
- ToolStripProgressBar
helpviewer_keywords:
- toolbars [Windows Forms], progress bars
- progress controls [Windows Forms]
- ToolStripProgressBar control [Windows Forms], about ToolStripProgressBar control
ms.assetid: ec3ab522-5fe4-4b4d-a551-bc19e84f4774
ms.openlocfilehash: 57a8c61c71fa17e1d3df309007823eab76d9efb1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528630"
---
# <a name="toolstripprogressbar-control-overview"></a><span data-ttu-id="32243-102">ToolStripProgressBar 컨트롤 개요</span><span class="sxs-lookup"><span data-stu-id="32243-102">ToolStripProgressBar Control Overview</span></span>
<span data-ttu-id="32243-103">합니다 <xref:System.Windows.Forms.ToolStripProgressBar> 래프팅 및 모든 렌더링 기능이 결합 <xref:System.Windows.Forms.ToolStrip> 일반적인 프로세스 추적 기능을 사용 하 여 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="32243-103">The <xref:System.Windows.Forms.ToolStripProgressBar> combines the rafting and rendering functionality of all <xref:System.Windows.Forms.ToolStrip> controls with its typical process-tracking functionality.</span></span> <span data-ttu-id="32243-104"><xref:System.Windows.Forms.ToolStripProgressBar> 가장 일반적으로 호스팅하 <xref:System.Windows.Forms.StatusStrip>에 의해서도 자주를 <xref:System.Windows.Forms.ToolStrip>합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-104">A <xref:System.Windows.Forms.ToolStripProgressBar> is most usually hosted by <xref:System.Windows.Forms.StatusStrip>, and less frequently by a <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
 <span data-ttu-id="32243-105">하지만 <xref:System.Windows.Forms.ToolStripProgressBar> 대체 하 고 이전 버전에서는 컨트롤에 기능 추가 <xref:System.Windows.Forms.ToolStripProgressBar> 원하는 경우 이전 버전과 호환성 및 향후 사용을 위해 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32243-105">Although <xref:System.Windows.Forms.ToolStripProgressBar> replaces and adds functionality to the control in previous versions, <xref:System.Windows.Forms.ToolStripProgressBar> is retained for both backward compatibility and future use if desired.</span></span>  
  
### <a name="important-toolstripprogressbar-members"></a><span data-ttu-id="32243-106">중요 한 ToolStripProgressBar 멤버</span><span class="sxs-lookup"><span data-stu-id="32243-106">Important ToolStripProgressBar Members</span></span>  
  
|<span data-ttu-id="32243-107">이름</span><span class="sxs-lookup"><span data-stu-id="32243-107">Name</span></span>|<span data-ttu-id="32243-108">설명</span><span class="sxs-lookup"><span data-stu-id="32243-108">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripProgressBar.MarqueeAnimationSpeed%2A>|<span data-ttu-id="32243-109">각 <xref:System.Windows.Forms.ProgressBarStyle.Marquee> 표시 업데이트 사이의 지연 시간(밀리초)을 나타내는 값을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-109">Gets or sets a value representing the delay between each <xref:System.Windows.Forms.ProgressBarStyle.Marquee> display update, in milliseconds.</span></span>|  
|<xref:System.Windows.Forms.ProgressBar.Maximum%2A>|<span data-ttu-id="32243-110">이 <xref:System.Windows.Forms.ToolStripProgressBar>에 대해 정의된 범위의 상한을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-110">Gets or sets the upper bound of the range that is defined for this <xref:System.Windows.Forms.ToolStripProgressBar>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.Minimum%2A>|<span data-ttu-id="32243-111">이 <xref:System.Windows.Forms.ToolStripProgressBar>에 대해 정의된 범위의 하한을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-111">Gets or sets the lower bound of the range that is defined for this <xref:System.Windows.Forms.ToolStripProgressBar>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.Style%2A>|<span data-ttu-id="32243-112">스타일을 가져오거나는 <xref:System.Windows.Forms.ToolStripProgressBar> 사용 하 여 작업의 진행률을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-112">Gets or sets the style that the <xref:System.Windows.Forms.ToolStripProgressBar> uses to display the progress of an operation.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.Value%2A>|<span data-ttu-id="32243-113"><xref:System.Windows.Forms.ToolStripProgressBar>의 현재 값을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-113">Gets or sets the current value of the <xref:System.Windows.Forms.ToolStripProgressBar>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.PerformStep%2A>|<span data-ttu-id="32243-114">진행률 표시줄의 현재 위치를 <xref:System.Windows.Forms.ToolStripProgressBar.Step%2A> 속성의 크기만큼 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="32243-114">Advances the current position of the progress bar by the amount of the <xref:System.Windows.Forms.ToolStripProgressBar.Step%2A> property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="32243-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="32243-115">See also</span></span>
- <xref:System.Windows.Forms.ToolStripProgressBar>
