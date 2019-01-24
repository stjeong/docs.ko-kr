---
title: ICorDebugExceptionDebugEvent 인터페이스
ms.date: 03/30/2017
ms.assetid: f9ba60d8-b54d-417e-bb3e-fde4b41ca44c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7d2407e56b029d22d25a4836f4def1c55f979ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550528"
---
# <a name="icordebugexceptiondebugevent-interface"></a><span data-ttu-id="8a6cf-102">ICorDebugExceptionDebugEvent 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8a6cf-102">ICorDebugExceptionDebugEvent Interface</span></span>
<span data-ttu-id="8a6cf-103">확장 된 [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) 예외 이벤트를 지 원하는 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-103">Extends the [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface to support exception events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8a6cf-104">메서드</span><span class="sxs-lookup"><span data-stu-id="8a6cf-104">Methods</span></span>  
  
|<span data-ttu-id="8a6cf-105">메서드</span><span class="sxs-lookup"><span data-stu-id="8a6cf-105">Method</span></span>|<span data-ttu-id="8a6cf-106">설명</span><span class="sxs-lookup"><span data-stu-id="8a6cf-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8a6cf-107">GetFlags 메서드</span><span class="sxs-lookup"><span data-stu-id="8a6cf-107">GetFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getflags-method.md)|<span data-ttu-id="8a6cf-108">예외를 가로챌 수 있는지 여부를 나타내는 플래그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-108">Gets a flag that indicates whether the exception is can be intercepted.</span></span>|  
|[<span data-ttu-id="8a6cf-109">GetNativeIP 메서드</span><span class="sxs-lookup"><span data-stu-id="8a6cf-109">GetNativeIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getnativeip-method.md)|<span data-ttu-id="8a6cf-110">이 예외 디버그 이벤트에 대한 네이티브 인터페이스 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-110">Gets the native interface pointer for this exception debug event.</span></span>|  
|[<span data-ttu-id="8a6cf-111">GetStackPointer 메서드</span><span class="sxs-lookup"><span data-stu-id="8a6cf-111">GetStackPointer Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getstackpointer-method.md)|<span data-ttu-id="8a6cf-112">이 예외 디버그 이벤트에 대한 스택 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-112">Gets the stack pointer for this exception debug event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a6cf-113">설명</span><span class="sxs-lookup"><span data-stu-id="8a6cf-113">Remarks</span></span>  
 <span data-ttu-id="8a6cf-114">`ICorDebugExceptionDebugEvent` 인터페이스는 다음 이벤트 유형을 통해 구현됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-114">The `ICorDebugExceptionDebugEvent` interface is implemented by the following event types:</span></span>  
  
-   [<span data-ttu-id="8a6cf-115">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="8a6cf-115">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="8a6cf-116">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="8a6cf-116">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="8a6cf-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="8a6cf-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="8a6cf-118">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="8a6cf-118">MANAGED_EXCEPTION_UNHANDLED</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
> [!NOTE]
>  <span data-ttu-id="8a6cf-119">이 인터페이스는 .NET 네이티브에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-119">The interface is available with .NET Native only.</span></span> <span data-ttu-id="8a6cf-120">.NET 네이티브 외부의 ICorDebug 시나리오에 대해 `QueryInterface`를 호출하여 인터페이스 포인터를 검색하려고 하면 `E_NOINTERFACE`가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-120">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a6cf-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8a6cf-121">Requirements</span></span>  
 <span data-ttu-id="8a6cf-122">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="8a6cf-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a6cf-123">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8a6cf-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8a6cf-124">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a6cf-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a6cf-125">**.NET Framework 버전:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a6cf-125">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a6cf-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="8a6cf-126">See also</span></span>
- [<span data-ttu-id="8a6cf-127">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8a6cf-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="8a6cf-128">디버깅</span><span class="sxs-lookup"><span data-stu-id="8a6cf-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
