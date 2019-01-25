---
title: IMetaDataTables::GetBlobHeapSize 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetBlobHeapSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetBlobHeapSize
helpviewer_keywords:
- GetBlobHeapSize method [.NET Framework metadata]
- IMetaDataTables::GetBlobHeapSize method [.NET Framework metadata]
ms.assetid: 6330a9ee-8cd5-4299-86f1-b4de2c701a0d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3f9f49219b810ac85b1f021c206bfab21d11a055
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745988"
---
# <a name="imetadatatablesgetblobheapsize-method"></a><span data-ttu-id="a282b-102">IMetaDataTables::GetBlobHeapSize 메서드</span><span class="sxs-lookup"><span data-stu-id="a282b-102">IMetaDataTables::GetBlobHeapSize Method</span></span>
<span data-ttu-id="a282b-103">(BLOB) 이진 대형 개체 힙 바이트의 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a282b-103">Gets the size, in bytes, of the binary large object (BLOB) heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a282b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a282b-104">Syntax</span></span>  
  
```  
HRESULT GetBlobHeapSize (  
    [out] ULONG     *pcbBlobs  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="a282b-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a282b-105">Parameters</span></span>  
 `pcbBlobs`  
 <span data-ttu-id="a282b-106">[out] 크기 (바이트)는 BLOB 힙에서의 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="a282b-106">[out] A pointer to the size, in bytes, of the BLOB heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a282b-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a282b-107">Requirements</span></span>  
 <span data-ttu-id="a282b-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a282b-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a282b-109">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a282b-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a282b-110">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="a282b-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a282b-111">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a282b-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a282b-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="a282b-112">See also</span></span>
- [<span data-ttu-id="a282b-113">IMetaDataTables 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a282b-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="a282b-114">IMetaDataTables2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a282b-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
