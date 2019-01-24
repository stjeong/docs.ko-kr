---
title: ICorDebugController::IsRunning 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugController.IsRunning
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::IsRunning
helpviewer_keywords:
- IsRunning method [.NET Framework debugging]
- ICorDebugController::IsRunning method [.NET Framework debugging]
ms.assetid: b33ff059-40c4-4dfe-9cb2-21bfed2de0b0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd54792e37523ea5bf0c2e7a4082ee00c30d00ea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54496298"
---
# <a name="icordebugcontrollerisrunning-method"></a><span data-ttu-id="6517e-102">ICorDebugController::IsRunning 메서드</span><span class="sxs-lookup"><span data-stu-id="6517e-102">ICorDebugController::IsRunning Method</span></span>
<span data-ttu-id="6517e-103">프로세스의 스레드는 자유롭게 실행 현재 여부를 나타내는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6517e-103">Gets a value that indicates whether the threads in the process are currently running freely.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6517e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6517e-104">Syntax</span></span>  
  
```  
HRESULT IsRunning (  
    [out] BOOL *pbRunning  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6517e-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6517e-105">Parameters</span></span>  
 `pbRunning`  
 <span data-ttu-id="6517e-106">[out] 값에 대 한 포인터 `true` 자유롭게 그렇지 않은 경우 프로세스의 스레드가 실행 중인 경우 `false`합니다.</span><span class="sxs-lookup"><span data-stu-id="6517e-106">[out] A pointer to a value that is `true` if the threads in the process are running freely; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6517e-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6517e-107">Requirements</span></span>  
 <span data-ttu-id="6517e-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6517e-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6517e-109">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6517e-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6517e-110">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6517e-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6517e-111">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6517e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6517e-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="6517e-112">See also</span></span>

