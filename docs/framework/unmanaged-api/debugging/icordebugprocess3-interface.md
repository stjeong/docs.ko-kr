---
title: ICorDebugProcess3 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugProcess3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess3
helpviewer_keywords:
- ICorDebugProcess3 interface [.NET Framework debugging]
ms.assetid: ced9c82e-d7b0-4806-a151-98b6611d3097
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 75dc379baf8d92b9b27bdb58ccab930c2d4f91e9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709171"
---
# <a name="icordebugprocess3-interface"></a><span data-ttu-id="595a1-102">ICorDebugProcess3 인터페이스</span><span class="sxs-lookup"><span data-stu-id="595a1-102">ICorDebugProcess3 Interface</span></span>
<span data-ttu-id="595a1-103">사용자 지정 디버거 알림을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="595a1-103">Controls custom debugger notifications.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="595a1-104">메서드</span><span class="sxs-lookup"><span data-stu-id="595a1-104">Methods</span></span>  
  
|<span data-ttu-id="595a1-105">메서드</span><span class="sxs-lookup"><span data-stu-id="595a1-105">Method</span></span>|<span data-ttu-id="595a1-106">설명</span><span class="sxs-lookup"><span data-stu-id="595a1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="595a1-107">SetEnableCustomNotification 메서드</span><span class="sxs-lookup"><span data-stu-id="595a1-107">SetEnableCustomNotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-setenablecustomnotification-method.md)|<span data-ttu-id="595a1-108">사용 하도록 설정 하 고 지정 된 형식의 사용자 지정 디버거 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="595a1-108">Enables and disables custom debugger notifications of the specified type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="595a1-109">설명</span><span class="sxs-lookup"><span data-stu-id="595a1-109">Remarks</span></span>  
 <span data-ttu-id="595a1-110">이 인터페이스는 ICorDebugProcess 및 ICorDebugProcess2 인터페이스를 논리적으로 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="595a1-110">This interface logically extends the ICorDebugProcess and ICorDebugProcess2 interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="595a1-111">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="595a1-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="595a1-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="595a1-112">Requirements</span></span>  
 <span data-ttu-id="595a1-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="595a1-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="595a1-114">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="595a1-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="595a1-115">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="595a1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="595a1-116">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="595a1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="595a1-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="595a1-117">See also</span></span>
- [<span data-ttu-id="595a1-118">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="595a1-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="595a1-119">디버깅</span><span class="sxs-lookup"><span data-stu-id="595a1-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
