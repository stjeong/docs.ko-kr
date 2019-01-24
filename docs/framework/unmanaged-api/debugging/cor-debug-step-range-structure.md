---
title: COR_DEBUG_STEP_RANGE 구조체
ms.date: 03/30/2017
api_name:
- COR_DEBUG_STEP_RANGE
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_STEP_RANGE
helpviewer_keywords:
- COR_DEBUG_STEP_RANGE structure [.NET Framework debugging]
ms.assetid: 8809d00e-beaa-4dcf-b4e8-e89d0a5406b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 45340a26b3351ca03b453fbcdb626de199bd6d19
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710367"
---
# <a name="cordebugsteprange-structure"></a><span data-ttu-id="947ba-102">COR_DEBUG_STEP_RANGE 구조체</span><span class="sxs-lookup"><span data-stu-id="947ba-102">COR_DEBUG_STEP_RANGE Structure</span></span>
<span data-ttu-id="947ba-103">코드 범위에 대한 오프셋 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="947ba-103">Contains the offset information for a range of code.</span></span>  
  
 <span data-ttu-id="947ba-104">이 구조체를 사용 합니다 [icordebugstepper:: Steprange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="947ba-104">This structure is used by the [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="947ba-105">구문</span><span class="sxs-lookup"><span data-stu-id="947ba-105">Syntax</span></span>  
  
```  
typedef struct {  
    ULONG32 startOffset;  
    ULONG32 endOffset;  
} COR_DEBUG_STEP_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="947ba-106">멤버</span><span class="sxs-lookup"><span data-stu-id="947ba-106">Members</span></span>  
  
|<span data-ttu-id="947ba-107">멤버</span><span class="sxs-lookup"><span data-stu-id="947ba-107">Member</span></span>|<span data-ttu-id="947ba-108">설명</span><span class="sxs-lookup"><span data-stu-id="947ba-108">Description</span></span>|  
|------------|-----------------|  
|`startOffset`|<span data-ttu-id="947ba-109">범위의 시작 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="947ba-109">The offset of the beginning of the range.</span></span>|  
|`endOffset`|<span data-ttu-id="947ba-110">범위의 끝 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="947ba-110">The offset of the end of the range.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="947ba-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="947ba-111">Requirements</span></span>  
 <span data-ttu-id="947ba-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="947ba-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="947ba-113">**헤더:** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="947ba-113">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="947ba-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="947ba-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="947ba-115">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="947ba-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="947ba-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="947ba-116">See also</span></span>
- [<span data-ttu-id="947ba-117">StepRange 메서드</span><span class="sxs-lookup"><span data-stu-id="947ba-117">StepRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md)
- [<span data-ttu-id="947ba-118">디버깅 구조체</span><span class="sxs-lookup"><span data-stu-id="947ba-118">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="947ba-119">디버깅</span><span class="sxs-lookup"><span data-stu-id="947ba-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
