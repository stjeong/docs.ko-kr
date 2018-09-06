---
title: Call Duration
ms.date: 03/30/2017
ms.assetid: e4973ec3-3c66-4c0b-b5d0-294b62c83f7d
ms.openlocfilehash: 1e1ee72f3dd8209cf8afa179d5590072466c5a63
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43768350"
---
# <a name="calls-duration"></a><span data-ttu-id="2c8b9-102">Call Duration</span><span class="sxs-lookup"><span data-stu-id="2c8b9-102">Calls Duration</span></span>
<span data-ttu-id="2c8b9-103">카운터 이름: 통화 기간</span><span class="sxs-lookup"><span data-stu-id="2c8b9-103">Counter Name: Calls Duration</span></span>  
  
## <a name="description"></a><span data-ttu-id="2c8b9-104">설명</span><span class="sxs-lookup"><span data-stu-id="2c8b9-104">Description</span></span>  
 <span data-ttu-id="2c8b9-105">이 작업에 대한 평균 호출 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-105">The average duration of calls to this operation.</span></span> <span data-ttu-id="2c8b9-106">평균 기간은 (N1-N0)/(D1-D0) 공식을 사용해 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-106">The average duration is calculated based on this equation: (N1-N0)/(D1-D0).</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="2c8b9-107">호출 기간 카운터는 항상 비동기 WCF 서비스를 사용 하는 경우-1을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-107">When used on an asynchronous WCF service the Calls Duration counter will always return -1.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c8b9-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2c8b9-108">See Also</span></span>  
 [<span data-ttu-id="2c8b9-109">PERF_AVERAGE_TIMER</span><span class="sxs-lookup"><span data-stu-id="2c8b9-109">PERF_AVERAGE_TIMER</span></span>](https://go.microsoft.com/fwlink/?LinkId=95015)
