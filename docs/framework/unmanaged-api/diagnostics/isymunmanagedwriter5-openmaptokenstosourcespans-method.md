---
title: ISymUnmanagedWriter5::OpenMapTokensToSourceSpans 메서드
ms.date: 03/30/2017
ms.assetid: 93ad2517-b0dc-464c-8688-a58a30eda18d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 60c1984e6193481efdaaeb82a2bc025aef67a33f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534444"
---
# <a name="isymunmanagedwriter5openmaptokenstosourcespans-method"></a><span data-ttu-id="2d52b-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans 메서드</span><span class="sxs-lookup"><span data-stu-id="2d52b-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="2d52b-103">토큰에서 소스로 범위 매핑 정보를 내보내는 데 특별 한 사용자 지정 데이터 섹션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2d52b-103">Open a special custom data section to emit token-to-source span mapping information into.</span></span> <span data-ttu-id="2d52b-104">가 이미 열려 메서드나 그 반대의 경우 오류가 발생 하는 경우이 섹션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2d52b-104">Opening this section when a method is already open, or vice versa, is an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d52b-105">구문</span><span class="sxs-lookup"><span data-stu-id="2d52b-105">Syntax</span></span>  
  
```idl  
HRESULT OpenMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="2d52b-106">반환 값</span><span class="sxs-lookup"><span data-stu-id="2d52b-106">Return Value</span></span>  
 <span data-ttu-id="2d52b-107">`HRESULT`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2d52b-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d52b-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2d52b-108">Requirements</span></span>  
 <span data-ttu-id="2d52b-109">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2d52b-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d52b-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="2d52b-110">See also</span></span>
- [<span data-ttu-id="2d52b-111">ISymUnmanagedWriter5 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2d52b-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
