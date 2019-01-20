---
title: IXCLRDataProcess::GetAppDomainByUniqueId Method
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 83e7d4e1a4ff3c2e6f573d6c097c7cdb9c5f3c54
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416698"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="2671e-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span><span class="sxs-lookup"><span data-stu-id="2671e-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="2671e-103">가져옵니다는 `AppDomain` 해당 고유 식별자를 기반으로 하는 프로세스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2671e-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="2671e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2671e-104">Syntax</span></span>
```
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

### <a name="parameters"></a><span data-ttu-id="2671e-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2671e-105">Parameters</span></span>
<span data-ttu-id="2671e-106">`id` [in] AppDomain의 고유 식별자</span><span class="sxs-lookup"><span data-stu-id="2671e-106">`id` [in] The unique identifier of the AppDomain</span></span>

<span data-ttu-id="2671e-107">`appDomain` [out] AppDomain</span><span class="sxs-lookup"><span data-stu-id="2671e-107">`appDomain` [out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="2671e-108">설명</span><span class="sxs-lookup"><span data-stu-id="2671e-108">Remarks</span></span>

<span data-ttu-id="2671e-109">제공 된 메서드는의 일부는 `IXCLRDataProcess` 인터페이스 및 가상 메서드 테이블의 20 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2671e-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="2671e-110">`IXCLRDataAppDomain*` 반환 된 다른 Api와의 상호 작용에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2671e-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2671e-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2671e-111">Requirements</span></span>
<span data-ttu-id="2671e-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="2671e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="2671e-113">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="2671e-113">**Header:** None</span></span>  
<span data-ttu-id="2671e-114">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="2671e-114">**Library:** None</span></span>  
<span data-ttu-id="2671e-115">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2671e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="2671e-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2671e-116">See Also</span></span>
- [<span data-ttu-id="2671e-117">디버깅</span><span class="sxs-lookup"><span data-stu-id="2671e-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="2671e-118">IXCLRDataProcess 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2671e-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
