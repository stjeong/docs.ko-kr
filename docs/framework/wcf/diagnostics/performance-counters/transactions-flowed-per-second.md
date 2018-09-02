---
title: Transactions Flowed Per Second
ms.date: 03/30/2017
ms.assetid: b9f661e1-576c-48fc-9fdf-91853e0749e8
ms.openlocfilehash: e77aef4cfff1e64f112e720183675dfb7aa25d27
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43392938"
---
# <a name="transactions-flowed-per-second"></a><span data-ttu-id="6b508-102">Transactions Flowed Per Second</span><span class="sxs-lookup"><span data-stu-id="6b508-102">Transactions Flowed Per Second</span></span>
<span data-ttu-id="6b508-103">카운터 이름: Transactions Flowed Per Second</span><span class="sxs-lookup"><span data-stu-id="6b508-103">Counter Name:  Transactions Flowed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="6b508-104">설명</span><span class="sxs-lookup"><span data-stu-id="6b508-104">Description</span></span>  
 <span data-ttu-id="6b508-105">이 작업에 적용된 초당 트랜잭션의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6b508-105">Number of transactions flowed to this operation in a second.</span></span> <span data-ttu-id="6b508-106">작업에 전송된 메시지에 트랜잭션 ID가 있을 때마다 이 카운터가 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="6b508-106">This counter is incremented any time a transaction ID is present in a message that is sent to the operation.</span></span>  
  
 <span data-ttu-id="6b508-107">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b508-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="6b508-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="6b508-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
