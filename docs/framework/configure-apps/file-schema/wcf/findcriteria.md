---
title: '&lt;findCriteria&gt;'
ms.date: 03/30/2017
ms.assetid: 5454cd19-6bf5-4ba8-94d1-f58d10dc1917
ms.openlocfilehash: b90e6cab923075dbf750dc0d26a0eb1196cfde32
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741249"
---
# <a name="ltfindcriteriagt"></a><span data-ttu-id="52e64-102">&lt;findCriteria&gt;</span><span class="sxs-lookup"><span data-stu-id="52e64-102">&lt;findCriteria&gt;</span></span>
<span data-ttu-id="52e64-103">클라이언트 응용 프로그램에서 검색 서비스를 찾기 위해 사용하는 조건 집합을 제공하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-103">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="52e64-104">조건 (찾으려는 서비스 지정) 하는 검색 조건으로 그룹화 할 수 있습니다 및 찾기 종료 조건 (검색 지속 기간).</span><span class="sxs-lookup"><span data-stu-id="52e64-104">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>  
  
 <span data-ttu-id="52e64-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="52e64-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="52e64-106">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="52e64-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52e64-107">구문</span><span class="sxs-lookup"><span data-stu-id="52e64-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String"
                   namespace="String" />
            </contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI" />
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      </standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="52e64-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="52e64-108">Attributes and Elements</span></span>  
 <span data-ttu-id="52e64-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="52e64-110">특성</span><span class="sxs-lookup"><span data-stu-id="52e64-110">Attributes</span></span>  
  
|<span data-ttu-id="52e64-111">특성</span><span class="sxs-lookup"><span data-stu-id="52e64-111">Attribute</span></span>|<span data-ttu-id="52e64-112">설명</span><span class="sxs-lookup"><span data-stu-id="52e64-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="52e64-113">duration</span><span class="sxs-lookup"><span data-stu-id="52e64-113">duration</span></span>|<span data-ttu-id="52e64-114">네트워크에서 서비스로부터 응답을 기다리는 최대 시간을 지정하는 Timespan 값입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-114">A Timespan value that specifies the maximum time to wait for replies from services on the network.</span></span> <span data-ttu-id="52e64-115">기본 시간은 20초입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-115">The default duration is 20 seconds.</span></span>|  
|<span data-ttu-id="52e64-116">maxResults</span><span class="sxs-lookup"><span data-stu-id="52e64-116">maxResults</span></span>|<span data-ttu-id="52e64-117">네트워크 또는 인터넷에서 서비스로부터 기다리는 최대 응답 횟수를 지정하는 정수입니다</span><span class="sxs-lookup"><span data-stu-id="52e64-117">An integer that specifies the maximum number of replies to wait for, from services on a network or the Internet.</span></span> <span data-ttu-id="52e64-118">`duration` 특성에 지정된 시간이 경과되기 전에 최대 응답이 수신되는 경우 찾기 작업이 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-118">If maximum replies are received before the value specified in the `duration` attribute has elapsed, the find operation ends.</span></span>|  
|<span data-ttu-id="52e64-119">scopeMatchBy</span><span class="sxs-lookup"><span data-stu-id="52e64-119">scopeMatchBy</span></span>|<span data-ttu-id="52e64-120">Probe 메시지의 범위와 엔드포인트의 범위를 일치시키는 동안 사용할 일치 알고리즘을 지정하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-120">A URI that specify the matching algorithm to use while matching the scopes in the Probe message with that of the endpoint.</span></span><br /><br /> <span data-ttu-id="52e64-121">다섯 가지의 범위 일치 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-121">There are five supported scope-matching rules.</span></span> <span data-ttu-id="52e64-122">범위 일치 규칙을 지정하지 않으면 `ScopeMatchByPrefix`가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-122">If you do not specify a scope-matching rule, `ScopeMatchByPrefix` is used.</span></span> <span data-ttu-id="52e64-123">이에 대한 자세한 내용은 <xref:System.ServiceModel.Discovery.FindCriteria>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="52e64-123">For more information on this, see <xref:System.ServiceModel.Discovery.FindCriteria>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="52e64-124">자식 요소</span><span class="sxs-lookup"><span data-stu-id="52e64-124">Child Elements</span></span>  
  
|<span data-ttu-id="52e64-125">요소</span><span class="sxs-lookup"><span data-stu-id="52e64-125">Element</span></span>|<span data-ttu-id="52e64-126">설명</span><span class="sxs-lookup"><span data-stu-id="52e64-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="52e64-127">\<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="52e64-127">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="52e64-128">워크플로 서비스 계약 형식의 이름을 포함 하는 구성 요소의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-128">A collection of configuration elements that contain the names of workflow service contract types.</span></span>|  
|<span data-ttu-id="52e64-129">\<확장 >의 \<findCriteria ></span><span class="sxs-lookup"><span data-stu-id="52e64-129">\<extensions> of \<findCriteria></span></span>|<span data-ttu-id="52e64-130">확장명을 제공하는 XML 요소 개체의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-130">A collection of XML element objects that provide extensions.</span></span>|  
|[<span data-ttu-id="52e64-131">\<scopes></span><span class="sxs-lookup"><span data-stu-id="52e64-131">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="52e64-132">찾기 작업 중에 특정 서비스를 찾기 위해 사용하는 절대 URI를 포함하는 개체의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-132">A collection of objects that contain absolute URIs that are used during a find operation to locate a specific service or services.</span></span><br /><br /> <span data-ttu-id="52e64-133">특정 서비스를 찾으면 서비스 URI와 범위 URI 간에 성공한 일치 항목이 생깁니다. 이때 경우에 따라 일치의 복잡한 문제를 처리하는 범위 규칙이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-133">If the specific service is found, a successful match has been made between the service URI and the Scope URI, sometimes with the help of scope rules that handle complications of matching.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="52e64-134">부모 요소</span><span class="sxs-lookup"><span data-stu-id="52e64-134">Parent Elements</span></span>  
  
|<span data-ttu-id="52e64-135">요소</span><span class="sxs-lookup"><span data-stu-id="52e64-135">Element</span></span>|<span data-ttu-id="52e64-136">설명</span><span class="sxs-lookup"><span data-stu-id="52e64-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="52e64-137">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="52e64-137">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="52e64-138">응용 프로그램에서 서비스 검색 프로세스에 클라이언트로 참여하기 위해 필요한 설정이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="52e64-138">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="52e64-139">참고자료</span><span class="sxs-lookup"><span data-stu-id="52e64-139">See also</span></span>
- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
