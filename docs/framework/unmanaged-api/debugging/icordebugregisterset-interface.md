---
title: ICorDebugRegisterSet 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet
helpviewer_keywords:
- ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: d3d9676d-0b87-4bc3-b679-7bbc7a186c88
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8db70faf418bc89a4543845890f65e4859d507e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592603"
---
# <a name="icordebugregisterset-interface"></a><span data-ttu-id="8bd23-102">ICorDebugRegisterSet 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8bd23-102">ICorDebugRegisterSet Interface</span></span>
<span data-ttu-id="8bd23-103">현재 코드를 실행 하는 컴퓨터에서 사용할 수 있는 레지스터 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-103">Represents the set of registers available on the computer that is currently executing code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8bd23-104">메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-104">Methods</span></span>  
  
|<span data-ttu-id="8bd23-105">메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-105">Method</span></span>|<span data-ttu-id="8bd23-106">설명</span><span class="sxs-lookup"><span data-stu-id="8bd23-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8bd23-107">GetRegisters 메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-107">GetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregisters-method.md)|<span data-ttu-id="8bd23-108">(코드는 현재 실행 중인 컴퓨터)에서 각 레지스터의 값을 가져옵니다 비트 마스크에 의해 지정 된 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-108">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="8bd23-109">GetRegistersAvailable 메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-109">GetRegistersAvailable Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregistersavailable-method.md)|<span data-ttu-id="8bd23-110">비트 마스크를 가져옵니다가 등록을 나타내는 `ICorDebugRegisterSet` 현재 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-110">Gets a bit mask indicating which registers in this `ICorDebugRegisterSet` are currently available.</span></span>|  
|[<span data-ttu-id="8bd23-111">GetThreadContext 메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-111">GetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getthreadcontext-method.md)|<span data-ttu-id="8bd23-112">현재 스레드의 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-112">Gets the context of the current thread.</span></span>|  
|[<span data-ttu-id="8bd23-113">SetRegisters 메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-113">SetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-setregisters-method.md)|<span data-ttu-id="8bd23-114">.NET Framework 버전 2.0에 대 한 구현 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-114">Not implemented for the .NET Framework version 2.0.</span></span>|  
|[<span data-ttu-id="8bd23-115">SetThreadContext 메서드</span><span class="sxs-lookup"><span data-stu-id="8bd23-115">SetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-setthreadcontext-method.md)|<span data-ttu-id="8bd23-116">.NET Framework 2.0에 대 한 구현 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-116">Not implemented for the .NET Framework 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8bd23-117">설명</span><span class="sxs-lookup"><span data-stu-id="8bd23-117">Remarks</span></span>  
 <span data-ttu-id="8bd23-118">`ICorDebugRegisterSet` 인터페이스에서 32 비트 레지스터를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-118">The `ICorDebugRegisterSet` interface supports only 32-bit registers.</span></span> <span data-ttu-id="8bd23-119">사용 된 [ICorDebugRegisterSet2](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md) 추가 레지스터를 필요로 하는 IA-64와 같은 플랫폼에서 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-119">Use the [ICorDebugRegisterSet2](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md) interface on platforms such as IA-64 that require additional registers.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8bd23-120">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bd23-120">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8bd23-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8bd23-121">Requirements</span></span>  
 <span data-ttu-id="8bd23-122">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="8bd23-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8bd23-123">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8bd23-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8bd23-124">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8bd23-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8bd23-125">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8bd23-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8bd23-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="8bd23-126">See also</span></span>
- [<span data-ttu-id="8bd23-127">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8bd23-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="8bd23-128">ICorDebugRegisterSet2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8bd23-128">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
