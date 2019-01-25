---
title: ICorDebugManagedCallback::ControlCTrap 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ControlCTrap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ControlCTrap
helpviewer_keywords:
- ICorDebugManagedCallback::ControlCTrap method [.NET Framework debugging]
- ControlCTrap method [.NET Framework debugging]
ms.assetid: 0500854e-2121-43d9-a028-64312da35258
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f13800bcecbf6e7bdc5fede4e11c2ea15ecdec93
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54603900"
---
# <a name="icordebugmanagedcallbackcontrolctrap-method"></a><span data-ttu-id="db2c8-102">ICorDebugManagedCallback::ControlCTrap 메서드</span><span class="sxs-lookup"><span data-stu-id="db2c8-102">ICorDebugManagedCallback::ControlCTrap Method</span></span>
<span data-ttu-id="db2c8-103">CTRL + C는 디버깅 중인 프로세스에서 포착 되는 디버거에 알립니다.</span><span class="sxs-lookup"><span data-stu-id="db2c8-103">Notifies the debugger that a CTRL+C is trapped in the process that is being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db2c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="db2c8-104">Syntax</span></span>  
  
```  
HRESULT ControlCTrap (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="db2c8-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="db2c8-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="db2c8-106">[in] CTRL + C를 트래핑 하는 프로세스를 나타내는 ICorDebugProcess 개체에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="db2c8-106">[in] A pointer to an ICorDebugProcess object that represents the process in which the CTRL+C is trapped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="db2c8-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="db2c8-107">Return Value</span></span>  
  
|<span data-ttu-id="db2c8-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="db2c8-108">HRESULT</span></span>|<span data-ttu-id="db2c8-109">설명</span><span class="sxs-lookup"><span data-stu-id="db2c8-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="db2c8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="db2c8-110">S_OK</span></span>|<span data-ttu-id="db2c8-111">디버거는 CTRL + C 트랩을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="db2c8-111">The debugger will handle the CTRL+C trap.</span></span>|  
|<span data-ttu-id="db2c8-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="db2c8-112">S_FALSE</span></span>|<span data-ttu-id="db2c8-113">디버거는 CTRL + C 트랩을 처리 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db2c8-113">The debugger will not handle the CTRL+C trap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="db2c8-114">설명</span><span class="sxs-lookup"><span data-stu-id="db2c8-114">Remarks</span></span>  
 <span data-ttu-id="db2c8-115">이 콜백에 대 한 프로세스 내에서 모든 응용 프로그램 도메인 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db2c8-115">All application domains within the process are stopped for this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db2c8-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="db2c8-116">Requirements</span></span>  
 <span data-ttu-id="db2c8-117">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="db2c8-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db2c8-118">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db2c8-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db2c8-119">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db2c8-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db2c8-120">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db2c8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db2c8-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="db2c8-121">See also</span></span>
- [<span data-ttu-id="db2c8-122">ICorDebugManagedCallback 인터페이스</span><span class="sxs-lookup"><span data-stu-id="db2c8-122">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
