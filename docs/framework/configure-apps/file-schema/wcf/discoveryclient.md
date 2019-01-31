---
title: <discoveryClient>
ms.date: 03/30/2017
ms.assetid: a78f74c3-1152-4149-ab29-3f12d316caeb
ms.openlocfilehash: 512a91bf25180606213eb9eb3b4f7c6a0cb4cbbf
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55284807"
---
# <a name="discoveryclient"></a><span data-ttu-id="d1f41-101">\<discoveryClient></span><span class="sxs-lookup"><span data-stu-id="d1f41-101">\<discoveryClient></span></span>
<span data-ttu-id="d1f41-102">클라이언트 응용 프로그램에서 런타임에 검색 가능 서비스를 자동으로 검색하고 해당 주소를 찾을 수 있도록 하는 사용자 지정 바인딩을 만들기 위한 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f41-102">A configuration element for creating a custom binding that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>  
  
<span data-ttu-id="d1f41-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="d1f41-103">\<system.serviceModel></span></span>  
<span data-ttu-id="d1f41-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="d1f41-104">\<bindings></span></span>  
<span data-ttu-id="d1f41-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="d1f41-105">\<customBinding></span></span>  
<span data-ttu-id="d1f41-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="d1f41-106">\<binding></span></span>  
<span data-ttu-id="d1f41-107">\<discoveryClient></span><span class="sxs-lookup"><span data-stu-id="d1f41-107">\<discoveryClient></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1f41-108">구문</span><span class="sxs-lookup"><span data-stu-id="d1f41-108">Syntax</span></span>  
  
```xml  
<discoveryClient discoveryEndpoint="String">
  <findCriteria duration="TimeSpan"
                maxResults="Integer"
                scopeMatchBy="Uri">
    <contractTypeNames>
      <add name="String"
           namespace="String" />
    </contractTypeNames>
    <extensions />
    <scopes>
      <add scope="URI"/>
    </scopes>
  </findCriteria>
</discoveryClient>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d1f41-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="d1f41-109">Attributes and Elements</span></span>  
 <span data-ttu-id="d1f41-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f41-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d1f41-111">특성</span><span class="sxs-lookup"><span data-stu-id="d1f41-111">Attributes</span></span>  
  
|<span data-ttu-id="d1f41-112">특성</span><span class="sxs-lookup"><span data-stu-id="d1f41-112">Attribute</span></span>|<span data-ttu-id="d1f41-113">설명</span><span class="sxs-lookup"><span data-stu-id="d1f41-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d1f41-114">discoveryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1f41-114">discoveryEndpoint</span></span>|<span data-ttu-id="d1f41-115">클라이언트 응용 프로그램에서 런타임에 검색 가능한 서비스를 자동으로 검색하고 해당 주소를 찾을 수 있도록 하는 검색 엔드포인트의 이름을 포함하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f41-115">A string that contains the name of the Discovery Endpoint that enables a client application to automatically search for a discoverable service and find its address at runtime.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d1f41-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="d1f41-116">Child Elements</span></span>  
  
|<span data-ttu-id="d1f41-117">요소</span><span class="sxs-lookup"><span data-stu-id="d1f41-117">Element</span></span>|<span data-ttu-id="d1f41-118">설명</span><span class="sxs-lookup"><span data-stu-id="d1f41-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d1f41-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="d1f41-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="d1f41-120">클라이언트 응용 프로그램에서 검색 서비스를 찾기 위해 사용하는 조건 집합을 제공하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f41-120">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="d1f41-121">조건 (찾으려는 서비스 지정) 하는 검색 조건으로 그룹화 할 수 있습니다 및 찾기 종료 조건 (검색 지속 기간).</span><span class="sxs-lookup"><span data-stu-id="d1f41-121">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d1f41-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="d1f41-122">Parent Elements</span></span>  
  
|<span data-ttu-id="d1f41-123">요소</span><span class="sxs-lookup"><span data-stu-id="d1f41-123">Element</span></span>|<span data-ttu-id="d1f41-124">설명</span><span class="sxs-lookup"><span data-stu-id="d1f41-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d1f41-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="d1f41-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="d1f41-126">사용자 지정 바인딩의 모든 바인딩 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f41-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d1f41-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="d1f41-127">See also</span></span>
- <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>
- <xref:System.ServiceModel.Discovery.Configuration.DiscoveryClientElement>
