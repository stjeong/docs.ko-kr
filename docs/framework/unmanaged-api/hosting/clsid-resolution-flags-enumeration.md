---
title: CLSID_RESOLUTION_FLAGS 열거형
ms.date: 03/30/2017
api_name:
- CLSID_RESOLUTION_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLSID_RESOLUTION_FLAGS
helpviewer_keywords:
- CLSID_RESOLUTION_FLAGS enumeration [.NET Framework hosting]
ms.assetid: cd8b9879-962a-4811-aa46-2e2b6bae0d84
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bee25122920a6fcec3bbd4e9e53bbdad008d5304
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514108"
---
# <a name="clsidresolutionflags-enumeration"></a><span data-ttu-id="e7e56-102">CLSID_RESOLUTION_FLAGS 열거형</span><span class="sxs-lookup"><span data-stu-id="e7e56-102">CLSID_RESOLUTION_FLAGS Enumeration</span></span>
<span data-ttu-id="e7e56-103">CLR (공용 언어 런타임) 확인 하는 방법을 나타내는 값을 포함 한 `CLSID`합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e56-103">Contains values that indicate how the common language runtime (CLR) should resolve a `CLSID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7e56-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7e56-104">Syntax</span></span>  
  
```  
typedef enum {  
    CLSID_RESOLUTION_DEFAULT      = 0x0,  
    CLSID_RESOLUTION_REGISTERED   = 0x1  
} CLSID_RESOLUTION_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="e7e56-105">멤버</span><span class="sxs-lookup"><span data-stu-id="e7e56-105">Members</span></span>  
  
|<span data-ttu-id="e7e56-106">멤버</span><span class="sxs-lookup"><span data-stu-id="e7e56-106">Member</span></span>|<span data-ttu-id="e7e56-107">설명</span><span class="sxs-lookup"><span data-stu-id="e7e56-107">Description</span></span>|  
|------------|-----------------|  
|`CLSID_RESOLUTION_DEFAULT`|<span data-ttu-id="e7e56-108">기본 동작을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7e56-108">Indicates the default behavior.</span></span>|  
|`CLSID_RESOLUTION_REGISTERED`|<span data-ttu-id="e7e56-109">런타임 레지스트리를 검색 하 고 shim 정책 적용을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7e56-109">Indicates that the runtime searches the registry and applies shim policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e7e56-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e7e56-110">Requirements</span></span>  
 <span data-ttu-id="e7e56-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e7e56-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7e56-112">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e7e56-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e7e56-113">**.NET Framework 버전:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7e56-113">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7e56-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="e7e56-114">See also</span></span>
- [<span data-ttu-id="e7e56-115">호스팅 열거형</span><span class="sxs-lookup"><span data-stu-id="e7e56-115">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
