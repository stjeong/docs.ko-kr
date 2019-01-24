---
title: IObjectHandle::Unwrap 메서드
ms.date: 03/30/2017
api_name:
- IObjectHandle.Unwrap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Unwrap
helpviewer_keywords:
- Unwrap method [.NET Framework hosting]
- IObjectHandle::Unwrap method [.NET Framework hosting]
ms.assetid: 794c6f8e-ed58-416b-b756-e864f2c958f7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: da25055917743481f5a8314023ed94d552fe49ce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54526420"
---
# <a name="iobjecthandleunwrap-method"></a><span data-ttu-id="3fdb2-102">IObjectHandle::Unwrap 메서드</span><span class="sxs-lookup"><span data-stu-id="3fdb2-102">IObjectHandle::Unwrap Method</span></span>
<span data-ttu-id="3fdb2-103">간접 참조의 값으로 마샬링된 개체를 래핑 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fdb2-103">Unwraps a marshal-by-value object from indirection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fdb2-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fdb2-104">Syntax</span></span>  
  
```  
HRESULT Unwrap (  
    [out, retval] VARIANT *ppv  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3fdb2-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3fdb2-105">Parameters</span></span>  
 `ppv`  
 <span data-ttu-id="3fdb2-106">[out] 래핑 해제할 개체에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="3fdb2-106">[out] A pointer to the object to be unwrapped.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fdb2-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3fdb2-107">Requirements</span></span>  
 <span data-ttu-id="3fdb2-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="3fdb2-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fdb2-109">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3fdb2-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3fdb2-110">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="3fdb2-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3fdb2-111">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fdb2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fdb2-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="3fdb2-112">See also</span></span>

