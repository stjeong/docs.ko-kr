---
title: '&lt;netMsmqBinding&gt;의 &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 001d11a9-7439-498c-b09d-fca20eaf8cd3
ms.openlocfilehash: 71f0c10c336a9682971bc774141cb0c3bd37c092
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696388"
---
# <a name="ltsecuritygt-of-ltnetmsmqbindinggt"></a><span data-ttu-id="d766e-102">&lt;netMsmqBinding&gt;의 &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="d766e-102">&lt;security&gt; of &lt;netMsmqBinding&gt;</span></span>
<span data-ttu-id="d766e-103">MSMQ 바인딩에 대한 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-103">Defines the security settings for a MSMQ binding.</span></span> <span data-ttu-id="d766e-104">이 클래스는 전송 또는 SOAP 보안의 사용 여부 그리고 보안이 사용된다면 어떤 인증 모드 및 보호 수준을 사용하는지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-104">It specifies whether transport or SOAP security is enabled and, if so, what authentication mode and protection levels are in use.</span></span>  
  
 <span data-ttu-id="d766e-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d766e-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="d766e-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="d766e-106">\<bindings></span></span>  
<span data-ttu-id="d766e-107">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="d766e-107">\<netMsmqBinding></span></span>  
<span data-ttu-id="d766e-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="d766e-108">\<binding></span></span>  
<span data-ttu-id="d766e-109">\<security></span><span class="sxs-lookup"><span data-stu-id="d766e-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d766e-110">구문</span><span class="sxs-lookup"><span data-stu-id="d766e-110">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/Both">
  <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
             msmqEncryptionAlgorithm="RC4Stream/AES"
             msmqProtectionLevel="None/Sign/EncryptAndSign"
             msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
             clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d766e-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="d766e-111">Attributes and Elements</span></span>  
 <span data-ttu-id="d766e-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d766e-113">특성</span><span class="sxs-lookup"><span data-stu-id="d766e-113">Attributes</span></span>  
  
|<span data-ttu-id="d766e-114">특성</span><span class="sxs-lookup"><span data-stu-id="d766e-114">Attribute</span></span>|<span data-ttu-id="d766e-115">설명</span><span class="sxs-lookup"><span data-stu-id="d766e-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d766e-116">모드</span><span class="sxs-lookup"><span data-stu-id="d766e-116">mode</span></span>|<span data-ttu-id="d766e-117">무결성, 기밀성 및 인증을 제어하는 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-117">Specifies the type of security that controls integrity, confidentiality and authentication.</span></span> <span data-ttu-id="d766e-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="d766e-119">-None. 이렇게 하면 보안이 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-119">-   None: This disables security.</span></span><br /><span data-ttu-id="d766e-120">-전송 합니다. 보호 및 인증이 전송에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-120">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="d766e-121">이는 두 큐 관리자 간의 메시지 보안에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-121">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="d766e-122">응용 프로그램 및 큐 관리자 간에는 제공되는 보안이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-122">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="d766e-123">기존 Msmq 응용 프로그램이 이러한 보안 모드 형식과 동일한 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-123">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><span data-ttu-id="d766e-124">-메시지: 종단 간 응용 프로그램 보안을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-124">-   Message: Specifies end-end application security.</span></span> <span data-ttu-id="d766e-125">전송 계층에는 보안이 제공되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-125">There is no security offered at the transport layer.</span></span> <span data-ttu-id="d766e-126">이는 다른 표준 바인딩에서 제공하는 보안과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-126">This is similar to the security offered by other standard bindings.</span></span><br /><span data-ttu-id="d766e-127">-모두: 전송과 SOAP 메시징 계층에서 보안을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-127">-   Both: Offers security at both the transport and SOAP messaging layer.</span></span> <span data-ttu-id="d766e-128">두 수준 모두에서 동일한 자격 증명이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-128">The same credential is required at both the levels.</span></span><br /><br /> <span data-ttu-id="d766e-129">기본값은 Transport입니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-129">The default value is Transport.</span></span> <span data-ttu-id="d766e-130">이 특성은 <xref:System.ServiceModel.NetMsmqSecurityMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-130">This attribute is of type <xref:System.ServiceModel.NetMsmqSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d766e-131">자식 요소</span><span class="sxs-lookup"><span data-stu-id="d766e-131">Child Elements</span></span>  
  
|<span data-ttu-id="d766e-132">요소</span><span class="sxs-lookup"><span data-stu-id="d766e-132">Element</span></span>|<span data-ttu-id="d766e-133">설명</span><span class="sxs-lookup"><span data-stu-id="d766e-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d766e-134">\<message></span><span class="sxs-lookup"><span data-stu-id="d766e-134">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-netmsmqbinding.md)|<span data-ttu-id="d766e-135">SOAP 메시지 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-135">Defines the SOAP message security settings.</span></span> <span data-ttu-id="d766e-136">이 요소는 <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-136">This element is of type <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>.</span></span>|  
|[<span data-ttu-id="d766e-137">\<transport></span><span class="sxs-lookup"><span data-stu-id="d766e-137">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netmsmqbinding.md)|<span data-ttu-id="d766e-138">MSMQ 전송의 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-138">Defines the security settings for the MSMQ transport.</span></span> <span data-ttu-id="d766e-139">이 요소는 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d766e-139">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d766e-140">부모 요소</span><span class="sxs-lookup"><span data-stu-id="d766e-140">Parent Elements</span></span>  
  
|<span data-ttu-id="d766e-141">요소</span><span class="sxs-lookup"><span data-stu-id="d766e-141">Element</span></span>|<span data-ttu-id="d766e-142">설명</span><span class="sxs-lookup"><span data-stu-id="d766e-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d766e-143">바인딩</span><span class="sxs-lookup"><span data-stu-id="d766e-143">binding</span></span>|<span data-ttu-id="d766e-144">바인딩 요소를 [ \<netMsmqBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span><span class="sxs-lookup"><span data-stu-id="d766e-144">The binding element of the [\<netMsmqBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d766e-145">참고자료</span><span class="sxs-lookup"><span data-stu-id="d766e-145">See also</span></span>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>
- <xref:System.ServiceModel.NetMsmqBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetMsmqBindingElement.Security%2A>
- <xref:System.ServiceModel.NetMsmqSecurity>
- [<span data-ttu-id="d766e-146">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="d766e-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="d766e-147">바인딩</span><span class="sxs-lookup"><span data-stu-id="d766e-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="d766e-148">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="d766e-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="d766e-149">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="d766e-149">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="d766e-150">\<binding></span><span class="sxs-lookup"><span data-stu-id="d766e-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
- [<span data-ttu-id="d766e-151">WCF의 큐</span><span class="sxs-lookup"><span data-stu-id="d766e-151">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
