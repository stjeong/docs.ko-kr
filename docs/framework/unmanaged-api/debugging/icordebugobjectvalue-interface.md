---
title: ICorDebugObjectValue Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue
helpviewer_keywords:
- ICorDebugObjectValue interface [.NET Framework debugging]
ms.assetid: 937de6a0-6fbf-4ddc-80ea-a6217b73e62b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5cd991049c159b96a0f0717b31d6a2834b250f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631993"
---
# <a name="icordebugobjectvalue-interface1"></a><span data-ttu-id="79f3d-102">ICorDebugObjectValue Interface1</span><span class="sxs-lookup"><span data-stu-id="79f3d-102">ICorDebugObjectValue Interface1</span></span>
<span data-ttu-id="79f3d-103">개체를 포함 하는 값을 나타내는 "ICorDebugValue"의 하위 클래스.</span><span class="sxs-lookup"><span data-stu-id="79f3d-103">A subclass of "ICorDebugValue" that represents a value that contains an object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="79f3d-104">메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-104">Methods</span></span>  
  
|<span data-ttu-id="79f3d-105">메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-105">Method</span></span>|<span data-ttu-id="79f3d-106">설명</span><span class="sxs-lookup"><span data-stu-id="79f3d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="79f3d-107">GetClass 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-107">GetClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md)|<span data-ttu-id="79f3d-108">CLR (공용 언어 런타임)에 인터페이스 포인터를 가져옵니다 <xref:System.Type> 개체의이 `ICorDebugObjectValue` 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-108">Gets an interface pointer to the common language runtime (CLR) <xref:System.Type> of the object that this `ICorDebugObjectValue` references.</span></span>|  
|[<span data-ttu-id="79f3d-109">GetContext 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-109">GetContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getcontext-method.md)|<span data-ttu-id="79f3d-110">구현되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-110">Not implemented.</span></span>|  
|[<span data-ttu-id="79f3d-111">GetFieldValue 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-111">GetFieldValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getfieldvalue-method.md)|<span data-ttu-id="79f3d-112">한 인터페이스 포인터를 가져옵니다는 [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-interface.md) 지정된 된 클래스의 지정된 된 필드의 값을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-112">Gets an interface pointer to an [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-interface.md) that represents the value of the specified field of the specified class.</span></span>|  
|[<span data-ttu-id="79f3d-113">GetManagedCopy 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-113">GetManagedCopy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getmanagedcopy-method.md)|<span data-ttu-id="79f3d-114">사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-114">Obsolete.</span></span> <span data-ttu-id="79f3d-115">이 메서드를 호출 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="79f3d-115">Do not call this method.</span></span>|  
|[<span data-ttu-id="79f3d-116">GetVirtualMethod 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-116">GetVirtualMethod Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getvirtualmethod-method.md)|<span data-ttu-id="79f3d-117">구현되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-117">Not implemented.</span></span>|  
|[<span data-ttu-id="79f3d-118">IsValueClass 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-118">IsValueClass Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-isvalueclass-method.md)|<span data-ttu-id="79f3d-119">이 개체를 참조 하는지 여부를 나타내는 값을 가져옵니다 `ICorDebugObjectValue` 값 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-119">Gets a value that indicates whether the object referenced by this `ICorDebugObjectValue` is a value type.</span></span>|  
|[<span data-ttu-id="79f3d-120">SetFromManagedCopy 메서드</span><span class="sxs-lookup"><span data-stu-id="79f3d-120">SetFromManagedCopy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-setfrommanagedcopy-method.md)|<span data-ttu-id="79f3d-121">사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-121">Obsolete.</span></span> <span data-ttu-id="79f3d-122">이 메서드를 호출 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="79f3d-122">Do not call this method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="79f3d-123">설명</span><span class="sxs-lookup"><span data-stu-id="79f3d-123">Remarks</span></span>  
 <span data-ttu-id="79f3d-124">`ICorDebugObjectValue` 디버깅 중인 프로세스가 계속 될 때까지 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-124">An `ICorDebugObjectValue` remains valid until the process being debugged is continued.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="79f3d-125">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79f3d-125">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79f3d-126">요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f3d-126">Requirements</span></span>  
 <span data-ttu-id="79f3d-127">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="79f3d-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79f3d-128">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="79f3d-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="79f3d-129">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79f3d-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79f3d-130">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79f3d-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79f3d-131">참고자료</span><span class="sxs-lookup"><span data-stu-id="79f3d-131">See also</span></span>
- [<span data-ttu-id="79f3d-132">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="79f3d-132">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)

