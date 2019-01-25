---
title: ICorDebugInternalFrame Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame
helpviewer_keywords:
- ICorDebugInternalFrame interface [.NET Framework debugging]
ms.assetid: bb4772ca-0d54-4185-b738-7a6ffe9ea85a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1fab8221bd160a74bb44c3ed0721ad4620e93419
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692797"
---
# <a name="icordebuginternalframe-interface1"></a><span data-ttu-id="e6f8b-102">ICorDebugInternalFrame Interface1</span><span class="sxs-lookup"><span data-stu-id="e6f8b-102">ICorDebugInternalFrame Interface1</span></span>
<span data-ttu-id="e6f8b-103">스택에 런타임 내부 프레임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e6f8b-103">Represents a runtime-internal frame on the stack.</span></span> <span data-ttu-id="e6f8b-104">이 인터페이스는 ICorDebugFrame 인터페이스의 서브 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f8b-104">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e6f8b-105">메서드</span><span class="sxs-lookup"><span data-stu-id="e6f8b-105">Methods</span></span>  
  
|<span data-ttu-id="e6f8b-106">메서드</span><span class="sxs-lookup"><span data-stu-id="e6f8b-106">Method</span></span>|<span data-ttu-id="e6f8b-107">설명</span><span class="sxs-lookup"><span data-stu-id="e6f8b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e6f8b-108">GetFrameType 메서드</span><span class="sxs-lookup"><span data-stu-id="e6f8b-108">GetFrameType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe-getframetype-method.md)|<span data-ttu-id="e6f8b-109">이 내부 프레임의 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6f8b-109">Gets the type of this internal frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e6f8b-110">설명</span><span class="sxs-lookup"><span data-stu-id="e6f8b-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e6f8b-111">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6f8b-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6f8b-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e6f8b-112">Requirements</span></span>  
 <span data-ttu-id="e6f8b-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e6f8b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6f8b-114">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e6f8b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e6f8b-115">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6f8b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e6f8b-116">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6f8b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6f8b-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="e6f8b-117">See also</span></span>
- [<span data-ttu-id="e6f8b-118">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e6f8b-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
