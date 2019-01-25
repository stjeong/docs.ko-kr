---
title: ICorThreadpool::CorGetAvailableThreads 메서드
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorGetAvailableThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorGetAvailableThreads
helpviewer_keywords:
- CorGetAvailableThreads method [.NET Framework hosting]
- ICorThreadpool::CorGetAvailableThreads method [.NET Framework hosting]
ms.assetid: 0b09b750-0b86-4ba4-9621-041857cfe8ba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 20b600eb50ca4992e20b991406d18a91feae5c54
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574458"
---
# <a name="icorthreadpoolcorgetavailablethreads-method"></a><span data-ttu-id="b14f4-102">ICorThreadpool::CorGetAvailableThreads 메서드</span><span class="sxs-lookup"><span data-stu-id="b14f4-102">ICorThreadpool::CorGetAvailableThreads Method</span></span>
<span data-ttu-id="b14f4-103">이 메서드는 .NET Framework 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b14f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="b14f4-104">Syntax</span></span>  
  
```  
HRESULT CorGetAvailableThreads (  
    [out] DWORD *AvailableWorkerThreads,  
    [out] DWORD *AvailableIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="b14f4-105">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b14f4-105">Requirements</span></span>  
 <span data-ttu-id="b14f4-106">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b14f4-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b14f4-107">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b14f4-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b14f4-108">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="b14f4-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b14f4-109">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b14f4-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b14f4-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="b14f4-110">See also</span></span>
- [<span data-ttu-id="b14f4-111">ICorThreadpool 인터페이스</span><span class="sxs-lookup"><span data-stu-id="b14f4-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
