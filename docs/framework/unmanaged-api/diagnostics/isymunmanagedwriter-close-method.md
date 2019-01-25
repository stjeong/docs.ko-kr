---
title: ISymUnmanagedWriter::Close 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Close
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Close
helpviewer_keywords:
- Close method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::Close method [.NET Framework debugging]
ms.assetid: 4cce59e1-80b9-4fc4-b3aa-126f1c5876bc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 780c19acd3d6980c0fb3e31d01e569a61fd04d6d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647311"
---
# <a name="isymunmanagedwriterclose-method"></a><span data-ttu-id="202da-102">ISymUnmanagedWriter::Close 메서드</span><span class="sxs-lookup"><span data-stu-id="202da-102">ISymUnmanagedWriter::Close Method</span></span>
<span data-ttu-id="202da-103">기호를 기호 저장소에 커밋한 후 기호 작성기를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="202da-103">Closes the symbol writer after committing the symbols to the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="202da-104">구문</span><span class="sxs-lookup"><span data-stu-id="202da-104">Syntax</span></span>  
  
```  
HRESULT Close();  
```  
  
## <a name="return-value"></a><span data-ttu-id="202da-105">반환 값</span><span class="sxs-lookup"><span data-stu-id="202da-105">Return Value</span></span>  
 <span data-ttu-id="202da-106">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="202da-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="202da-107">설명</span><span class="sxs-lookup"><span data-stu-id="202da-107">Remarks</span></span>  
 <span data-ttu-id="202da-108">이 호출 후 기호 작성기를 추가로 업데이트할 무효화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="202da-108">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="202da-109">기호를 커밋하지 않고 기호 작성기를 닫으려면 다음을 사용 합니다 [isymunmanagedwriter:: Abort](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md) 메서드 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="202da-109">To close the symbol writer without committing the symbols, use the [ISymUnmanagedWriter::Abort](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md) method instead.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="202da-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="202da-110">Requirements</span></span>  
 <span data-ttu-id="202da-111">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="202da-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="202da-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="202da-112">See also</span></span>
- [<span data-ttu-id="202da-113">ISymUnmanagedWriter 인터페이스</span><span class="sxs-lookup"><span data-stu-id="202da-113">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
