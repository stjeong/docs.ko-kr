---
title: IHostIoCompletionManager::Bind 메서드
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.Bind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::Bind
helpviewer_keywords:
- IHostIoCompletionManager::Bind method [.NET Framework hosting]
- Bind method [.NET Framework hosting]
ms.assetid: acd74cb5-7e22-4a07-83c3-82288e1abd9f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c03cdb9f9205676d17d6e18b9b2e074132ee26f1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594774"
---
# <a name="ihostiocompletionmanagerbind-method"></a><span data-ttu-id="aab81-102">IHostIoCompletionManager::Bind 메서드</span><span class="sxs-lookup"><span data-stu-id="aab81-102">IHostIoCompletionManager::Bind Method</span></span>
<span data-ttu-id="aab81-103">지정된 된 핸들에 대 한 이전 호출에서 생성 된 I/O 완료 포트에 바인딩합니다 [CreateIoCompletionPort](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-createiocompletionport-method.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-103">Binds the specified handle to an I/O completion port that has been created by an earlier call to [CreateIoCompletionPort](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-createiocompletionport-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aab81-104">구문</span><span class="sxs-lookup"><span data-stu-id="aab81-104">Syntax</span></span>  
  
```  
HRESULT Bind (  
    [in] HANDLE hPort,  
    [in] HANDLE hHandle  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aab81-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aab81-105">Parameters</span></span>  
 `hPort`  
 <span data-ttu-id="aab81-106">[in] I/O 완료 포트를 바인딩할 `hHandle`합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-106">[in] The I/O completion port to which to bind `hHandle`.</span></span> <span data-ttu-id="aab81-107">경우 값 `hPort` 이 null 이면 `hHandle` 기본 I/O 완료 포트에 바인딩되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-107">If the value of `hPort` is null, `hHandle` is bound to the default I/O completion port.</span></span>  
  
 `hHandle`  
 <span data-ttu-id="aab81-108">[in] 운영 체제 핸들을 바인딩할 `hPort`합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-108">[in] The operating system handle to bind to `hPort`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="aab81-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="aab81-109">Return Value</span></span>  
  
|<span data-ttu-id="aab81-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="aab81-110">HRESULT</span></span>|<span data-ttu-id="aab81-111">설명</span><span class="sxs-lookup"><span data-stu-id="aab81-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="aab81-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="aab81-112">S_OK</span></span>|<span data-ttu-id="aab81-113">`Bind` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-113">`Bind` returned successfully.</span></span>|  
|<span data-ttu-id="aab81-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="aab81-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="aab81-115">프로세스에는 CLR (공용 언어 런타임)에 로드 되지 또는 CLR 상태인는 관리 코드를 실행 하거나 호출을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="aab81-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="aab81-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="aab81-117">호출 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-117">The call timed out.</span></span>|  
|<span data-ttu-id="aab81-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="aab81-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="aab81-119">호출자가 잠금을 소유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="aab81-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="aab81-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="aab81-121">이벤트가 차단 된 스레드가 취소 된 또는 파이버를 대기 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="aab81-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="aab81-122">E_FAIL</span></span>|<span data-ttu-id="aab81-123">알 수 없는 치명적인 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="aab81-124">메서드 E_FAIL을 반환 하는 경우 CLR은 프로세스 내에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="aab81-125">메서드를 호스트 하는 데 대 한 후속 호출 HOST_E_CLRNOTAVAILABLE를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aab81-126">설명</span><span class="sxs-lookup"><span data-stu-id="aab81-126">Remarks</span></span>  
 <span data-ttu-id="aab81-127">I/O 완료 포트에 대 한 호출을 사용 하 여 만들어지는 `CreateIoCompletionPort`합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-127">An I/O completion port is created by using a call to `CreateIoCompletionPort`.</span></span> <span data-ttu-id="aab81-128">CLR에서는 `Bind` 핸들을 해당 포트에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="aab81-128">The CLR calls `Bind` to bind a handle to that port.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="aab81-129">I/O 요청을 완료 되 면 호스트를 호출 해야 합니다 [iclriocompletionmanager:: Oncomplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="aab81-129">When an I/O request completes, the host must call the [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aab81-130">요구 사항</span><span class="sxs-lookup"><span data-stu-id="aab81-130">Requirements</span></span>  
 <span data-ttu-id="aab81-131">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="aab81-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aab81-132">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="aab81-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="aab81-133">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="aab81-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="aab81-134">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aab81-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aab81-135">참고자료</span><span class="sxs-lookup"><span data-stu-id="aab81-135">See also</span></span>
- [<span data-ttu-id="aab81-136">ICLRIoCompletionManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="aab81-136">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)
