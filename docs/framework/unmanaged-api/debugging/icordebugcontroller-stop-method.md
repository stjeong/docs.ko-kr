---
title: ICorDebugController::Stop 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugController.Stop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Stop
helpviewer_keywords:
- Stop method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Stop method [.NET Framework debugging]
ms.assetid: c34e79be-a7fb-479e-8dec-d126a4c330e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4cb5b091aadbdd503dd7988f713f40a00876a2dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608324"
---
# <a name="icordebugcontrollerstop-method"></a><span data-ttu-id="bff29-102">ICorDebugController::Stop 메서드</span><span class="sxs-lookup"><span data-stu-id="bff29-102">ICorDebugController::Stop Method</span></span>
<span data-ttu-id="bff29-103">프로세스에서 관리 되는 코드를 실행 하는 모든 스레드에서 동시에 중지를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-103">Performs a cooperative stop on all threads that are running managed code in the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bff29-104">구문</span><span class="sxs-lookup"><span data-stu-id="bff29-104">Syntax</span></span>  
  
```  
HRESULT Stop (  
    [in] DWORD dwTimeoutIgnored  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bff29-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bff29-105">Parameters</span></span>  
 `dwTimeoutIgnored`  
 <span data-ttu-id="bff29-106">사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-106">Not used.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bff29-107">설명</span><span class="sxs-lookup"><span data-stu-id="bff29-107">Remarks</span></span>  
 <span data-ttu-id="bff29-108">`Stop` 프로세스에서 코드를 관리 되는 실행 중인 모든 스레드에서 협조적 중지를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-108">`Stop` performs a cooperative stop on all threads running managed code in the process.</span></span> <span data-ttu-id="bff29-109">관리 전용 디버깅 세션 중에 관리 되지 않는 스레드 계속 실행할 수 있습니다 (그러나 관리 코드를 호출 하려고 하면 차단 됩니다).</span><span class="sxs-lookup"><span data-stu-id="bff29-109">During a managed-only debugging session, unmanaged threads may continue to run (but will be blocked when trying to call managed code).</span></span> <span data-ttu-id="bff29-110">Interop 디버깅 세션 중 관리 되지 않는 스레드 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-110">During an interop debugging session, unmanaged threads will also be stopped.</span></span> <span data-ttu-id="bff29-111">`dwTimeoutIgnored` 값 현재 무시 되 고 무한 (-1)으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-111">The `dwTimeoutIgnored` value is currently ignored and treated as INFINITE (-1).</span></span> <span data-ttu-id="bff29-112">동시 중지 교착 상태로 인해 실패 하면 모든 스레드가 일시 중단 되 고 E_TIMEOUT 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-112">If the cooperative stop fails due to a deadlock, all threads are suspended and E_TIMEOUT is returned.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bff29-113">`Stop` 디버깅 API의 동기 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-113">`Stop` is the only synchronous method in the debugging API.</span></span> <span data-ttu-id="bff29-114">때 `Stop` 반환 하는 S_OK, 프로세스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-114">When `Stop` returns S_OK, the process is stopped.</span></span> <span data-ttu-id="bff29-115">콜백이 없는 정지의 수신기에 알리기 위해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-115">No callback is given to notify listeners of the stop.</span></span> <span data-ttu-id="bff29-116">디버거를 호출 해야 합니다 [icordebugcontroller:: Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) 프로세스를 다시 시작할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-116">The debugger must call [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) to allow the process to resume.</span></span>  
  
 <span data-ttu-id="bff29-117">디버거 중지 카운터를 유지 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-117">The debugger maintains a stop counter.</span></span> <span data-ttu-id="bff29-118">카운터가 0이 되 면 컨트롤러 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-118">When the counter goes to zero, the controller is resumed.</span></span> <span data-ttu-id="bff29-119">호출할 때마다 `Stop` 또는 디스패치 된 콜백을 카운터를 증가 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-119">Each call to `Stop` or each dispatched callback increments the counter.</span></span> <span data-ttu-id="bff29-120">호출할 때마다 `ICorDebugController::Continue` 감소 카운터입니다.</span><span class="sxs-lookup"><span data-stu-id="bff29-120">Each call to `ICorDebugController::Continue` decrements the counter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bff29-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="bff29-121">Requirements</span></span>  
 <span data-ttu-id="bff29-122">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="bff29-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bff29-123">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bff29-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bff29-124">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bff29-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bff29-125">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bff29-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bff29-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="bff29-126">See also</span></span>

