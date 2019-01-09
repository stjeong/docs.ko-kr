---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: 6156f102573333ec0d5533b8f1a8506d91215f47
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151932"
---
# <a name="ltknowntypegt"></a><span data-ttu-id="4de6c-102">&lt;knownType&gt;</span><span class="sxs-lookup"><span data-stu-id="4de6c-102">&lt;knownType&gt;</span></span>
<span data-ttu-id="4de6c-103">deserialization을 수행하는 동안 <xref:System.Runtime.Serialization.DataContractSerializer>에서 사용하는 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-103">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="4de6c-104">요소는 "선언된 형식"의 필드 또는 속성에서 반환하는 "알려진 형식"을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-104">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="4de6c-105">자세한 내용은 [데이터 계약 알려진 형식을](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-105">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="4de6c-106">\<system.runtime.serialization ></span><span class="sxs-lookup"><span data-stu-id="4de6c-106">\<system.runtime.serialization></span></span>  
<span data-ttu-id="4de6c-107">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="4de6c-107">\<dataContractSerializer></span></span>  
<span data-ttu-id="4de6c-108">\<declaredTypes > 요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-108">\<declaredTypes> Element</span></span>  
<span data-ttu-id="4de6c-109">\<추가 >의 \<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="4de6c-109">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="4de6c-110">\<knownType > 요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-110">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4de6c-111">구문</span><span class="sxs-lookup"><span data-stu-id="4de6c-111">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="4de6c-112">형식</span><span class="sxs-lookup"><span data-stu-id="4de6c-112">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4de6c-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-113">Attributes and Elements</span></span>  
 <span data-ttu-id="4de6c-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4de6c-115">특성</span><span class="sxs-lookup"><span data-stu-id="4de6c-115">Attributes</span></span>  
  
|<span data-ttu-id="4de6c-116">특성</span><span class="sxs-lookup"><span data-stu-id="4de6c-116">Attribute</span></span>|<span data-ttu-id="4de6c-117">설명</span><span class="sxs-lookup"><span data-stu-id="4de6c-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4de6c-118">형식</span><span class="sxs-lookup"><span data-stu-id="4de6c-118">type</span></span>|<span data-ttu-id="4de6c-119">형식(네임스페이스 포함), 어셈블리 이름, 버전, 문화권 및 공개 키 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-119">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4de6c-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-120">Child Elements</span></span>  
  
|<span data-ttu-id="4de6c-121">요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-121">Element</span></span>|<span data-ttu-id="4de6c-122">설명</span><span class="sxs-lookup"><span data-stu-id="4de6c-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4de6c-123">\<매개 변수 ></span><span class="sxs-lookup"><span data-stu-id="4de6c-123">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="4de6c-124">선언된 형식이 제네릭 형식이면 매개 변수 인덱스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-124">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4de6c-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-125">Parent Elements</span></span>  
  
|<span data-ttu-id="4de6c-126">요소</span><span class="sxs-lookup"><span data-stu-id="4de6c-126">Element</span></span>|<span data-ttu-id="4de6c-127">설명</span><span class="sxs-lookup"><span data-stu-id="4de6c-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4de6c-128">\<add></span><span class="sxs-lookup"><span data-stu-id="4de6c-128">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="4de6c-129">선언된 형식을 선언된 형식의 컬렉션에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-129">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4de6c-130">설명</span><span class="sxs-lookup"><span data-stu-id="4de6c-130">Remarks</span></span>  
 <span data-ttu-id="4de6c-131">알려진된 형식에 대 한 자세한 내용은 참조 하세요. [데이터 계약 알려진 형식을](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) 고 <xref:System.Runtime.Serialization.DataContractSerializer>입니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-131">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="4de6c-132">참조 된 [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) 이 요소를 사용 하는 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4de6c-132">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4de6c-133">예제</span><span class="sxs-lookup"><span data-stu-id="4de6c-133">Example</span></span>  
  
```xml  
<add type="MyCompany.Library.Shape,
           MyAssembly, Version=2.0.0.0, Culture=neutral,
           PublicKeyToken=XXXXXX, processorArchitecture=MSIL">
  <knownType type="MyCompany.Library.Circle,
                   MyAssembly, Version=2.0.0.0, Culture=neutral,
                   PublicKeyToken=XXXXXX,
                   processorArchitecture=MSIL"/>
</add>
```  
  
## <a name="see-also"></a><span data-ttu-id="4de6c-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4de6c-134">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 [<span data-ttu-id="4de6c-135">데이터 계약 알려진 형식</span><span class="sxs-lookup"><span data-stu-id="4de6c-135">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)  
 [<span data-ttu-id="4de6c-136">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="4de6c-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
 [<span data-ttu-id="4de6c-137">\<add></span><span class="sxs-lookup"><span data-stu-id="4de6c-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
