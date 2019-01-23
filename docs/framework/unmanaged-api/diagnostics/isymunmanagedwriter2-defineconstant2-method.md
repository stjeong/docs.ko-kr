---
title: ISymUnmanagedWriter2::DefineConstant2 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineConstant2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineConstant2
helpviewer_keywords:
- DefineConstant2 method [.NET Framework debugging]
- ISymUnmanagedWriter2::DefineConstant2 method [.NET Framework debugging]
ms.assetid: dd2bc956-7dbe-49fc-a646-daa0d267f2df
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e843acc82d52e2c7a772f4799e7bb0af8ecff10d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545727"
---
# <a name="isymunmanagedwriter2defineconstant2-method"></a><span data-ttu-id="d0be0-102">ISymUnmanagedWriter2::DefineConstant2 메서드</span><span class="sxs-lookup"><span data-stu-id="d0be0-102">ISymUnmanagedWriter2::DefineConstant2 Method</span></span>
<span data-ttu-id="d0be0-103">상수 값에 대 한 이름을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d0be0-103">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0be0-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0be0-104">Syntax</span></span>  
  
```  
HRESULT DefineConstant2(  
    [in] const WCHAR  *name,  
    [in] VARIANT      value,  
    [in] mdSignature  sigToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d0be0-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0be0-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="d0be0-106">[in] 상수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0be0-106">[in] The constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="d0be0-107">[in] 상수의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d0be0-107">[in] The value of the constant.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="d0be0-108">[in] 메타 데이터 토큰 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="d0be0-108">[in] The metadata token of the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d0be0-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="d0be0-109">Return Value</span></span>  
 <span data-ttu-id="d0be0-110">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="d0be0-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0be0-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d0be0-111">Requirements</span></span>  
 <span data-ttu-id="d0be0-112">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d0be0-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0be0-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="d0be0-113">See also</span></span>
- [<span data-ttu-id="d0be0-114">ISymUnmanagedWriter2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="d0be0-114">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="d0be0-115">DefineConstant 메서드</span><span class="sxs-lookup"><span data-stu-id="d0be0-115">DefineConstant Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineconstant-method.md)
