---
title: ICLRAssemblyIdentityManager::GetBindingIdentityFromStream 메서드
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetBindingIdentityFromStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetBindingIdentityFromStream
helpviewer_keywords:
- GetBindingIdentityFromStream method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::GetBindingIdentityFromStream method [.NET Framework hosting]
ms.assetid: 40123b30-a589-46b3-95d3-af7b2b0baa05
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1b0f4b184a11e769291c64d83d11d57b5b3d19c7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498806"
---
# <a name="iclrassemblyidentitymanagergetbindingidentityfromstream-method"></a><span data-ttu-id="98eac-102">ICLRAssemblyIdentityManager::GetBindingIdentityFromStream 메서드</span><span class="sxs-lookup"><span data-stu-id="98eac-102">ICLRAssemblyIdentityManager::GetBindingIdentityFromStream Method</span></span>
<span data-ttu-id="98eac-103">지정한 스트림에서 어셈블리에 대 한 정식 어셈블리 id 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-103">Gets the canonical assembly identity data for the assembly in the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98eac-104">구문</span><span class="sxs-lookup"><span data-stu-id="98eac-104">Syntax</span></span>  
  
```  
HRESULT GetBindingIdentityFromStream (  
    [in] IStream    *pStream,  
    [in] DWORD       dwFlags,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="98eac-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="98eac-105">Parameters</span></span>  
 `pStream`  
 <span data-ttu-id="98eac-106">[in] 계산할 어셈블리 스트림입니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-106">[in] The assembly stream to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="98eac-107">[in] 향후 확장성을 위해 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-107">[in] Provided for future extensibility.</span></span> <span data-ttu-id="98eac-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT에는 CLR (공용 언어 런타임)의 현재 버전을 지 원하는 유일한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="98eac-109">[out] 불투명 한 어셈블리 id 데이터를 포함 하는 버퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-109">[out] A buffer containing the opaque assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="98eac-110">[out에서] 크기 `pwzBuffer`합니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-110">[in, out] The size of `pwzBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="98eac-111">반환 값</span><span class="sxs-lookup"><span data-stu-id="98eac-111">Return Value</span></span>  
  
|<span data-ttu-id="98eac-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="98eac-112">HRESULT</span></span>|<span data-ttu-id="98eac-113">설명</span><span class="sxs-lookup"><span data-stu-id="98eac-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="98eac-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="98eac-114">S_OK</span></span>|<span data-ttu-id="98eac-115">메서드가 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-115">The method returned successfully.</span></span>|  
|<span data-ttu-id="98eac-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="98eac-116">E_INVALIDARG</span></span>|<span data-ttu-id="98eac-117">제공 된 `pStream` null입니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-117">The supplied `pStream` is null.</span></span>|  
|<span data-ttu-id="98eac-118">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="98eac-118">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="98eac-119">크기 `pwzBuffer` 너무 작습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-119">The size of `pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="98eac-120">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="98eac-120">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="98eac-121">CLR이 로드 된 프로세스에 또는 CLR 상태인는 관리 코드를 실행 하거나 호출을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-121">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="98eac-122">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="98eac-122">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="98eac-123">호출 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-123">The call timed out.</span></span>|  
|<span data-ttu-id="98eac-124">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="98eac-124">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="98eac-125">호출자가 잠금을 소유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-125">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="98eac-126">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="98eac-126">HOST_E_ABANDONED</span></span>|<span data-ttu-id="98eac-127">이벤트가 차단 된 스레드가 취소 된 또는 파이버를 대기 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-127">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="98eac-128">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="98eac-128">E_FAIL</span></span>|<span data-ttu-id="98eac-129">알 수 없는 치명적인 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-129">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="98eac-130">메서드가 E_FAIL을 반환 하는 경우 CLR은 프로세스 내에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-130">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="98eac-131">메서드를 호스트 하는 데 대 한 후속 호출 HOST_E_CLRNOTAVAILABLE를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98eac-131">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="98eac-132">요구 사항</span><span class="sxs-lookup"><span data-stu-id="98eac-132">Requirements</span></span>  
 <span data-ttu-id="98eac-133">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="98eac-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="98eac-134">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="98eac-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="98eac-135">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="98eac-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="98eac-136">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="98eac-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98eac-137">참고자료</span><span class="sxs-lookup"><span data-stu-id="98eac-137">See also</span></span>
- [<span data-ttu-id="98eac-138">ICLRAssemblyIdentityManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="98eac-138">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="98eac-139">ICLRAssemblyReferenceList 인터페이스</span><span class="sxs-lookup"><span data-stu-id="98eac-139">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
