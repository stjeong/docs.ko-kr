---
title: IMetaDataEmit2::SetGenericParamProps 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SetGenericParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SetGenericParamProps
helpviewer_keywords:
- IMetaDataEmit2::SetGenericParamProps method [.NET Framework metadata]
- SetGenericParamProps method [.NET Framework metadata]
ms.assetid: cd93a48d-1fed-4706-bec6-a05dc3b64fbd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4c998d70fa5dd41ab4c1656f129bb77767a8ab97
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574627"
---
# <a name="imetadataemit2setgenericparamprops-method"></a><span data-ttu-id="53a5c-102">IMetaDataEmit2::SetGenericParamProps 메서드</span><span class="sxs-lookup"><span data-stu-id="53a5c-102">IMetaDataEmit2::SetGenericParamProps Method</span></span>
<span data-ttu-id="53a5c-103">지정 된 토큰에서 참조 하는 제네릭 매개 변수 정의 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-103">Sets property values for the generic parameter definition referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53a5c-104">구문</span><span class="sxs-lookup"><span data-stu-id="53a5c-104">Syntax</span></span>  
  
```  
HRESULT SetGenericParamProps (  
    [in] mdGenericParam   gp,   
    [in] DWORD            dwParamFlags,   
    [in] LPCWSTR          szName,   
    [in] DWORD            reserved,   
    [in] mdToken          rtkConstraints[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="53a5c-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="53a5c-105">Parameters</span></span>  
 `gp`  
 <span data-ttu-id="53a5c-106">[in] 토큰 값을 설정 하는 제네릭 매개 변수 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-106">[in] The token for the generic parameter definition for which to set values.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="53a5c-107">[in] 값을 [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) 제네릭 매개 변수 형식을 설명 하는 열거형입니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-107">[in] A value of the [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) enumeration that describes the type for the generic parameter.</span></span>  
  
 `szName`  
 <span data-ttu-id="53a5c-108">[in] 선택적 항목으로,</span><span class="sxs-lookup"><span data-stu-id="53a5c-108">[in] Optional.</span></span> <span data-ttu-id="53a5c-109">값을 설정 하려는 매개 변수의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-109">The name of the parameter for which to set values.</span></span>  
  
 `reserved`  
 <span data-ttu-id="53a5c-110">[in] 향후 확장성을 위해 예약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-110">[in] Reserved for future extensibility.</span></span>  
  
 `rtkConstraints`  
 <span data-ttu-id="53a5c-111">[in] 선택적 항목으로,</span><span class="sxs-lookup"><span data-stu-id="53a5c-111">[in] Optional.</span></span> <span data-ttu-id="53a5c-112">형식 제약 조건과 0으로 끝나는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-112">A zero-terminated array of type constraints.</span></span> <span data-ttu-id="53a5c-113">배열 멤버 이어야 합니다는 `mdTypeDef`, `mdTypeRef`, 또는 `mdTypeSpec` 메타 데이터 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="53a5c-113">Array members must be an `mdTypeDef`, `mdTypeRef`, or `mdTypeSpec` metadata token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53a5c-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="53a5c-114">Requirements</span></span>  
 <span data-ttu-id="53a5c-115">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="53a5c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53a5c-116">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="53a5c-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="53a5c-117">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="53a5c-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="53a5c-118">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="53a5c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53a5c-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="53a5c-119">See also</span></span>
- [<span data-ttu-id="53a5c-120">IMetaDataEmit2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="53a5c-120">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="53a5c-121">IMetaDataEmit 인터페이스</span><span class="sxs-lookup"><span data-stu-id="53a5c-121">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
