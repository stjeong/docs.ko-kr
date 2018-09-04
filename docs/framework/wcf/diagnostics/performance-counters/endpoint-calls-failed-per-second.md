---
title: '엔드포인트: Calls Failed Per Second'
ms.date: 03/30/2017
ms.assetid: bcbe9da4-c8dd-4e27-b630-11611adc7580
ms.openlocfilehash: fa4fc1d8a875557f1da9e54e7a05eb012e7c221c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43531799"
---
# <a name="endpoint-calls-failed-per-second"></a><span data-ttu-id="78fb8-102">엔드포인트: Calls Failed Per Second</span><span class="sxs-lookup"><span data-stu-id="78fb8-102">Endpoint: Calls Failed Per Second</span></span>
<span data-ttu-id="78fb8-103">카운터 이름: Calls Failed Per Second</span><span class="sxs-lookup"><span data-stu-id="78fb8-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="78fb8-104">설명</span><span class="sxs-lookup"><span data-stu-id="78fb8-104">Description</span></span>  
 <span data-ttu-id="78fb8-105">처리되지 않은 예외가 있고 초당 이 엔드포인트에서 받은 호출 수입니다.</span><span class="sxs-lookup"><span data-stu-id="78fb8-105">Number of calls that have unhandled exceptions and are received by this endpoint in a second.</span></span>  
  
 <span data-ttu-id="78fb8-106">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fb8-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="78fb8-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="78fb8-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="78fb8-108">이 카운터는 이 엔드포인트에서 처리되지 않은 예외가 발생할 때마다 증가됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fb8-108">This counter is incremented every time there is an unhandled exception at this endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="78fb8-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="78fb8-109">See Also</span></span>  
 [<span data-ttu-id="78fb8-110">계약 및 서비스에서 오류 지정 및 처리</span><span class="sxs-lookup"><span data-stu-id="78fb8-110">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
