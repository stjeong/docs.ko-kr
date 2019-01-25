---
title: ISymUnmanagedScope::GetMethod 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetMethod
helpviewer_keywords:
- GetMethod method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetMethod method [.NET Framework debugging]
ms.assetid: a61866ee-221a-45b9-a1b7-395825b77872
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 12dd485f2b89dc76076410e76a132ff547681597
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616825"
---
# <a name="isymunmanagedscopegetmethod-method"></a><span data-ttu-id="7a78a-102">ISymUnmanagedScope::GetMethod 메서드</span><span class="sxs-lookup"><span data-stu-id="7a78a-102">ISymUnmanagedScope::GetMethod Method</span></span>
<span data-ttu-id="7a78a-103">이 범위를 포함 하는 메서드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a78a-103">Gets the method that contains this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a78a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a78a-104">Syntax</span></span>  
  
```  
HRESULT GetMethod(  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7a78a-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a78a-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="7a78a-106">[out] 반환 된 포인터 [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="7a78a-106">[out] A pointer to the returned [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7a78a-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="7a78a-107">Return Value</span></span>  
 <span data-ttu-id="7a78a-108">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="7a78a-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a78a-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7a78a-109">Requirements</span></span>  
 <span data-ttu-id="7a78a-110">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7a78a-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a78a-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="7a78a-111">See also</span></span>
- [<span data-ttu-id="7a78a-112">ISymUnmanagedScope 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7a78a-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
