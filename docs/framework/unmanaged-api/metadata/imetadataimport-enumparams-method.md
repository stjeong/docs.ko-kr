---
title: IMetaDataImport::EnumParams 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumParams
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumParams
helpviewer_keywords:
- IMetaDataImport::EnumParams method [.NET Framework metadata]
- EnumParams method [.NET Framework metadata]
ms.assetid: 52118dc9-fe6e-4b39-aa48-c3cc3ea4214d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dadfabf1d2507b2bd719b5b73238bb38c9ae7563
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602431"
---
# <a name="imetadataimportenumparams-method"></a><span data-ttu-id="43e85-102">IMetaDataImport::EnumParams 메서드</span><span class="sxs-lookup"><span data-stu-id="43e85-102">IMetaDataImport::EnumParams Method</span></span>
<span data-ttu-id="43e85-103">지정한 MethodDef 토큰이 참조하는 메서드의 매개 변수를 나타내는 ParamDef 토큰을 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-103">Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43e85-104">구문</span><span class="sxs-lookup"><span data-stu-id="43e85-104">Syntax</span></span>  
  
```  
HRESULT EnumParams (  
   [in, out] HCORENUM    *phEnum,  
   [in]  mdMethodDef     mb,  
   [out] mdParamDef      rParams[],  
   [in]  ULONG           cMax,  
   [out] ULONG          *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="43e85-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="43e85-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="43e85-106">[out에서] 열거자에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="43e85-107">이 메서드의 첫 번째 호출에 대 한 NULL 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-107">This must be NULL for the first call of this method.</span></span>  
  
 `mb`  
 <span data-ttu-id="43e85-108">[in] 열거를 매개 변수를 사용 하 여 메서드를 나타내는 MethodDef 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-108">[in] A MethodDef token representing the method with the parameters to enumerate.</span></span>  
  
 `rParams`  
 <span data-ttu-id="43e85-109">[out] ParamDef 토큰을 저장 하는 데 사용 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-109">[out] The array used to store the ParamDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="43e85-110">[in] `rParams` 배열의 최대 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-110">[in] The maximum size of the `rParams` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="43e85-111">[out] ParamDef 토큰에서 반환 된 수가 `rParams`합니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-111">[out] The number of ParamDef tokens returned in `rParams`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="43e85-112">반환 값</span><span class="sxs-lookup"><span data-stu-id="43e85-112">Return Value</span></span>  
  
|<span data-ttu-id="43e85-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="43e85-113">HRESULT</span></span>|<span data-ttu-id="43e85-114">설명</span><span class="sxs-lookup"><span data-stu-id="43e85-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="43e85-115">`EnumParams` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-115">`EnumParams` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="43e85-116">열거할 토큰이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="43e85-117">이런 경우 `pcTokens` 0입니다.</span><span class="sxs-lookup"><span data-stu-id="43e85-117">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="43e85-118">요구 사항</span><span class="sxs-lookup"><span data-stu-id="43e85-118">Requirements</span></span>  
 <span data-ttu-id="43e85-119">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="43e85-119">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43e85-120">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="43e85-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="43e85-121">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="43e85-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="43e85-122">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43e85-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43e85-123">참고자료</span><span class="sxs-lookup"><span data-stu-id="43e85-123">See also</span></span>
- [<span data-ttu-id="43e85-124">IMetaDataImport 인터페이스</span><span class="sxs-lookup"><span data-stu-id="43e85-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="43e85-125">IMetaDataImport2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="43e85-125">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
