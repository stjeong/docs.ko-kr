---
title: IIdentityAuthority 인터페이스
ms.date: 03/30/2017
api_name:
- IIdentityAuthority
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IIdentityAuthority
helpviewer_keywords:
- IIdentityAuthority interface [.NET Framework fusion]
ms.assetid: 6277f914-51a8-49be-bec6-52d6d648527d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ab8965ca5d6c9c96cea5f5b351547ce2d4dfacc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54546282"
---
# <a name="iidentityauthority-interface"></a><span data-ttu-id="3e7d7-102">IIdentityAuthority 인터페이스</span><span class="sxs-lookup"><span data-stu-id="3e7d7-102">IIdentityAuthority Interface</span></span>
<span data-ttu-id="3e7d7-103">코드 개체에 대 한 id 키를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-103">Manages identity keys for code objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3e7d7-104">메서드</span><span class="sxs-lookup"><span data-stu-id="3e7d7-104">Methods</span></span>  
  
|<span data-ttu-id="3e7d7-105">메서드</span><span class="sxs-lookup"><span data-stu-id="3e7d7-105">Method</span></span>|<span data-ttu-id="3e7d7-106">설명</span><span class="sxs-lookup"><span data-stu-id="3e7d7-106">Description</span></span>|  
|------------|-----------------|  
|`IIdentityAuthority::AreDefinitionsEqual`|<span data-ttu-id="3e7d7-107">두 개의 지정 되었는지 여부를 나타내는 값을 가져옵니다 [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) 인스턴스는 서로 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-107">Gets a value that indicates whether the two specified [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instances are equal.</span></span>|  
|`IIdentityAuthority::AreReferencesEqual`|<span data-ttu-id="3e7d7-108">두 개의 지정 되었는지 여부를 나타내는 값을 가져옵니다 [IReferenceIdentity](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md) 인스턴스는 서로 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-108">Gets a value that indicates whether the two specified [IReferenceIdentity](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md) instances are equal.</span></span>|  
|`IIdentityAuthority::AreTextualDefinitionsEqual`|<span data-ttu-id="3e7d7-109">두 지정 된 문자열 정의 id 표현이 같은지 여부를 나타내는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-109">Gets a value that indicates whether the two specified string definition identity representations are equal.</span></span>|  
|`IIdentityAuthority::AreTextualReferencesEqual`|<span data-ttu-id="3e7d7-110">두 지정 된 문자열 참조 id 표현이 같은지 여부를 나타내는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-110">Gets a value that indicates whether the two specified string reference identity representations are equal.</span></span>|  
|`IIdentityAuthority::CreateDefinition`|<span data-ttu-id="3e7d7-111">새 포인터를 가져옵니다 `IDefinitionIdentity` 현재 범위에 있는 코드 개체를 나타내는 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-111">Gets a pointer to a new `IDefinitionIdentity` instance that represents the code object in the current scope.</span></span>|  
|`IIdentityAuthority::CreateReference`|<span data-ttu-id="3e7d7-112">새 포인터를 가져옵니다 `IReferenceIdentity` 현재 범위에 있는 코드 개체를 나타내는 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-112">Gets a pointer to a new `IReferenceIdentity` instance that represents the code object in the current scope.</span></span>|  
|`IIdentityAuthority::DefinitionToText`|<span data-ttu-id="3e7d7-113">지정 된 형식의 문자열 버전을 가져옵니다 `IDefinitionIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-113">Gets a formatted string version of the specified `IDefinitionIdentity`.</span></span>|  
|`IIdentityAuthority::DefinitionToTextBuffer`|<span data-ttu-id="3e7d7-114">지정 된 문자열 버전을 사용 하 여 지정 된 와이드 문자 버퍼를 채웁니다 `IDefinitionIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-114">Fills the specified wide character buffer with a string version of the specified `IDefinitionIdentity`.</span></span>|  
|`IIdentityAuthority::DoesDefinitionMatchReference`|<span data-ttu-id="3e7d7-115">나타내는 값을 가져옵니다 여부를 지정 된 `IDefinitionIdentity` 고 `IReferenceIdentity` 인스턴스가 동일한 코드 개체를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-115">Gets a value that indicates whether the specified `IDefinitionIdentity` and `IReferenceIdentity` instances refer to the same code object.</span></span>|  
|`IIdentityAuthority::DoesTextualDefinitionMatchTextualReference`|<span data-ttu-id="3e7d7-116">지정된 된 문자열이 동일한 코드 개체를 참조 하는지 여부를 나타내는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-116">Gets a value that indicates whether the specified strings refer to the same code object.</span></span>|  
|`IIdentityAuthority::GenerateDefinitionKey`|<span data-ttu-id="3e7d7-117">지정 된 문자열을 새로 만든된 키에 대 한 포인터를 가져옵니다 `IDefinitionIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-117">Gets a pointer to a newly created string key for the specified `IDefinitionIdentity`.</span></span>|  
|`IIdentityAuthority::GenerateReferenceKey`|<span data-ttu-id="3e7d7-118">지정 된 문자열을 새로 만든된 키에 대 한 포인터를 가져옵니다 `IReferenceIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-118">Gets a pointer to a newly created string key for the specified `IReferenceIdentity`.</span></span>|  
|`IIdentityAuthority::HashDefinition`|<span data-ttu-id="3e7d7-119">지정 된 해시 값을 가져옵니다 `IDefinitionIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-119">Gets a hash value for the specified `IDefinitionIdentity`.</span></span>|  
|`IIdentityAuthority::HashReference`|<span data-ttu-id="3e7d7-120">지정 된 해시 값을 가져옵니다 `IreferenceIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-120">Gets a hash value for the specified `IreferenceIdentity`.</span></span>|  
|`IIdentityAuthority::ReferenceToText`|<span data-ttu-id="3e7d7-121">지정 된 형식의 문자열 버전을 가져옵니다 `IReferenceIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-121">Gets a formatted string version of the specified `IReferenceIdentity`.</span></span>|  
|`IIdentityAuthority::ReferenceToTextBuffer`|<span data-ttu-id="3e7d7-122">지정 된 문자열 버전을 사용 하 여 지정 된 와이드 문자 버퍼를 채웁니다 `IReferenceIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-122">Fills the specified wide character buffer with a string version of the specified `IReferenceIdentity`.</span></span>|  
|`IIdentityAuthority::TextToDefinition`|<span data-ttu-id="3e7d7-123">한 인터페이스 포인터를 가져옵니다는 `IDefinitionIdentity` 형식 지정 문자열로 지정 된 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-123">Gets an interface pointer to an `IDefinitionIdentity` instance generated from the specified formatted string.</span></span>|  
|`IIdentityAuthority::TextToReference`|<span data-ttu-id="3e7d7-124">한 인터페이스 포인터를 가져옵니다는 `IReferenceIdentity` 형식 지정 문자열로 지정 된 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-124">Gets an interface pointer to an `IReferenceIdentity` instance generated from the specified formatted string.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3e7d7-125">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3e7d7-125">Requirements</span></span>  
 <span data-ttu-id="3e7d7-126">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="3e7d7-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e7d7-127">**헤더:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="3e7d7-127">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="3e7d7-128">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e7d7-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e7d7-129">참고자료</span><span class="sxs-lookup"><span data-stu-id="3e7d7-129">See also</span></span>
- [<span data-ttu-id="3e7d7-130">Fusion 인터페이스</span><span class="sxs-lookup"><span data-stu-id="3e7d7-130">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
