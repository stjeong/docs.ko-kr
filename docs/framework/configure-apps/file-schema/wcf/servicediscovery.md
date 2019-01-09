---
title: '&lt;serviceDiscovery&gt;'
ms.date: 03/30/2017
ms.assetid: a3c68a4a-fc95-43c5-aacb-785936c0cf39
ms.openlocfilehash: 2b3061274ef670ccd672c3155ca7285d567834bd
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146903"
---
# <a name="ltservicediscoverygt"></a><span data-ttu-id="6c2ac-102">&lt;serviceDiscovery&gt;</span><span class="sxs-lookup"><span data-stu-id="6c2ac-102">&lt;serviceDiscovery&gt;</span></span>
<span data-ttu-id="6c2ac-103">서비스 엔드포인트의 검색 기능을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-103">Specifies the discoverability of service endpoints.</span></span>  
  
 <span data-ttu-id="6c2ac-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6c2ac-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="6c2ac-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="6c2ac-105">\<behaviors></span></span>  
<span data-ttu-id="6c2ac-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="6c2ac-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="6c2ac-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="6c2ac-107">\<behavior></span></span>  
<span data-ttu-id="6c2ac-108">\<serviceDiscovery ></span><span class="sxs-lookup"><span data-stu-id="6c2ac-108">\<serviceDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c2ac-109">구문</span><span class="sxs-lookup"><span data-stu-id="6c2ac-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceDiscovery>
        <announcementEndpoints>
          <endpoint name="String"
                    kind="Type" />
        </announcementEndpoints>
        <discoveryEndpoints>
          <endpoint name="String"
                    kind="Type" />
        </discoveryEndpoints>
      </serviceDiscovery>
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6c2ac-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="6c2ac-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6c2ac-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6c2ac-112">특성</span><span class="sxs-lookup"><span data-stu-id="6c2ac-112">Attributes</span></span>  
 <span data-ttu-id="6c2ac-113">없음</span><span class="sxs-lookup"><span data-stu-id="6c2ac-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6c2ac-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="6c2ac-114">Child Elements</span></span>  
  
|<span data-ttu-id="6c2ac-115">요소</span><span class="sxs-lookup"><span data-stu-id="6c2ac-115">Element</span></span>|<span data-ttu-id="6c2ac-116">설명</span><span class="sxs-lookup"><span data-stu-id="6c2ac-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6c2ac-117">\<announcementEndpoint ></span><span class="sxs-lookup"><span data-stu-id="6c2ac-117">\<announcementEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)|<span data-ttu-id="6c2ac-118">알림 엔드포인트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-118">A collection of announcement endpoints.</span></span> <span data-ttu-id="6c2ac-119">이 섹션을 사용하여 알림 메시지를 보내기 위해 사용할 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-119">Use this section to specify the endpoints to use for sending announcement messages.</span></span>|  
|[<span data-ttu-id="6c2ac-120">\<discoveryEndpoint ></span><span class="sxs-lookup"><span data-stu-id="6c2ac-120">\<discoveryEndpoint></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)|<span data-ttu-id="6c2ac-121">검색 엔드포인트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-121">A collection of discovery endpoints.</span></span> <span data-ttu-id="6c2ac-122">이 섹션을 사용하여 검색 메시지를 수신할 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-122">Use this section to specify the endpoints on which to listen for the discovery messages.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6c2ac-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="6c2ac-123">Parent Elements</span></span>  
  
|<span data-ttu-id="6c2ac-124">요소</span><span class="sxs-lookup"><span data-stu-id="6c2ac-124">Element</span></span>|<span data-ttu-id="6c2ac-125">설명</span><span class="sxs-lookup"><span data-stu-id="6c2ac-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6c2ac-126">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="6c2ac-126">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="6c2ac-127">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-127">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c2ac-128">설명</span><span class="sxs-lookup"><span data-stu-id="6c2ac-128">Remarks</span></span>  
 <span data-ttu-id="6c2ac-129">이 구성 요소가 서비스의 동작 구성에 추가되는 경우 서비스의 모든 엔드포인트를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-129">When added to the service’s behavior configuration, this configuration element makes all of the endpoints of that service discoverable.</span></span> <span data-ttu-id="6c2ac-130">사용 하 여 이러한 끝점의 검색 기능을 추가로 구성할 수 있습니다 합니다 [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) 하거나 [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) 자식 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-130">You can further configure the discovery features of such endpoints by using the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) or [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) child elements.</span></span> <span data-ttu-id="6c2ac-131">사용 된 [ \<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) 서비스 알림 (온라인/Hello 및 Bye/오프 라인)를 보내는 데 사용할 끝점 구성을 지정 하 여 알림을 구성 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-131">Use the [\<announcementEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md) section to configure the announcements by specifying the endpoint configuration to be use to send service announcements (online/Hello and offline/Bye).</span></span> <span data-ttu-id="6c2ac-132">사용 된 [ \<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) 섹션을 수동으로 검색 메시지를 수신 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-132">Use the [\<discoveryEndpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md) section to manually specify the endpoint on which to listen for the discovery messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6c2ac-133">예제</span><span class="sxs-lookup"><span data-stu-id="6c2ac-133">Example</span></span>  
 <span data-ttu-id="6c2ac-134">다음 구성 예제에서는 CalculatorService를 검색할 수 있도록 지정하고 선택적으로 알림 엔드포인트를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c2ac-134">The following configuration example specifies that the CalculatorService to be discoverable, and optionally specifies the announcement endpoint to be used.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    ...
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery>
        <announcementEndpoints>
          <endpoint name="udpEndpoint"
                    kind="udpAnnouncementEndpoint" />
        </announcementEndpoints>
      </serviceDiscovery>
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="6c2ac-135">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6c2ac-135">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior>
