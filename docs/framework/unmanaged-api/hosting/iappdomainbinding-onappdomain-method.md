---
title: IAppDomainBinding::OnAppDomain 메서드
ms.date: 03/30/2017
api_name:
- IAppDomainBinding.OnAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- OnAppDomain
helpviewer_keywords:
- IAppDomainBinding::OnAppDomain method [.NET Framework hosting]
- OnAppDomain method [.NET Framework hosting]
ms.assetid: b419dcc9-e8aa-484b-af0d-0f40358edb99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c1c22ee61769fdcbb92a73ca0dd55299ebbcf934
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305768"
---
# <a name="iappdomainbindingonappdomain-method"></a><span data-ttu-id="9eba5-102">IAppDomainBinding::OnAppDomain 메서드</span><span class="sxs-lookup"><span data-stu-id="9eba5-102">IAppDomainBinding::OnAppDomain Method</span></span>
<span data-ttu-id="9eba5-103">CLR (공용 언어 런타임) 응용 프로그램 도메인이 만들어졌는지 호스트에 알리기 위해 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eba5-103">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9eba5-104">구문</span><span class="sxs-lookup"><span data-stu-id="9eba5-104">Syntax</span></span>  
  
```  
HRESULT OnAppDomain (  
    [in] IUnknown* pAppdomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9eba5-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9eba5-105">Parameters</span></span>  
 `pAppdomain`  
 <span data-ttu-id="9eba5-106">[in] 에 대 한 포인터를 [IUnknown](/cpp/atl/iunknown) 새 응용 프로그램 도메인을 나타내는 인터페이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9eba5-106">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) interface object that represents the new application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9eba5-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9eba5-107">Requirements</span></span>  
 <span data-ttu-id="9eba5-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9eba5-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9eba5-109">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9eba5-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9eba5-110">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="9eba5-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9eba5-111">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9eba5-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9eba5-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="9eba5-112">See also</span></span>
- [<span data-ttu-id="9eba5-113">IAppDomainBinding 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9eba5-113">IAppDomainBinding Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iappdomainbinding-interface.md)
