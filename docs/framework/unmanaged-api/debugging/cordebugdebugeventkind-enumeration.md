---
title: CorDebugDebugEventKind 열거형
ms.date: 03/30/2017
api_name:
- CorDebugDebugEventKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6075a6cd-97e6-4472-a090-0dd14860d1f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a45929c3eef5e9127e89dd88346c6207f3f1bc65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559494"
---
# <a name="cordebugdebugeventkind-enumeration"></a><span data-ttu-id="be316-102">CorDebugDebugEventKind 열거형</span><span class="sxs-lookup"><span data-stu-id="be316-102">CorDebugDebugEventKind Enumeration</span></span>
<span data-ttu-id="be316-103">정보를 가져올 디코딩되는 이벤트의 형식을 나타내는 합니다 [DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="be316-103">Indicates the type of event whose information is decoded by the [DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be316-104">구문</span><span class="sxs-lookup"><span data-stu-id="be316-104">Syntax</span></span>  
  
```  
typedef enum CorDebugDebugEventKind {  
    DEBUG_EVENT_KIND_MODULE_LOADED                          = 1,  
    DEBUG_EVENT_KIND_MODULE_UNLOADED                        = 2,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE         = 3,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE    = 4,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND  = 5,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED            = 6  
} CorDebugRecordFormat;  
```  
  
## <a name="members"></a><span data-ttu-id="be316-105">멤버</span><span class="sxs-lookup"><span data-stu-id="be316-105">Members</span></span>  
  
|<span data-ttu-id="be316-106">멤버</span><span class="sxs-lookup"><span data-stu-id="be316-106">Member</span></span>|<span data-ttu-id="be316-107">설명</span><span class="sxs-lookup"><span data-stu-id="be316-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EVENT_KIND_MODULE_LOADED`|<span data-ttu-id="be316-108">모듈 로드 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="be316-108">A module load event.</span></span>|  
|`DEBUG_EVENT_KIND_MODULE_UNLOADED`|<span data-ttu-id="be316-109">모듈 언로드 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="be316-109">A module unload event.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE`|<span data-ttu-id="be316-110">첫째 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="be316-110">A first-chance exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE`|<span data-ttu-id="be316-111">첫째 사용자 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="be316-111">A first-chance user exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND`|<span data-ttu-id="be316-112">`catch` 처리기가 있는 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="be316-112">An exception for which a `catch` handler exists.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED`|<span data-ttu-id="be316-113">처리되지 않은 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="be316-113">An unhandled exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be316-114">설명</span><span class="sxs-lookup"><span data-stu-id="be316-114">Remarks</span></span>  
 <span data-ttu-id="be316-115">멤버는 `CorDebugDebugEventKind` 열거형이 호출 하 여 반환 합니다 [icordebugdebugevent:: Geteventkind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="be316-115">A member of the `CorDebugDebugEventKind` enumeration is returned by calling the [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="be316-116">이 열거형은 .NET 네이티브 디버깅 시나리오에서만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="be316-116">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be316-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="be316-117">Requirements</span></span>  
 <span data-ttu-id="be316-118">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="be316-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be316-119">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="be316-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="be316-120">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="be316-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="be316-121">**.NET Framework 버전:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be316-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be316-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="be316-122">See also</span></span>
- [<span data-ttu-id="be316-123">디버깅 열거형</span><span class="sxs-lookup"><span data-stu-id="be316-123">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
