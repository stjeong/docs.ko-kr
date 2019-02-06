---
title: 스레딩 개체 및 기능
ms.date: 10/01/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 745cd1e17e2c06a513c6fdafe8f6b5f464b95d5f
ms.sourcegitcommit: dcc8feeff4718664087747529638ec9b47e65234
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55479661"
---
# <a name="threading-objects-and-features"></a><span data-ttu-id="b5ce9-102">스레딩 개체 및 기능</span><span class="sxs-lookup"><span data-stu-id="b5ce9-102">Threading objects and features</span></span>

<span data-ttu-id="b5ce9-103"><xref:System.Threading.Thread?displayProperty=nameWithType> 클래스와 함께 .NET 다중 스레드 애플리케이션을 개발하는 데 도움이 되는 여러 클래스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-103">Along with the <xref:System.Threading.Thread?displayProperty=nameWithType> class, .NET provides a number of classes that help you develop multithreaded applications.</span></span> <span data-ttu-id="b5ce9-104">다음 문서에서는 해당 클래스의 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-104">The following articles provide overview of those classes:</span></span>

|<span data-ttu-id="b5ce9-105">제목</span><span class="sxs-lookup"><span data-stu-id="b5ce9-105">Title</span></span>|<span data-ttu-id="b5ce9-106">설명</span><span class="sxs-lookup"><span data-stu-id="b5ce9-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="b5ce9-107">관리되는 스레드 풀</span><span class="sxs-lookup"><span data-stu-id="b5ce9-107">The managed thread pool</span></span>](the-managed-thread-pool.md)|<span data-ttu-id="b5ce9-108">.NET에서 관리하는 작업자 스레드 풀을 제공하는 <xref:System.Threading.ThreadPool?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-108">Describes the <xref:System.Threading.ThreadPool?displayProperty=nameWithType> class, which provides a pool of worker threads that are managed by .NET.</span></span>|  
|[<span data-ttu-id="b5ce9-109">타이머</span><span class="sxs-lookup"><span data-stu-id="b5ce9-109">Timers</span></span>](timers.md)|<span data-ttu-id="b5ce9-110">다중 스레드 환경에서 사용할 수 있는 .NET 타이머에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-110">Describes .NET timers that can be used in a multithreaded environment.</span></span>|
|[<span data-ttu-id="b5ce9-111">동기화 기본 형식 개요</span><span class="sxs-lookup"><span data-stu-id="b5ce9-111">Overview of synchronization primitives</span></span>](overview-of-synchronization-primitives.md)|<span data-ttu-id="b5ce9-112">공유 리소스에 대한 액세스를 동기화하거나 스레드 상호 작용을 제어하는 데 사용할 수 있는 형식을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-112">Describes types that can be used to synchronize access to a shared resource or control thread interaction.</span></span>|
|[<span data-ttu-id="b5ce9-113">EventWaitHandle, CountdownEvent</span><span class="sxs-lookup"><span data-stu-id="b5ce9-113">EventWaitHandle, CountdownEvent</span></span>](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|<span data-ttu-id="b5ce9-114">신호 전송 및 신호 대기를 통해 스레드 작업을 동기화하는 데 사용되는 관리되는 이벤트 대기 핸들을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-114">Describes managed event wait handles, which are used to synchronize thread activities by signaling and waiting for signals.</span></span>|
|[<span data-ttu-id="b5ce9-115">뮤텍스</span><span class="sxs-lookup"><span data-stu-id="b5ce9-115">Mutexes</span></span>](mutexes.md)|<span data-ttu-id="b5ce9-116">공유 리소스에 대한 배타적 액세스 권한을 부여하는 <xref:System.Threading.Mutex?displayProperty=nameWithType>에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-116">Describes <xref:System.Threading.Mutex?displayProperty=nameWithType>, which grants exclusive access to a shared resource.</span></span>|
|[<span data-ttu-id="b5ce9-117">세마포 및 SemaphoreSlim</span><span class="sxs-lookup"><span data-stu-id="b5ce9-117">Semaphore and SemaphoreSlim</span></span>](semaphore-and-semaphoreslim.md)|<span data-ttu-id="b5ce9-118">공유 리소스 또는 리소스 풀에 동시에 액세스할 수 있는 스레드 수를 제한하는 <xref:System.Threading.Semaphore?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-118">Describes the <xref:System.Threading.Semaphore?displayProperty=nameWithType> class, which limits number of threads that can access a shared resource or a pool of resources concurrently.</span></span>|
|[<span data-ttu-id="b5ce9-119">장벽</span><span class="sxs-lookup"><span data-stu-id="b5ce9-119">Barrier</span></span>](barrier.md)|<span data-ttu-id="b5ce9-120">단계별 작업에서 스레드를 조정하기 위해 장벽 패턴을 구현하는 <xref:System.Threading.Barrier?displayProperty=nameWithType> 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-120">Describes the <xref:System.Threading.Barrier?displayProperty=nameWithType> class that implements the barrier pattern for coordination of threads in phased operations.</span></span>|
|[<span data-ttu-id="b5ce9-121">스핀 잠금</span><span class="sxs-lookup"><span data-stu-id="b5ce9-121">SpinLock</span></span>](spinlock.md)|<span data-ttu-id="b5ce9-122">특정 하위 수준 잠금 시나리오의 <xref:System.Threading.Monitor?displayProperty=nameWithType> 클래스에 대한 간단한 대체 항목인 <xref:System.Threading.SpinLock?displayProperty=nameWithType> 구조체를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-122">Describes the <xref:System.Threading.SpinLock?displayProperty=nameWithType> structure, which is a lightweight alternative to the <xref:System.Threading.Monitor?displayProperty=nameWithType> class for certain low-level locking scenarios.</span></span>|
|[<span data-ttu-id="b5ce9-123">스핀 대기</span><span class="sxs-lookup"><span data-stu-id="b5ce9-123">SpinWait</span></span>](spinwait.md)|<span data-ttu-id="b5ce9-124">회전 기반 대기를 지원하는 <xref:System.Threading.SpinWait?displayProperty=nameWithType> 구조체를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ce9-124">Describes the <xref:System.Threading.SpinWait?displayProperty=nameWithType> structure, which provides support for spin-based waiting.</span></span>|

## <a name="see-also"></a><span data-ttu-id="b5ce9-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b5ce9-125">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [<span data-ttu-id="b5ce9-126">스레드 및 스레딩 사용</span><span class="sxs-lookup"><span data-stu-id="b5ce9-126">Using threads and threading</span></span>](using-threads-and-threading.md)
- [<span data-ttu-id="b5ce9-127">Asynchronous File I/O</span><span class="sxs-lookup"><span data-stu-id="b5ce9-127">Asynchronous File I/O</span></span>](../io/asynchronous-file-i-o.md)
- [<span data-ttu-id="b5ce9-128">병렬 프로그래밍</span><span class="sxs-lookup"><span data-stu-id="b5ce9-128">Parallel Programming</span></span>](../parallel-programming/index.md)
- [<span data-ttu-id="b5ce9-129">TPL(작업 병렬 라이브러리)</span><span class="sxs-lookup"><span data-stu-id="b5ce9-129">Task Parallel Library (TPL)</span></span>](../parallel-programming/task-parallel-library-tpl.md)
