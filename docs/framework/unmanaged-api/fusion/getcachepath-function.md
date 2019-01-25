---
title: GetCachePath 함수
ms.date: 03/30/2017
api_name:
- GetCachePath
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- GetCachePath
helpviewer_keywords:
- GetCachePath function [.NET Framework fusion]
ms.assetid: d977ad29-6619-42e1-b0be-bc25ea950e80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac0b6ac09db452eb06c633027e9596bda6627005
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509391"
---
# <a name="getcachepath-function"></a><span data-ttu-id="aac9c-102">GetCachePath 함수</span><span class="sxs-lookup"><span data-stu-id="aac9c-102">GetCachePath Function</span></span>
<span data-ttu-id="aac9c-103">지정된 된 플래그를 사용 하 여 캐시 된 어셈블리에 경로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aac9c-103">Gets the path to the cached assembly, using the specified flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aac9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="aac9c-104">Syntax</span></span>  
  
```  
HRESULT GetCachePath (  
    [in]      ASM_CACHE_FLAGS  dwCacheFlags,  
    [in]      LPWSTR           pwzCachePath,  
    [in, out] PDWORD           pcchPath  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aac9c-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aac9c-105">Parameters</span></span>  
 `dwCacheFlags`  
 <span data-ttu-id="aac9c-106">[in] [ASM_CACHE_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md) 캐시 된 어셈블리의 소스를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="aac9c-106">[in] An [ASM_CACHE_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md) value that indicates the source of the cached assembly.</span></span>  
  
 `pwzCachePath`  
 <span data-ttu-id="aac9c-107">[out] 경로에 반환 된 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="aac9c-107">[out] The returned pointer to the path.</span></span>  
  
 `pcchPath`  
 <span data-ttu-id="aac9c-108">[out에서] 요청한 최대 길이인 `pwzCachePath`, 및의 실제 길이가 반환 될 때 `pwzCachePath`합니다.</span><span class="sxs-lookup"><span data-stu-id="aac9c-108">[in, out] The requested maximum length of `pwzCachePath`, and upon return, the actual length of `pwzCachePath`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aac9c-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="aac9c-109">Requirements</span></span>  
 <span data-ttu-id="aac9c-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="aac9c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aac9c-111">**헤더:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="aac9c-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="aac9c-112">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aac9c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aac9c-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="aac9c-113">See also</span></span>
- [<span data-ttu-id="aac9c-114">ASM_CACHE_FLAGS 열거형</span><span class="sxs-lookup"><span data-stu-id="aac9c-114">ASM_CACHE_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md)
- [<span data-ttu-id="aac9c-115">Fusion 전역 정적 함수</span><span class="sxs-lookup"><span data-stu-id="aac9c-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
