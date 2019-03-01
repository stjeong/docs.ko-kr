---
title: ICorDebugChain 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain
helpviewer_keywords:
- ICorDebugChain interface [.NET Framework debugging]
ms.assetid: f671f519-1cb3-4ae5-b9f1-abc5e783459f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eb21712066e7b351e974a66f61ec0326a110aed6
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56982039"
---
# <a name="icordebugchain-interface"></a><span data-ttu-id="f530a-102">ICorDebugChain 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f530a-102">ICorDebugChain Interface</span></span>

<span data-ttu-id="f530a-103">실제 또는 논리 호출 스택의 세그먼트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-103">Represents a segment of a physical or logical call stack.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f530a-104">메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-104">Methods</span></span>  
  
|<span data-ttu-id="f530a-105">메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-105">Method</span></span>|<span data-ttu-id="f530a-106">설명</span><span class="sxs-lookup"><span data-stu-id="f530a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f530a-107">EnumerateFrames 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-107">EnumerateFrames Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-enumerateframes-method.md)|<span data-ttu-id="f530a-108">가장 최근의 프레임부터 체인의 모든 관리 되는 스택 프레임을 포함 하는 열거자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-108">Gets an enumerator that contains all the managed stack frames in the chain, starting with the most recent frame.</span></span>|  
|[<span data-ttu-id="f530a-109">GetActiveFrame 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-109">GetActiveFrame Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getactiveframe-method.md)|<span data-ttu-id="f530a-110">활성 가져옵니다 (즉, 가장 최근) 체인에서 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-110">Gets the active (that is, most recent) frame on the chain.</span></span>|  
|[<span data-ttu-id="f530a-111">GetCallee 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-111">GetCallee Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcallee-method.md)|<span data-ttu-id="f530a-112">이 체인에 의해 호출 된 체인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-112">Gets the chain that was called by this chain.</span></span>|  
|[<span data-ttu-id="f530a-113">GetCaller 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-113">GetCaller Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcaller-method.md)|<span data-ttu-id="f530a-114">이 체인 호출 체인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-114">Gets the chain that called this chain.</span></span>|  
|[<span data-ttu-id="f530a-115">GetContext 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-115">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcontext-method.md)|<span data-ttu-id="f530a-116">구현되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-116">Not implemented.</span></span>|  
|[<span data-ttu-id="f530a-117">GetNext 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-117">GetNext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getnext-method.md)|<span data-ttu-id="f530a-118">스레드에 대 한 다음 프레임 체인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-118">Gets the next chain of frames for the thread.</span></span>|  
|[<span data-ttu-id="f530a-119">GetPrevious 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-119">GetPrevious Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getprevious-method.md)|<span data-ttu-id="f530a-120">스레드에 대 한 이전 프레임 체인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-120">Gets the previous chain of frames for the thread.</span></span>|  
|[<span data-ttu-id="f530a-121">GetReason 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-121">GetReason Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getreason-method.md)|<span data-ttu-id="f530a-122">이 호출 체인의 발생 한 이유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-122">Gets the reason for the genesis of this calling chain.</span></span>|  
|[<span data-ttu-id="f530a-123">GetRegisterSet 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-123">GetRegisterSet Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getregisterset-method.md)|<span data-ttu-id="f530a-124">이 체인의 활성 부분에 대해 설정 하는 레지스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-124">Gets the register set for the active part of this chain.</span></span>|  
|[<span data-ttu-id="f530a-125">GetStackRange 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-125">GetStackRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getstackrange-method.md)|<span data-ttu-id="f530a-126">이 체인에 대 한 스택 세그먼트의 주소 범위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-126">Gets the address range of the stack segment for this chain.</span></span>|  
|[<span data-ttu-id="f530a-127">GetThread 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-127">GetThread Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getthread-method.md)|<span data-ttu-id="f530a-128">이 호출 체인은 실제 스레드에서의 부분을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-128">Gets the physical thread this call chain is part of.</span></span>|  
|[<span data-ttu-id="f530a-129">IsManaged 메서드</span><span class="sxs-lookup"><span data-stu-id="f530a-129">IsManaged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-ismanaged-method.md)|<span data-ttu-id="f530a-130">이 체인 관리 코드를 실행 중인지 여부를 나타내는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-130">Gets a value that indicates whether this chain is running managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f530a-131">설명</span><span class="sxs-lookup"><span data-stu-id="f530a-131">Remarks</span></span>  
 <span data-ttu-id="f530a-132">체인의 스택 프레임을 인접 한 스택 공간을 차지 하 고 동일한 스레드 및 컨텍스트를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-132">The stack frames in a chain occupy contiguous stack space and share the same thread and context.</span></span> <span data-ttu-id="f530a-133">체인을 관리 또는 비관리 코드 체인 중 하나를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-133">A chain may represent either managed or unmanaged code chains.</span></span> <span data-ttu-id="f530a-134">빈 `ICorDebugChain` 인스턴스는 관리 되지 않는 코드 체인을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-134">An empty `ICorDebugChain` instance represents an unmanaged code chain.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f530a-135">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f530a-135">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f530a-136">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f530a-136">Requirements</span></span>  
 <span data-ttu-id="f530a-137">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f530a-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f530a-138">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f530a-138">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f530a-139">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f530a-139">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f530a-140">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f530a-140">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f530a-141">참고자료</span><span class="sxs-lookup"><span data-stu-id="f530a-141">See also</span></span>
- [<span data-ttu-id="f530a-142">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f530a-142">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
