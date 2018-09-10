---
title: ManualResetEvent 및 ManualResetEventSlim
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], ManualResetEvent class
- ManualResetEvent class, about ManualResetEvent class
ms.assetid: 465fdcf9-ba24-4d8d-a43f-d983b7cb0cc6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 69cd82ae2bd72db6a481188b3d7bf743e429f39c
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43864270"
---
# <a name="manualresetevent-and-manualreseteventslim"></a><span data-ttu-id="1f670-102">ManualResetEvent 및 ManualResetEventSlim</span><span class="sxs-lookup"><span data-stu-id="1f670-102">ManualResetEvent and ManualResetEventSlim</span></span>
<span data-ttu-id="1f670-103"><xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> 클래스는 신호를 받은 후 수동으로 다시 설정해야 하는 로컬 대기 핸들 이벤트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-103">The <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> class represents a local wait handle event that must be reset manually after it is signaled.</span></span> <span data-ttu-id="1f670-104">이 클래스는 기본 클래스인 <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>의 특수한 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-104">This class represents a special case of its base class, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>.</span></span> <span data-ttu-id="1f670-105">수동 재설정 이벤트의 사용 및 기능은 [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) 개념 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f670-105">See the [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) conceptual documentation for the use and features of manual reset events.</span></span>  
  
 <span data-ttu-id="1f670-106"><xref:System.Threading.ManualResetEvent> 개체는 <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> 메서드가 호출될 때까지 신호를 받은 것으로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-106">A <xref:System.Threading.ManualResetEvent> object remains signaled until its <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> method is called.</span></span> <span data-ttu-id="1f670-107">대기 스레드 또는 신호를 받은 후 이벤트를 기다리는 스레드 수는 제한 없이 개체의 상태가 신호를 받는 동안 해제될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-107">Any number of waiting threads, or threads that wait on the event after it has been signaled, can be released while the object's state is signaled.</span></span> <span data-ttu-id="1f670-108"><xref:System.Threading.ManualResetEvent>는 `bManualReset` 인수에 대해 `true`를 지정하는 Win32 `CreateEvent` 호출에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-108"><xref:System.Threading.ManualResetEvent> corresponds to a Win32 `CreateEvent` call, specifying `true` for the `bManualReset` argument.</span></span>  
  
 <span data-ttu-id="1f670-109">[!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)]에서는 대기 시간이 매우 짧을 것으로 예상되고 이벤트가 프로세스 경계를 넘어서지 않는 경우 <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> 클래스를 사용하여 성능을 향상시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-109">In the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], you can use the <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> class for better performance when wait times are expected to be very short, and when the event does not cross a process boundary.</span></span> <span data-ttu-id="1f670-110"><xref:System.Threading.ManualResetEventSlim>에서는 이벤트에 신호가 전달되기를 기다리는 짧은 시간 동안 고속 회전을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-110"><xref:System.Threading.ManualResetEventSlim> uses busy spinning for a short time while it waits for the event to become signaled.</span></span> <span data-ttu-id="1f670-111">대기 시간이 짧은 경우 대기 핸들을 사용하여 기다리는 것보다 회전하는 것이 비용이 적게 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-111">When wait times are short, spinning can be much less expensive than waiting by using wait handles.</span></span> <span data-ttu-id="1f670-112">그러나 이벤트가 특정 기간 내에 신호를 받지 않는 경우 일반적인 이벤트 핸들 대기에 <xref:System.Threading.ManualResetEventSlim>을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1f670-112">However, if the event does not become signaled within a certain period of time, <xref:System.Threading.ManualResetEventSlim> resorts to a regular event handle wait.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f670-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1f670-113">See also</span></span>

- [<span data-ttu-id="1f670-114">스레딩</span><span class="sxs-lookup"><span data-stu-id="1f670-114">Threading</span></span>](../../../docs/standard/threading/index.md)  
- [<span data-ttu-id="1f670-115">스레딩 개체 및 기능</span><span class="sxs-lookup"><span data-stu-id="1f670-115">Threading Objects and Features</span></span>](../../../docs/standard/threading/threading-objects-and-features.md)  
- [<span data-ttu-id="1f670-116">대기 핸들</span><span class="sxs-lookup"><span data-stu-id="1f670-116">Wait Handles</span></span>](https://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)  
- [<span data-ttu-id="1f670-117">AutoResetEvent</span><span class="sxs-lookup"><span data-stu-id="1f670-117">AutoResetEvent</span></span>](../../../docs/standard/threading/autoresetevent.md)  
- [<span data-ttu-id="1f670-118">스핀 대기</span><span class="sxs-lookup"><span data-stu-id="1f670-118">SpinWait</span></span>](../../../docs/standard/threading/spinwait.md)  
- [<span data-ttu-id="1f670-119">세마포 및 SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="1f670-119">Semaphore and SemaphoreSlim</span></span>](../../../docs/standard/threading/semaphore-and-semaphoreslim.md)
