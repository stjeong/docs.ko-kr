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
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43483660"
---
# <a name="threading-objects-and-features"></a>스레딩 개체 및 기능

<xref:System.Threading.Thread?displayProperty=nameWithType> 클래스와 함께 .NET 다중 스레드 응용 프로그램을 개발하는 데 도움이 되는 여러 클래스를 제공합니다. 다음 문서에서는 해당 클래스의 개요를 제공합니다.

|제목|설명|  
|-----------|-----------------|  
|[관리되는 스레드 풀](the-managed-thread-pool.md)|.NET에서 관리하는 작업자 스레드 풀을 제공하는 <xref:System.Threading.ThreadPool?displayProperty=nameWithType> 클래스를 설명합니다.|  
|[타이머](timers.md)|다중 스레드 환경에서 사용할 수 있는 타이머에 대해 설명합니다.|
|[동기화 기본 형식 개요](overview-of-synchronization-primitives.md)|데이터에 대한 엑세스를 동기화하거나 스레드 상호 작용을 제어하는 데 사용할 수 있는 클래스를 설명합니다.|
|[EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|신호 전송 및 신호 대기를 통해 스레드 작업을 동기화하는 데 사용되는 관리되는 이벤트 대기 핸들을 설명합니다.|
|[뮤텍스](mutexes.md)|<xref:System.Threading.Mutex?displayProperty=nameWithType>를 사용하여 개체에 대한 액세스를 동기화하거나 고유한 동기화 메커니즘을 빌드하는 방법을 설명합니다.|
|[연동 작업](interlocked-operations.md)|다중 스레드에서 공유하는 변수에 대한 원자 단위 연산을 제공하는 <xref:System.Threading.Interlocked?displayProperty=nameWithType> 클래스를 설명합니다.|
|[판독기 및 작성기 잠금](reader-writer-locks.md)|단일 작성기/다중 판독기 의미 체계를 제공하는 <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> 클래스를 설명합니다.|
|[세마포 및 SemaphoreSlim](semaphore-and-semaphoreslim.md)|<xref:System.Threading.Semaphore?displayProperty=nameWithType> 클래스를 설명하고 제한된 리소스에 대한 액세스를 제어하는 데 사용하는 방법을 설명합니다.|
|[장벽](barrier.md)|단계별 작업에서 스레드를 조정하기 위해 장벽 패턴을 구현하는 <xref:System.Threading.Barrier?displayProperty=nameWithType> 클래스를 설명합니다.|
|[스핀 잠금](spinlock.md)|특정 하위 수준 시나리오의 <xref:System.Threading.Monitor?displayProperty=nameWithType> 클래스에 대한 경량 대체 항목인 <xref:System.Threading.SpinLock?displayProperty=nameWithType> 클래스를 설명합니다.|
|[스핀 대기](spinwait.md)|커널 기반 대기를 시작하기 전에 사용 중인 회전을 수행하는 낮은 수준의 동기화 기본 형식인 <xref:System.Threading.SpinWait?displayProperty=nameWithType> 클래스를 설명합니다.|

## <a name="see-also"></a>참고 항목

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [스레드 및 스레딩 사용](using-threads-and-threading.md)
- [비동기 파일 I/O](../io/asynchronous-file-i-o.md)
- [병렬 프로그래밍](../parallel-programming/index.md)
- [TPL(작업 병렬 라이브러리)](../parallel-programming/task-parallel-library-tpl.md)
