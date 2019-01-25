---
title: IGCHost2 인터페이스
ms.date: 03/30/2017
api_name:
- IGCHost2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost2
helpviewer_keywords:
- IGCHost2 interface [.NET Framework hosting]
ms.assetid: e5323fa4-18ac-424d-859d-a65a550d08d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 742f738ca1a147c75b976d24fa4ac8e7fa4947c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622236"
---
# <a name="igchost2-interface"></a><span data-ttu-id="af0f5-102">IGCHost2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="af0f5-102">IGCHost2 Interface</span></span>
<span data-ttu-id="af0f5-103">가비지 컬렉션 시스템에 대 한 정보를 얻기 위한 고 가비지 컬렉션의 일부 측면을 제어 하기 위한 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="af0f5-103">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="af0f5-104">새로운 개발에 사용 하는 권장 합니다 [ICLRGCManager2](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-interface.md) 대신 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="af0f5-104">For new development, we recommend that you use the [ICLRGCManager2](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-interface.md) interface instead.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="af0f5-105">메서드</span><span class="sxs-lookup"><span data-stu-id="af0f5-105">Methods</span></span>  
  
|<span data-ttu-id="af0f5-106">메서드</span><span class="sxs-lookup"><span data-stu-id="af0f5-106">Method</span></span>|<span data-ttu-id="af0f5-107">설명</span><span class="sxs-lookup"><span data-stu-id="af0f5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="af0f5-108">SetGCStartupLimitsEx 메서드</span><span class="sxs-lookup"><span data-stu-id="af0f5-108">SetGCStartupLimitsEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md)|<span data-ttu-id="af0f5-109">0 세대에 대 한 세그먼트 크기 및 최대 크기를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="af0f5-109">Sets the segment size and the maximum size for generation 0.</span></span> <span data-ttu-id="af0f5-110">0 세대 및 세그먼트 크기 보다 큰 `DWORD`입니다.</span><span class="sxs-lookup"><span data-stu-id="af0f5-110">Enables generation 0 and segment sizes larger than `DWORD`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="af0f5-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="af0f5-111">Requirements</span></span>  
 <span data-ttu-id="af0f5-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="af0f5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="af0f5-113">**헤더:** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="af0f5-113">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="af0f5-114">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="af0f5-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="af0f5-115">**.NET Framework 버전:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="af0f5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af0f5-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="af0f5-116">See also</span></span>
- [<span data-ttu-id="af0f5-117">호스팅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="af0f5-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="af0f5-118">CLR 호스팅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="af0f5-118">CLR Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)
- [<span data-ttu-id="af0f5-119">CorRuntimeHost Coclass</span><span class="sxs-lookup"><span data-stu-id="af0f5-119">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
