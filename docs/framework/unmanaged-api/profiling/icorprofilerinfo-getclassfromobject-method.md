---
title: ICorProfilerInfo::GetClassFromObject 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassFromObject
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassFromObject
helpviewer_keywords:
- GetClassFromObject method [.NET Framework profiling]
- ICorProfilerInfo::GetClassFromObject method [.NET Framework profiling]
ms.assetid: b97493fb-713e-49d5-a73e-5688b2ad0700
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9031ae9b4870c182922baaa41883de4cddb469d2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676681"
---
# <a name="icorprofilerinfogetclassfromobject-method"></a><span data-ttu-id="e5297-102">ICorProfilerInfo::GetClassFromObject 메서드</span><span class="sxs-lookup"><span data-stu-id="e5297-102">ICorProfilerInfo::GetClassFromObject Method</span></span>
<span data-ttu-id="e5297-103">가져옵니다 합니다 `ClassID` 지정 된 개체의 해당 `ObjectID`합니다.</span><span class="sxs-lookup"><span data-stu-id="e5297-103">Gets the `ClassID` of an object, given its `ObjectID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5297-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5297-104">Syntax</span></span>  
  
```  
HRESULT GetClassFromObject(  
    [in]  ObjectID objectId,  
    [out] ClassID *pClassId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e5297-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5297-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="e5297-106">[in] 가져올 개체의 ID를 `ClassID`입니다.</span><span class="sxs-lookup"><span data-stu-id="e5297-106">[in] The ID of the object for which to get the `ClassID`.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="e5297-107">[out] 반환 된 포인터 `ClassID`합니다.</span><span class="sxs-lookup"><span data-stu-id="e5297-107">[out] A pointer to the returned `ClassID`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e5297-108">설명</span><span class="sxs-lookup"><span data-stu-id="e5297-108">Remarks</span></span>  
 <span data-ttu-id="e5297-109">Null `pClassId` 나타내는 `objectId` 형식이 언로드하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="e5297-109">A null `pClassId` indicates that `objectId` has a type that is unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5297-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e5297-110">Requirements</span></span>  
 <span data-ttu-id="e5297-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e5297-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5297-112">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e5297-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e5297-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5297-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5297-114">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5297-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5297-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="e5297-115">See also</span></span>
- [<span data-ttu-id="e5297-116">ICorProfilerInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e5297-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
