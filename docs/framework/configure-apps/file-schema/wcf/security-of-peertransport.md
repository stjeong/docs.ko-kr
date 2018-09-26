---
title: '&lt;peerTransport&gt;의 &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: f73634ed-f896-4968-bf74-5e5ac52d3b6b
author: BrucePerlerMS
ms.openlocfilehash: 152087550d3fa881a7a88271d9c91dfcc5c894c8
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47176762"
---
# <a name="ltsecuritygt-of-ltpeertransportgt"></a><span data-ttu-id="009b8-102">&lt;peerTransport&gt;의 &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="009b8-102">&lt;security&gt; of &lt;peerTransport&gt;</span></span>
<span data-ttu-id="009b8-103">메시지 전송에 사용되는 인증 형식 및 보안을 비롯하여 피어 채널과 연결된 보안 설정을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-103">Contains the security settings associated with a peer channel, including the type of authentication used and the security used for the message transport.</span></span>  
  
 <span data-ttu-id="009b8-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="009b8-104">\<system.serviceModel></span></span>  
<span data-ttu-id="009b8-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="009b8-105">\<bindings></span></span>  
<span data-ttu-id="009b8-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="009b8-106">\<customBinding></span></span>  
<span data-ttu-id="009b8-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="009b8-107">\<binding></span></span>  
<span data-ttu-id="009b8-108">\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="009b8-108">\<peerTransport></span></span>  
<span data-ttu-id="009b8-109">\<security></span><span class="sxs-lookup"><span data-stu-id="009b8-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="009b8-110">구문</span><span class="sxs-lookup"><span data-stu-id="009b8-110">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/TransportWithMessageCredential">  
    <transport clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />  
</security  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="009b8-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="009b8-111">Attributes and Elements</span></span>  
 <span data-ttu-id="009b8-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="009b8-113">특성</span><span class="sxs-lookup"><span data-stu-id="009b8-113">Attributes</span></span>  
  
|<span data-ttu-id="009b8-114">특성</span><span class="sxs-lookup"><span data-stu-id="009b8-114">Attribute</span></span>|<span data-ttu-id="009b8-115">설명</span><span class="sxs-lookup"><span data-stu-id="009b8-115">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="009b8-116">적용할 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-116">Specifies the type of security to be applied.</span></span> <span data-ttu-id="009b8-117">기본값은 Message입니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-117">The default value is Message.</span></span> <span data-ttu-id="009b8-118">이 특성은 <xref:System.ServiceModel.SecurityMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-118">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="009b8-119">mode 특성</span><span class="sxs-lookup"><span data-stu-id="009b8-119">mode Attribute</span></span>  
  
|<span data-ttu-id="009b8-120">값</span><span class="sxs-lookup"><span data-stu-id="009b8-120">Value</span></span>|<span data-ttu-id="009b8-121">설명</span><span class="sxs-lookup"><span data-stu-id="009b8-121">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="009b8-122">보안이 해제되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-122">Security is disabled.</span></span>|  
|`Transport`|<span data-ttu-id="009b8-123">HTTPS를 사용하여 보안이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-123">Security is provided using HTTPS.</span></span>|  
|`Message`|<span data-ttu-id="009b8-124">SOAP 전송은 무결성, 기밀성 및 인증을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-124">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|`TransportWithMessageCredential`|<span data-ttu-id="009b8-125">HTTPS는 인증 및 기밀성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-125">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="009b8-126">SOAP 메시지는 다양한 자격 증명 형식을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-126">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="009b8-127">자식 요소</span><span class="sxs-lookup"><span data-stu-id="009b8-127">Child Elements</span></span>  
  
|<span data-ttu-id="009b8-128">요소</span><span class="sxs-lookup"><span data-stu-id="009b8-128">Element</span></span>|<span data-ttu-id="009b8-129">설명</span><span class="sxs-lookup"><span data-stu-id="009b8-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="009b8-130">\<transport></span><span class="sxs-lookup"><span data-stu-id="009b8-130">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-peertransport.md)|<span data-ttu-id="009b8-131">사용자 지정 바인딩에 대한 피어 전송을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-131">Defines a peer transport for a custom binding.</span></span> <span data-ttu-id="009b8-132">이 요소에는 서비스와 상호 작용할 때 사용되는 자격 증명을 지정하는 `clientCredentialType` 특성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-132">This element has a `clientCredentialType` attribute that specifies the credentials to be used when interacting with a service.</span></span> <span data-ttu-id="009b8-133">이 특성은 <xref:System.ServiceModel.PeerTransportCredentialType> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-133">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span><br /><br /> <span data-ttu-id="009b8-134">이 요소는 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-134">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="009b8-135">부모 요소</span><span class="sxs-lookup"><span data-stu-id="009b8-135">Parent Elements</span></span>  
  
|<span data-ttu-id="009b8-136">요소</span><span class="sxs-lookup"><span data-stu-id="009b8-136">Element</span></span>|<span data-ttu-id="009b8-137">설명</span><span class="sxs-lookup"><span data-stu-id="009b8-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="009b8-138">\<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="009b8-138">\<peerTransport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peertransport.md)|<span data-ttu-id="009b8-139">사용자 지정 바인딩에 대한 피어 전송을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="009b8-139">Defines a peer transport for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="009b8-140">참고 항목</span><span class="sxs-lookup"><span data-stu-id="009b8-140">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement>  
 <xref:System.ServiceModel.PeerSecuritySettings>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="009b8-141">전송 보안</span><span class="sxs-lookup"><span data-stu-id="009b8-141">Transport Security</span></span>](../../../../../docs/framework/wcf/feature-details/transport-security.md)  
 [<span data-ttu-id="009b8-142">전송</span><span class="sxs-lookup"><span data-stu-id="009b8-142">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [<span data-ttu-id="009b8-143">전송 선택</span><span class="sxs-lookup"><span data-stu-id="009b8-143">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [<span data-ttu-id="009b8-144">바인딩</span><span class="sxs-lookup"><span data-stu-id="009b8-144">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="009b8-145">바인딩 확장</span><span class="sxs-lookup"><span data-stu-id="009b8-145">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="009b8-146">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="009b8-146">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="009b8-147">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="009b8-147">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
