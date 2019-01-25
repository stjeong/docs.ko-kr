---
title: EInitializeNewDomainFlags 열거형
ms.date: 03/30/2017
api_name:
- EInitializeNewDomainFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EInitializeNewDomainFlags
helpviewer_keywords:
- EInitializeNewDomainFlags enumeration [.NET Framework hosting]
ms.assetid: 3a120ab2-f5ef-4c9b-8595-d3ed7247c342
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 826e02789f6940923538f3e01744345dacf4b2ba
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54705286"
---
# <a name="einitializenewdomainflags-enumeration"></a><span data-ttu-id="80cd5-102">EInitializeNewDomainFlags 열거형</span><span class="sxs-lookup"><span data-stu-id="80cd5-102">EInitializeNewDomainFlags Enumeration</span></span>
<span data-ttu-id="80cd5-103">호스트 응용 프로그램 도메인의 초기화에 대 한 정보를 사용 하 여 런타임에 제공를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80cd5-103">Enables the host to provide the runtime with information about the initialization of an application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80cd5-104">구문</span><span class="sxs-lookup"><span data-stu-id="80cd5-104">Syntax</span></span>  
  
```  
typedef enum {  
    eInitializeNewDomainFlags_None              = 0x0000,  
    eInitializeNewDomainFlags_NoSecurityChanges = 0x0002  
} EInitializeNewDomainFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="80cd5-105">멤버</span><span class="sxs-lookup"><span data-stu-id="80cd5-105">Members</span></span>  
  
|<span data-ttu-id="80cd5-106">멤버</span><span class="sxs-lookup"><span data-stu-id="80cd5-106">Member</span></span>|<span data-ttu-id="80cd5-107">설명</span><span class="sxs-lookup"><span data-stu-id="80cd5-107">Description</span></span>|  
|------------|-----------------|  
|`eInitializeNewDomainFlags_None`|<span data-ttu-id="80cd5-108">플래그가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="80cd5-108">No flags.</span></span>|  
|`eInitializeNewDomainFlags_NoSecurityChanges`|<span data-ttu-id="80cd5-109">알립니다는 CLR (공용 언어 런타임)는 호스트를 변경 하면 안 응용 프로그램 도메인의 보안 상태를 <xref:System.AppDomainManager.InitializeNewDomain%2A> 메서드.</span><span class="sxs-lookup"><span data-stu-id="80cd5-109">Informs the common language runtime (CLR) that the host will not make changes to the security state of the application domain in the <xref:System.AppDomainManager.InitializeNewDomain%2A> method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="80cd5-110">설명</span><span class="sxs-lookup"><span data-stu-id="80cd5-110">Remarks</span></span>  
 <span data-ttu-id="80cd5-111">합니다 [iclrdomainmanager:: Setappdomainmanagertype](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md) 형식의 매개 변수를 사용 하는 메서드 `EInitializeNewDomainFlags`합니다.</span><span class="sxs-lookup"><span data-stu-id="80cd5-111">The [ICLRDomainManager::SetAppDomainManagerType](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md) method takes a parameter of type `EInitializeNewDomainFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="80cd5-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="80cd5-112">Requirements</span></span>  
 <span data-ttu-id="80cd5-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="80cd5-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80cd5-114">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="80cd5-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="80cd5-115">**라이브러리:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="80cd5-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="80cd5-116">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80cd5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80cd5-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="80cd5-117">See also</span></span>
- [<span data-ttu-id="80cd5-118">호스팅 열거형</span><span class="sxs-lookup"><span data-stu-id="80cd5-118">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
- [<span data-ttu-id="80cd5-119">SetAppDomainManagerType 메서드</span><span class="sxs-lookup"><span data-stu-id="80cd5-119">SetAppDomainManagerType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md)
