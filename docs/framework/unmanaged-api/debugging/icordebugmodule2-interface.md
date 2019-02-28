---
title: ICorDebugModule2 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugModule2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2
helpviewer_keywords:
- ICorDebugModule2 interface [.NET Framework debugging]
ms.assetid: 0847e64f-fdbe-4c96-8168-da20fdc84d80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 192f2476aff91d3a8302d070852ab2a3722d137c
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56970131"
---
# <a name="icordebugmodule2-interface"></a><span data-ttu-id="1e31e-102">ICorDebugModule2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="1e31e-102">ICorDebugModule2 Interface</span></span>

<span data-ttu-id="1e31e-103">ICorDebugModule 인터페이스를 논리적으로 확장으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-103">Serves as a logical extension to the ICorDebugModule interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1e31e-104">메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-104">Methods</span></span>  
  
|<span data-ttu-id="1e31e-105">메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-105">Method</span></span>|<span data-ttu-id="1e31e-106">설명</span><span class="sxs-lookup"><span data-stu-id="1e31e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1e31e-107">ApplyChanges 메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-107">ApplyChanges Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md)|<span data-ttu-id="1e31e-108">실행 중인 프로세스에 메타 데이터의 변경 내용 및 Microsoft의 MSIL (intermediate language) 코드의 변경 내용을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-108">Applies the changes in the metadata and the changes in the Microsoft intermediate language (MSIL) code to the running process.</span></span>|  
|[<span data-ttu-id="1e31e-109">GetJITCompilerFlags 메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-109">GetJITCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-getjitcompilerflags-method.md)|<span data-ttu-id="1e31e-110">이 시간 (JIT) 컴파일을 제어 하는 플래그를 가져옵니다 `ICorDebugModule2`합니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-110">Gets the flags that control the just-in-time (JIT) compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="1e31e-111">ResolveAssembly 메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-111">ResolveAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-resolveassembly-method.md)|<span data-ttu-id="1e31e-112">지정 된 메타 데이터 토큰이 참조 되는 어셈블리를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-112">Resolves the assembly referenced by the specified metadata token.</span></span>|  
|[<span data-ttu-id="1e31e-113">SetJITCompilerFlags 메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-113">SetJITCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjitcompilerflags-method.md)|<span data-ttu-id="1e31e-114">이 대 한 JIT 컴파일을 제어 하는 플래그를 설정 `ICorDebugModule2`합니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-114">Sets the flags that control the JIT compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="1e31e-115">SetJMCStatus 메서드</span><span class="sxs-lookup"><span data-stu-id="1e31e-115">SetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjmcstatus-method.md)|<span data-ttu-id="1e31e-116">이 모든 클래스의 모든 메서드의 코드 JMC (내) 상태를 설정 `ICorDebugModule2` 제외한 지정 된 값을 `pTokens` 반대 값으로 설정 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-116">Sets the Just My Code (JMC) status of all methods of all the classes in this `ICorDebugModule2` to the specified value, except those in the `pTokens` array, which it sets to the opposite value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1e31e-117">설명</span><span class="sxs-lookup"><span data-stu-id="1e31e-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1e31e-118">이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e31e-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e31e-119">요구 사항</span><span class="sxs-lookup"><span data-stu-id="1e31e-119">Requirements</span></span>  
 <span data-ttu-id="1e31e-120">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e31e-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e31e-121">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1e31e-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1e31e-122">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1e31e-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1e31e-123">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e31e-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e31e-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="1e31e-124">See also</span></span>
- [<span data-ttu-id="1e31e-125">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="1e31e-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
