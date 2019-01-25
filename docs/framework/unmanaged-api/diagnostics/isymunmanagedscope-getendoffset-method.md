---
title: ISymUnmanagedScope::GetEndOffset 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetEndOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedScope::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 1d0b15c9-8059-435f-9fce-346a08b9bd36
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 739398d8c20f58d8b5e458e2de4cbb6f56c50fd8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624171"
---
# <a name="isymunmanagedscopegetendoffset-method"></a><span data-ttu-id="19917-102">ISymUnmanagedScope::GetEndOffset 메서드</span><span class="sxs-lookup"><span data-stu-id="19917-102">ISymUnmanagedScope::GetEndOffset Method</span></span>
<span data-ttu-id="19917-103">이 범위의 끝 오프셋을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19917-103">Gets the end offset for this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19917-104">구문</span><span class="sxs-lookup"><span data-stu-id="19917-104">Syntax</span></span>  
  
```  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="19917-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19917-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="19917-106">[out] 에 대 한 포인터를 `ULONG32` 를 받는 끝 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="19917-106">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="19917-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="19917-107">Return Value</span></span>  
 <span data-ttu-id="19917-108">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="19917-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19917-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="19917-109">Requirements</span></span>  
 <span data-ttu-id="19917-110">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="19917-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19917-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="19917-111">See also</span></span>
- [<span data-ttu-id="19917-112">ISymUnmanagedScope 인터페이스</span><span class="sxs-lookup"><span data-stu-id="19917-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [<span data-ttu-id="19917-113">GetStartOffset 메서드</span><span class="sxs-lookup"><span data-stu-id="19917-113">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getstartoffset-method.md)
