---
title: 스레딩 개체 및 기능
ms.date: 08/16/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d56d962279120a03a6e4b89154ac1429ea5479e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44039331"
---
# <a name="threading-objects-and-features"></a><span data-ttu-id="94f9c-102">스레딩 개체 및 기능</span><span class="sxs-lookup"><span data-stu-id="94f9c-102">Threading objects and features</span></span>

<span data-ttu-id="94f9c-103"><xref:System.Threading.Thread?displayProperty=nameWithType> 클래스와 함께 .NET 다중 스레드 응용 프로그램을 개발하는 데 도움이 되는 여러 클래스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-103">Along with the <xref:System.Threading.Thread?displayProperty=nameWithType> class, .NET provides a number of classes that help you develop multithreaded applications.</span></span> <span data-ttu-id="94f9c-104">다음 문서에서는 해당 클래스의 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-104">The following articles provide overview of those classes:</span></span>

|<span data-ttu-id="94f9c-105">제목</span><span class="sxs-lookup"><span data-stu-id="94f9c-105">Title</span></span>|<span data-ttu-id="94f9c-106">설명</span><span class="sxs-lookup"><span data-stu-id="94f9c-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="94f9c-107">관리되는 스레드 풀</span><span class="sxs-lookup"><span data-stu-id="94f9c-107">The managed thread pool</span></span>](the-managed-thread-pool.md)|<span data-ttu-id="94f9c-108">.NET에서 관리하는 작업자 스레드 풀을 제공하는 <xref:System.Threading.ThreadPool?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-108">Describes the <xref:System.Threading.ThreadPool?displayProperty=nameWithType> class, which provides a pool of worker threads that are managed by .NET.</span></span>|  
|[<span data-ttu-id="94f9c-109">타이머</span><span class="sxs-lookup"><span data-stu-id="94f9c-109">Timers</span></span>](timers.md)|<span data-ttu-id="94f9c-110">다중 스레드 환경에서 사용할 수 있는 타이머에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-110">Describes timers that can be used in a multithreaded environment.</span></span>|
|[<span data-ttu-id="94f9c-111">동기화 기본 형식 개요</span><span class="sxs-lookup"><span data-stu-id="94f9c-111">Overview of synchronization primitives</span></span>](overview-of-synchronization-primitives.md)|<span data-ttu-id="94f9c-112">데이터에 대한 엑세스를 동기화하거나 스레드 상호 작용을 제어하는 데 사용할 수 있는 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-112">Describes classes that can be used to synchronize access to data or control thread interaction.</span></span>|
|[<span data-ttu-id="94f9c-113">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span><span class="sxs-lookup"><span data-stu-id="94f9c-113">EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|<span data-ttu-id="94f9c-114">신호 전송 및 신호 대기를 통해 스레드 작업을 동기화하는 데 사용되는 관리되는 이벤트 대기 핸들을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-114">Describes managed event wait handles, which are used to synchronize thread activities by signaling and waiting for signals.</span></span>|
|[<span data-ttu-id="94f9c-115">뮤텍스</span><span class="sxs-lookup"><span data-stu-id="94f9c-115">Mutexes</span></span>](mutexes.md)|<span data-ttu-id="94f9c-116"><xref:System.Threading.Mutex?displayProperty=nameWithType>를 사용하여 개체에 대한 액세스를 동기화하거나 고유한 동기화 메커니즘을 빌드하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-116">Describes how to use a <xref:System.Threading.Mutex?displayProperty=nameWithType> to synchronize access to an object or to build your own synchronization mechanisms.</span></span>|
|[<span data-ttu-id="94f9c-117">연동 작업</span><span class="sxs-lookup"><span data-stu-id="94f9c-117">Interlocked operations</span></span>](interlocked-operations.md)|<span data-ttu-id="94f9c-118">다중 스레드에서 공유하는 변수에 대한 원자 단위 연산을 제공하는 <xref:System.Threading.Interlocked?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-118">Describes the <xref:System.Threading.Interlocked?displayProperty=nameWithType> class, which provides atomic operations for variables that are shared by multiple threads.</span></span>|
|[<span data-ttu-id="94f9c-119">판독기 및 작성기 잠금</span><span class="sxs-lookup"><span data-stu-id="94f9c-119">Reader-Writer Locks</span></span>](reader-writer-locks.md)|<span data-ttu-id="94f9c-120">단일 작성기/다중 판독기 의미 체계를 제공하는 <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-120">Describes the <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> class, which provides single-writer/multiple-reader semantics.</span></span>|
|[<span data-ttu-id="94f9c-121">세마포 및 SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="94f9c-121">Semaphore and SemaphoreSlim</span></span>](semaphore-and-semaphoreslim.md)|<span data-ttu-id="94f9c-122"><xref:System.Threading.Semaphore?displayProperty=nameWithType> 클래스를 설명하고 제한된 리소스에 대한 액세스를 제어하는 데 사용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-122">Describes the <xref:System.Threading.Semaphore?displayProperty=nameWithType> class and explains how to use it to control access to limited resources.</span></span>|
|[<span data-ttu-id="94f9c-123">장벽</span><span class="sxs-lookup"><span data-stu-id="94f9c-123">Barrier</span></span>](barrier.md)|<span data-ttu-id="94f9c-124">단계별 작업에서 스레드를 조정하기 위해 장벽 패턴을 구현하는 <xref:System.Threading.Barrier?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-124">Describes the <xref:System.Threading.Barrier?displayProperty=nameWithType> class that implements the barrier pattern for coordination of threads in phased operations.</span></span>|
|[<span data-ttu-id="94f9c-125">스핀 잠금</span><span class="sxs-lookup"><span data-stu-id="94f9c-125">SpinLock</span></span>](spinlock.md)|<span data-ttu-id="94f9c-126">특정 하위 수준 시나리오의 <xref:System.Threading.Monitor?displayProperty=nameWithType> 클래스에 대한 경량 대체 항목인 <xref:System.Threading.SpinLock?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-126">Describes the <xref:System.Threading.SpinLock?displayProperty=nameWithType> class, which is a lightweight alternative to the <xref:System.Threading.Monitor?displayProperty=nameWithType> class for certain low-level scenarios.</span></span>|
|[<span data-ttu-id="94f9c-127">스핀 대기</span><span class="sxs-lookup"><span data-stu-id="94f9c-127">SpinWait</span></span>](spinwait.md)|<span data-ttu-id="94f9c-128">커널 기반 대기를 시작하기 전에 사용 중인 회전을 수행하는 낮은 수준의 동기화 기본 형식인 <xref:System.Threading.SpinWait?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="94f9c-128">Describes the <xref:System.Threading.SpinWait?displayProperty=nameWithType> class, which is a low-level synchronization primitive that performs busy spinning prior to initiating a kernel-based wait.</span></span>|

## <a name="see-also"></a><span data-ttu-id="94f9c-129">참고 항목</span><span class="sxs-lookup"><span data-stu-id="94f9c-129">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [<span data-ttu-id="94f9c-130">스레드 및 스레딩 사용</span><span class="sxs-lookup"><span data-stu-id="94f9c-130">Using threads and threading</span></span>](using-threads-and-threading.md)
- [<span data-ttu-id="94f9c-131">비동기 파일 I/O</span><span class="sxs-lookup"><span data-stu-id="94f9c-131">Asynchronous File I/O</span></span>](../io/asynchronous-file-i-o.md)
- [<span data-ttu-id="94f9c-132">병렬 프로그래밍</span><span class="sxs-lookup"><span data-stu-id="94f9c-132">Parallel Programming</span></span>](../parallel-programming/index.md)
- [<span data-ttu-id="94f9c-133">TPL(작업 병렬 라이브러리)</span><span class="sxs-lookup"><span data-stu-id="94f9c-133">Task Parallel Library (TPL)</span></span>](../parallel-programming/task-parallel-library-tpl.md)
