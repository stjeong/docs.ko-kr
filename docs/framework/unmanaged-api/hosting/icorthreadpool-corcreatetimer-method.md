---
title: ICorThreadpool::CorCreateTimer 메서드
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorCreateTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCreateTimer
helpviewer_keywords:
- CorCreateTimer method [.NET Framework hosting]
- ICorThreadpool::CorCreateTimer method [.NET Framework hosting]
ms.assetid: 0d56ef25-30f1-4499-8a1f-76e7654ec614
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 53b44a265e6bb4a2836b4ec053a5bc052afa6b1d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527005"
---
# <a name="icorthreadpoolcorcreatetimer-method"></a><span data-ttu-id="6c45c-102">ICorThreadpool::CorCreateTimer 메서드</span><span class="sxs-lookup"><span data-stu-id="6c45c-102">ICorThreadpool::CorCreateTimer Method</span></span>
<span data-ttu-id="6c45c-103">이 메서드는 .NET Framework 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6c45c-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c45c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c45c-104">Syntax</span></span>  
  
```  
HRESULT CorCreateTimer (  
    [in]  HANDLE*             phNewTimer,  
    [in]  WAITORTIMERCALLBACK Callback,  
    [in]  PVOID               Parameter,  
    [in]  DWORD               DueTime,  
    [in]  DWORD               Period,  
    [out] BOOL*               result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="6c45c-105">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6c45c-105">Requirements</span></span>  
 <span data-ttu-id="6c45c-106">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6c45c-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c45c-107">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6c45c-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6c45c-108">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="6c45c-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6c45c-109">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c45c-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c45c-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="6c45c-110">See also</span></span>
- [<span data-ttu-id="6c45c-111">ICorThreadpool 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6c45c-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
