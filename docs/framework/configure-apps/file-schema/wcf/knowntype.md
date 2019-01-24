---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: cb36a0d1d1ceb13a6db902904783ee15b14e673b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541068"
---
# <a name="ltknowntypegt"></a><span data-ttu-id="83106-102">&lt;knownType&gt;</span><span class="sxs-lookup"><span data-stu-id="83106-102">&lt;knownType&gt;</span></span>
<span data-ttu-id="83106-103">deserialization을 수행하는 동안 <xref:System.Runtime.Serialization.DataContractSerializer>에서 사용하는 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-103">Specifies a type to be used by <xref:System.Runtime.Serialization.DataContractSerializer> during deserialization.</span></span> <span data-ttu-id="83106-104">요소는 "선언된 형식"의 필드 또는 속성에서 반환하는 "알려진 형식"을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-104">The element specifies a "known type" that is returned by a field or property of a "declared type."</span></span> <span data-ttu-id="83106-105">자세한 내용은 [데이터 계약 알려진 형식을](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-105">For more information, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
 <span data-ttu-id="83106-106">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="83106-106">\<system.runtime.serialization></span></span>  
<span data-ttu-id="83106-107">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="83106-107">\<dataContractSerializer></span></span>  
<span data-ttu-id="83106-108">\<declaredTypes > 요소</span><span class="sxs-lookup"><span data-stu-id="83106-108">\<declaredTypes> Element</span></span>  
<span data-ttu-id="83106-109">\<추가 >의 \<declaredTypes ></span><span class="sxs-lookup"><span data-stu-id="83106-109">\<add> of \<declaredTypes></span></span>  
<span data-ttu-id="83106-110">\<knownType > 요소</span><span class="sxs-lookup"><span data-stu-id="83106-110">\<knownType> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83106-111">구문</span><span class="sxs-lookup"><span data-stu-id="83106-111">Syntax</span></span>  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a><span data-ttu-id="83106-112">형식</span><span class="sxs-lookup"><span data-stu-id="83106-112">Type</span></span>  
 `string`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="83106-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="83106-113">Attributes and Elements</span></span>  
 <span data-ttu-id="83106-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="83106-115">특성</span><span class="sxs-lookup"><span data-stu-id="83106-115">Attributes</span></span>  
  
|<span data-ttu-id="83106-116">특성</span><span class="sxs-lookup"><span data-stu-id="83106-116">Attribute</span></span>|<span data-ttu-id="83106-117">설명</span><span class="sxs-lookup"><span data-stu-id="83106-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="83106-118">형식</span><span class="sxs-lookup"><span data-stu-id="83106-118">type</span></span>|<span data-ttu-id="83106-119">형식(네임스페이스 포함), 어셈블리 이름, 버전, 문화권 및 공개 키 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-119">Specifies the type (including namespace), assembly name, version, culture, and public key token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="83106-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="83106-120">Child Elements</span></span>  
  
|<span data-ttu-id="83106-121">요소</span><span class="sxs-lookup"><span data-stu-id="83106-121">Element</span></span>|<span data-ttu-id="83106-122">설명</span><span class="sxs-lookup"><span data-stu-id="83106-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="83106-123">\<parameter></span><span class="sxs-lookup"><span data-stu-id="83106-123">\<parameter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|<span data-ttu-id="83106-124">선언된 형식이 제네릭 형식이면 매개 변수 인덱스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-124">Specifies a parameter index when the declared type is a generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="83106-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="83106-125">Parent Elements</span></span>  
  
|<span data-ttu-id="83106-126">요소</span><span class="sxs-lookup"><span data-stu-id="83106-126">Element</span></span>|<span data-ttu-id="83106-127">설명</span><span class="sxs-lookup"><span data-stu-id="83106-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="83106-128">\<add></span><span class="sxs-lookup"><span data-stu-id="83106-128">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|<span data-ttu-id="83106-129">선언된 형식을 선언된 형식의 컬렉션에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="83106-129">Adds a declared type to the collection of declared types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83106-130">설명</span><span class="sxs-lookup"><span data-stu-id="83106-130">Remarks</span></span>  
 <span data-ttu-id="83106-131">알려진된 형식에 대 한 자세한 내용은 참조 하세요. [데이터 계약 알려진 형식을](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) 고 <xref:System.Runtime.Serialization.DataContractSerializer>입니다.</span><span class="sxs-lookup"><span data-stu-id="83106-131">For more information about known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) and <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="83106-132">참조 된 [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) 이 요소를 사용 하는 예입니다.</span><span class="sxs-lookup"><span data-stu-id="83106-132">See the [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) for an example of using this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="83106-133">예제</span><span class="sxs-lookup"><span data-stu-id="83106-133">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="83106-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="83106-134">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [<span data-ttu-id="83106-135">데이터 계약 알려진 형식</span><span class="sxs-lookup"><span data-stu-id="83106-135">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [<span data-ttu-id="83106-136">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="83106-136">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [<span data-ttu-id="83106-137">\<add></span><span class="sxs-lookup"><span data-stu-id="83106-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
