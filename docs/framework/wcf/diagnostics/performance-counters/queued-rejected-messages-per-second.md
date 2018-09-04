---
title: Queued Rejected Messages Per Second
ms.date: 03/30/2017
ms.assetid: 77ea9aa3-b9e2-4a1d-a65e-5ca115ba0567
ms.openlocfilehash: 096e2188b13d0fd5a9be35e5e6473107a58c5566
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43507282"
---
# <a name="queued-rejected-messages-per-second"></a><span data-ttu-id="3a681-102">Queued Rejected Messages Per Second</span><span class="sxs-lookup"><span data-stu-id="3a681-102">Queued Rejected Messages Per Second</span></span>
<span data-ttu-id="3a681-103">카운터 이름: Queued Messages Rejected Per Second</span><span class="sxs-lookup"><span data-stu-id="3a681-103">Counter Name: Queued Messages Rejected Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="3a681-104">설명</span><span class="sxs-lookup"><span data-stu-id="3a681-104">Description</span></span>  
 <span data-ttu-id="3a681-105">초당 이 서비스에 대기 중인 전송에 의해 거부된 메시지의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3a681-105">Number of messages that are rejected by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="3a681-106">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a681-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="3a681-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="3a681-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
