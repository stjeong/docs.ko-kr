---
title: IHostGCManager::ThreadIsBlockingForSuspension 메서드
ms.date: 03/30/2017
api_name:
- IHostGCManager.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager::ThreadIsBlockingForSuspension
helpviewer_keywords:
- IHostGCManager::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: 2657d45d-26d2-4d0a-8473-32b652e3321d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d338b03247f1304f065afc459eb70aac725937c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709808"
---
# <a name="ihostgcmanagerthreadisblockingforsuspension-method"></a><span data-ttu-id="982b1-102">IHostGCManager::ThreadIsBlockingForSuspension 메서드</span><span class="sxs-lookup"><span data-stu-id="982b1-102">IHostGCManager::ThreadIsBlockingForSuspension Method</span></span>
<span data-ttu-id="982b1-103">메서드 호출이 만들어진 스레드는 호스트에 알리는 가비지 수집을 차단 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-103">Notifies the host that the thread from which the method call was made is about to block for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="982b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="982b1-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForSuspension ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="982b1-105">반환 값</span><span class="sxs-lookup"><span data-stu-id="982b1-105">Return Value</span></span>  
  
|<span data-ttu-id="982b1-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="982b1-106">HRESULT</span></span>|<span data-ttu-id="982b1-107">설명</span><span class="sxs-lookup"><span data-stu-id="982b1-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="982b1-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="982b1-108">S_OK</span></span>|<span data-ttu-id="982b1-109">`ThreadIsBlockingForSuspension` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-109">`ThreadIsBlockingForSuspension` returned successfully.</span></span>|  
|<span data-ttu-id="982b1-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="982b1-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="982b1-111">프로세스에는 CLR (공용 언어 런타임)에 로드 되지 또는 CLR 상태인는 관리 코드를 실행 하거나 호출을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="982b1-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="982b1-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="982b1-113">호출 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-113">The call timed out.</span></span>|  
|<span data-ttu-id="982b1-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="982b1-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="982b1-115">호출자가 잠금을 소유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="982b1-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="982b1-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="982b1-117">이벤트가 차단 된 스레드가 취소 된 또는 파이버를 대기 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="982b1-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="982b1-118">E_FAIL</span></span>|<span data-ttu-id="982b1-119">알 수 없는 치명적인 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="982b1-120">메서드 E_FAIL을 반환 하는 경우 CLR은 프로세스 내에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="982b1-121">메서드를 호스트 하는 데 대 한 후속 호출 HOST_E_CLRNOTAVAILABLE를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="982b1-122">설명</span><span class="sxs-lookup"><span data-stu-id="982b1-122">Remarks</span></span>  
 <span data-ttu-id="982b1-123">CLR은 일반적으로 호출 합니다.는 `ThreadIsBlockForSuspension` 메서드 호스트를 관리 되지 않는 작업에 대 한 스레드 일정을 재조정할 수 있도록 가비지 수집을 위해 준비에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-123">The CLR typically calls the `ThreadIsBlockForSuspension` method in preparation for a garbage collection, to give the host an opportunity to reschedule the thread for unmanaged tasks.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="982b1-124">호스트 수를 호출한 후에 작업을 다시 예약 `ThreadIsBlockingForSuspension`합니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-124">The host can reschedule tasks only after a call to `ThreadIsBlockingForSuspension`.</span></span> <span data-ttu-id="982b1-125">런타임 호출 후 [SuspensionStarting](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-suspensionstarting-method.md)를 호스트 해야 작업을 다시 예약 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="982b1-125">After the runtime calls [SuspensionStarting](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-suspensionstarting-method.md), the host must not reschedule a task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="982b1-126">요구 사항</span><span class="sxs-lookup"><span data-stu-id="982b1-126">Requirements</span></span>  
 <span data-ttu-id="982b1-127">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="982b1-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="982b1-128">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="982b1-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="982b1-129">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="982b1-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="982b1-130">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="982b1-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="982b1-131">참고자료</span><span class="sxs-lookup"><span data-stu-id="982b1-131">See also</span></span>
- [<span data-ttu-id="982b1-132">ICLRTask 인터페이스</span><span class="sxs-lookup"><span data-stu-id="982b1-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="982b1-133">ICLRTaskManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="982b1-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="982b1-134">IHostTask 인터페이스</span><span class="sxs-lookup"><span data-stu-id="982b1-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="982b1-135">IHostTaskManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="982b1-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="982b1-136">IHostGCManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="982b1-136">IHostGCManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-interface.md)
