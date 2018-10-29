---
title: Security Calls Not Authorized Per Second
ms.date: 03/30/2017
ms.assetid: 0f189767-8c05-478a-8f0b-9228e5d351e5
ms.openlocfilehash: 15890506aece94a07d4b97101519007accf3570a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196153"
---
# <a name="security-calls-not-authorized-per-second"></a><span data-ttu-id="8a66b-102">Security Calls Not Authorized Per Second</span><span class="sxs-lookup"><span data-stu-id="8a66b-102">Security Calls Not Authorized Per Second</span></span>
<span data-ttu-id="8a66b-103">카운터 이름: Security Calls Not Authorized Per Second</span><span class="sxs-lookup"><span data-stu-id="8a66b-103">Counter Name: Security Calls Not Authorized Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="8a66b-104">설명</span><span class="sxs-lookup"><span data-stu-id="8a66b-104">Description</span></span>  
 <span data-ttu-id="8a66b-105">이 작업에서 권한 부여에 실패한 초당 호출 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="8a66b-105">Number of calls that failed authorization in this operation in a second.</span></span>  
  
 <span data-ttu-id="8a66b-106">이 카운터는 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> 메서드가 `false`를 반환할 때 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="8a66b-106">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span> <span data-ttu-id="8a66b-107">들어오는 메시지가 올바른 사용자로부터 전송되고 적절하게 보호되지만 해당 사용자에게 특정 작업을 수행할 수 있는 권한이 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8a66b-107">It indicates that the incoming message is from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>  
  
 <span data-ttu-id="8a66b-108">이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a66b-108">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="8a66b-109">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="8a66b-109">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
