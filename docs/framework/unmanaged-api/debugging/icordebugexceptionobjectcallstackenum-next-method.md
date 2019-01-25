---
title: ICorDebugExceptionObjectCallStackEnum::Next 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectCallStackEnum::Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectCallStackEnum::Next
helpviewer_keywords:
- ICorDebugExceptionObjectCallStackEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugExceptionObjectCallStackEnum interface [.NET Framework debugging]
ms.assetid: 3328a2c0-1e48-4a54-802a-9b474cf82c21
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 998256d75e5a0efd368ff7eb60d0023c8db0e283
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531056"
---
# <a name="icordebugexceptionobjectcallstackenumnext-method"></a><span data-ttu-id="6d2bd-102">ICorDebugExceptionObjectCallStackEnum::Next 메서드</span><span class="sxs-lookup"><span data-stu-id="6d2bd-102">ICorDebugExceptionObjectCallStackEnum::Next Method</span></span>
<span data-ttu-id="6d2bd-103">지정 된 개수를 가져옵니다 [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) 예외 개체의 호출 스택 정보가 포함 된 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-103">Gets the specified number of [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) instances that contain information from an exception object's call stack.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d2bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d2bd-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)] CorDebugExceptionObjectStackFrame values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6d2bd-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d2bd-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="6d2bd-106">[in] 수가 [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) 인스턴스를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-106">[in] The number of [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="6d2bd-107">[out] 각각 가리키는 포인터 배열을 [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-107">[out] An array of pointers, each of which points to a [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="6d2bd-108">[out] 개수에 대 한 포인터 [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) 실제로 반환 된 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-108">[out] A pointer to the number of [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) instances actually returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6d2bd-109">설명</span><span class="sxs-lookup"><span data-stu-id="6d2bd-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d2bd-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6d2bd-110">Requirements</span></span>  
 <span data-ttu-id="6d2bd-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6d2bd-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d2bd-112">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6d2bd-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6d2bd-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6d2bd-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6d2bd-114">**.NET Framework 버전:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6d2bd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d2bd-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="6d2bd-115">See also</span></span>
- [<span data-ttu-id="6d2bd-116">ICorDebugExceptionObjectCallStackEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6d2bd-116">ICorDebugExceptionObjectCallStackEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-interface.md)
- [<span data-ttu-id="6d2bd-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6d2bd-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
