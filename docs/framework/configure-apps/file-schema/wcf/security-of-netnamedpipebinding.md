---
title: '&lt;netNamedPipeBinding&gt;의 &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: bb3cb022-637e-49fd-92e8-6766038affa7
ms.openlocfilehash: 4a80a8337a5b98ff30de60afbe4438e0d91b946b
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185682"
---
# <a name="ltsecuritygt-of-ltnetnamedpipebindinggt"></a><span data-ttu-id="24bfc-102">&lt;netNamedPipeBinding&gt;의 &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="24bfc-102">&lt;security&gt; of &lt;netNamedPipeBinding&gt;</span></span>
<span data-ttu-id="24bfc-103">바인딩에 대한 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-103">Defines the security settings for a binding.</span></span>  
  
 <span data-ttu-id="24bfc-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="24bfc-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="24bfc-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="24bfc-105">\<bindings></span></span>  
<span data-ttu-id="24bfc-106">\<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="24bfc-106">\<netNamedPipeBinding></span></span>  
<span data-ttu-id="24bfc-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="24bfc-107">\<binding></span></span>  
<span data-ttu-id="24bfc-108">\<security></span><span class="sxs-lookup"><span data-stu-id="24bfc-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24bfc-109">구문</span><span class="sxs-lookup"><span data-stu-id="24bfc-109">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>  
      <binding>  
            <security mode="None/Transport">  
                        <transport protectionLevel="None/Sign/EncryptAndSign" />  
            </security>  
      </binding>  
</netNamedPipeBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="24bfc-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="24bfc-110">Attributes and Elements</span></span>  
 <span data-ttu-id="24bfc-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="24bfc-112">특성</span><span class="sxs-lookup"><span data-stu-id="24bfc-112">Attributes</span></span>  
  
|<span data-ttu-id="24bfc-113">특성</span><span class="sxs-lookup"><span data-stu-id="24bfc-113">Attribute</span></span>|<span data-ttu-id="24bfc-114">설명</span><span class="sxs-lookup"><span data-stu-id="24bfc-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="24bfc-115">모드</span><span class="sxs-lookup"><span data-stu-id="24bfc-115">mode</span></span>|<span data-ttu-id="24bfc-116">이 바인딩에 적용되는 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-116">Specifies the type of security that is applied to this binding.</span></span> <span data-ttu-id="24bfc-117">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-117">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="24bfc-118">-None: 이렇게 하면 보안이 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-118">-   None: This disables security.</span></span><br /><span data-ttu-id="24bfc-119">-전송: 보안 기본 전송 기반 보안을 사용 하 여 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-119">-   Transport: Security is provided using underlying transport based security.</span></span> <span data-ttu-id="24bfc-120">이 모드에서는 보호 수준을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-120">It is possible to control the protection level with this mode.</span></span><br /><span data-ttu-id="24bfc-121">-기본값은 Transport입니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-121">-   The default value is Transport.</span></span> <span data-ttu-id="24bfc-122">이 특성은 <xref:System.ServiceModel.NetNamedPipeSecurityMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-122">This attribute is of type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="24bfc-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="24bfc-123">Child Elements</span></span>  
  
|<span data-ttu-id="24bfc-124">요소</span><span class="sxs-lookup"><span data-stu-id="24bfc-124">Element</span></span>|<span data-ttu-id="24bfc-125">설명</span><span class="sxs-lookup"><span data-stu-id="24bfc-125">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="24bfc-126">transport</span><span class="sxs-lookup"><span data-stu-id="24bfc-126">transport</span></span>|<span data-ttu-id="24bfc-127">전송의 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-127">Defines the security settings for the transport.</span></span> <span data-ttu-id="24bfc-128">이 요소는 <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-128">This element is of type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="24bfc-129">부모 요소</span><span class="sxs-lookup"><span data-stu-id="24bfc-129">Parent Elements</span></span>  
  
|<span data-ttu-id="24bfc-130">요소</span><span class="sxs-lookup"><span data-stu-id="24bfc-130">Element</span></span>|<span data-ttu-id="24bfc-131">설명</span><span class="sxs-lookup"><span data-stu-id="24bfc-131">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="24bfc-132">바인딩</span><span class="sxs-lookup"><span data-stu-id="24bfc-132">binding</span></span>|<span data-ttu-id="24bfc-133">바인딩 요소를 [ \<netNamedPipeBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="24bfc-133">The binding element of the [\<netNamedPipeBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netnamedpipebinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="24bfc-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="24bfc-134">See Also</span></span>  
 <xref:System.ServiceModel.NetNamedPipeSecurity>  
 <xref:System.ServiceModel.NetNamedPipeBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeBindingElement.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement>  
 [<span data-ttu-id="24bfc-135">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="24bfc-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="24bfc-136">자격 증명 형식 선택</span><span class="sxs-lookup"><span data-stu-id="24bfc-136">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="24bfc-137">바인딩</span><span class="sxs-lookup"><span data-stu-id="24bfc-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="24bfc-138">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="24bfc-138">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="24bfc-139">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="24bfc-139">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="24bfc-140">\<binding></span><span class="sxs-lookup"><span data-stu-id="24bfc-140">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
