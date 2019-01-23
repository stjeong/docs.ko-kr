---
title: '&lt;system.runtime.serialization&gt;'
ms.date: 03/30/2017
ms.assetid: a8cebf4c-06d2-4667-8f5b-c3e1fc90df6f
ms.openlocfilehash: 6321ab192161468142a4cd4d2155d3f787bb0165
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600263"
---
# <a name="ltsystemruntimeserializationgt"></a><span data-ttu-id="299db-102">&lt;system.runtime.serialization&gt;</span><span class="sxs-lookup"><span data-stu-id="299db-102">&lt;system.runtime.serialization&gt;</span></span>
<span data-ttu-id="299db-103"><xref:System.Runtime.Serialization> 네임스페이스 섹션의 루트 요소를 나타내며 <xref:System.Runtime.Serialization.DataContractSerializer>의 옵션을 설정하기 위한 요소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="299db-103">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="299db-104">system.runtime.serialization</span><span class="sxs-lookup"><span data-stu-id="299db-104">system.runtime.serialization</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="299db-105">구문</span><span class="sxs-lookup"><span data-stu-id="299db-105">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="299db-106">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="299db-106">Attributes and Elements</span></span>  
 <span data-ttu-id="299db-107">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="299db-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="299db-108">특성</span><span class="sxs-lookup"><span data-stu-id="299db-108">Attributes</span></span>  
 <span data-ttu-id="299db-109">없음</span><span class="sxs-lookup"><span data-stu-id="299db-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="299db-110">자식 요소</span><span class="sxs-lookup"><span data-stu-id="299db-110">Child Elements</span></span>  
  
|<span data-ttu-id="299db-111">요소</span><span class="sxs-lookup"><span data-stu-id="299db-111">Element</span></span>|<span data-ttu-id="299db-112">설명</span><span class="sxs-lookup"><span data-stu-id="299db-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="299db-113">\<dataContractSerializer></span><span class="sxs-lookup"><span data-stu-id="299db-113">\<dataContractSerializer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-of-system-runtime-serialization.md)|<span data-ttu-id="299db-114">deserialization 시 사용할 알려진 형식을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="299db-114">Enables addition of known types to be used when deserialization.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="299db-115">부모 요소</span><span class="sxs-lookup"><span data-stu-id="299db-115">Parent Elements</span></span>  
  
|<span data-ttu-id="299db-116">요소</span><span class="sxs-lookup"><span data-stu-id="299db-116">Element</span></span>|<span data-ttu-id="299db-117">설명</span><span class="sxs-lookup"><span data-stu-id="299db-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="299db-118">\<configuration> 요소</span><span class="sxs-lookup"><span data-stu-id="299db-118">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="299db-119">구성의 최상위 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="299db-119">The top level element for configuration.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="299db-120">참고자료</span><span class="sxs-lookup"><span data-stu-id="299db-120">See also</span></span>
- <xref:System.Runtime.Serialization>
- [<span data-ttu-id="299db-121">데이터 계약 사용</span><span class="sxs-lookup"><span data-stu-id="299db-121">Using Data Contracts</span></span>](../../../../../docs/framework/wcf/feature-details/using-data-contracts.md)
- [<span data-ttu-id="299db-122">데이터 계약 알려진 형식</span><span class="sxs-lookup"><span data-stu-id="299db-122">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
