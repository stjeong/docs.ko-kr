---
title: IMetaDataImport::EnumMembersWithName 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMembersWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMembersWithName
helpviewer_keywords:
- IMetaDataImport::EnumMembersWithName method [.NET Framework metadata]
- EnumMembersWithName method [.NET Framework metadata]
ms.assetid: 7c9e9120-3104-42f0-86ce-19a025f20dcc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a830a4cc881912d52ec33959104957d0b858b16a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539469"
---
# <a name="imetadataimportenummemberswithname-method"></a><span data-ttu-id="330cb-102">IMetaDataImport::EnumMembersWithName 메서드</span><span class="sxs-lookup"><span data-stu-id="330cb-102">IMetaDataImport::EnumMembersWithName Method</span></span>
<span data-ttu-id="330cb-103">지정한 이름을 가진 지정한 형식의 멤버를 나타내는 MemberDef 토큰을 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-103">Enumerates MemberDef tokens representing members of the specified type with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="330cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="330cb-104">Syntax</span></span>  
  
```  
HRESULT EnumMembersWithName (  
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   cl,   
   [in]      LPCWSTR     szName,   
   [out]     mdToken     rMembers[],   
   [in]      ULONG       cMax,   
   [out]     ULONG       *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="330cb-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="330cb-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="330cb-106">[out에서] 열거자에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="330cb-107">[in] 열거 하는 멤버 형식을 나타내는 TypeDef 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-107">[in] A TypeDef token representing the type with members to enumerate.</span></span>  
  
 `szName`  
 <span data-ttu-id="330cb-108">[in] 열거자의 범위를 제한 하는 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-108">[in] The member name that limits the scope of the enumerator.</span></span>  
  
 `rMembers`  
 <span data-ttu-id="330cb-109">[out] MemberDef 토큰을 저장 하는 데 사용 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-109">[out] The array used to store the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="330cb-110">[in] `rMembers` 배열의 최대 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-110">[in] The maximum size of the `rMembers` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="330cb-111">[out] 실제 MemberDef 토큰에서 반환 된 수가 `rMembers`합니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-111">[out] The actual number of MemberDef tokens returned in `rMembers`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="330cb-112">설명</span><span class="sxs-lookup"><span data-stu-id="330cb-112">Remarks</span></span>  
 <span data-ttu-id="330cb-113">이 메서드는 필드 및 메서드 하지만 하지 속성 또는 이벤트를 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-113">This method enumerates fields and methods, but not properties or events.</span></span> <span data-ttu-id="330cb-114">와 달리 [imetadataimport:: Enummembers](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enummembers-method.md), `EnumMembersWithName` 지정 된 이름이 없는 모든 필드와 멤버 토큰을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-114">Unlike [IMetaDataImport::EnumMembers](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enummembers-method.md), `EnumMembersWithName` discards all field and member tokens that do not have the specified name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="330cb-115">반환 값</span><span class="sxs-lookup"><span data-stu-id="330cb-115">Return Value</span></span>  
  
|<span data-ttu-id="330cb-116">HRESULT</span><span class="sxs-lookup"><span data-stu-id="330cb-116">HRESULT</span></span>|<span data-ttu-id="330cb-117">설명</span><span class="sxs-lookup"><span data-stu-id="330cb-117">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="330cb-118">`EnumTypeDefs` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-118">`EnumTypeDefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="330cb-119">열거할 MemberDef 토큰이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-119">There are no MemberDef tokens to enumerate.</span></span> <span data-ttu-id="330cb-120">이런 경우 `pcTokens` 0입니다.</span><span class="sxs-lookup"><span data-stu-id="330cb-120">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="330cb-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="330cb-121">Requirements</span></span>  
 <span data-ttu-id="330cb-122">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="330cb-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="330cb-123">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="330cb-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="330cb-124">**라이브러리:** MsCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="330cb-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="330cb-125">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="330cb-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="330cb-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="330cb-126">See also</span></span>
- [<span data-ttu-id="330cb-127">IMetaDataImport 인터페이스</span><span class="sxs-lookup"><span data-stu-id="330cb-127">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="330cb-128">IMetaDataImport2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="330cb-128">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
