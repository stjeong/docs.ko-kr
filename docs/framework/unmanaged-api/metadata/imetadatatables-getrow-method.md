---
title: IMetaDataTables::GetRow 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetRow
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetRow
helpviewer_keywords:
- IMetaDataTables::GetRow method [.NET Framework metadata]
- GetRow method [.NET Framework metadata]
ms.assetid: a7408d51-0bce-45a2-b58f-da4660bbc039
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d24dbcbdd8b0ed0736f7b59564cf72dffaa5a8f8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44196714"
---
# <a name="imetadatatablesgetrow-method"></a><span data-ttu-id="1d2a4-102">IMetaDataTables::GetRow 메서드</span><span class="sxs-lookup"><span data-stu-id="1d2a4-102">IMetaDataTables::GetRow Method</span></span>
<span data-ttu-id="1d2a4-103">지정된 된 테이블 인덱스에 있는 표에 지정 된 행 인덱스에 행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-103">Gets the row at the specified row index, in the table at the specified table index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d2a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d2a4-104">Syntax</span></span>  
  
```  
HRESULT GetRow (   
    [in]  ULONG   ixTbl,  
    [in]  ULONG   rid,  
    [out] void    **ppRow  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1d2a4-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d2a4-105">Parameters</span></span>  
 `ixTbl`  
 <span data-ttu-id="1d2a4-106">[in] 행을 검색할 테이블의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-106">[in] The index of the table from which the row will be retrieved.</span></span>  
  
 `rid`  
 <span data-ttu-id="1d2a4-107">[in] 가져올 행의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-107">[in] The index of the row to get.</span></span>  
  
 `ppRow`  
 <span data-ttu-id="1d2a4-108">[out] 행에 대 한 포인터에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-108">[out] A pointer to a pointer to the row.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1d2a4-109">설명</span><span class="sxs-lookup"><span data-stu-id="1d2a4-109">Remarks</span></span>  
 <span data-ttu-id="1d2a4-110">바람직하지 않습니다이 메서드를 사용 하 여 일관 된 결과 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-110">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="1d2a4-111">GUID 테이블에 대 한 내용은 "II: 메타 데이터 정의 및 의미" 공용 언어 인프라 (CLI) 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-111">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="1d2a4-112">이 설명서는 온라인으로 제공됩니다. MSDN의 [ECMA C# 및 공용 언어 인프라 표준](https://go.microsoft.com/fwlink/?LinkID=99212) 및 Ecma International 웹 사이트의 [표준 ECMA-335 - CLI(공용 언어 인프라)](https://go.microsoft.com/fwlink/?LinkID=65552)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-112">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) on MSDN and [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) on the Ecma International Web site.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1d2a4-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="1d2a4-113">Requirements</span></span>  
 <span data-ttu-id="1d2a4-114">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d2a4-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1d2a4-115">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1d2a4-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1d2a4-116">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="1d2a4-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1d2a4-117">**.NET framework 버전**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1d2a4-117">**.NET Framework Versions**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d2a4-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1d2a4-118">See Also</span></span>  
 [<span data-ttu-id="1d2a4-119">IMetaDataTables 인터페이스</span><span class="sxs-lookup"><span data-stu-id="1d2a4-119">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="1d2a4-120">IMetaDataTables2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="1d2a4-120">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
