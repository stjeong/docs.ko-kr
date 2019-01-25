---
title: ICorDebugCode::GetFunction 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetFunction method [.NET Framework debugging]
ms.assetid: c568b737-fdb2-4816-accd-051f5ab760f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dd544619f9e5fb85a0b08b91ead8231ea25743cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54651231"
---
# <a name="icordebugcodegetfunction-method"></a><span data-ttu-id="24527-102">ICorDebugCode::GetFunction 메서드</span><span class="sxs-lookup"><span data-stu-id="24527-102">ICorDebugCode::GetFunction Method</span></span>
<span data-ttu-id="24527-103">"ICorDebugFunction을"이 "ICorDebugCode"를 사용 하 여 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24527-103">Gets the "ICorDebugFunction" associated with this "ICorDebugCode".</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24527-104">구문</span><span class="sxs-lookup"><span data-stu-id="24527-104">Syntax</span></span>  
  
```  
HRESULT GetFunction (  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="24527-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="24527-105">Parameters</span></span>  
 `ppFunction`  
 <span data-ttu-id="24527-106">[out] 함수 주소에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="24527-106">[out] A pointer to the address of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="24527-107">설명</span><span class="sxs-lookup"><span data-stu-id="24527-107">Remarks</span></span>  
 <span data-ttu-id="24527-108">`ICorDebugCode` 및 `ICorDebugFunction` 한 일 관계를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="24527-108">`ICorDebugCode` and `ICorDebugFunction` maintain a one-to-one relationship.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24527-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="24527-109">Requirements</span></span>  
 <span data-ttu-id="24527-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="24527-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24527-111">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="24527-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="24527-112">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="24527-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="24527-113">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24527-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24527-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="24527-114">See also</span></span>

