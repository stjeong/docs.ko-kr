---
title: ICorProfilerCallback2::FinalizeableObjectQueued 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.FinalizeableObjectQueued
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::FinalizeableObjectQueued
helpviewer_keywords:
- FinalizeableObjectQueued method [.NET Framework profiling]
- ICorProfilerCallback2::FinalizeableObjectQueued method [.NET Framework profiling]
ms.assetid: 92d76893-683c-475d-9996-5bff03cdb10f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9b8a952bb2827d1946787f15151887fa25b8da52
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733729"
---
# <a name="icorprofilercallback2finalizeableobjectqueued-method"></a><span data-ttu-id="2d33c-102">ICorProfilerCallback2::FinalizeableObjectQueued 메서드</span><span class="sxs-lookup"><span data-stu-id="2d33c-102">ICorProfilerCallback2::FinalizeableObjectQueued Method</span></span>
<span data-ttu-id="2d33c-103">실행에 대 한 종료자 스레드에 개체 종료자를 사용 하 여 큐에 대기 되었습니다는 코드 프로파일러에 알립니다. 해당 `Finalize` 메서드.</span><span class="sxs-lookup"><span data-stu-id="2d33c-103">Notifies the code profiler that an object with a finalizer has been queued to the finalizer thread for execution of its `Finalize` method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d33c-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d33c-104">Syntax</span></span>  
  
```  
HRESULT FinalizeableObjectQueued(  
    [in] DWORD finalizerFlags,  
    [in] ObjectID objectID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2d33c-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2d33c-105">Parameters</span></span>  
 `finalizerFlags`  
 <span data-ttu-id="2d33c-106">[in] 값을 [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) 종료자의 측면을 설명 하는 열거형입니다.</span><span class="sxs-lookup"><span data-stu-id="2d33c-106">[in] A value of the [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) enumeration that describes aspects of the finalizer.</span></span>  
  
 `objectID`  
 <span data-ttu-id="2d33c-107">[in] 큐에 대기 하는 개체의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2d33c-107">[in] The ID of the object that has been queued.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d33c-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2d33c-108">Requirements</span></span>  
 <span data-ttu-id="2d33c-109">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="2d33c-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d33c-110">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2d33c-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2d33c-111">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d33c-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d33c-112">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d33c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d33c-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="2d33c-113">See also</span></span>
- [<span data-ttu-id="2d33c-114">ICorProfilerCallback 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2d33c-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="2d33c-115">ICorProfilerCallback2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2d33c-115">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
