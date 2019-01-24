---
title: ICorDebugValueEnum::Next 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugValueEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueEnum::Next
helpviewer_keywords:
- ICorDebugValueEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugValueEnum interface [.NET Framework debugging]
ms.assetid: f5ef94dd-dfee-49d3-a398-b110f8906dd8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 020df45f7f18a029f8c098fcc4dea1c131da017c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706919"
---
# <a name="icordebugvalueenumnext-method"></a><span data-ttu-id="c0d98-102">ICorDebugValueEnum::Next 메서드</span><span class="sxs-lookup"><span data-stu-id="c0d98-102">ICorDebugValueEnum::Next Method</span></span>
<span data-ttu-id="c0d98-103">"ICorDebugValue" 인스턴스 수가 지정 된 현재 위치부터 시작 하는 열거형에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c0d98-103">Gets the specified number of "ICorDebugValue" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0d98-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0d98-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugValue *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c0d98-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0d98-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="c0d98-106">[in] 수가 `ICorDebugValue` 인스턴스를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d98-106">[in] The number of `ICorDebugValue` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="c0d98-107">[out] 각각 가리키는 포인터 배열을 `ICorDebugValue` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d98-107">[out] An array of pointers, each of which points to an `ICorDebugValue` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="c0d98-108">[out] 개수에 대 한 포인터 `ICorDebugValue` 실제로 반환 된 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="c0d98-108">[out] Pointer to the number of `ICorDebugValue` instances actually returned.</span></span> <span data-ttu-id="c0d98-109">이 값은 null 일 수 있으면 `celt` 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="c0d98-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0d98-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c0d98-110">Requirements</span></span>  
 <span data-ttu-id="c0d98-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="c0d98-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0d98-112">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c0d98-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c0d98-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c0d98-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c0d98-114">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0d98-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0d98-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="c0d98-115">See also</span></span>


