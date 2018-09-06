---
title: IMetaDataTables::GetNextUserString 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextUserString
helpviewer_keywords:
- GetNextUserString method [.NET Framework metadata]
- IMetaDataTables::GetNextUserString method [.NET Framework metadata]
ms.assetid: b7cb40ee-67b7-4f4e-8dcc-ee7ac8bc986b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 01b326765e792bf97658d951a2d5590d22eff546
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43735191"
---
# <a name="imetadatatablesgetnextuserstring-method"></a><span data-ttu-id="1b28b-102">IMetaDataTables::GetNextUserString 메서드</span><span class="sxs-lookup"><span data-stu-id="1b28b-102">IMetaDataTables::GetNextUserString Method</span></span>
<span data-ttu-id="1b28b-103">현재 테이블 열에 다음 하드 코드 된 문자열을 포함 하는 행의 인덱스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1b28b-103">Gets the index of the row that contains the next hard-coded string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b28b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b28b-104">Syntax</span></span>  
  
```  
HRESULT GetNextUserString (  
    [in]  ULONG   ixUserString,  
    [out] ULONG   *pNext  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1b28b-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b28b-105">Parameters</span></span>  
 `ixUserString`  
 <span data-ttu-id="1b28b-106">[in] 현재 문자열 열을 인덱스 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1b28b-106">[in] An index value from the current string column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="1b28b-107">[out] 열에 다음 문자열의 행 인덱스에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="1b28b-107">[out] A pointer to the row index of the next string in the column.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1b28b-108">설명</span><span class="sxs-lookup"><span data-stu-id="1b28b-108">Remarks</span></span>  
 <span data-ttu-id="1b28b-109">바람직하지 않습니다이 메서드를 사용 하 여 일관 된 결과 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b28b-109">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="1b28b-110">GUID 테이블에 대 한 내용은 "II: 메타 데이터 정의 및 의미" 공용 언어 인프라 (CLI) 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b28b-110">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="1b28b-111">이 설명서는 온라인으로 제공됩니다. MSDN의 [ECMA C# 및 공용 언어 인프라 표준](https://go.microsoft.com/fwlink/?LinkID=99212) 및 Ecma International 웹 사이트의 [표준 ECMA-335 - CLI(공용 언어 인프라)](https://go.microsoft.com/fwlink/?LinkID=65552)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b28b-111">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) on MSDN and [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) on the Ecma International Web site.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1b28b-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="1b28b-112">Requirements</span></span>  
 <span data-ttu-id="1b28b-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b28b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b28b-114">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1b28b-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1b28b-115">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="1b28b-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1b28b-116">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b28b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b28b-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1b28b-117">See Also</span></span>  
 [<span data-ttu-id="1b28b-118">IMetaDataTables 인터페이스</span><span class="sxs-lookup"><span data-stu-id="1b28b-118">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="1b28b-119">IMetaDataTables2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="1b28b-119">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
