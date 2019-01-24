---
title: ICorPublishEnum::Clone 메서드
ms.date: 03/30/2017
api_name:
- ICorPublishEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum::Clone
helpviewer_keywords:
- Clone method, ICorPublishEnum interface [.NET Framework debugging]
- ICorPublishEnum::Clone method [.NET Framework debugging]
ms.assetid: c9a26ea3-b8eb-4b8e-854f-9a2ca26b3b39
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fdc8c274cd6949977b3e0ad5df8e1e14692ad167
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563589"
---
# <a name="icorpublishenumclone-method"></a><span data-ttu-id="57bae-102">ICorPublishEnum::Clone 메서드</span><span class="sxs-lookup"><span data-stu-id="57bae-102">ICorPublishEnum::Clone Method</span></span>
<span data-ttu-id="57bae-103">이 파일의 복사본을 만듭니다 [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57bae-103">Creates a copy of this [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57bae-104">구문</span><span class="sxs-lookup"><span data-stu-id="57bae-104">Syntax</span></span>  
  
```  
HRESULT Clone (  
    [out] ICorPublishEnum   **ppEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="57bae-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="57bae-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="57bae-106">[out] 주소에 대 한 포인터를 `ICorPublishEnum` 개체의 복사본 인 `ICorPublishEnum` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57bae-106">[out] A pointer to the address of an `ICorPublishEnum` object that is a copy of this `ICorPublishEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57bae-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="57bae-107">Requirements</span></span>  
 <span data-ttu-id="57bae-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="57bae-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57bae-109">**헤더:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="57bae-109">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="57bae-110">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57bae-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57bae-111">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57bae-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57bae-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="57bae-112">See also</span></span>
- [<span data-ttu-id="57bae-113">ICorPublishEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="57bae-113">ICorPublishEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md)
