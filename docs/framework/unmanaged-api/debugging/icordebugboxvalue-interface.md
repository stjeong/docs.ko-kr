---
title: ICorDebugBoxValue 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugBoxValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBoxValue
helpviewer_keywords:
- ICorDebugBoxValue interface [.NET Framework debugging]
ms.assetid: 3d3ae7e2-97d4-46de-a2c3-cb78f3490f9d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f7238574334b599c7922693c7e9a476a51785491
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56967331"
---
# <a name="icordebugboxvalue-interface"></a><span data-ttu-id="7df98-102">ICorDebugBoxValue 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7df98-102">ICorDebugBoxValue Interface</span></span>

<span data-ttu-id="7df98-103">Boxed 값 클래스 개체를 나타내는 "ICorDebugHeapValue"의 하위 클래스.</span><span class="sxs-lookup"><span data-stu-id="7df98-103">A subclass of "ICorDebugHeapValue" that represents a boxed value class object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7df98-104">메서드</span><span class="sxs-lookup"><span data-stu-id="7df98-104">Methods</span></span>  
  
|<span data-ttu-id="7df98-105">메서드</span><span class="sxs-lookup"><span data-stu-id="7df98-105">Method</span></span>|<span data-ttu-id="7df98-106">설명</span><span class="sxs-lookup"><span data-stu-id="7df98-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7df98-107">GetObject 메서드</span><span class="sxs-lookup"><span data-stu-id="7df98-107">GetObject Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugboxvalue-getobject-method.md)|<span data-ttu-id="7df98-108">Boxed "ICorDebugObjectValue" 인스턴스에 대 한 인터페이스 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7df98-108">Gets an interface pointer to the boxed "ICorDebugObjectValue" instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7df98-109">설명</span><span class="sxs-lookup"><span data-stu-id="7df98-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7df98-110">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7df98-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7df98-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7df98-111">Requirements</span></span>  
 <span data-ttu-id="7df98-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="7df98-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7df98-113">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7df98-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7df98-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7df98-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7df98-115">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7df98-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7df98-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="7df98-116">See also</span></span>
- [<span data-ttu-id="7df98-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7df98-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
