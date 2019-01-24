---
title: ICorProfilerCallback9::DynamicMethodUnloaded 메서드
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9.DynamicMethodUnloaded
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27e68c82a04b78a18f51f0a2c9ec712036521368
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513544"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a><span data-ttu-id="b6646-102">ICorProfilerCallback9::DynamicMethodUnloaded 메서드</span><span class="sxs-lookup"><span data-stu-id="b6646-102">ICorProfilerCallback9::DynamicMethodUnloaded Method</span></span>
<span data-ttu-id="b6646-103">[.NET Framework 4.7.2 이상 버전에서 지원 됨]</span><span class="sxs-lookup"><span data-stu-id="b6646-103">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  
  
<span data-ttu-id="b6646-104">동적 메서드는 가비지 수집 되 고 이후에 언로드될 때마다 프로파일러를 알립니다.</span><span class="sxs-lookup"><span data-stu-id="b6646-104">Notifies the profiler whenever a dynamic method is garbage collected and subsequently unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6646-105">구문</span><span class="sxs-lookup"><span data-stu-id="b6646-105">Syntax</span></span>  
  
```  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b6646-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6646-106">Parameters</span></span>  
<span data-ttu-id="b6646-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="b6646-107">[in] `functionId`</span></span>  
<span data-ttu-id="b6646-108">가비지 수집 되 고 언로드된 된 메모리 내 함수의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b6646-108">The identifier of the in-memory function that has been garbage collected and unloaded.</span></span>   

## <a name="requirements"></a><span data-ttu-id="b6646-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b6646-109">Requirements</span></span>  
 <span data-ttu-id="b6646-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="b6646-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6646-111">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b6646-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b6646-112">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b6646-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b6646-113">**.NET Framework 버전:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="b6646-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6646-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="b6646-114">See also</span></span>
- [<span data-ttu-id="b6646-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted 메서드</span><span class="sxs-lookup"><span data-stu-id="b6646-115">ICorProfilerCallback8.DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="b6646-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished 메서드</span><span class="sxs-lookup"><span data-stu-id="b6646-116">ICorProfilerCallback8.DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
- [<span data-ttu-id="b6646-117">ICorProfilerCallback9 인터페이스</span><span class="sxs-lookup"><span data-stu-id="b6646-117">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="b6646-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span><span class="sxs-lookup"><span data-stu-id="b6646-118">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span></span>](cor-prf-high-monitor-enumeration.md)
