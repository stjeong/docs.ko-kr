---
title: ISymUnmanagedMethod::GetSequencePoints 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSequencePoints
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSequencePoints
helpviewer_keywords:
- ISymUnmanagedMethod::GetSequencePoints method [.NET Framework debugging]
- GetSequencePoints method [.NET Framework debugging]
ms.assetid: f909ac48-3d8f-49fb-a369-e3d9959151cd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bf6528e8fe6a979db26ae44819bf34a36592ed6b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623627"
---
# <a name="isymunmanagedmethodgetsequencepoints-method"></a><span data-ttu-id="ebebf-102">ISymUnmanagedMethod::GetSequencePoints 메서드</span><span class="sxs-lookup"><span data-stu-id="ebebf-102">ISymUnmanagedMethod::GetSequencePoints Method</span></span>
<span data-ttu-id="ebebf-103">이 메서드 내에서 모든 시퀀스 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-103">Gets all the sequence points within this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebebf-104">구문</span><span class="sxs-lookup"><span data-stu-id="ebebf-104">Syntax</span></span>  
  
```  
HRESULT GetSequencePoints(  
    [in]  ULONG32  cPoints,  
    [out] ULONG32  *pcPoints,  
    [in, size_is(cPoints)] ULONG32  offsets[],  
    [in, size_is(cPoints)] ISymUnmanagedDocument* documents[],  
    [in, size_is(cPoints)] ULONG32  lines[],  
    [in, size_is(cPoints)] ULONG32  columns[],  
    [in, size_is(cPoints)] ULONG32  endLines[],  
    [in, size_is(cPoints)] ULONG32  endColumns[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ebebf-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ebebf-105">Parameters</span></span>  
 `cPoints`  
 <span data-ttu-id="ebebf-106">[in] `ULONG32` 의 크기를 받는 합니다 `offsets`, `documents`, `lines`, `columns`를 `endLines`, 및 `endColumns` 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-106">[in] A `ULONG32` that receives the size of the `offsets`, `documents`, `lines`, `columns`, `endLines`, and `endColumns` arrays.</span></span>  
  
 `pcPoints`  
 <span data-ttu-id="ebebf-107">[out] 에 대 한 포인터를 `ULONG32` 시퀀스 위치를 포함 하는 데 필요한 버퍼의 길이 받는입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-107">[out] A pointer to a `ULONG32` that receives the length of the buffer required to contain the sequence points.</span></span>  
  
 `offsets`  
 <span data-ttu-id="ebebf-108">[in] 저장할 Microsoft 중간 언어 (MSIL) 시퀀스 위치에 대 한 메서드 시작 부분 으로부터의 오프셋 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-108">[in] An array in which to store the Microsoft intermediate language (MSIL) offsets from the beginning of the method for the sequence points.</span></span>  
  
 `documents`  
 <span data-ttu-id="ebebf-109">[in] 시퀀스 위치가 있는 문서를 저장 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-109">[in] An array in which to store the documents in which the sequence points are located.</span></span>  
  
 `lines`  
 <span data-ttu-id="ebebf-110">[in] 시퀀스 위치가 있는 문서의 줄을 저장할 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-110">[in] An array in which to store the lines in the documents at which the sequence points are located.</span></span>  
  
 `columns`  
 <span data-ttu-id="ebebf-111">[in] 시퀀스 위치가 있는 문서의 열을 저장 하는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-111">[in] An array in which to store the columns in the documents at which the sequence points are located.</span></span>  
  
 `endLines`  
 <span data-ttu-id="ebebf-112">[in] 시퀀스 위치가 끝나는 문서의 줄 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-112">[in] The array of lines in the documents at which the sequence points end.</span></span>  
  
 `endColumns`  
 <span data-ttu-id="ebebf-113">[in] 시퀀스 위치가 끝나는 문서의 열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-113">[in] The array of columns in the documents at which the sequence points end.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ebebf-114">반환 값</span><span class="sxs-lookup"><span data-stu-id="ebebf-114">Return Value</span></span>  
 <span data-ttu-id="ebebf-115">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="ebebf-115">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ebebf-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ebebf-116">Requirements</span></span>  
 <span data-ttu-id="ebebf-117">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ebebf-117">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebebf-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="ebebf-118">See also</span></span>
- [<span data-ttu-id="ebebf-119">ISymUnmanagedMethod 인터페이스</span><span class="sxs-lookup"><span data-stu-id="ebebf-119">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
