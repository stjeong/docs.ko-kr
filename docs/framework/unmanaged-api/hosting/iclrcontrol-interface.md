---
title: ICLRControl 인터페이스
ms.date: 03/30/2017
api_name:
- ICLRControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl
helpviewer_keywords:
- ICLRControl interface [.NET Framework hosting]
ms.assetid: a24fd905-1fa6-45a0-ad65-e9e2ee58861e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 61f9448735f5d26d122ed44c4f41c4fd2a9f7478
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614304"
---
# <a name="iclrcontrol-interface"></a><span data-ttu-id="9b800-102">ICLRControl 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-102">ICLRControl Interface</span></span>
<span data-ttu-id="9b800-103">참조 하는 데 사용 하는 CLR (공용 언어 런타임)의 측면을 구성 하는 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b800-103">Provides methods that allow a host to get references to, and configure aspects of, the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9b800-104">메서드</span><span class="sxs-lookup"><span data-stu-id="9b800-104">Methods</span></span>  
  
|<span data-ttu-id="9b800-105">메서드</span><span class="sxs-lookup"><span data-stu-id="9b800-105">Method</span></span>|<span data-ttu-id="9b800-106">설명</span><span class="sxs-lookup"><span data-stu-id="9b800-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9b800-107">GetCLRManager 메서드</span><span class="sxs-lookup"><span data-stu-id="9b800-107">GetCLRManager Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md)|<span data-ttu-id="9b800-108">호스트 CLR을 구성 하 여 관리자 형식의 모든 인스턴스에 대 한 인터페이스 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b800-108">Gets an interface pointer to an instance of any of the manager types the host can use to configure the CLR.</span></span>|  
|[<span data-ttu-id="9b800-109">SetAppDomainManagerType 메서드</span><span class="sxs-lookup"><span data-stu-id="9b800-109">SetAppDomainManagerType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)|<span data-ttu-id="9b800-110">파생 된 형식을 설정 <xref:System.AppDomainManager> 응용 프로그램 도메인 관리자에 대 한 형식으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b800-110">Sets a type derived from <xref:System.AppDomainManager> as the type for application domain managers.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9b800-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9b800-111">Requirements</span></span>  
 <span data-ttu-id="9b800-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b800-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b800-113">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9b800-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9b800-114">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="9b800-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9b800-115">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b800-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b800-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="9b800-116">See also</span></span>
- [<span data-ttu-id="9b800-117">ICLRAssemblyIdentityManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-117">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="9b800-118">ICLRDebugManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-118">ICLRDebugManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md)
- [<span data-ttu-id="9b800-119">ICLRGCManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-119">ICLRGCManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md)
- [<span data-ttu-id="9b800-120">ICLRHostBindingPolicyManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-120">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="9b800-121">ICLRHostProtectionManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-121">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="9b800-122">ICLROnEventManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-122">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
- [<span data-ttu-id="9b800-123">ICLRPolicyManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-123">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [<span data-ttu-id="9b800-124">IHostControl 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-124">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
- [<span data-ttu-id="9b800-125">호스팅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b800-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
