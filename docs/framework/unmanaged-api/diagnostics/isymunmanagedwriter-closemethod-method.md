---
title: ISymUnmanagedWriter::CloseMethod 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseMethod
helpviewer_keywords:
- ISymUnmanagedWriter::CloseMethod method [.NET Framework debugging]
- CloseMethod method [.NET Framework debugging]
ms.assetid: b8025e04-f0e5-40c8-849c-8cd51323420e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a6f8c8b522aabfce3b83b6b624bd0ca9757448ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666022"
---
# <a name="isymunmanagedwriterclosemethod-method"></a><span data-ttu-id="2f24f-102">ISymUnmanagedWriter::CloseMethod 메서드</span><span class="sxs-lookup"><span data-stu-id="2f24f-102">ISymUnmanagedWriter::CloseMethod Method</span></span>
<span data-ttu-id="2f24f-103">현재 메서드를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="2f24f-103">Closes the current method.</span></span> <span data-ttu-id="2f24f-104">메서드 종료 되 면 그 없습니다 자세한 기호를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f24f-104">Once a method is closed, no more symbols can be defined within it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f24f-105">구문</span><span class="sxs-lookup"><span data-stu-id="2f24f-105">Syntax</span></span>  
  
```  
HRESULT CloseMethod();  
```  
  
## <a name="return-value"></a><span data-ttu-id="2f24f-106">반환 값</span><span class="sxs-lookup"><span data-stu-id="2f24f-106">Return Value</span></span>  
 <span data-ttu-id="2f24f-107">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="2f24f-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f24f-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2f24f-108">Requirements</span></span>  
 <span data-ttu-id="2f24f-109">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2f24f-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f24f-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="2f24f-110">See also</span></span>
- [<span data-ttu-id="2f24f-111">ISymUnmanagedWriter 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2f24f-111">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="2f24f-112">OpenMethod 메서드</span><span class="sxs-lookup"><span data-stu-id="2f24f-112">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
