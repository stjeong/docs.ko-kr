---
title: IAssemblyCache::CreateAssemblyCacheItem 메서드
ms.date: 03/30/2017
api_name:
- IAssemblyCache.CreateAssemblyCacheItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::CreateAssemblyCacheItem
helpviewer_keywords:
- IAssemblyCache::CreateAssemblyCacheItem method [.NET Framework fusion]
- CreateAssemblyCacheItem method [.NET Framework fusion]
ms.assetid: 017a7ba5-aaaf-44e2-9cbe-ceebef259df0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27001f8560dcd128b5d737ed0f219387be86d6e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672308"
---
# <a name="iassemblycachecreateassemblycacheitem-method"></a><span data-ttu-id="cbc66-102">IAssemblyCache::CreateAssemblyCacheItem 메서드</span><span class="sxs-lookup"><span data-stu-id="cbc66-102">IAssemblyCache::CreateAssemblyCacheItem Method</span></span>
<span data-ttu-id="cbc66-103">새 참조를 가져옵니다 [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-103">Gets a reference to a new [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbc66-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbc66-104">Syntax</span></span>  
  
```  
HRESULT CreateAssemblyCacheItem (  
    [in]  DWORD dwFlags,  
    [in]  PVOID pvReserved,  
    [out] IAssemblyCacheItem **ppAsmItem,  
    [in, optional] LPCWSTR pszAssemblyName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cbc66-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbc66-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="cbc66-106">[in] 같은 값이 지원에 정의 된 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-106">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="cbc66-107">다음 값이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="cbc66-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="cbc66-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span></span>  
  
-   <span data-ttu-id="cbc66-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="cbc66-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="cbc66-110">[in] 향후 확장성을 위해 예약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="cbc66-111">`pvReserved` null 참조 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-111">`pvReserved` must be a null reference.</span></span>  
  
 `ppAsmItem`  
 <span data-ttu-id="cbc66-112">[out] 반환 된 `IAssemblyCacheItem` 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-112">[out] The returned `IAssemblyCacheItem` pointer.</span></span>  
  
 `pszAssemblyName`  
 <span data-ttu-id="cbc66-113">[in, 선택 사항] Uncanonicalized, 쉼표로 구분 된 `name=value` 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc66-113">[in, optional] Uncanonicalized, comma-separated `name=value` pairs.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cbc66-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="cbc66-114">Requirements</span></span>  
 <span data-ttu-id="cbc66-115">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cbc66-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cbc66-116">**헤더:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="cbc66-116">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="cbc66-117">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cbc66-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cbc66-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="cbc66-118">See also</span></span>
- [<span data-ttu-id="cbc66-119">IAssemblyCache 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cbc66-119">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
- [<span data-ttu-id="cbc66-120">IAssemblyCacheItem 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cbc66-120">IAssemblyCacheItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
