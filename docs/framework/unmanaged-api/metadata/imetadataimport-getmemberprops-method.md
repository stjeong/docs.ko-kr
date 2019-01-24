---
title: IMetaDataImport::GetMemberProps 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberProps
helpviewer_keywords:
- IMetaDataImport::GetMemberProps method [.NET Framework metadata]
- GetMemberProps method [.NET Framework metadata]
ms.assetid: 42790918-4142-4938-b8f4-a56979a55846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 98d7be5adc81cff09b121265e7d5b5f712122607
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611412"
---
# <a name="imetadataimportgetmemberprops-method"></a><span data-ttu-id="f2766-102">IMetaDataImport::GetMemberProps 메서드</span><span class="sxs-lookup"><span data-stu-id="f2766-102">IMetaDataImport::GetMemberProps Method</span></span>
<span data-ttu-id="f2766-103">이름, 이진 서명 및 상대 가상 주소를 포함 한 메타 데이터 정보를 가져옵니다는 <xref:System.Type> 지정 된 메타 데이터 토큰에서 참조 하는 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-103">Gets metadata information, including the name, binary signature, and relative virtual address, of the <xref:System.Type> member referenced by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2766-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2766-104">Syntax</span></span>  
  
```  
HRESULT GetMemberProps (  
   [in]  mdToken           mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] DWORD             *pdwAttr,  
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] ULONG             *pulCodeRVA,   
   [out] DWORD             *pdwImplFlags,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f2766-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2766-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="f2766-106">[in] 연결 된 메타 데이터를 가져올 멤버를 참조 하는 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-106">[in] The token that references the member to get the associated metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="f2766-107">[out] 멤버의 클래스를 나타내는 메타 데이터 토큰에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-107">[out] A pointer to the metadata token that represents the class of the member.</span></span>  
  
 `szMember`  
 <span data-ttu-id="f2766-108">[out] 멤버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-108">[out] The name of the member.</span></span>  
  
 `cchMember`  
 <span data-ttu-id="f2766-109">[in] 와이드 문자에서 크기를 `szMember` 버퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-109">[in] The size in wide characters of the `szMember` buffer.</span></span>  
  
 `pchMember`  
 <span data-ttu-id="f2766-110">[out] 반환 된 이름의 와이드 문자 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-110">[out] The size in wide characters of the returned name.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="f2766-111">[out] 모든 플래그 멤버에 적용 되는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-111">[out] Any flag values applied to the member.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="f2766-112">[out] 멤버의 이진 메타 데이터 서명에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-112">[out] A pointer to the binary metadata signature of the member.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="f2766-113">[out] 크기 (바이트) `ppvSigBlob`합니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-113">[out] The size in bytes of `ppvSigBlob`.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="f2766-114">[out] 멤버의 상대 가상 주소에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-114">[out] A pointer to the relative virtual address of the member.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="f2766-115">[out] 멤버에 연결 된 모든 메서드 구현 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-115">[out] Any method implementation flags associated with the member.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="f2766-116">[out] 표시 하는 플래그를 <xref:System.ValueType>입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-116">[out] A flag that marks a <xref:System.ValueType>.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="f2766-117">[out] 이 멤버에 의해 반환 되는 상수 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-117">[out] A constant string value returned by this member.</span></span>  
  
 `pcchValue`  
 <span data-ttu-id="f2766-118">[out] 크기의 문자 `ppValue`, 또는 경우에는 0 `ppValue` 문자열이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2766-118">[out] The size in characters of `ppValue`, or zero if `ppValue` does not hold a string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2766-119">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f2766-119">Requirements</span></span>  
 <span data-ttu-id="f2766-120">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f2766-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2766-121">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f2766-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f2766-122">**라이브러리:** MsCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="f2766-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f2766-123">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2766-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2766-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="f2766-124">See also</span></span>
- [<span data-ttu-id="f2766-125">IMetaDataImport 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f2766-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="f2766-126">IMetaDataImport2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f2766-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
