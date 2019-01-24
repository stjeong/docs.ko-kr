---
title: CorManifestResourceFlags 열거형
ms.date: 03/30/2017
api_name:
- CorManifestResourceFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorManifestResourceFlags
helpviewer_keywords:
- CorManifestResourceFlags enumeration [.NET Framework metadata]
ms.assetid: 1b0306b7-622b-4b57-8edc-3c713bb147ae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a3d3ef78da9dd639d0f9050a8b61d1e365cd8b42
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650251"
---
# <a name="cormanifestresourceflags-enumeration"></a><span data-ttu-id="80429-102">CorManifestResourceFlags 열거형</span><span class="sxs-lookup"><span data-stu-id="80429-102">CorManifestResourceFlags Enumeration</span></span>
<span data-ttu-id="80429-103">어셈블리 매니페스트에 인코딩된 리소스의 표시 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80429-103">Indicates the visibility of resources encoded in an assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80429-104">구문</span><span class="sxs-lookup"><span data-stu-id="80429-104">Syntax</span></span>  
  
```  
typedef enum CorManifestResourceFlags {  
  
    mrVisibilityMask        =   0x0007,  
    mrPublic                =   0x0001,  
    mrPrivate               =   0x0002  
  
} CorManifestResourceFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="80429-105">멤버</span><span class="sxs-lookup"><span data-stu-id="80429-105">Members</span></span>  
  
|<span data-ttu-id="80429-106">멤버</span><span class="sxs-lookup"><span data-stu-id="80429-106">Member</span></span>|<span data-ttu-id="80429-107">설명</span><span class="sxs-lookup"><span data-stu-id="80429-107">Description</span></span>|  
|------------|-----------------|  
|`mrVisibilityMask`|<span data-ttu-id="80429-108">예약됨.</span><span class="sxs-lookup"><span data-stu-id="80429-108">Reserved.</span></span>|  
|`mrPublic`|<span data-ttu-id="80429-109">리소스는 공용입니다.</span><span class="sxs-lookup"><span data-stu-id="80429-109">The resources are public.</span></span>|  
|`mrPrivate`|<span data-ttu-id="80429-110">리소스는 private입니다.</span><span class="sxs-lookup"><span data-stu-id="80429-110">The resources are private.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="80429-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="80429-111">Requirements</span></span>  
 <span data-ttu-id="80429-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="80429-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80429-113">**헤더:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="80429-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="80429-114">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80429-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80429-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="80429-115">See also</span></span>
- [<span data-ttu-id="80429-116">메타데이터 열거형</span><span class="sxs-lookup"><span data-stu-id="80429-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
