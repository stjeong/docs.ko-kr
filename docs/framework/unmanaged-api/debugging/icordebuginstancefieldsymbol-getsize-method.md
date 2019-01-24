---
title: ICorDebugInstanceFieldSymbol::GetSize 메서드
ms.date: 03/30/2017
ms.assetid: a4af1e3b-6a9f-4855-95ba-5317565c8e2b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 04d866888c15585ff5058f870257b317ac888be7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696986"
---
# <a name="icordebuginstancefieldsymbolgetsize-method"></a><span data-ttu-id="9ad88-102">ICorDebugInstanceFieldSymbol::GetSize 메서드</span><span class="sxs-lookup"><span data-stu-id="9ad88-102">ICorDebugInstanceFieldSymbol::GetSize Method</span></span>
<span data-ttu-id="9ad88-103">인스턴스 필드의 크기(바이트)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad88-103">Gets the size in bytes of the instance field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ad88-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ad88-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9ad88-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9ad88-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="9ad88-106">[out] 필드 길이에 대한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad88-106">[out] A pointer to length of the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9ad88-107">설명</span><span class="sxs-lookup"><span data-stu-id="9ad88-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9ad88-108">이 메서드는 .NET 네이티브에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad88-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ad88-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9ad88-109">Requirements</span></span>  
 <span data-ttu-id="9ad88-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9ad88-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ad88-111">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ad88-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ad88-112">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ad88-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ad88-113">**.NET Framework 버전:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ad88-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ad88-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="9ad88-114">See also</span></span>
- [<span data-ttu-id="9ad88-115">ICorDebugInstanceFieldSymbol 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9ad88-115">ICorDebugInstanceFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="9ad88-116">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9ad88-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
