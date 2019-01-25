---
title: '&lt;exposedMethod&gt;'
ms.date: 03/30/2017
ms.assetid: 61c938cd-4ee9-4b06-ab28-922ef491ab11
ms.openlocfilehash: 0bfb56395217283eeba69c2f3b7569a89f576423
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702043"
---
# <a name="ltexposedmethodgt"></a><span data-ttu-id="b969d-102">&lt;exposedMethod&gt;</span><span class="sxs-lookup"><span data-stu-id="b969d-102">&lt;exposedMethod&gt;</span></span>
<span data-ttu-id="b969d-103">COM+ 구성 요소의 인터페이스가 웹 서비스로 노출될 때 노출되는 COM+ 메서드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-103">Represents a COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>  
  
 <span data-ttu-id="b969d-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b969d-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b969d-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="b969d-105">\<comContracts></span></span>  
<span data-ttu-id="b969d-106">\<comContract></span><span class="sxs-lookup"><span data-stu-id="b969d-106">\<comContract></span></span>  
<span data-ttu-id="b969d-107">\<methods></span><span class="sxs-lookup"><span data-stu-id="b969d-107">\<methods></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b969d-108">구문</span><span class="sxs-lookup"><span data-stu-id="b969d-108">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <exposedMethods>
      <exposedMethod name="String" />
    </exposedMethods>
  </comContract>
</comContracts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b969d-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="b969d-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b969d-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b969d-111">특성</span><span class="sxs-lookup"><span data-stu-id="b969d-111">Attributes</span></span>  
  
|<span data-ttu-id="b969d-112">특성</span><span class="sxs-lookup"><span data-stu-id="b969d-112">Attribute</span></span>|<span data-ttu-id="b969d-113">설명</span><span class="sxs-lookup"><span data-stu-id="b969d-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b969d-114">name</span><span class="sxs-lookup"><span data-stu-id="b969d-114">name</span></span>|<span data-ttu-id="b969d-115">COM+ 구성 요소의 인터페이스가 웹 서비스로 공개될 때 노출되는 COM+ 메서드를 포함하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-115">A string that contains the COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b969d-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="b969d-116">Child Elements</span></span>  
 <span data-ttu-id="b969d-117">없음</span><span class="sxs-lookup"><span data-stu-id="b969d-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b969d-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="b969d-118">Parent Elements</span></span>  
  
|<span data-ttu-id="b969d-119">요소</span><span class="sxs-lookup"><span data-stu-id="b969d-119">Element</span></span>|<span data-ttu-id="b969d-120">설명</span><span class="sxs-lookup"><span data-stu-id="b969d-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b969d-121">\<exposedMethods></span><span class="sxs-lookup"><span data-stu-id="b969d-121">\<exposedMethods></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethods.md)|<span data-ttu-id="b969d-122">컬렉션인 [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-122">A collection of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b969d-123">설명</span><span class="sxs-lookup"><span data-stu-id="b969d-123">Remarks</span></span>  
 <span data-ttu-id="b969d-124">COM+ 통합 구성 도구(ComSvcConfig.exe)는 COM 인터페이스의 특정 메서드를 생성된 서비스 계약에 나타나도록 추가하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-124">The COM+ integration configuration tool (ComSvcConfig.exe) can be used to add specific methods from a COM interface to appear on the generated service contract.</span></span>  
  
 <span data-ttu-id="b969d-125">예를 들어, 다음 명령을 사용하여 생성된 서비스 계약에 `IFinances`.Financial 구성 요소의 `ItemOrders` COM 인터페이스에 있는 명명된 메서드 3개를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-125">For example, you can use the following command to add the three named methods from the `IFinances` COM interface on the `ItemOrders`.Financial component, to the generated service contract.</span></span>  
  
 `ComSvcConfig.exe /i /application:OnlineStore /contract:ItemOrders.Financial,IFinances.{TransferFunds,AddFunds,RemoveFunds} /hosting:complus`  
  
 <span data-ttu-id="b969d-126">앞에서 언급 한 메서드를 나열 합니다. 다음 서비스 계약이 생성 됩니다 또한 ComSvcConfig.exe를 실행 하면 [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-126">When you also run the ComSvcConfig.exe, it then generates the following service contract listing the previously mentioned methods as [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>  
  
```xml  
<comContract contractType="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}"
             name="IFinances"
             namespace="http://contoso.com/services/financial">
  <exposedMethod name="TransferFunds"/>
  <exposedMethod name="AddFunds"/>
  <exposedMethod name="RemoveFunds"/>
</comContract>
```  
  
 <span data-ttu-id="b969d-127">서비스 초기화 시 런타임에서 검토 하 고 목록에 포함 된 메서드만 추가 하 여 서비스 계약을 생성 하려고 [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-127">At service initialization time, the runtime attempts to generate a service contract by reflecting over and adding only the methods included in the list of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span> <span data-ttu-id="b969d-128">서비스 계약에 포함되지 않은 모든 인터페이스 메서드에 대해서는 추적이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b969d-128">A trace is produced for every interface method that is not included on the service contract.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b969d-129">참고자료</span><span class="sxs-lookup"><span data-stu-id="b969d-129">See also</span></span>
- <xref:System.ServiceModel.Configuration.ComMethodElementCollection>
- <xref:System.ServiceModel.Configuration.ComMethodElement>
- [<span data-ttu-id="b969d-130">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="b969d-130">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="b969d-131">COM+ 애플리케이션과 통합</span><span class="sxs-lookup"><span data-stu-id="b969d-131">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="b969d-132">방법: COM + 서비스 설정 구성</span><span class="sxs-lookup"><span data-stu-id="b969d-132">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
