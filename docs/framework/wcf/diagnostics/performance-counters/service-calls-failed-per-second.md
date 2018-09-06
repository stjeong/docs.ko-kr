---
title: '서비스: Calls Failed Per Second'
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: 9cd649788e1304c68caa1bbf4b5fd27e6fc9d508
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861818"
---
# <a name="service-calls-failed-per-second"></a><span data-ttu-id="0e814-102">서비스: Calls Failed Per Second</span><span class="sxs-lookup"><span data-stu-id="0e814-102">Service: Calls Failed Per Second</span></span>
<span data-ttu-id="0e814-103">카운터 이름: Calls Failed Per Second</span><span class="sxs-lookup"><span data-stu-id="0e814-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="0e814-104">설명</span><span class="sxs-lookup"><span data-stu-id="0e814-104">Description</span></span>  
 <span data-ttu-id="0e814-105">초당 이 서비스에서 받은, 처리되지 않은 예외가 있는 호출 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0e814-105">Number of calls that have unhandled exceptions, and are received by this service in a second.</span></span>  
  
 <span data-ttu-id="0e814-106">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e814-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="0e814-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="0e814-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="0e814-108">관리 코드에서 오류 조건이 발생하면 예외가 throw됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e814-108">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="0e814-109">관리 코드에서 오류 조건이 발생하면 예외가 throw됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e814-109">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="0e814-110">이 서비스에 처리되지 않은 예외가 있을 때마다 이 카운터가 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e814-110">This counter is incremented every time there is an unhandled exception in this service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e814-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0e814-111">See Also</span></span>  
 [<span data-ttu-id="0e814-112">계약 및 서비스에서 오류 지정 및 처리</span><span class="sxs-lookup"><span data-stu-id="0e814-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
