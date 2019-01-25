---
title: ISymUnmanagedSymbolSearchInfo::GetHRESULT 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetHRESULT
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT method [.NET Framework debugging]
- GetHRESULT method [.NET Framework debugging]
ms.assetid: 6999dc3d-65d7-4bf6-bb0a-6efc0fc72588
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15f85a6f5ab418692d747cc9ad415c637d7b96e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614369"
---
# <a name="isymunmanagedsymbolsearchinfogethresult-method"></a><span data-ttu-id="cc16c-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT 메서드</span><span class="sxs-lookup"><span data-stu-id="cc16c-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT Method</span></span>
<span data-ttu-id="cc16c-103">HRESULT를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc16c-103">Gets the HRESULT.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc16c-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc16c-104">Syntax</span></span>  
  
```  
HRESULT GetHRESULT(  
    [out] HRESULT *phr);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cc16c-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cc16c-105">Parameters</span></span>  
 `phr`  
 <span data-ttu-id="cc16c-106">[out] HRESULT에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="cc16c-106">[out] A pointer to the HRESULT.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cc16c-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="cc16c-107">Return Value</span></span>  
 <span data-ttu-id="cc16c-108">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="cc16c-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc16c-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="cc16c-109">Requirements</span></span>  
 <span data-ttu-id="cc16c-110">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="cc16c-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc16c-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="cc16c-111">See also</span></span>
- [<span data-ttu-id="cc16c-112">ISymUnmanagedSymbolSearchInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cc16c-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
