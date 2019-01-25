---
title: ICorDebugExceptionObjectCallStackEnum 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectCallStackEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectCallStackEnum
helpviewer_keywords:
- ICorDebugExceptionObjectCallStackEnum interface [.NET Framework debugging]
ms.assetid: 39dffa18-c71b-48c4-b11d-e814631ab1e9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 00b52f9f058853ba14fcfd1986366527de25a427
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680704"
---
# <a name="icordebugexceptionobjectcallstackenum-interface"></a><span data-ttu-id="fdd5c-102">ICorDebugExceptionObjectCallStackEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="fdd5c-102">ICorDebugExceptionObjectCallStackEnum Interface</span></span>
<span data-ttu-id="fdd5c-103">예외 개체에 포함된 호출 스택 정보에 대한 열거자를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd5c-103">Provides an enumerator for call stack information that is embedded in an exception object.</span></span> <span data-ttu-id="fdd5c-104">이 인터페이스는 ICorDebugEnum 인터페이스의 서브 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd5c-104">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fdd5c-105">메서드</span><span class="sxs-lookup"><span data-stu-id="fdd5c-105">Methods</span></span>  
  
|<span data-ttu-id="fdd5c-106">메서드</span><span class="sxs-lookup"><span data-stu-id="fdd5c-106">Method</span></span>|<span data-ttu-id="fdd5c-107">설명</span><span class="sxs-lookup"><span data-stu-id="fdd5c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fdd5c-108">ICorDebugExceptionObjectCallStackEnum::Next</span><span class="sxs-lookup"><span data-stu-id="fdd5c-108">ICorDebugExceptionObjectCallStackEnum::Next</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-next-method.md)|<span data-ttu-id="fdd5c-109">지정된 된 수를 가져옵니다 [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) 예외 개체의 호출 스택에 대 한 정보를 포함 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd5c-109">Gets a specified number of [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) objects that contain information about an exception object's call stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fdd5c-110">설명</span><span class="sxs-lookup"><span data-stu-id="fdd5c-110">Remarks</span></span>  
 <span data-ttu-id="fdd5c-111">`ICorDebugExceptionObjectCallStackEnum` ICorDebugEnum 인터페이스를 구현 하는 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd5c-111">The `ICorDebugExceptionObjectCallStackEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="fdd5c-112">`ICorDebugExceptionObjectCallStackEnum` 인스턴스 채워집니다 [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) 호출 하 여 개체를 [icordebugexceptionobjectvalue:: Enumerateexceptioncallstack](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="fdd5c-112">An `ICorDebugExceptionObjectCallStackEnum` instance is populated with [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) objects by calling the [ICorDebugExceptionObjectValue::EnumerateExceptionCallStack](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md) method.</span></span> <span data-ttu-id="fdd5c-113">호출 하 여 컬렉션의 호출 스택 항목을 열거할 수 있습니다 합니다 [icordebugexceptionobjectcallstackenum:: Next](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-next-method.md) 메서드</span><span class="sxs-lookup"><span data-stu-id="fdd5c-113">The call stack items in the collection can be enumerated by calling the [ICorDebugExceptionObjectCallStackEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-next-method.md) method</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fdd5c-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="fdd5c-114">Requirements</span></span>  
 <span data-ttu-id="fdd5c-115">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="fdd5c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fdd5c-116">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fdd5c-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fdd5c-117">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fdd5c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fdd5c-118">**.NET Framework 버전:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fdd5c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdd5c-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="fdd5c-119">See also</span></span>
- [<span data-ttu-id="fdd5c-120">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="fdd5c-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="fdd5c-121">디버깅</span><span class="sxs-lookup"><span data-stu-id="fdd5c-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
