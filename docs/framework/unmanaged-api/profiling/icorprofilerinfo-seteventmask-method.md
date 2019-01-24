---
title: ICorProfilerInfo::SetEventMask 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetEventMask
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetEventMask
helpviewer_keywords:
- ICorProfilerInfo::SetEventMask method [.NET Framework profiling]
- SetEventMask method [.NET Framework profiling]
ms.assetid: 44bc0f56-32fa-491e-a62d-52fc96d48125
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 34aba20704ff8dc0d699ebee9440745d19c697b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566010"
---
# <a name="icorprofilerinfoseteventmask-method"></a><span data-ttu-id="22486-102">ICorProfilerInfo::SetEventMask 메서드</span><span class="sxs-lookup"><span data-stu-id="22486-102">ICorProfilerInfo::SetEventMask Method</span></span>
<span data-ttu-id="22486-103">프로파일러가 CLR(공용 언어 런타임)에서 알림을 받고 싶은 이벤트 형식을 지정하는 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="22486-103">Sets a value that specifies the types of events for which the profiler wants to receive notification from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22486-104">구문</span><span class="sxs-lookup"><span data-stu-id="22486-104">Syntax</span></span>  
  
```  
HRESULT SetEventMask(  
    [in] DWORD dwEvents);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="22486-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="22486-105">Parameters</span></span>  
 `dwEvents`  
 <span data-ttu-id="22486-106">[in] 이벤트 범주를 지정하는 4바이트 값입니다.</span><span class="sxs-lookup"><span data-stu-id="22486-106">[in] A 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="22486-107">각 비트는 서로 다른 기능, 동작 또는 이벤트 형식을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="22486-107">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="22486-108">설명 하는 비트를 [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) 열거형입니다.</span><span class="sxs-lookup"><span data-stu-id="22486-108">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="22486-109">설명</span><span class="sxs-lookup"><span data-stu-id="22486-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="22486-110">호출 해야 합니다 [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) 이 메서드 대신 메서드.</span><span class="sxs-lookup"><span data-stu-id="22486-110">You should call the [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method instead of this method.</span></span> <span data-ttu-id="22486-111">하지만 합니다 `SetEventMask` 메서드는 계속 지원 될 [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) 추가 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="22486-111">Although the `SetEventMask` method continues to be supported, [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) provides additional functionality.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22486-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="22486-112">Requirements</span></span>  
 <span data-ttu-id="22486-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="22486-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22486-114">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="22486-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="22486-115">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22486-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22486-116">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22486-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22486-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="22486-117">See also</span></span>
- [<span data-ttu-id="22486-118">ICorProfilerInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="22486-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="22486-119">SetEventMask2 메서드</span><span class="sxs-lookup"><span data-stu-id="22486-119">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
