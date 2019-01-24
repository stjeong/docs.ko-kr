---
title: ICorDebugHeapValue3 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3
helpviewer_keywords:
- ICorDebugHeapValue3 interface [.NET Framework debugging]
ms.assetid: 9c421bb0-e647-4b2d-a986-f3d578cc7f20
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08a9bc8aa4aa70ad6b01c58abccd145ae43d8a52
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568295"
---
# <a name="icordebugheapvalue3-interface"></a><span data-ttu-id="8ea87-102">ICorDebugHeapValue3 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8ea87-102">ICorDebugHeapValue3 Interface</span></span>
<span data-ttu-id="8ea87-103">개체의 모니터 잠금 속성을 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea87-103">Exposes the monitor lock properties of objects.</span></span> <span data-ttu-id="8ea87-104">이 인터페이스는 ICorDebugHeapValue 및 ICorDebugHeapValue2 인터페이스를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea87-104">This interface extends the ICorDebugHeapValue and ICorDebugHeapValue2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8ea87-105">메서드</span><span class="sxs-lookup"><span data-stu-id="8ea87-105">Methods</span></span>  
  
|<span data-ttu-id="8ea87-106">메서드</span><span class="sxs-lookup"><span data-stu-id="8ea87-106">Method</span></span>|<span data-ttu-id="8ea87-107">설명</span><span class="sxs-lookup"><span data-stu-id="8ea87-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8ea87-108">GetThreadOwningMonitorLock 메서드</span><span class="sxs-lookup"><span data-stu-id="8ea87-108">GetThreadOwningMonitorLock Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue3-getthreadowningmonitorlock-method.md)|<span data-ttu-id="8ea87-109">이 개체의 모니터 잠금을 소유 하는 관리 되는 스레드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea87-109">Returns the managed thread that owns the monitor lock on this object.</span></span>|  
|[<span data-ttu-id="8ea87-110">GetMonitorEventWaitList 메서드</span><span class="sxs-lookup"><span data-stu-id="8ea87-110">GetMonitorEventWaitList Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue3-getmonitoreventwaitlist-method.md)|<span data-ttu-id="8ea87-111">모니터 잠금과 사용 하 여 연결 된 이벤트에 대 한 큐에 대기 중인 스레드는 정렬 된 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea87-111">Provides an ordered list of threads that are queued on the event that is associated with a monitor lock.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8ea87-112">설명</span><span class="sxs-lookup"><span data-stu-id="8ea87-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8ea87-113">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea87-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ea87-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8ea87-114">Requirements</span></span>  
 <span data-ttu-id="8ea87-115">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="8ea87-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ea87-116">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8ea87-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8ea87-117">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ea87-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ea87-118">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ea87-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ea87-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="8ea87-119">See also</span></span>
- [<span data-ttu-id="8ea87-120">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8ea87-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="8ea87-121">디버깅</span><span class="sxs-lookup"><span data-stu-id="8ea87-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
