---
title: COR_PRF_FINALIZER_FLAGS 열거형
ms.date: 03/30/2017
api_name:
- COR_PRF_FINALIZER_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FINALIZER_FLAGS
helpviewer_keywords:
- COR_PRF_FINALIZER_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 297d7721-3911-4f36-9e34-d9da0c33e22a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7800567f51196154f49c93dbbbe819f77cefdfe8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499040"
---
# <a name="corprffinalizerflags-enumeration"></a><span data-ttu-id="67cc5-102">COR_PRF_FINALIZER_FLAGS 열거형</span><span class="sxs-lookup"><span data-stu-id="67cc5-102">COR_PRF_FINALIZER_FLAGS Enumeration</span></span>
<span data-ttu-id="67cc5-103">개체에 대한 종료자를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="67cc5-103">Describes the finalizer for an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67cc5-104">구문</span><span class="sxs-lookup"><span data-stu-id="67cc5-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_FINALIZER_CRITICAL = 0x1  
} COR_PRF_FINALIZER_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="67cc5-105">멤버</span><span class="sxs-lookup"><span data-stu-id="67cc5-105">Members</span></span>  
  
|<span data-ttu-id="67cc5-106">멤버</span><span class="sxs-lookup"><span data-stu-id="67cc5-106">Member</span></span>|<span data-ttu-id="67cc5-107">설명</span><span class="sxs-lookup"><span data-stu-id="67cc5-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FINALIZER_CRITICAL`|<span data-ttu-id="67cc5-108">종료 자가 매우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="67cc5-108">The finalizer is critical.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="67cc5-109">설명</span><span class="sxs-lookup"><span data-stu-id="67cc5-109">Remarks</span></span>  
 <span data-ttu-id="67cc5-110">합니다 `COR_PRF_FINALIZER_FLAGS` 열거형에서 사용 되는 [ICorProfilerCallback2::FinalizeableObjectQueued](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-finalizeableobjectqueued-method.md) 개체에 대 한 종료자를 설명 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="67cc5-110">The `COR_PRF_FINALIZER_FLAGS` enumeration is used by the [ICorProfilerCallback2::FinalizeableObjectQueued](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-finalizeableobjectqueued-method.md) method to describe the finalizer for an object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67cc5-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="67cc5-111">Requirements</span></span>  
 <span data-ttu-id="67cc5-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="67cc5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67cc5-113">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="67cc5-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="67cc5-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="67cc5-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="67cc5-115">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67cc5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67cc5-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="67cc5-116">See also</span></span>
- [<span data-ttu-id="67cc5-117">프로파일링 열거형</span><span class="sxs-lookup"><span data-stu-id="67cc5-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
