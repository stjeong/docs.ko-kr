---
title: '&lt;netPeerBinding&gt;의 &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 1ef40d8c-f903-4426-9b08-da81462766d8
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 45000554226fcde753041fca283bfc8b1eeba5ce
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43489762"
---
# <a name="ltsecuritygt-of-ltnetpeerbindinggt"></a><span data-ttu-id="e0161-102">&lt;netPeerBinding&gt;의 &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="e0161-102">&lt;security&gt; of &lt;netPeerBinding&gt;</span></span>
<span data-ttu-id="e0161-103">보안 설정을 정의 합니다 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md), 인증 유형 등 사용 및 보안 메시지 전송에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-103">Defines the security settings of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md), including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="e0161-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e0161-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="e0161-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="e0161-105">\<bindings></span></span>  
<span data-ttu-id="e0161-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="e0161-106">\<netPeerBinding></span></span>  
<span data-ttu-id="e0161-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="e0161-107">\<binding></span></span>  
<span data-ttu-id="e0161-108">\<security></span><span class="sxs-lookup"><span data-stu-id="e0161-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0161-109">구문</span><span class="sxs-lookup"><span data-stu-id="e0161-109">Syntax</span></span>  
  
```xml  
<netPeerBinding>  
    <binding>  
        <security mode="Message/None/Transport//TransportWithMessageCredential">  
            <transport credentialType="Certificate/Password" />  
        </security>  
    </binding>  
</netPeerBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e0161-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="e0161-110">Attributes and Elements</span></span>  
 <span data-ttu-id="e0161-111">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e0161-112">특성</span><span class="sxs-lookup"><span data-stu-id="e0161-112">Attributes</span></span>  
  
|<span data-ttu-id="e0161-113">특성</span><span class="sxs-lookup"><span data-stu-id="e0161-113">Attribute</span></span>|<span data-ttu-id="e0161-114">설명</span><span class="sxs-lookup"><span data-stu-id="e0161-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e0161-115">모드</span><span class="sxs-lookup"><span data-stu-id="e0161-115">mode</span></span>|<span data-ttu-id="e0161-116">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-116">Optional.</span></span> <span data-ttu-id="e0161-117">이 바인딩으로 구성된 피어에서 사용하는 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-117">Specifies the type of security used by peers configured with this binding.</span></span> <span data-ttu-id="e0161-118">기본값은 `Message`입니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-118">The default value is `Message`.</span></span> <span data-ttu-id="e0161-119">이 특성은 <xref:System.ServiceModel.SecurityMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-119">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="e0161-120">mode 특성</span><span class="sxs-lookup"><span data-stu-id="e0161-120">mode Attribute</span></span>  
  
|<span data-ttu-id="e0161-121">값</span><span class="sxs-lookup"><span data-stu-id="e0161-121">Value</span></span>|<span data-ttu-id="e0161-122">설명</span><span class="sxs-lookup"><span data-stu-id="e0161-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="e0161-123">메시지</span><span class="sxs-lookup"><span data-stu-id="e0161-123">Message</span></span>|<span data-ttu-id="e0161-124">SOAP 전송은 무결성, 기밀성 및 인증을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|<span data-ttu-id="e0161-125">없음</span><span class="sxs-lookup"><span data-stu-id="e0161-125">None</span></span>|<span data-ttu-id="e0161-126">보안이 해제되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-126">Security is disabled.</span></span>|  
|<span data-ttu-id="e0161-127">전송</span><span class="sxs-lookup"><span data-stu-id="e0161-127">Transport</span></span>|<span data-ttu-id="e0161-128">HTTPS를 사용하여 보안이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-128">Security is provided using HTTPS.</span></span>|  
|<span data-ttu-id="e0161-129">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="e0161-129">TransportWithMessageCredential</span></span>|<span data-ttu-id="e0161-130">HTTPS는 인증 및 기밀성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-130">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="e0161-131">SOAP 메시지는 다양한 자격 증명 형식을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-131">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e0161-132">자식 요소</span><span class="sxs-lookup"><span data-stu-id="e0161-132">Child Elements</span></span>  
  
|<span data-ttu-id="e0161-133">요소</span><span class="sxs-lookup"><span data-stu-id="e0161-133">Element</span></span>|<span data-ttu-id="e0161-134">설명</span><span class="sxs-lookup"><span data-stu-id="e0161-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0161-135">\<transport></span><span class="sxs-lookup"><span data-stu-id="e0161-135">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netpeertcpbinding.md)|<span data-ttu-id="e0161-136">이 바인딩으로 구성된 피어에서 보낸 보안 메시지의 전송 형식을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-136">Defines the transport type for secured messages sent by peers configured with this binding.</span></span> <span data-ttu-id="e0161-137">이 요소는 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-137">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e0161-138">부모 요소</span><span class="sxs-lookup"><span data-stu-id="e0161-138">Parent Elements</span></span>  
  
|<span data-ttu-id="e0161-139">요소</span><span class="sxs-lookup"><span data-stu-id="e0161-139">Element</span></span>|<span data-ttu-id="e0161-140">설명</span><span class="sxs-lookup"><span data-stu-id="e0161-140">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0161-141">\<binding></span><span class="sxs-lookup"><span data-stu-id="e0161-141">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="e0161-142">모든 바인딩 기능을 정의 합니다 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-142">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e0161-143">설명</span><span class="sxs-lookup"><span data-stu-id="e0161-143">Remarks</span></span>  
 <span data-ttu-id="e0161-144">보안은 메시지 또는 전송별로 고유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0161-144">Security can be either message- or transport-specific.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0161-145">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e0161-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement>  
 <xref:System.ServiceModel.NetPeerTcpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Security%2A>  
 <xref:System.ServiceModel.PeerSecuritySettings>  
 [<span data-ttu-id="e0161-146">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="e0161-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="e0161-147">자격 증명 형식 선택</span><span class="sxs-lookup"><span data-stu-id="e0161-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="e0161-148">바인딩</span><span class="sxs-lookup"><span data-stu-id="e0161-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="e0161-149">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="e0161-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="e0161-150">바인딩을 사용 하 여 Windows Communication Foundation 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="e0161-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="e0161-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="e0161-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
