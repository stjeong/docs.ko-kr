---
title: COR_VERSION 구조체
ms.date: 03/30/2017
api_name:
- COR_VERSION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_VERSION
helpviewer_keywords:
- COR_VERSION structure [.NET Framework debugging]
ms.assetid: 5efaee1c-a001-4c73-9525-4160f4c71567
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e07487f536454d9d2dcfff15eb871124112d250e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634963"
---
# <a name="corversion-structure"></a><span data-ttu-id="0f806-102">COR_VERSION 구조체</span><span class="sxs-lookup"><span data-stu-id="0f806-102">COR_VERSION Structure</span></span>
<span data-ttu-id="0f806-103">공용 언어 런타임의 4부분으로 구성된 표준 버전 번호를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0f806-103">Stores the standard four-part version number of the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f806-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f806-104">Syntax</span></span>  
  
```  
typedef struct _COR_VERSION {  
    DWORD dwMajor;  
    DWORD dwMinor;  
    DWORD dwBuild;  
    DWORD dwSubBuild;  
} COR_VERSION;  
```  
  
## <a name="members"></a><span data-ttu-id="0f806-105">멤버</span><span class="sxs-lookup"><span data-stu-id="0f806-105">Members</span></span>  
  
|<span data-ttu-id="0f806-106">멤버</span><span class="sxs-lookup"><span data-stu-id="0f806-106">Member</span></span>|<span data-ttu-id="0f806-107">설명</span><span class="sxs-lookup"><span data-stu-id="0f806-107">Description</span></span>|  
|------------|-----------------|  
|`dwMajor`|<span data-ttu-id="0f806-108">주 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="0f806-108">The major version number.</span></span>|  
|`dwMinor`|<span data-ttu-id="0f806-109">부 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="0f806-109">The minor version number.</span></span>|  
|`dwBuild`|<span data-ttu-id="0f806-110">빌드 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="0f806-110">The build number.</span></span>|  
|`dwSubBuild`|<span data-ttu-id="0f806-111">하위 빌드 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="0f806-111">The sub-build number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0f806-112">설명</span><span class="sxs-lookup"><span data-stu-id="0f806-112">Remarks</span></span>  
 <span data-ttu-id="0f806-113">버전 번호를 1.0.3705.288 인 경우 1 주 버전 번호, 0은 부 버전 번호를, 3705 빌드 번호 이며 288 하위 빌드입니다.</span><span class="sxs-lookup"><span data-stu-id="0f806-113">If the version number is 1.0.3705.288, 1 is the major version number, 0 is the minor version number, 3705 is the build number, and 288 is the sub-build number.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f806-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="0f806-114">Requirements</span></span>  
 <span data-ttu-id="0f806-115">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="0f806-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f806-116">**헤더:** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="0f806-116">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="0f806-117">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f806-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f806-118">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f806-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f806-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="0f806-119">See also</span></span>
- [<span data-ttu-id="0f806-120">디버깅 구조체</span><span class="sxs-lookup"><span data-stu-id="0f806-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="0f806-121">디버깅</span><span class="sxs-lookup"><span data-stu-id="0f806-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
