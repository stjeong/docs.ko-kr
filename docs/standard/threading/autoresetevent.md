---
title: AutoResetEvent
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], AutoResetEvent class
- AutoResetEvent class
ms.assetid: 6d39c48d-6b37-4a9b-8631-f2924cfd9c18
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 519776b5c1c237deb520476384495b8dd96a4e39
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50201308"
---
# <a name="autoresetevent"></a><span data-ttu-id="e1b7e-102">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="e1b7e-102">AutoResetEvent</span></span>
<span data-ttu-id="e1b7e-103"><xref:System.Threading.AutoResetEvent> 클래스는 단일 대기 스레드를 해제한 후 신호를 받을 때 자동으로 다시 설정되는 로컬 대기 핸들 이벤트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7e-103">The <xref:System.Threading.AutoResetEvent> class represents a local wait handle event that resets automatically when signaled, after releasing a single waiting thread.</span></span> <span data-ttu-id="e1b7e-104">이 클래스는 기본 클래스인 <xref:System.Threading.EventWaitHandle>의 특수한 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7e-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle>.</span></span> <span data-ttu-id="e1b7e-105">자동 재설정 이벤트의 사용 및 기능은 [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) 개념 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1b7e-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of automatic reset events.</span></span>  
  
 <span data-ttu-id="e1b7e-106">단일 대기 스레드가 해제된 후 <xref:System.Threading.AutoResetEvent> 개체가 시스템의 신호를 받지 않음으로 자동으로 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7e-106">An <xref:System.Threading.AutoResetEvent> object is automatically reset to non-signaled by the system after a single waiting thread has been released.</span></span> <span data-ttu-id="e1b7e-107">대기 스레드가 없으면 이벤트 개체의 상태는 신호를 받은 것으로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7e-107">If no threads are waiting, the event object's state remains signaled.</span></span>
  
 <span data-ttu-id="e1b7e-108"><xref:System.Threading.AutoResetEvent>를 사용하는 예제는 <xref:System.Threading.Monitor>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1b7e-108">For an example that uses <xref:System.Threading.AutoResetEvent>, see <xref:System.Threading.Monitor>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1b7e-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e1b7e-109">See also</span></span>

- <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- [<span data-ttu-id="e1b7e-110">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="e1b7e-110">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
- [<span data-ttu-id="e1b7e-111">스레딩 개체 및 기능</span><span class="sxs-lookup"><span data-stu-id="e1b7e-111">Threading objects and features</span></span>](threading-objects-and-features.md)  
- [<span data-ttu-id="e1b7e-112">스레딩</span><span class="sxs-lookup"><span data-stu-id="e1b7e-112">Threading</span></span>](index.md)  
