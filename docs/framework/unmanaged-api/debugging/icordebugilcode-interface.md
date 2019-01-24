---
title: ICorDebugILCode 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugILCode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 51c4de0c-3813-4142-be25-a85bb84efb90
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b13968e999fb737c954fc41ed2ec220e7894b73b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634093"
---
# <a name="icordebugilcode-interface"></a><span data-ttu-id="094bc-102">ICorDebugILCode 인터페이스</span><span class="sxs-lookup"><span data-stu-id="094bc-102">ICorDebugILCode Interface</span></span>
<span data-ttu-id="094bc-103">[.NET Framework 4.5.2 이상 버전에서 지원됨]</span><span class="sxs-lookup"><span data-stu-id="094bc-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="094bc-104">IL(중간 언어) 코드 세그먼트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="094bc-104">Represents a segment of intermediate language (IL) code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="094bc-105">메서드</span><span class="sxs-lookup"><span data-stu-id="094bc-105">Methods</span></span>  
  
|<span data-ttu-id="094bc-106">메서드</span><span class="sxs-lookup"><span data-stu-id="094bc-106">Method</span></span>|<span data-ttu-id="094bc-107">설명</span><span class="sxs-lookup"><span data-stu-id="094bc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="094bc-108">GetEHClauses 메서드</span><span class="sxs-lookup"><span data-stu-id="094bc-108">GetEHClauses Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-getehclauses-method.md)|<span data-ttu-id="094bc-109">이 IL에 대해 정의된 EH(예외 처리) 절 목록에 대한 포인터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="094bc-109">Returns a pointer to a list of exception handling (EH) clauses that are defined for this IL.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="094bc-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="094bc-110">Requirements</span></span>  
 <span data-ttu-id="094bc-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="094bc-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="094bc-112">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="094bc-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="094bc-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="094bc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="094bc-114">**.NET Framework 버전:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="094bc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="094bc-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="094bc-115">See also</span></span>
- [<span data-ttu-id="094bc-116">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="094bc-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="094bc-117">디버깅</span><span class="sxs-lookup"><span data-stu-id="094bc-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
