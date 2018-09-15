---
title: ISymUnmanagedENCUpdate::UpdateSymbolStore2 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateSymbolStore2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2
helpviewer_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2 method [.NET Framework debugging]
- UpdateSymbolStore2 method [.NET Framework debugging]
ms.assetid: 35588317-6184-485c-ab41-4b15fc1765d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 78d9e27299c9d7ed7d6cb9b09dd659ba081c5fde
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45616064"
---
# <a name="isymunmanagedencupdateupdatesymbolstore2-method"></a><span data-ttu-id="9d841-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 메서드</span><span class="sxs-lookup"><span data-stu-id="9d841-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 Method</span></span>
<span data-ttu-id="9d841-103">컴파일러가 줄 정보를 요구 사항을 충족 하는 제공 된 프로그램 데이터베이스 (PDB) 스트림, 수정 되지 않은 함수를 생략할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d841-103">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided the line information meets the requirements.</span></span> <span data-ttu-id="9d841-104">이전 PDB 줄 정보를 및 모든 줄은 함수에 대 한 델타를 사용 하 여 올바른 줄 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d841-104">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d841-105">구문</span><span class="sxs-lookup"><span data-stu-id="9d841-105">Syntax</span></span>  
  
```  
HRESULT UpdateSymbolStore2(  
    [in]  IStream      *pIStream,  
    [in]  SYMLINEDELTA* pDeltaLines,  
    [in]  ULONG         cDeltaLines);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9d841-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9d841-106">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="9d841-107">[in] 에 대 한 포인터를 [IStream](/windows/desktop/api/objidl/nn-objidl-istream) 줄 정보를 포함 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d841-107">[in] A pointer to an [IStream](/windows/desktop/api/objidl/nn-objidl-istream) that contains the line information.</span></span>  
  
 `pDeltaLines`  
 <span data-ttu-id="9d841-108">[in] 에 대 한 포인터를 [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) 변경 된 줄을 포함 하는 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="9d841-108">[in] A pointer to a [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure that contains the lines that have changed.</span></span>  
  
 `cDeltaLines`  
 <span data-ttu-id="9d841-109">[in] `ULONG` 변경 된 줄 수를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="9d841-109">[in] A `ULONG` that represents the number of lines that have changed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9d841-110">반환 값</span><span class="sxs-lookup"><span data-stu-id="9d841-110">Return Value</span></span>  
 <span data-ttu-id="9d841-111">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="9d841-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d841-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9d841-112">Requirements</span></span>  
 <span data-ttu-id="9d841-113">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9d841-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d841-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9d841-114">See Also</span></span>  
 [<span data-ttu-id="9d841-115">ISymUnmanagedENCUpdate 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9d841-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
