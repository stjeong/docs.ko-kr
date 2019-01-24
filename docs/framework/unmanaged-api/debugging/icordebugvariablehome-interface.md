---
title: ICorDebugVariableHome 인터페이스
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugVariableHome
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome
helpviewer_keywords:
- ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 76f2bf3b-759f-4eed-bce7-119415b25915
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 78325236ab262c474e57b0d903033990b0e85f12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721997"
---
# <a name="icordebugvariablehome-interface"></a><span data-ttu-id="7069a-102">ICorDebugVariableHome 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7069a-102">ICorDebugVariableHome Interface</span></span>
<span data-ttu-id="7069a-103">지역 변수 또는 함수의 인수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-103">Represents a local variable or argument of a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7069a-104">메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-104">Methods</span></span>  
  
|<span data-ttu-id="7069a-105">메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-105">Method</span></span>|<span data-ttu-id="7069a-106">설명</span><span class="sxs-lookup"><span data-stu-id="7069a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7069a-107">GetArgumentIndex 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-107">GetArgumentIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getargumentindex-method.md)|<span data-ttu-id="7069a-108">함수 인수의 인덱스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-108">Gets the index of a function argument.</span></span>|  
|[<span data-ttu-id="7069a-109">GetCode 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-109">GetCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getcode-method.md)|<span data-ttu-id="7069a-110">이 포함 하는 "ICorDebugCode" 인스턴스를 가져옵니다 `ICorDebugVariableHome` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-110">Gets the "ICorDebugCode" instance that contains this `ICorDebugVariableHome` object.</span></span>|  
|[<span data-ttu-id="7069a-111">GetLiveRange 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-111">GetLiveRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getliverange-method.md)|<span data-ttu-id="7069a-112">이 변수는 라이브 기본 범위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-112">Gets the native range over which this variable is live.</span></span>|  
|[<span data-ttu-id="7069a-113">GetLocationType 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-113">GetLocationType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md)|<span data-ttu-id="7069a-114">변수의 네이티브 위치 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-114">Gets the type of the variable's native location.</span></span>|  
|[<span data-ttu-id="7069a-115">GetOffset 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-115">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getoffset-method.md)|<span data-ttu-id="7069a-116">변수에 대 한 기본 등록에서 오프셋을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-116">Gets the offset from the base register for a variable.</span></span>|  
|[<span data-ttu-id="7069a-117">GetRegister 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-117">GetRegister Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getregister-method.md)|<span data-ttu-id="7069a-118">위치 형식의 변수를 포함 하는 레지스터를 가져옵니다 `VLT_REGISTER`, 및 위치 형식의 변수에 대 한 기본 등록 `VLT_REGISTER_RELATIVE`합니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-118">Gets the register that contains a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>|  
|[<span data-ttu-id="7069a-119">GetSlotIndex 메서드</span><span class="sxs-lookup"><span data-stu-id="7069a-119">GetSlotIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getslotindex-method.md)|<span data-ttu-id="7069a-120">지역 변수의 관리 되는 슬롯 인덱스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-120">Gets the managed slot-index of a local variable.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="7069a-121">예제</span><span class="sxs-lookup"><span data-stu-id="7069a-121">Example</span></span>  
 <span data-ttu-id="7069a-122">다음 코드 조각을 사용 합니다 [ICorDebugCode4](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md) 라는 개체 `pCode4`합니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-122">The following code fragment uses the [ICorDebugCode4](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md) object named `pCode4`.</span></span>  
  
```cpp  
ICorDebugCode4 *pCode4 = NULL;  
pCode->QueryInterface(IID_ICorDebugCode4, &pCode4);  
  
ICorDebugVariableEnum *pVarLocEnum = NULL;  
pCode4->EnumerateVariableHomes(&pVarLocEnum);  
  
// retrieve local variables and arguments  
ULONG celt = 0;  
pVarLocEnum->GetCount(&celt);  
ICorDebugVariableHome **homes = new ICorDebugVariableHome *[celt];  
ULONG celtFetched = 0;  
pVarLocEnum->Next(celt, homes, &celtFetched);  
  
for (int i = 0; i < celtFetched; i++)  
{  
    VariableLocationType locType = VLT_INVALID;  
    homes[i].GetLocationType(&locType);  
    switch (locType)  
    {  
    case VLT_REGISTER:  
        CorDebugRegister register = 0;  
        locals[i].GetRegister(&register);  
        // now we know which register it is in  
        break;  
    case VLT_REGISTER_RELATIVE:  
        CorDebugRegister baseRegister = 0;  
        LONG offset = 0;  
        locals[i].GetRegister(&register);  
        locals[i].GetOffset(&offset);  
        // now we know the register-relative offset  
        break;  
    case VLT_INVALID:  
        // handle case where we can't access the location  
        break;  
    }  
}  
```  
  
## <a name="requirements"></a><span data-ttu-id="7069a-123">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7069a-123">Requirements</span></span>  
 <span data-ttu-id="7069a-124">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="7069a-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7069a-125">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7069a-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7069a-126">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7069a-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7069a-127">**.NET Framework 버전:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7069a-127">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7069a-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="7069a-128">See also</span></span>
- [<span data-ttu-id="7069a-129">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7069a-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="7069a-130">ICorDebugVariableHomeEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7069a-130">ICorDebugVariableHomeEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md)
