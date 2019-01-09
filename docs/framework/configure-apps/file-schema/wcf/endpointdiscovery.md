---
title: '&lt;endpointDiscovery&gt;'
ms.date: 03/30/2017
ms.assetid: 70812717-888a-4748-9640-0df6715ff029
ms.openlocfilehash: 58bab9aef2e20d762c303e8b698214125531a136
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150918"
---
# <a name="ltendpointdiscoverygt"></a><span data-ttu-id="0425e-102">&lt;endpointDiscovery&gt;</span><span class="sxs-lookup"><span data-stu-id="0425e-102">&lt;endpointDiscovery&gt;</span></span>
<span data-ttu-id="0425e-103">검색 기능, 범위 및 해당 메타데이터에 대한 사용자 지정 확장 등 엔드포인트에 대한 다양한 검색 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-103">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>  
  
<span data-ttu-id="0425e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0425e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0425e-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="0425e-105">\<behaviors></span></span>  
<span data-ttu-id="0425e-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="0425e-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="0425e-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="0425e-107">\<behavior></span></span>  
<span data-ttu-id="0425e-108">\<endpointDiscovery ></span><span class="sxs-lookup"><span data-stu-id="0425e-108">\<endpointDiscovery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0425e-109">구문</span><span class="sxs-lookup"><span data-stu-id="0425e-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enabled="Boolean">
        <scopes>
          <add scope="URI"/>
        </scopes>
        <extensions />
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0425e-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="0425e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0425e-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0425e-112">특성</span><span class="sxs-lookup"><span data-stu-id="0425e-112">Attributes</span></span>  
  
|<span data-ttu-id="0425e-113">특성</span><span class="sxs-lookup"><span data-stu-id="0425e-113">Attribute</span></span>|<span data-ttu-id="0425e-114">설명</span><span class="sxs-lookup"><span data-stu-id="0425e-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0425e-115">사용</span><span class="sxs-lookup"><span data-stu-id="0425e-115">enabled</span></span>|<span data-ttu-id="0425e-116">이 끝점에서 검색 기능이 사용 되는지 여부를 지정 하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-116">A Boolean value that specifies whether discoverability is enabled on this endpoint.</span></span> <span data-ttu-id="0425e-117">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-117">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0425e-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="0425e-118">Child Elements</span></span>  
  
|<span data-ttu-id="0425e-119">요소</span><span class="sxs-lookup"><span data-stu-id="0425e-119">Element</span></span>|<span data-ttu-id="0425e-120">설명</span><span class="sxs-lookup"><span data-stu-id="0425e-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0425e-121">\<범위 ></span><span class="sxs-lookup"><span data-stu-id="0425e-121">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="0425e-122">엔드포인트에 대한 범위 URI의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-122">A collection of scope URIs for the endpoint.</span></span> <span data-ttu-id="0425e-123">단일 엔드포인트에 둘 이상의 범위 URI를 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-123">More than one scope Uris can be associated with a single endpoint.</span></span>|  
|<span data-ttu-id="0425e-124">[\<확장 >](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) [의 \<endpointDiscovery >]</span><span class="sxs-lookup"><span data-stu-id="0425e-124">[\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) [of \<endpointDiscovery>]</span></span>|<span data-ttu-id="0425e-125">엔드포인트에 대해 게시되는 사용자 지정 메타데이터를 지정할 수 있는 XML 요소의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-125">A collection of XML elements that allows you to specify custom metadata to be published for an endpoint.</span></span>|  
|<span data-ttu-id="0425e-126">\<형식 ></span><span class="sxs-lookup"><span data-stu-id="0425e-126">\<types></span></span>|<span data-ttu-id="0425e-127">검색할 인터페이스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-127">A collection of interfaces to search for.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0425e-128">부모 요소</span><span class="sxs-lookup"><span data-stu-id="0425e-128">Parent Elements</span></span>  
  
|<span data-ttu-id="0425e-129">요소</span><span class="sxs-lookup"><span data-stu-id="0425e-129">Element</span></span>|<span data-ttu-id="0425e-130">설명</span><span class="sxs-lookup"><span data-stu-id="0425e-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0425e-131">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="0425e-131">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="0425e-132">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-132">Specifies a behavior element.</span></span>|  
|||  
  
## <a name="remarks"></a><span data-ttu-id="0425e-133">설명</span><span class="sxs-lookup"><span data-stu-id="0425e-133">Remarks</span></span>  
 <span data-ttu-id="0425e-134">엔드포인트의 동작 구성에 추가되고 `enabled` 특성이 `true`로 설정되면 이 구성 요소에 대한 검색 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-134">When added to the endpoint’s behavior configuration and with the `enabled` attribute set to `true`, this configuration element enables its discoverability.</span></span> <span data-ttu-id="0425e-135">또한 사용할 수 있습니다는 [ \<범위 >](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)자식 요소 사용자 지정 범위를 쿼리 하는 동안 서비스 끝점을 필터링 하는 Uri를 지정 하는 것과 같이 [ \<확장 >](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) 자식 요소를 표준 검색 가능 메타 데이터 (EPR, ContractTypeName, BindingName, 범위 및 ListenURI)와 함께 게시 되어야 하는 사용자 지정 메타 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-135">In addition, you can use the [\<scopes>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)child element to specifying custom scope Uris that can be used to filter service endpoints during query, as well as the [\<extensions>](../../../../../docs/framework/configure-apps/file-schema/wcf/extensions.md) child element to specify custom metadata that should be published along with the standard discoverable metadata (EPR, ContractTypeName, BindingName, Scope and ListenURI).</span></span>  
  
 <span data-ttu-id="0425e-136">이 구성 요소에 종속 되는 [ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) 검색 기능의 서비스 수준 제어를 제공 하는 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-136">This configuration element is dependent on the [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) element that provides the service level control of discoverability.</span></span> <span data-ttu-id="0425e-137">이 경우는이 요소의 설정이 무시 됩니다 의미 [ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) 구성에 없는 합니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-137">This means that this element’s settings are ignored if [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) is not present in the configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0425e-138">예제</span><span class="sxs-lookup"><span data-stu-id="0425e-138">Example</span></span>  
 <span data-ttu-id="0425e-139">다음 구성 예제에서는 필터링 범위 및 엔드포인트에 게시되는 확장 메타데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0425e-139">The following configuration example specifies filtering scopes and extension metadata to be published for an endpoint.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService"
              behaviorConfiguration="calculatorEndpointBehavior" />
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery />
    </behavior>
  </serviceBehaviors>
  <endpointBehaviors>
    <behavior name="calculatorEndpointBehavior">
      <endpointDiscovery enabled="true">
        <scopes>
          <add scope="http://contoso/test1" />
          <add scope="http://contoso/test2" />
        </scopes>
        <extensions>
          <e:Publisher xmlns:e="http://example.org">
            <e:Name>The Example Organization</e:Name>
            <e:Address>One Example Way, ExampleTown, EX 12345</e:Address>
            <e:Contact>support@example.org</e:Contact>
          </e:Publisher>
          <AnotherCustomMetadata>Custom Metadata</AnotherCustomMetadata>
        </extensions>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="0425e-140">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0425e-140">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
