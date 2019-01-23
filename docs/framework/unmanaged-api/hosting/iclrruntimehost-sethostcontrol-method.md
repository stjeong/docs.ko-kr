---
title: ICLRRuntimeHost::SetHostControl 메서드
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.SetHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::SetHostControl
helpviewer_keywords:
- SetHostControl method [.NET Framework hosting]
- ICLRRuntimeHost::SetHostControl method [.NET Framework hosting]
ms.assetid: 6136be87-e631-4756-81ed-74b66581bad4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e385744f1a9ecef2cbe1f6074501061dc2f15fe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602262"
---
# <a name="iclrruntimehostsethostcontrol-method"></a><span data-ttu-id="ed8ca-102">ICLRRuntimeHost::SetHostControl 메서드</span><span class="sxs-lookup"><span data-stu-id="ed8ca-102">ICLRRuntimeHost::SetHostControl Method</span></span>
<span data-ttu-id="ed8ca-103">CLR (공용 언어 런타임) 호스트의 구현을 가져오는 데 사용할 수 있는 인터페이스 포인터를 설정 [IHostControl 인터페이스](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-103">Sets the interface pointer that the common language runtime (CLR) can use to get the host's implementation of [IHostControl Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed8ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed8ca-104">Syntax</span></span>  
  
```  
HRESULT SetHostControl(  
    [in] IHostControl* pHostControl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ed8ca-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed8ca-105">Parameters</span></span>  
 `pHostControl`  
 <span data-ttu-id="ed8ca-106">[in] 호스트의 구현에 대 한 인터페이스 포인터 [IHostControl 인터페이스](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-106">[in] An interface pointer to the host's implementation of [IHostControl Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ed8ca-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="ed8ca-107">Return Value</span></span>  
  
|<span data-ttu-id="ed8ca-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ed8ca-108">HRESULT</span></span>|<span data-ttu-id="ed8ca-109">설명</span><span class="sxs-lookup"><span data-stu-id="ed8ca-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ed8ca-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed8ca-110">S_OK</span></span>|<span data-ttu-id="ed8ca-111">`SetHostControl` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-111">`SetHostControl` returned successfully.</span></span>|  
|<span data-ttu-id="ed8ca-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ed8ca-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ed8ca-113">CLR이 로드 된 프로세스에 또는 CLR 상태인는 관리 코드를 실행 하거나 호출을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ed8ca-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ed8ca-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ed8ca-115">호출 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-115">The call timed out.</span></span>|  
|<span data-ttu-id="ed8ca-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ed8ca-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ed8ca-117">호출자가 잠금을 소유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ed8ca-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ed8ca-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ed8ca-119">이벤트가 차단 된 스레드가 취소 된 또는 파이버를 대기 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ed8ca-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ed8ca-120">E_FAIL</span></span>|<span data-ttu-id="ed8ca-121">알 수 없는 치명적인 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ed8ca-122">메서드가 E_FAIL을 반환 하는 경우 CLR은 프로세스 내에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ed8ca-123">메서드를 호스트 하는 데 대 한 후속 호출 HOST_E_CLRNOTAVAILABLE를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ed8ca-124">E_CLR_ALREADY_STARTED</span><span class="sxs-lookup"><span data-stu-id="ed8ca-124">E_CLR_ALREADY_STARTED</span></span>|<span data-ttu-id="ed8ca-125">CLR 이미 초기화 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-125">The CLR has already been initialized.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ed8ca-126">설명</span><span class="sxs-lookup"><span data-stu-id="ed8ca-126">Remarks</span></span>  
 <span data-ttu-id="ed8ca-127">호출 해야 합니다 `SetHostControl` CLR을 초기화 하기 전에, 즉, 호출 하기 전에 [메서드 시작](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) 양립 합니다 [메타 데이터 인터페이스](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-127">You must call `SetHostControl` before the CLR is initialized, that is, before you call [Start Method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) or use any of the [Metadata Interfaces](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span></span> <span data-ttu-id="ed8ca-128">호출 하는 것이 좋습니다 `SetHostControl` 호출한 직후 [CorBindToCurrentRuntime 함수](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md) 하거나 [CorBindToRuntimeEx 함수](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-128">It is recommended that you call `SetHostControl` immediately after calling [CorBindToCurrentRuntime Function](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md) or [CorBindToRuntimeEx Function](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed8ca-129">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ed8ca-129">Requirements</span></span>  
 <span data-ttu-id="ed8ca-130">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ed8ca-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed8ca-131">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ed8ca-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ed8ca-132">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="ed8ca-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ed8ca-133">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed8ca-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed8ca-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="ed8ca-134">See also</span></span>
- [<span data-ttu-id="ed8ca-135">ICLRRuntimeHost 인터페이스</span><span class="sxs-lookup"><span data-stu-id="ed8ca-135">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
- [<span data-ttu-id="ed8ca-136">IHostControl 인터페이스</span><span class="sxs-lookup"><span data-stu-id="ed8ca-136">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
