---
title: ICorDebugAppDomain4 인터페이스
ms.date: 03/30/2017
ms.assetid: c536b9dc-148e-4924-bde1-1daa98d49d90
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 14f358de02f24a304cf0d5249b0f8916c7290b36
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590463"
---
# <a name="icordebugappdomain4-interface"></a><span data-ttu-id="905ba-102">ICorDebugAppDomain4 인터페이스</span><span class="sxs-lookup"><span data-stu-id="905ba-102">ICorDebugAppDomain4 Interface</span></span>
<span data-ttu-id="905ba-103">관리 되는 개체를 COM 호출 가능 래퍼를 활용 하려면 ICorDebugAppDomain 인터페이스를 논리적으로 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="905ba-103">Logically extends the ICorDebugAppDomain interface to get a managed object from a COM callable wrapper.</span></span>  
  
## <a name="method"></a><span data-ttu-id="905ba-104">메서드</span><span class="sxs-lookup"><span data-stu-id="905ba-104">Method</span></span>  
  
|<span data-ttu-id="905ba-105">메서드</span><span class="sxs-lookup"><span data-stu-id="905ba-105">Method</span></span>|<span data-ttu-id="905ba-106">설명</span><span class="sxs-lookup"><span data-stu-id="905ba-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="905ba-107">GetObjectForCCW 메서드</span><span class="sxs-lookup"><span data-stu-id="905ba-107">GetObjectForCCW Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain4-getobjectforccw-method.md)|<span data-ttu-id="905ba-108">CCW(COM 호출 가능 래퍼) 포인터에서 관리되는 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="905ba-108">Gets a managed object from a COM callable wrapper (CCW) pointer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="905ba-109">설명</span><span class="sxs-lookup"><span data-stu-id="905ba-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="905ba-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="905ba-110">Requirements</span></span>  
 <span data-ttu-id="905ba-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="905ba-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="905ba-112">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="905ba-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="905ba-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="905ba-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="905ba-114">**.NET Framework 버전:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="905ba-114">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="905ba-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="905ba-115">See also</span></span>
- [<span data-ttu-id="905ba-116">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="905ba-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="905ba-117">디버깅</span><span class="sxs-lookup"><span data-stu-id="905ba-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
