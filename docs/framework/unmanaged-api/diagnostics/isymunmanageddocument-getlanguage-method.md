---
title: ISymUnmanagedDocument::GetLanguage 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguage
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguage
helpviewer_keywords:
- ISymUnmanagedDocument::GetLanguage method [.NET Framework debugging]
- GetLanguage method [.NET Framework debugging]
ms.assetid: c6639418-e9f2-4a99-8ce2-ec9876e0bc79
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 186ea5fd46ca5c6205ff1f98d8964e656655a2ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666035"
---
# <a name="isymunmanageddocumentgetlanguage-method"></a><span data-ttu-id="bfda8-102">ISymUnmanagedDocument::GetLanguage 메서드</span><span class="sxs-lookup"><span data-stu-id="bfda8-102">ISymUnmanagedDocument::GetLanguage Method</span></span>
<span data-ttu-id="bfda8-103">이 문서의 언어 식별자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfda8-103">Gets the language identifier of this document</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfda8-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfda8-104">Syntax</span></span>  
  
```  
HRESULT GetLanguage(  
    [out, retval]  GUID*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bfda8-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bfda8-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="bfda8-106">[out] 언어 식별자를 수신 하는 변수에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="bfda8-106">[out] A pointer to a variable that receives the language identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bfda8-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="bfda8-107">Return Value</span></span>  
 <span data-ttu-id="bfda8-108">메서드가 성공 하면 S_OK입니다.</span><span class="sxs-lookup"><span data-stu-id="bfda8-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfda8-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="bfda8-109">See also</span></span>
- [<span data-ttu-id="bfda8-110">ISymUnmanagedDocument 인터페이스</span><span class="sxs-lookup"><span data-stu-id="bfda8-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
