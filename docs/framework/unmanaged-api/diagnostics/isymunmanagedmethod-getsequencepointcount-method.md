---
title: ISymUnmanagedMethod::GetSequencePointCount 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSequencePointCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSequencePointCount
helpviewer_keywords:
- ISymUnmanagedMethod::GetSequencePointCount method [.NET Framework debugging]
- GetSequencePointCount method [.NET Framework debugging]
ms.assetid: 836133e8-6108-4b9b-b0a9-bce4e08dccda
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e8e919c546df93a2023858c31ebc4d2dec507513
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730141"
---
# <a name="isymunmanagedmethodgetsequencepointcount-method"></a><span data-ttu-id="3ae8e-102">ISymUnmanagedMethod::GetSequencePointCount 메서드</span><span class="sxs-lookup"><span data-stu-id="3ae8e-102">ISymUnmanagedMethod::GetSequencePointCount Method</span></span>
<span data-ttu-id="3ae8e-103">이 메서드 내에서 시퀀스 위치의 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ae8e-103">Gets the count of sequence points within this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ae8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ae8e-104">Syntax</span></span>  
  
```  
HRESULT GetSequencePointCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3ae8e-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ae8e-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="3ae8e-106">[out] 에 대 한 포인터를 `ULONG32` 시퀀스 위치를 포함 하는 데 필요한 버퍼의 크기를 받는 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae8e-106">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the sequence points.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3ae8e-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="3ae8e-107">Return Value</span></span>  
 <span data-ttu-id="3ae8e-108">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3ae8e-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ae8e-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3ae8e-109">Requirements</span></span>  
 <span data-ttu-id="3ae8e-110">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3ae8e-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ae8e-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="3ae8e-111">See also</span></span>
- [<span data-ttu-id="3ae8e-112">ISymUnmanagedMethod 인터페이스</span><span class="sxs-lookup"><span data-stu-id="3ae8e-112">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
