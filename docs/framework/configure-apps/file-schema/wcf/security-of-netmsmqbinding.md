---
title: <security>의 <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 001d11a9-7439-498c-b09d-fca20eaf8cd3
ms.openlocfilehash: bb509bb0c4f7192aefbb51a98042f3f359969321
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55272619"
---
# <a name="security-of-netmsmqbinding"></a><span data-ttu-id="e8eb5-102">\<보안 >의 \<netMsmqBinding ></span><span class="sxs-lookup"><span data-stu-id="e8eb5-102">\<security> of \<netMsmqBinding></span></span>
<span data-ttu-id="e8eb5-103">MSMQ 바인딩에 대한 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-103">Defines the security settings for a MSMQ binding.</span></span> <span data-ttu-id="e8eb5-104">이 클래스는 전송 또는 SOAP 보안의 사용 여부 그리고 보안이 사용된다면 어떤 인증 모드 및 보호 수준을 사용하는지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-104">It specifies whether transport or SOAP security is enabled and, if so, what authentication mode and protection levels are in use.</span></span>  
  
 <span data-ttu-id="e8eb5-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e8eb5-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="e8eb5-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="e8eb5-106">\<bindings></span></span>  
<span data-ttu-id="e8eb5-107">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="e8eb5-107">\<netMsmqBinding></span></span>  
<span data-ttu-id="e8eb5-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="e8eb5-108">\<binding></span></span>  
<span data-ttu-id="e8eb5-109">\<security></span><span class="sxs-lookup"><span data-stu-id="e8eb5-109">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8eb5-110">구문</span><span class="sxs-lookup"><span data-stu-id="e8eb5-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e8eb5-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="e8eb5-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e8eb5-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e8eb5-113">특성</span><span class="sxs-lookup"><span data-stu-id="e8eb5-113">Attributes</span></span>  
  
|<span data-ttu-id="e8eb5-114">특성</span><span class="sxs-lookup"><span data-stu-id="e8eb5-114">Attribute</span></span>|<span data-ttu-id="e8eb5-115">설명</span><span class="sxs-lookup"><span data-stu-id="e8eb5-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e8eb5-116">모드</span><span class="sxs-lookup"><span data-stu-id="e8eb5-116">mode</span></span>|<span data-ttu-id="e8eb5-117">무결성, 기밀성 및 인증을 제어하는 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-117">Specifies the type of security that controls integrity, confidentiality and authentication.</span></span> <span data-ttu-id="e8eb5-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="e8eb5-119">-None. 이렇게 하면 보안이 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-119">-   None: This disables security.</span></span><br /><span data-ttu-id="e8eb5-120">-전송 합니다. 보호 및 인증이 전송에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-120">-   Transport: Protection and authentication are offered by the transport.</span></span> <span data-ttu-id="e8eb5-121">이는 두 큐 관리자 간의 메시지 보안에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-121">This applies to the message security between the two queue managers.</span></span> <span data-ttu-id="e8eb5-122">응용 프로그램 및 큐 관리자 간에는 제공되는 보안이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-122">There is no security offered between the application and queue manager.</span></span> <span data-ttu-id="e8eb5-123">기존 Msmq 응용 프로그램이 이러한 보안 모드 형식과 동일한 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-123">Existing Msmq applications are functionally equivalent with this type of security mode.</span></span><br /><span data-ttu-id="e8eb5-124">-메시지: 종단 간 응용 프로그램 보안을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-124">-   Message: Specifies end-end application security.</span></span> <span data-ttu-id="e8eb5-125">전송 계층에는 보안이 제공되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-125">There is no security offered at the transport layer.</span></span> <span data-ttu-id="e8eb5-126">이는 다른 표준 바인딩에서 제공하는 보안과 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-126">This is similar to the security offered by other standard bindings.</span></span><br /><span data-ttu-id="e8eb5-127">-모두: 전송과 SOAP 메시징 계층에서 보안을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-127">-   Both: Offers security at both the transport and SOAP messaging layer.</span></span> <span data-ttu-id="e8eb5-128">두 수준 모두에서 동일한 자격 증명이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-128">The same credential is required at both the levels.</span></span><br /><br /> <span data-ttu-id="e8eb5-129">기본값은 Transport입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-129">The default value is Transport.</span></span> <span data-ttu-id="e8eb5-130">이 특성은 <xref:System.ServiceModel.NetMsmqSecurityMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-130">This attribute is of type <xref:System.ServiceModel.NetMsmqSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e8eb5-131">자식 요소</span><span class="sxs-lookup"><span data-stu-id="e8eb5-131">Child Elements</span></span>  
  
|<span data-ttu-id="e8eb5-132">요소</span><span class="sxs-lookup"><span data-stu-id="e8eb5-132">Element</span></span>|<span data-ttu-id="e8eb5-133">설명</span><span class="sxs-lookup"><span data-stu-id="e8eb5-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e8eb5-134">\<message></span><span class="sxs-lookup"><span data-stu-id="e8eb5-134">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-netmsmqbinding.md)|<span data-ttu-id="e8eb5-135">SOAP 메시지 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-135">Defines the SOAP message security settings.</span></span> <span data-ttu-id="e8eb5-136">이 요소는 <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-136">This element is of type <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>.</span></span>|  
|[<span data-ttu-id="e8eb5-137">\<transport></span><span class="sxs-lookup"><span data-stu-id="e8eb5-137">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-netmsmqbinding.md)|<span data-ttu-id="e8eb5-138">MSMQ 전송의 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-138">Defines the security settings for the MSMQ transport.</span></span> <span data-ttu-id="e8eb5-139">이 요소는 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e8eb5-139">This element is of type <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e8eb5-140">부모 요소</span><span class="sxs-lookup"><span data-stu-id="e8eb5-140">Parent Elements</span></span>  
  
|<span data-ttu-id="e8eb5-141">요소</span><span class="sxs-lookup"><span data-stu-id="e8eb5-141">Element</span></span>|<span data-ttu-id="e8eb5-142">설명</span><span class="sxs-lookup"><span data-stu-id="e8eb5-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e8eb5-143">바인딩</span><span class="sxs-lookup"><span data-stu-id="e8eb5-143">binding</span></span>|<span data-ttu-id="e8eb5-144">바인딩 요소를 [ \<netMsmqBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span><span class="sxs-lookup"><span data-stu-id="e8eb5-144">The binding element of the [\<netMsmqBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e8eb5-145">참고자료</span><span class="sxs-lookup"><span data-stu-id="e8eb5-145">See also</span></span>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>
- <xref:System.ServiceModel.NetMsmqBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetMsmqBindingElement.Security%2A>
- <xref:System.ServiceModel.NetMsmqSecurity>
- [<span data-ttu-id="e8eb5-146">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="e8eb5-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="e8eb5-147">바인딩</span><span class="sxs-lookup"><span data-stu-id="e8eb5-147">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="e8eb5-148">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="e8eb5-148">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="e8eb5-149">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="e8eb5-149">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="e8eb5-150">\<binding></span><span class="sxs-lookup"><span data-stu-id="e8eb5-150">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
- [<span data-ttu-id="e8eb5-151">WCF의 큐</span><span class="sxs-lookup"><span data-stu-id="e8eb5-151">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
