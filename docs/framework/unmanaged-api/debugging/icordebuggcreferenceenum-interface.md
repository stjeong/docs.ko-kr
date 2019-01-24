---
title: ICorDebugGCReferenceEnum 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugGCReferenceEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGCReferenceEnum
helpviewer_keywords:
- ICorDebugGCReferenceEnum interface [.NET Framework debugging]
ms.assetid: 5f3c91c9-c035-454f-96cc-011cab1ea06b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d228e548255cd70f34f6609aff613789f94fe5d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54507527"
---
# <a name="icordebuggcreferenceenum-interface"></a><span data-ttu-id="76a09-102">ICorDebugGCReferenceEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="76a09-102">ICorDebugGCReferenceEnum Interface</span></span>
<span data-ttu-id="76a09-103">가비지 수집되는 개체에 대한 열거자를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-103">Provides an enumerator for objects that will be garbage-collected.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="76a09-104">메서드</span><span class="sxs-lookup"><span data-stu-id="76a09-104">Methods</span></span>  
  
|<span data-ttu-id="76a09-105">메서드</span><span class="sxs-lookup"><span data-stu-id="76a09-105">Method</span></span>|<span data-ttu-id="76a09-106">설명</span><span class="sxs-lookup"><span data-stu-id="76a09-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="76a09-107">Next 메서드</span><span class="sxs-lookup"><span data-stu-id="76a09-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md)|<span data-ttu-id="76a09-108">지정 된 개수를 가져옵니다 [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) 가비지 수집 될 개체에 대 한 정보가 포함 된 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="76a09-108">Gets the specified number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="76a09-109">설명</span><span class="sxs-lookup"><span data-stu-id="76a09-109">Remarks</span></span>  
 <span data-ttu-id="76a09-110">`ICorDebugGCReferenceEnum` "ICorDebugEnum" 인터페이스를 구현 하는 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-110">The `ICorDebugGCReferenceEnum` interface implements the "ICorDebugEnum" interface.</span></span>  
  
 <span data-ttu-id="76a09-111">`ICorDebugGCReferenceEnum` 인스턴스 채워집니다 [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) 호출 하 여 인스턴스를 [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="76a09-111">An `ICorDebugGCReferenceEnum` instance is populated with [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances by calling the [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) method.</span></span> <span data-ttu-id="76a09-112">[COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) 개체를 호출 하 여 열거할 수는 [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="76a09-112">[COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects can be enumerated by calling the [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) method.</span></span>  
  
 <span data-ttu-id="76a09-113">합니다 [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) 이 메서드에서 입력 컬렉션에 개체 세 종류의 개체를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-113">The [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects in the collection populated by this method represent three kinds of objects:</span></span>  
  
-   <span data-ttu-id="76a09-114">모든 관리 되는 스택 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-114">Objects from all managed stacks.</span></span> <span data-ttu-id="76a09-115">공용 언어 런타임에서 생성 된 개체를 비롯 하 여 관리 코드에 대 한 라이브 참조가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-115">This includes live references in managed code as well as objects created by the common language runtime.</span></span>  
  
-   <span data-ttu-id="76a09-116">핸들 테이블의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-116">Objects from the handle table.</span></span> <span data-ttu-id="76a09-117">여기에 강력한 참조 (`HNDTYPE_STRONG` 및 `HNDTYPE_REFCOUNT`) 및 모듈의 정적 변수.</span><span class="sxs-lookup"><span data-stu-id="76a09-117">This includes strong references (`HNDTYPE_STRONG` and `HNDTYPE_REFCOUNT`) and static variables in a module.</span></span>  
  
-   <span data-ttu-id="76a09-118">종료자 큐의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-118">Objects from the finalizer queue.</span></span> <span data-ttu-id="76a09-119">종료자 큐는 종료 자가 실행 될 때까지 개체 루트입니다.</span><span class="sxs-lookup"><span data-stu-id="76a09-119">The finalizer queue roots objects until the finalizer has run.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76a09-120">요구 사항</span><span class="sxs-lookup"><span data-stu-id="76a09-120">Requirements</span></span>  
 <span data-ttu-id="76a09-121">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="76a09-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76a09-122">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="76a09-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="76a09-123">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="76a09-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="76a09-124">**.NET Framework 버전:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76a09-124">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76a09-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="76a09-125">See also</span></span>
- [<span data-ttu-id="76a09-126">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="76a09-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
