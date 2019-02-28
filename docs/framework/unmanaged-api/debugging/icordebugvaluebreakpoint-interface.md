---
title: ICorDebugValueBreakpoint 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint
helpviewer_keywords:
- ICorDebugValueBreakpoint interface [.NET Framework debugging]
ms.assetid: c02338fe-da6c-467f-9567-70ebb387e901
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e4c291c12de9cb95416e12e1a5fca273c542df36
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966369"
---
# <a name="icordebugvaluebreakpoint-interface"></a><span data-ttu-id="53f15-102">ICorDebugValueBreakpoint 인터페이스</span><span class="sxs-lookup"><span data-stu-id="53f15-102">ICorDebugValueBreakpoint Interface</span></span>
<span data-ttu-id="53f15-103">특정 값에 액세스할 수 있도록 ICorDebugBreakpoint 인터페이스를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f15-103">Extends the ICorDebugBreakpoint interface to provide access to specific values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="53f15-104">메서드</span><span class="sxs-lookup"><span data-stu-id="53f15-104">Methods</span></span>  
  
|<span data-ttu-id="53f15-105">메서드</span><span class="sxs-lookup"><span data-stu-id="53f15-105">Method</span></span>|<span data-ttu-id="53f15-106">설명</span><span class="sxs-lookup"><span data-stu-id="53f15-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="53f15-107">GetValue 메서드</span><span class="sxs-lookup"><span data-stu-id="53f15-107">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvaluebreakpoint-getvalue-method.md)|<span data-ttu-id="53f15-108">중단점이 설정 된 개체의 값을 나타내는 ICorDebugValue 개체에 대 한 인터페이스 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53f15-108">Gets an interface pointer to an ICorDebugValue object that represents the value of the object upon which the breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="53f15-109">설명</span><span class="sxs-lookup"><span data-stu-id="53f15-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="53f15-110">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f15-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53f15-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="53f15-111">Requirements</span></span>  
 <span data-ttu-id="53f15-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="53f15-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53f15-113">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="53f15-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="53f15-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="53f15-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="53f15-115">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="53f15-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53f15-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="53f15-116">See also</span></span>
- [<span data-ttu-id="53f15-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="53f15-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
