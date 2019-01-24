---
title: IHostTaskManager::EndDelayAbort 메서드
ms.date: 03/30/2017
api_name:
- IHostTaskManager.EndDelayAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::EndDelayAbort
helpviewer_keywords:
- EndDelayAbort method [.NET Framework hosting]
- IHostTaskManager::EndDelayAbort method [.NET Framework hosting]
ms.assetid: 6e02facb-2504-4356-9af5-0cee1f8436a7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c93a7f92e7cd5891bac415956c7132a6da62a98c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582359"
---
# <a name="ihosttaskmanagerenddelayabort-method"></a><span data-ttu-id="6b92f-102">IHostTaskManager::EndDelayAbort 메서드</span><span class="sxs-lookup"><span data-stu-id="6b92f-102">IHostTaskManager::EndDelayAbort Method</span></span>
<span data-ttu-id="6b92f-103">관리 코드는 호스트가 종료는 현재 작업을 중단 하지 말아야, 기간에 대 한 이전 호출을 다음 알립니다 [ihosttaskmanager:: Begindelayabort](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-begindelayabort-method.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-103">Notifies the host that managed code is exiting the period in which the current task must not be aborted, following an earlier call to [IHostTaskManager::BeginDelayAbort](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-begindelayabort-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b92f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b92f-104">Syntax</span></span>  
  
```  
HRESULT EndDelayAbort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="6b92f-105">반환 값</span><span class="sxs-lookup"><span data-stu-id="6b92f-105">Return Value</span></span>  
  
|<span data-ttu-id="6b92f-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6b92f-106">HRESULT</span></span>|<span data-ttu-id="6b92f-107">설명</span><span class="sxs-lookup"><span data-stu-id="6b92f-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6b92f-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b92f-108">S_OK</span></span>|<span data-ttu-id="6b92f-109">`EndDelayAbort` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-109">`EndDelayAbort` returned successfully.</span></span>|  
|<span data-ttu-id="6b92f-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6b92f-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6b92f-111">프로세스에는 CLR (공용 언어 런타임)에 로드 되지 또는 CLR 상태인는 관리 코드를 실행 하거나 호출을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6b92f-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6b92f-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6b92f-113">호출 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-113">The call timed out.</span></span>|  
|<span data-ttu-id="6b92f-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6b92f-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6b92f-115">호출자가 잠금을 소유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6b92f-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6b92f-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6b92f-117">이벤트가 차단 된 스레드가 취소 된 또는 파이버를 대기 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6b92f-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6b92f-118">E_FAIL</span></span>|<span data-ttu-id="6b92f-119">알 수 없는 치명적인 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6b92f-120">메서드 E_FAIL을 반환 하는 경우 CLR은 프로세스 내에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6b92f-121">메서드를 호스트 하는 데 대 한 후속 호출 HOST_E_CLRNOTAVAILABLE를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="6b92f-122">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="6b92f-122">E_UNEXPECTED</span></span>|<span data-ttu-id="6b92f-123">`EndDelayAbort` 해당 호출 없이 호출한 `BeginDelayAbort`합니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-123">`EndDelayAbort` was called without a corresponding call to `BeginDelayAbort`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6b92f-124">설명</span><span class="sxs-lookup"><span data-stu-id="6b92f-124">Remarks</span></span>  
 <span data-ttu-id="6b92f-125">CLR에서는 해당 호출 `BeginDelayAbort` 호출 하기 전에 현재 작업에서 `EndDelayAbort`합니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-125">The CLR makes a corresponding call to `BeginDelayAbort` on the current task before calling `EndDelayAbort`.</span></span> <span data-ttu-id="6b92f-126">이러한 해당 호출에 없는 경우 호스트의 구현을 [IHostTaskManager](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md) 에서 E_UNEXPECTED를 반환 해야 `EndDelayAbort`, 어떠한 작업도 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b92f-126">In the absence of such a corresponding call, the host's implementation of [IHostTaskManager](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md) should return E_UNEXPECTED from `EndDelayAbort`, and should take no action.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b92f-127">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6b92f-127">Requirements</span></span>  
 <span data-ttu-id="6b92f-128">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6b92f-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6b92f-129">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6b92f-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6b92f-130">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="6b92f-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6b92f-131">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6b92f-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b92f-132">참고자료</span><span class="sxs-lookup"><span data-stu-id="6b92f-132">See also</span></span>
- <xref:System.Threading>
- [<span data-ttu-id="6b92f-133">ICLRTask 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6b92f-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="6b92f-134">ICLRTaskManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6b92f-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="6b92f-135">IHostTask 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6b92f-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="6b92f-136">IHostTaskManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6b92f-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
