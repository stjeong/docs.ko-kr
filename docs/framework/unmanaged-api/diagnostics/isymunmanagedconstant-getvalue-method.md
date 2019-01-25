---
title: ISymUnmanagedConstant::GetValue 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetValue
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetValue
helpviewer_keywords:
- GetValue method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetValue method [.NET Framework debugging]
ms.assetid: 0036fc10-e768-47a8-b9cf-bf47faf8d194
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1043a7efe70798fbbc52ce6d1d0e16510e7c0503
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499147"
---
# <a name="isymunmanagedconstantgetvalue-method"></a><span data-ttu-id="48547-102">ISymUnmanagedConstant::GetValue 메서드</span><span class="sxs-lookup"><span data-stu-id="48547-102">ISymUnmanagedConstant::GetValue Method</span></span>
<span data-ttu-id="48547-103">상수 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48547-103">Gets the value of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48547-104">구문</span><span class="sxs-lookup"><span data-stu-id="48547-104">Syntax</span></span>  
  
```  
HRESULT GetValue(  
    [out]  VARIANT* pValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="48547-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48547-105">Parameters</span></span>  
 `pValue`  
 <span data-ttu-id="48547-106">[out] 값을 수신 하는 변수에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="48547-106">[out] A pointer to a variable that receives the value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="48547-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="48547-107">Return Value</span></span>  
 <span data-ttu-id="48547-108">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="48547-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48547-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="48547-109">Requirements</span></span>  
 <span data-ttu-id="48547-110">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="48547-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48547-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="48547-111">See also</span></span>
- [<span data-ttu-id="48547-112">ISymUnmanagedConstant 인터페이스</span><span class="sxs-lookup"><span data-stu-id="48547-112">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)
- [<span data-ttu-id="48547-113">GetName 메서드</span><span class="sxs-lookup"><span data-stu-id="48547-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="48547-114">GetSignature 메서드</span><span class="sxs-lookup"><span data-stu-id="48547-114">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getsignature-method.md)
