---
title: ICorDebugStringValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue
helpviewer_keywords:
- ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: bf84d0af-53e1-4c04-bc5b-7e5f81ba2cc2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b9160b9013481de294e6c8dd032cfa2d0ebb405d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596841"
---
# <a name="icordebugstringvalue-interface1"></a><span data-ttu-id="ffe3e-102">ICorDebugStringValue Interface1</span><span class="sxs-lookup"><span data-stu-id="ffe3e-102">ICorDebugStringValue Interface1</span></span>
<span data-ttu-id="ffe3e-103">문자열 값에 적용 되는 ICorDebugHeapValue의 하위 클래스.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-103">A subclass of ICorDebugHeapValue that applies to string values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ffe3e-104">메서드</span><span class="sxs-lookup"><span data-stu-id="ffe3e-104">Methods</span></span>  
  
|<span data-ttu-id="ffe3e-105">메서드</span><span class="sxs-lookup"><span data-stu-id="ffe3e-105">Method</span></span>|<span data-ttu-id="ffe3e-106">설명</span><span class="sxs-lookup"><span data-stu-id="ffe3e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ffe3e-107">GetLength 메서드</span><span class="sxs-lookup"><span data-stu-id="ffe3e-107">GetLength Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getlength-method.md)|<span data-ttu-id="ffe3e-108">이 참조 하는 문자열의 문자 수를 가져옵니다 `ICorDebugStringValue`합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-108">Gets the number of characters in the string referenced by this `ICorDebugStringValue`.</span></span>|  
|[<span data-ttu-id="ffe3e-109">GetString 메서드</span><span class="sxs-lookup"><span data-stu-id="ffe3e-109">GetString Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getstring-method.md)|<span data-ttu-id="ffe3e-110">이 참조 하는 문자열을 가져옵니다 `ICorDebugStringValue`합니다.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-110">Gets the string referenced by this `ICorDebugStringValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ffe3e-111">설명</span><span class="sxs-lookup"><span data-stu-id="ffe3e-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ffe3e-112">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffe3e-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ffe3e-113">Requirements</span></span>  
 <span data-ttu-id="ffe3e-114">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ffe3e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffe3e-115">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ffe3e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ffe3e-116">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ffe3e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ffe3e-117">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffe3e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffe3e-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="ffe3e-118">See also</span></span>
- [<span data-ttu-id="ffe3e-119">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="ffe3e-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
