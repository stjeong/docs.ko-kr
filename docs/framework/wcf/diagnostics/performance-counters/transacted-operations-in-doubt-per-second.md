---
title: Transacted Operations In Doubt Per Second
ms.date: 03/30/2017
ms.assetid: 7e6b0716-c107-42e5-a21d-31d988e7a691
ms.openlocfilehash: f7365c4e5f03711129916c8c6964f7e25e9b553e
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46005693"
---
# <a name="transacted-operations-in-doubt-per-second"></a><span data-ttu-id="314a6-102">Transacted Operations In Doubt Per Second</span><span class="sxs-lookup"><span data-stu-id="314a6-102">Transacted Operations In Doubt Per Second</span></span>
<span data-ttu-id="314a6-103">카운터 이름: Transacted Operations In Doubt Per Second</span><span class="sxs-lookup"><span data-stu-id="314a6-103">Counter Name: Transacted Operations In Doubt Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="314a6-104">설명</span><span class="sxs-lookup"><span data-stu-id="314a6-104">Description</span></span>  
 <span data-ttu-id="314a6-105">초당 이 서비스에서 확실하지 않은 결과가 있는 트랜잭션 작업의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="314a6-105">Number of transactional operations with an in-doubt outcome in this service in a second.</span></span>  
  
 <span data-ttu-id="314a6-106">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="314a6-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="314a6-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="314a6-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
