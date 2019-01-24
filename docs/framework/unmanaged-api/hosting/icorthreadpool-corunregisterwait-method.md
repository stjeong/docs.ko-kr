---
title: ICorThreadpool::CorUnregisterWait 메서드
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorUnregisterWait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorUnregisterWait
helpviewer_keywords:
- CorUnregisterWait method [.NET Framework hosting]
- ICorThreadpool::CorUnregisterWait method [.NET Framework hosting]
ms.assetid: 42c933f1-30a8-4011-bdea-e117f3c3265e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eacc9152200b9b57e8a1c5506ecac2e0010fbe9f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54698975"
---
# <a name="icorthreadpoolcorunregisterwait-method"></a><span data-ttu-id="37e7a-102">ICorThreadpool::CorUnregisterWait 메서드</span><span class="sxs-lookup"><span data-stu-id="37e7a-102">ICorThreadpool::CorUnregisterWait Method</span></span>
<span data-ttu-id="37e7a-103">이 메서드는 .NET Framework 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37e7a-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37e7a-104">구문</span><span class="sxs-lookup"><span data-stu-id="37e7a-104">Syntax</span></span>  
  
```  
HRESULT CorUnregisterWait (  
    [in] HANDLE hWaitObject,  
    [in] HANDLE CompletionEvent,  
    [out] BOOL* result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="37e7a-105">요구 사항</span><span class="sxs-lookup"><span data-stu-id="37e7a-105">Requirements</span></span>  
 <span data-ttu-id="37e7a-106">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="37e7a-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="37e7a-107">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="37e7a-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="37e7a-108">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="37e7a-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="37e7a-109">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37e7a-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37e7a-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="37e7a-110">See also</span></span>
- [<span data-ttu-id="37e7a-111">ICorThreadpool 인터페이스</span><span class="sxs-lookup"><span data-stu-id="37e7a-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
