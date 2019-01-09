---
title: '&lt;DataContractSerializer&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- dataContractSerializer element
- <dataContractSerializer> element
- DataContractSerializer
- KnownTypes
ms.assetid: f41fb4d5-24e7-4059-8010-286a30bfea93
ms.openlocfilehash: c79c8e8db2a4ea4526000bcbe336d1e664f9c4c2
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150957"
---
# <a name="ltdatacontractserializergt"></a><span data-ttu-id="03e14-102">&lt;DataContractSerializer&gt;</span><span class="sxs-lookup"><span data-stu-id="03e14-102">&lt;dataContractSerializer&gt;</span></span>
<span data-ttu-id="03e14-103"><xref:System.Runtime.Serialization.DataContractSerializer>에 대한 구성 데이터를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="03e14-104">이 요소는 서로 다른 두 가지 계층 구조에서 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-104">This element occurs in two different hierarchies.</span></span> <span data-ttu-id="03e14-105">하나는 다음 스키마 계층 구조 부분에 나열되고 다른 하나는 설명 부분에 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-105">One is listed the following Schema Hierarchy section and the other is listed in the Remarks section.</span></span>  
  
 <span data-ttu-id="03e14-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="03e14-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="03e14-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="03e14-107">\<behaviors></span></span>  
<span data-ttu-id="03e14-108">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="03e14-108">\<serviceBehaviors></span></span>  
<span data-ttu-id="03e14-109">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="03e14-109">\<behavior></span></span>  
<span data-ttu-id="03e14-110">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="03e14-110">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03e14-111">구문</span><span class="sxs-lookup"><span data-stu-id="03e14-111">Syntax</span></span>  
  
```xml  
<dataContractSerializer ignoreExtensionDataObject="Boolean"
                        maxItemsInObjectGraph="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="03e14-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="03e14-112">Attributes and Elements</span></span>  
 <span data-ttu-id="03e14-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="03e14-114">특성</span><span class="sxs-lookup"><span data-stu-id="03e14-114">Attributes</span></span>  
  
|<span data-ttu-id="03e14-115">요소</span><span class="sxs-lookup"><span data-stu-id="03e14-115">Element</span></span>|<span data-ttu-id="03e14-116">설명</span><span class="sxs-lookup"><span data-stu-id="03e14-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="03e14-117">ignoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="03e14-117">ignoreExtensionDataObject</span></span>|<span data-ttu-id="03e14-118">끝점이 serialize되거나 deserialize될 때 해당 끝점에서 제공하는 데이터를 무시할지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-118">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="03e14-119">이 특성은 `<dataContractSerializer>` 요소의 `<behavior>`에서만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-119">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="03e14-120">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="03e14-120">maxItemsInObjectGraph</span></span>|<span data-ttu-id="03e14-121">serialize 또는 deserialize할 항목의 최대 수를 지정하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-121">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="03e14-122">이 특성은 65536입니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-122">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="03e14-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="03e14-123">Child Elements</span></span>  
 <span data-ttu-id="03e14-124">없음</span><span class="sxs-lookup"><span data-stu-id="03e14-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="03e14-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="03e14-125">Parent Elements</span></span>  
  
|<span data-ttu-id="03e14-126">요소</span><span class="sxs-lookup"><span data-stu-id="03e14-126">Element</span></span>|<span data-ttu-id="03e14-127">설명</span><span class="sxs-lookup"><span data-stu-id="03e14-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="03e14-128">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="03e14-128">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md)|<span data-ttu-id="03e14-129">서비스의 동작에 대한 설정 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-129">A collection of settings for the behavior of a service.</span></span>|  
|[<span data-ttu-id="03e14-130">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="03e14-130">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="03e14-131"><xref:System.Runtime.Serialization> 네임스페이스 섹션의 루트 요소를 나타내며 <xref:System.Runtime.Serialization.DataContractSerializer>의 옵션을 설정하기 위한 요소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-131">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="03e14-132">설명</span><span class="sxs-lookup"><span data-stu-id="03e14-132">Remarks</span></span>  
 <span data-ttu-id="03e14-133">이는 두 번째 계층 구조는이 항목의 소개에서 설명 했 듯이 \<X509Extension > 요소가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e14-133">As stated in the Introduction of this topic, this is the second hierarchy in which the \<X509Extension> element occurs.</span></span>  
  
 [<span data-ttu-id="03e14-134">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="03e14-134">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)  
  
 [<span data-ttu-id="03e14-135">\<dataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="03e14-135">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)  
  
 <span data-ttu-id="03e14-136">알려진 형식에 대한 자세한 내용은 <xref:System.Runtime.Serialization.DataContractSerializer>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e14-136">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03e14-137">참고 항목</span><span class="sxs-lookup"><span data-stu-id="03e14-137">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>  
 <xref:System.ServiceModel.Configuration.DataContractSerializerElement>  
 [<span data-ttu-id="03e14-138">데이터 계약 알려진 형식</span><span class="sxs-lookup"><span data-stu-id="03e14-138">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)  
 [<span data-ttu-id="03e14-139">데이터 전송 및 Serialization</span><span class="sxs-lookup"><span data-stu-id="03e14-139">Data Transfer and Serialization</span></span>](../../../../../docs/framework/wcf/feature-details/data-transfer-and-serialization.md)
