---
title: IMetaDataImport::EnumInterfaceImpls 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumInterfaceImpls
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumInterfaceImpls
helpviewer_keywords:
- IMetaDataImport::EnumInterfaceImpls method [.NET Framework metadata]
- EnumInterfaceImpls method [.NET Framework metadata]
ms.assetid: ba6e178f-128b-4e47-a13c-b4be73eb106c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c94960478e6b2eb4e7b8f1e9592b0831af3ec686
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54603770"
---
# <a name="imetadataimportenuminterfaceimpls-method"></a><span data-ttu-id="e8140-102">IMetaDataImport::EnumInterfaceImpls 메서드</span><span class="sxs-lookup"><span data-stu-id="e8140-102">IMetaDataImport::EnumInterfaceImpls Method</span></span>
<span data-ttu-id="e8140-103">인터페이스 구현을 나타내는 MethodDef 토큰을 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-103">Enumerates MethodDef tokens representing interface implementations.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8140-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8140-104">Syntax</span></span>  
  
```  
HRESULT EnumInterfaceImpls (  
   [in, out]  HCORENUM       *phEnum,   
   [in]   mdTypeDef          td,  
   [out]  mdInterfaceImpl    rImpls[],   
   [in]   ULONG              cMax,  
   [out]  ULONG*             pcImpls  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8140-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8140-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="e8140-106">[out에서] 열거자에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `td`  
 <span data-ttu-id="e8140-107">[in] 토큰 인터페이스 구현을 나타내는 MethodDef 토큰 인 열거할는 TypeDef입니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-107">[in] The token of the TypeDef whose MethodDef tokens representing interface implementations are to be enumerated.</span></span>  
  
 `rImpls`  
 <span data-ttu-id="e8140-108">[out] MethodDef 토큰을 저장 하는 데 사용 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-108">[out] The array used to store the MethodDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="e8140-109">[in] `rImpls` 배열의 최대 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-109">[in] The maximum size of the `rImpls` array.</span></span>  
  
 `pcImpls`  
 <span data-ttu-id="e8140-110">[out] 반환 된 토큰의 실제 수 `rImpls`입니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-110">[out] The actual number of tokens returned in `rImpls`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e8140-111">반환 값</span><span class="sxs-lookup"><span data-stu-id="e8140-111">Return Value</span></span>  
  
|<span data-ttu-id="e8140-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e8140-112">HRESULT</span></span>|<span data-ttu-id="e8140-113">설명</span><span class="sxs-lookup"><span data-stu-id="e8140-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="e8140-114">`EnumInterfaceImpls` 성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-114">`EnumInterfaceImpls` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="e8140-115">열거할 MethodDef 토큰이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-115">There are no MethodDef tokens to enumerate.</span></span> <span data-ttu-id="e8140-116">이런 경우 `pcImpls` 0으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8140-116">In that case, `pcImpls` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e8140-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e8140-117">Requirements</span></span>  
 <span data-ttu-id="e8140-118">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e8140-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8140-119">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e8140-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e8140-120">**라이브러리:** MsCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="e8140-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e8140-121">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8140-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8140-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="e8140-122">See also</span></span>
- [<span data-ttu-id="e8140-123">IMetaDataImport 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e8140-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="e8140-124">IMetaDataImport2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e8140-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
