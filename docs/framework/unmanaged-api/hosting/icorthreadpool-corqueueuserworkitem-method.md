---
title: ICorThreadpool::CorQueueUserWorkItem 메서드
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorQueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorQueueUserWorkItem
helpviewer_keywords:
- ICorThreadpool::CorQueueUserWorkItem method [.NET Framework hosting]
- CorQueueUserWorkItem method [.NET Framework hosting]
ms.assetid: 29ac7898-a7c7-433e-8f79-cd5237e0bab8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6b13a2342510b48e72c7fd535cd085d0f50ca474
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534659"
---
# <a name="icorthreadpoolcorqueueuserworkitem-method"></a><span data-ttu-id="dd1c6-102">ICorThreadpool::CorQueueUserWorkItem 메서드</span><span class="sxs-lookup"><span data-stu-id="dd1c6-102">ICorThreadpool::CorQueueUserWorkItem Method</span></span>
<span data-ttu-id="dd1c6-103">이 메서드는 .NET Framework 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c6-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd1c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd1c6-104">Syntax</span></span>  
  
```  
HRESULT CorQueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID                  Context,  
    [in] BOOL                   executeOnlyOnce,  
    [out] BOOL*                 result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="dd1c6-105">요구 사항</span><span class="sxs-lookup"><span data-stu-id="dd1c6-105">Requirements</span></span>  
 <span data-ttu-id="dd1c6-106">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="dd1c6-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd1c6-107">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="dd1c6-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dd1c6-108">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="dd1c6-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dd1c6-109">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd1c6-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd1c6-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="dd1c6-110">See also</span></span>
- [<span data-ttu-id="dd1c6-111">ICorThreadpool 인터페이스</span><span class="sxs-lookup"><span data-stu-id="dd1c6-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
