---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod 메서드
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f20039318d6e1230ccc0fbd203fc44686806bb2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604472"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="38b19-102">ISymUnmanagedAsyncMethod::GetKickoffMethod 메서드</span><span class="sxs-lookup"><span data-stu-id="38b19-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>
<span data-ttu-id="38b19-103">참조 [DefineKickoffMethod 메서드](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="38b19-103">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38b19-104">구문</span><span class="sxs-lookup"><span data-stu-id="38b19-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="38b19-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="38b19-105">Parameters</span></span>  
  
|<span data-ttu-id="38b19-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="38b19-106">Parameter</span></span>|<span data-ttu-id="38b19-107">설명</span><span class="sxs-lookup"><span data-stu-id="38b19-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="38b19-108">반환 값</span><span class="sxs-lookup"><span data-stu-id="38b19-108">Return Value</span></span>  
 <span data-ttu-id="38b19-109">`HRESULT`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="38b19-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38b19-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="38b19-110">Requirements</span></span>  
 <span data-ttu-id="38b19-111">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="38b19-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38b19-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="38b19-112">See also</span></span>
- [<span data-ttu-id="38b19-113">ISymUnmanagedAsyncMethod 인터페이스</span><span class="sxs-lookup"><span data-stu-id="38b19-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
