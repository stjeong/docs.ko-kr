---
title: ICorDebugModuleEnum 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugModuleEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleEnum
helpviewer_keywords:
- ICorDebugModuleEnum interface [.NET Framework debugging]
ms.assetid: 2fb93cd6-6d47-4fdc-a9a0-047726fd03a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6bf3d72b2439250fd8fbdc1bf1dc9ca28352c9ad
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976839"
---
# <a name="icordebugmoduleenum-interface"></a><span data-ttu-id="6b4c0-102">ICorDebugModuleEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6b4c0-102">ICorDebugModuleEnum Interface</span></span>

<span data-ttu-id="6b4c0-103">ICorDebugEnum 메서드를 구현 하 고 ICorDebugModule 배열을 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4c0-103">Implements ICorDebugEnum methods, and enumerates ICorDebugModule arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6b4c0-104">메서드</span><span class="sxs-lookup"><span data-stu-id="6b4c0-104">Methods</span></span>  
  
|<span data-ttu-id="6b4c0-105">메서드</span><span class="sxs-lookup"><span data-stu-id="6b4c0-105">Method</span></span>|<span data-ttu-id="6b4c0-106">설명</span><span class="sxs-lookup"><span data-stu-id="6b4c0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6b4c0-107">Next 메서드</span><span class="sxs-lookup"><span data-stu-id="6b4c0-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduleenum-next-method.md)|<span data-ttu-id="6b4c0-108">지정 된 수를 가져옵니다 `ICorDebugModule` 인스턴스는 열거형에서 현재 위치에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4c0-108">Gets the specified number of `ICorDebugModule` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6b4c0-109">설명</span><span class="sxs-lookup"><span data-stu-id="6b4c0-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6b4c0-110">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b4c0-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b4c0-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6b4c0-111">Requirements</span></span>  
 <span data-ttu-id="6b4c0-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6b4c0-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6b4c0-113">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6b4c0-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6b4c0-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6b4c0-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6b4c0-115">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6b4c0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b4c0-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="6b4c0-116">See also</span></span>
- [<span data-ttu-id="6b4c0-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6b4c0-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
