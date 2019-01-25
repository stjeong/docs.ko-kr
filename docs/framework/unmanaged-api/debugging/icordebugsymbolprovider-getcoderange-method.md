---
title: ICorDebugSymbolProvider::GetCodeRange 메서드
ms.date: 03/30/2017
ms.assetid: 49a2451f-d250-4e73-aa96-9ff49d9f11c6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bfaa8ce16a3874d28e06bdb77f1e903548c0a03b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54684790"
---
# <a name="icordebugsymbolprovidergetcoderange-method"></a><span data-ttu-id="8bd62-102">ICorDebugSymbolProvider::GetCodeRange 메서드</span><span class="sxs-lookup"><span data-stu-id="8bd62-102">ICorDebugSymbolProvider::GetCodeRange Method</span></span>
<span data-ttu-id="8bd62-103">메서드의 RVA(상대 가상 주소)가 지정된 경우 메서드 시작 주소와 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8bd62-103">Gets the method start address and size given a relative virtual address (RVA) in a method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8bd62-104">구문</span><span class="sxs-lookup"><span data-stu-id="8bd62-104">Syntax</span></span>  
  
```  
HRESULT GetCodeRange(  
   [in] ULONG32 codeRva,   
   [out] ULONG32* pCodeStartAddress,   
   [out] ULONG32* pCodeSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8bd62-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8bd62-105">Parameters</span></span>  
 `codeRva`  
 <span data-ttu-id="8bd62-106">[in] 메서드의 RVA(상대 가상 주소)입니다.</span><span class="sxs-lookup"><span data-stu-id="8bd62-106">[in] The relative virtual address (RVA) in a method.</span></span>  
  
 `pCodeStartAddress`  
 <span data-ttu-id="8bd62-107">[out] 메서드의 시작 주소에 대한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="8bd62-107">[out] A pointer to the starting address of the method.</span></span>  
  
 `pCodeSize`  
 <span data-ttu-id="8bd62-108">메서드 코드 크기(메서드 코드의 바이트 수)에 대한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="8bd62-108">A pointer to the method code size (the number of bytes of the method's code).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8bd62-109">설명</span><span class="sxs-lookup"><span data-stu-id="8bd62-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8bd62-110">이 메서드는 .NET 네이티브에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bd62-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8bd62-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8bd62-111">Requirements</span></span>  
 <span data-ttu-id="8bd62-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="8bd62-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8bd62-113">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8bd62-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8bd62-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8bd62-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8bd62-115">**.NET Framework 버전:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8bd62-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8bd62-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="8bd62-116">See also</span></span>
- [<span data-ttu-id="8bd62-117">ICorDebugSymbolProvider 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8bd62-117">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="8bd62-118">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8bd62-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
