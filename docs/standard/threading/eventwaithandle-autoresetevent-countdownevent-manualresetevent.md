---
title: EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent
ms.date: 09/14/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- wait handles
- threading [.NET Framework], EventWaitHandle class
- event wait handles [.NET Framework]
ms.assetid: cd94fc34-ac15-427f-b723-a1240a4fab7d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: be9c858d7c76fdcc1b3e02485eb0b459f4e7555c
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583154"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a><span data-ttu-id="e7c5d-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="e7c5d-102">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>

<span data-ttu-id="e7c5d-103">이벤트 대기 핸들을 통해 스레드가 서로 신호를 보내고 상대방의 신호를 대기하여 작업을 동기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-103">Event wait handles allow threads to synchronize activities by signaling each other and by waiting on each other's signals.</span></span> <span data-ttu-id="e7c5d-104">이러한 동기화 이벤트는 운영 체제 대기 핸들을 기반으로 하며, 신호를 보낼 때 자동으로 다시 설정되는 이벤트 및 수동으로 다시 설정되는 이벤트라는 두 가지 유형으로 나눌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-104">These synchronization events are based on operating system wait handles and can be divided into two types: those that reset automatically when signaled and those that are reset manually.</span></span>  
  
<span data-ttu-id="e7c5d-105">이벤트 대기 핸들은 <xref:System.Threading.Monitor> 클래스와 동일한 여러 동기화 시나리오에서 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-105">Event wait handles are useful in many of the same synchronization scenarios as the <xref:System.Threading.Monitor> class.</span></span> <span data-ttu-id="e7c5d-106">이벤트 대기 핸들은 대개 <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> 및 <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> 메서드보다 사용하기가 더 쉬우며 신호 보내기에 대해 더 많은 제어를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-106">Event wait handles are often easier to use than the <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> and <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType> methods, and they offer more control over signaling.</span></span> <span data-ttu-id="e7c5d-107">명명된 이벤트 대기 핸들은 응용 프로그램 도메인 및 프로세스에 작업을 동기화하는 데 사용할 수 있습니다. 이 때 모니터는 응용 프로그램 도메인에 대해 로컬입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-107">Named event wait handles can also be used to synchronize activities across application domains and processes, whereas monitors are local to an application domain.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e7c5d-108">단원 내용</span><span class="sxs-lookup"><span data-stu-id="e7c5d-108">In this section</span></span>

 [<span data-ttu-id="e7c5d-109">EventWaitHandle</span><span class="sxs-lookup"><span data-stu-id="e7c5d-109">EventWaitHandle</span></span>](eventwaithandle.md)  
 <span data-ttu-id="e7c5d-110"><xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> 클래스는 자동 또는 수동 재설정 이벤트를 나타내거나 로컬 이벤트 또는 명명된 시스템 이벤트를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-110">The <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> class can represent either automatic or manual reset events and either local events or named system events.</span></span>  
  
 [<span data-ttu-id="e7c5d-111">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="e7c5d-111">AutoResetEvent</span></span>](autoresetevent.md)  
 <span data-ttu-id="e7c5d-112"><xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> 클래스는 <xref:System.Threading.EventWaitHandle>에서 파생되며 자동으로 다시 설정되는 로컬 이벤트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-112">The <xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that resets automatically.</span></span>  
  
 [<span data-ttu-id="e7c5d-113">ManualResetEvent 및 ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="e7c5d-113">ManualResetEvent and ManualResetEventSlim</span></span>](manualresetevent-and-manualreseteventslim.md)  
 <span data-ttu-id="e7c5d-114"><xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> 클래스는 <xref:System.Threading.EventWaitHandle>에서 파생되며 수동으로 다시 설정해야 하는 로컬 이벤트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-114">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class derives from <xref:System.Threading.EventWaitHandle> and represents a local event that must be reset manually.</span></span> <span data-ttu-id="e7c5d-115"><xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> 클래스는 동일한 프로세스 내의 이벤트에 사용할 수 있는 간단하고 빠른 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-115">The <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class is a lightweight, faster version that can be used for events within the same process.</span></span>  
  
 [<span data-ttu-id="e7c5d-116">CountdownEvent</span><span class="sxs-lookup"><span data-stu-id="e7c5d-116">CountdownEvent</span></span>](countdownevent.md)  
 <span data-ttu-id="e7c5d-117"><xref:System.Threading.CountdownEvent?displayProperty=nameWithType> 클래스는 대기 핸들을 사용하는 코드에서 포크/조인 병렬 처리 패턴을 구현하는 간단한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-117">The <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> class provides a simplified way to implement fork/join parallelism patterns in code that uses wait handles.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e7c5d-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e7c5d-118">See also</span></span>

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.Threading.Barrier?displayProperty=nameWithType>
- [<span data-ttu-id="e7c5d-119">스레딩 개체 및 기능</span><span class="sxs-lookup"><span data-stu-id="e7c5d-119">Threading objects and features</span></span>](threading-objects-and-features.md)
- [<span data-ttu-id="e7c5d-120">관리되는 스레딩 기본 사항</span><span class="sxs-lookup"><span data-stu-id="e7c5d-120">Managed threading basics</span></span>](managed-threading-basics.md)
