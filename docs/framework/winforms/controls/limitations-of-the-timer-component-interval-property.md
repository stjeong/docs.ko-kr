---
title: Windows Forms Timer 구성 요소의 제한 사항 Interval 속성
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: 86cfcce65998d19aea8592ae33c5baf58e1ff0fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54516956"
---
# <a name="limitations-of-the-windows-forms-timer-component39s-interval-property"></a><span data-ttu-id="ad513-102">Windows Forms Timer 구성 요소의 제한 사항 Interval 속성</span><span class="sxs-lookup"><span data-stu-id="ad513-102">Limitations of the Windows Forms Timer Component&#39;s Interval Property</span></span>
<span data-ttu-id="ad513-103">Windows Forms <xref:System.Windows.Forms.Timer> 구성 요소에는 <xref:System.Windows.Forms.Timer.Interval%2A> 타이머 이벤트 및 다음 간에 전달 하는 시간을 밀리초 단위로 지정 하는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-103">The Windows Forms <xref:System.Windows.Forms.Timer> component has an <xref:System.Windows.Forms.Timer.Interval%2A> property that specifies the number of milliseconds that pass between one timer event and the next.</span></span> <span data-ttu-id="ad513-104">구성 요소를 사용 하지 않도록 설정 하지 않으면 타이머를 계속 수신 하는 <xref:System.Windows.Forms.Timer.Tick> 거의 같은 시간 간격으로 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-104">Unless the component is disabled, a timer continues to receive the <xref:System.Windows.Forms.Timer.Tick> event at roughly equal intervals of time.</span></span>  
  
 <span data-ttu-id="ad513-105">이 구성 요소는 Windows Forms 환경에 맞게 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-105">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="ad513-106">서버 환경에 적합한 타이머가 필요한 경우 [서버 기반 타이머 소개](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ad513-106">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span></span>  
  
## <a name="the-interval-property"></a><span data-ttu-id="ad513-107">간격 속성</span><span class="sxs-lookup"><span data-stu-id="ad513-107">The Interval Property</span></span>  
 <span data-ttu-id="ad513-108">합니다 <xref:System.Windows.Forms.Timer.Interval%2A> 속성이 프로그래밍할 때 고려해 야 할 몇 가지 제한이 <xref:System.Windows.Forms.Timer> 구성 요소:</span><span class="sxs-lookup"><span data-stu-id="ad513-108">The <xref:System.Windows.Forms.Timer.Interval%2A> property has a few limitations to consider when you are programming a <xref:System.Windows.Forms.Timer> component:</span></span>  
  
-   <span data-ttu-id="ad513-109">응용 프로그램 또는 다른 응용 프로그램은 시스템에 큰 부담을 주므로 할 경우-긴 루프, 과도 한 계산 또는 드라이브, 네트워크 또는 포트 액세스 같은-응용 프로그램으로 타이머 이벤트를 자주를 얻지 못할 수는 <xref:System.Windows.Forms.Timer.Interval%2A> 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-109">If your application or another application is making heavy demands on the system — such as long loops, intensive calculations, or drive, network, or port access — your application may not get timer events as often as the <xref:System.Windows.Forms.Timer.Interval%2A> property specifies.</span></span>  
  
-   <span data-ttu-id="ad513-110">간격이 경과 시간에 정확 하 게 보장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-110">The interval is not guaranteed to elapse exactly on time.</span></span> <span data-ttu-id="ad513-111">정확성을 위해 타이머 필요에 따라 시스템 시간을 확인 대신 해야 계속 누적된 시간을 내부적으로 추적 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-111">To ensure accuracy, the timer should check the system clock as needed, rather than try to keep track of accumulated time internally.</span></span>  
  
-   <span data-ttu-id="ad513-112">전체 자릿수는 <xref:System.Windows.Forms.Timer.Interval%2A> 속성이 밀리초에서입니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-112">The precision of the <xref:System.Windows.Forms.Timer.Interval%2A> property is in milliseconds.</span></span> <span data-ttu-id="ad513-113">일부 컴퓨터에는 시간 (밀리초) 보다 더 높은 해상도 고해상도 카운터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-113">Some computers provide a high-resolution counter that has a resolution higher than milliseconds.</span></span> <span data-ttu-id="ad513-114">이러한 카운터 컴퓨터의 프로세서 하드웨어에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="ad513-114">The availability of such a counter depends on the processor hardware of your computer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad513-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="ad513-115">See also</span></span>
- <xref:System.Windows.Forms.Timer>
- [<span data-ttu-id="ad513-116">Timer 구성 요소</span><span class="sxs-lookup"><span data-stu-id="ad513-116">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)
- [<span data-ttu-id="ad513-117">Timer 구성 요소 개요</span><span class="sxs-lookup"><span data-stu-id="ad513-117">Timer Component Overview</span></span>](../../../../docs/framework/winforms/controls/timer-component-overview-windows-forms.md)
