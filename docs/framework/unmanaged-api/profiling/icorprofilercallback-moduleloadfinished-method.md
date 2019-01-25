---
title: ICorProfilerCallback::ModuleLoadFinished 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadFinished
helpviewer_keywords:
- ModuleLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadFinished method [.NET Framework profiling]
ms.assetid: 050649e5-ffc0-4458-a0a4-d9ee128a219e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d15656079c087026a905d9268edf4966d8ef4034
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54503562"
---
# <a name="icorprofilercallbackmoduleloadfinished-method"></a><span data-ttu-id="b592b-102">ICorProfilerCallback::ModuleLoadFinished 메서드</span><span class="sxs-lookup"><span data-stu-id="b592b-102">ICorProfilerCallback::ModuleLoadFinished Method</span></span>
<span data-ttu-id="b592b-103">모듈 로드 되었음을 프로파일러에 알립니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-103">Notifies the profiler that a module has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b592b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b592b-104">Syntax</span></span>  
  
```  
HRESULT ModuleLoadFinished(  
    [in] ModuleID moduleId,  
    [in] HRESULT  hrStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b592b-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b592b-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="b592b-106">[in] 로드가 완료 되는 모듈의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-106">[in] The ID of the module that has finished loading.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="b592b-107">[in] 모듈을 성공적으로 로드 되었는지 여부를 나타내는 HRESULT입니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-107">[in] An HRESULT that indicates whether the module was loaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b592b-108">설명</span><span class="sxs-lookup"><span data-stu-id="b592b-108">Remarks</span></span>  
 <span data-ttu-id="b592b-109">값 `moduleId` 될 때까지 정보 요청에 적합 하지 않습니다는 `ModuleLoadFinished` 메서드가 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-109">The value of `moduleId` is not valid for an information request until the `ModuleLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="b592b-110">일부 모듈 로드 후 계속 사용할 수는 `ModuleLoadFinished` 콜백 합니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-110">Some parts of loading the module might continue after the `ModuleLoadFinished` callback.</span></span> <span data-ttu-id="b592b-111">오류 HRESULT에서 `hrStatus` 오류가 발생 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="b592b-112">그러나 성공 HRESULT에서 `hrStatus` 모듈 로드에 대 한 첫 번째 부분 성공 했다는 것만 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b592b-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the module has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b592b-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b592b-113">Requirements</span></span>  
 <span data-ttu-id="b592b-114">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b592b-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b592b-115">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b592b-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b592b-116">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b592b-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b592b-117">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b592b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b592b-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="b592b-118">See also</span></span>
- [<span data-ttu-id="b592b-119">ICorProfilerCallback 인터페이스</span><span class="sxs-lookup"><span data-stu-id="b592b-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="b592b-120">ModuleLoadStarted 메서드</span><span class="sxs-lookup"><span data-stu-id="b592b-120">ModuleLoadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadstarted-method.md)
