---
title: '&lt;scopes&gt;'
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 1235b483f63ab71405803c16f2d3c9926b15cfad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642989"
---
# <a name="ltscopesgt"></a><span data-ttu-id="8145b-102">&lt;scopes&gt;</span><span class="sxs-lookup"><span data-stu-id="8145b-102">&lt;scopes&gt;</span></span>
<span data-ttu-id="8145b-103">쿼리 중에 서비스 엔드포인트를 필터링하기 위해 사용할 수 있는 사용자 지정 범위 URI를 지정하는 구성 요소의 컬렉션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="8145b-103">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>  
  
<span data-ttu-id="8145b-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="8145b-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="8145b-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="8145b-105">\<behaviors></span></span>  
<span data-ttu-id="8145b-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="8145b-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="8145b-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="8145b-107">\<behavior></span></span>  
<span data-ttu-id="8145b-108">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="8145b-108">\<endpointDiscovery></span></span>  
<span data-ttu-id="8145b-109">\<scopes></span><span class="sxs-lookup"><span data-stu-id="8145b-109">\<scopes></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8145b-110">구문</span><span class="sxs-lookup"><span data-stu-id="8145b-110">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI" />
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8145b-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="8145b-111">Attributes and Elements</span></span>  
 <span data-ttu-id="8145b-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8145b-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8145b-113">특성</span><span class="sxs-lookup"><span data-stu-id="8145b-113">Attributes</span></span>  
 <span data-ttu-id="8145b-114">없음</span><span class="sxs-lookup"><span data-stu-id="8145b-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8145b-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="8145b-115">Child Elements</span></span>  
  
|<span data-ttu-id="8145b-116">특성</span><span class="sxs-lookup"><span data-stu-id="8145b-116">Attribute</span></span>|<span data-ttu-id="8145b-117">설명</span><span class="sxs-lookup"><span data-stu-id="8145b-117">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="8145b-118">\<add></span><span class="sxs-lookup"><span data-stu-id="8145b-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|<span data-ttu-id="8145b-119">서비스를 찾기 위한 일치 기준으로 사용할 수 있는 엔드포인트의 범위 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8145b-119">Adds the scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8145b-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="8145b-120">Parent Elements</span></span>  
  
|<span data-ttu-id="8145b-121">요소</span><span class="sxs-lookup"><span data-stu-id="8145b-121">Element</span></span>|<span data-ttu-id="8145b-122">설명</span><span class="sxs-lookup"><span data-stu-id="8145b-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8145b-123">\<endpointDiscovery></span><span class="sxs-lookup"><span data-stu-id="8145b-123">\<endpointDiscovery></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|<span data-ttu-id="8145b-124">검색 기능, 범위 및 해당 메타데이터에 대한 사용자 지정 확장 등 엔드포인트에 대한 다양한 검색 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8145b-124">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8145b-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="8145b-125">See also</span></span>
- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
