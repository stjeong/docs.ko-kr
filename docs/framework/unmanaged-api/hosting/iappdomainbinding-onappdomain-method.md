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
ms.openlocfilehash: 8dfd396568424c3a2300ed5d982e766afd5f925f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725495"
---
# <a name="iappdomainbindingonappdomain-method"></a><span data-ttu-id="26160-102">IAppDomainBinding::OnAppDomain 메서드</span><span class="sxs-lookup"><span data-stu-id="26160-102">IAppDomainBinding::OnAppDomain Method</span></span>
<span data-ttu-id="26160-103">CLR (공용 언어 런타임) 응용 프로그램 도메인이 만들어졌는지 호스트에 알리기 위해 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26160-103">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26160-104">구문</span><span class="sxs-lookup"><span data-stu-id="26160-104">Syntax</span></span>  
  
```  
HRESULT OnAppDomain (  
    [in] IUnknown* pAppdomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="26160-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26160-105">Parameters</span></span>  
 `pAppdomain`  
 <span data-ttu-id="26160-106">[in] 에 대 한 포인터를 [IUnknown](https://msdn.microsoft.com/library/94as6ehy(v=vs.110).aspx) 새 응용 프로그램 도메인을 나타내는 인터페이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26160-106">[in] A pointer to an [IUnknown](https://msdn.microsoft.com/library/94as6ehy(v=vs.110).aspx) interface object that represents the new application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26160-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="26160-107">Requirements</span></span>  
 <span data-ttu-id="26160-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="26160-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26160-109">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="26160-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="26160-110">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="26160-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="26160-111">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26160-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26160-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="26160-112">See also</span></span>
- [<span data-ttu-id="26160-113">IAppDomainBinding 인터페이스</span><span class="sxs-lookup"><span data-stu-id="26160-113">IAppDomainBinding Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iappdomainbinding-interface.md)
