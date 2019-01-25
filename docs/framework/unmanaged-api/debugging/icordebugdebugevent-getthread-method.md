---
title: ICorDebugDebugEvent::GetThread 메서드
ms.date: 03/30/2017
ms.assetid: 4f2e9a2c-8369-4a07-a881-ad5422626353
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51d674159b33cad1a77a82e39b9f11a38c98cbd3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687403"
---
# <a name="icordebugdebugeventgetthread-method"></a><span data-ttu-id="c8750-102">ICorDebugDebugEvent::GetThread 메서드</span><span class="sxs-lookup"><span data-stu-id="c8750-102">ICorDebugDebugEvent::GetThread Method</span></span>
<span data-ttu-id="c8750-103">이벤트가 발생한 스레드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c8750-103">Gets the thread on which the event occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8750-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8750-104">Syntax</span></span>  
  
```  
HRESULT GetThread(  
        [out]ICorDebugThread **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c8750-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8750-105">Parameters</span></span>  
 <span data-ttu-id="c8750-106">ppThread</span><span class="sxs-lookup"><span data-stu-id="c8750-106">ppThread</span></span>  
 <span data-ttu-id="c8750-107">[out] 이벤트가 발생 한 스레드를 나타내는 ICorDebugThread 개체의 주소에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="c8750-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread on which the event occurred.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c8750-108">설명</span><span class="sxs-lookup"><span data-stu-id="c8750-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c8750-109">이 메서드는 .NET 네이티브에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8750-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8750-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c8750-110">Requirements</span></span>  
 <span data-ttu-id="c8750-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="c8750-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8750-112">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c8750-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c8750-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c8750-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c8750-114">**.NET Framework 버전:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8750-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8750-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="c8750-115">See also</span></span>
- [<span data-ttu-id="c8750-116">ICorDebugDebugEvent 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c8750-116">ICorDebugDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)
- [<span data-ttu-id="c8750-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c8750-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
