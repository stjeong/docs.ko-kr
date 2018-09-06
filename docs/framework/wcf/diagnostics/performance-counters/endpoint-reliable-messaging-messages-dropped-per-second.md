---
title: '엔드포인트: Reliable Messaging Messages Dropped Per Second'
ms.date: 03/30/2017
ms.assetid: ea3c4fc0-1e0f-4863-8879-57bc6c113018
ms.openlocfilehash: 8f935bee06d175ce454bd7f58a1afbbe9ab505ad
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43737583"
---
# <a name="endpoint-reliable-messaging-messages-dropped-per-second"></a><span data-ttu-id="bf9a4-102">엔드포인트: Reliable Messaging Messages Dropped Per Second</span><span class="sxs-lookup"><span data-stu-id="bf9a4-102">Endpoint: Reliable Messaging Messages Dropped Per Second</span></span>
<span data-ttu-id="bf9a4-103">카운터 이름: Reliable Messaging Sessions Dropped Per Second.</span><span class="sxs-lookup"><span data-stu-id="bf9a4-103">Counter Name: Reliable Messaging Sessions Dropped Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="bf9a4-104">설명</span><span class="sxs-lookup"><span data-stu-id="bf9a4-104">Description</span></span>  
 <span data-ttu-id="bf9a4-105">이 엔드포인트에서 삭제된 신뢰할 수 있는 메시징 메시지의 초당 총 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9a4-105">Total number of reliable messaging messages that have been dropped at this endpoint in a second.</span></span>  
  
 <span data-ttu-id="bf9a4-106">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf9a4-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="bf9a4-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="bf9a4-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
