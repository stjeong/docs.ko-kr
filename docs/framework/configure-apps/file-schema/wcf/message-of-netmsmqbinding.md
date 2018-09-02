---
title: '&lt;netMsmqBinding&gt;의 &lt;message&gt;'
ms.date: 03/30/2017
ms.assetid: 6ebf0240-d7be-4493-b0fe-f00fd5989d77
ms.openlocfilehash: 65a8b0fa120d23931ad218ac67846c066b050af8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43402246"
---
# <a name="ltmessagegt-of-ltnetmsmqbindinggt"></a><span data-ttu-id="3c259-102">&lt;netMsmqBinding&gt;의 &lt;message&gt;</span><span class="sxs-lookup"><span data-stu-id="3c259-102">&lt;message&gt; of &lt;netMsmqBinding&gt;</span></span>
<span data-ttu-id="3c259-103">이 `netMsmqBinding` 바인딩에 대한 SOAP 메시지 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-103">Defines the SOAP message security settings on this `netMsmqBinding` binding.</span></span>  
  
 <span data-ttu-id="3c259-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3c259-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3c259-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="3c259-105">\<bindings></span></span>  
<span data-ttu-id="3c259-106">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="3c259-106">\<netMsmqBinding></span></span>  
<span data-ttu-id="3c259-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="3c259-107">\<binding></span></span>  
<span data-ttu-id="3c259-108">\<security></span><span class="sxs-lookup"><span data-stu-id="3c259-108">\<security></span></span>  
<span data-ttu-id="3c259-109">\<message></span><span class="sxs-lookup"><span data-stu-id="3c259-109">\<message></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c259-110">구문</span><span class="sxs-lookup"><span data-stu-id="3c259-110">Syntax</span></span>  
  
```xml  
<netMsmqBinding>  
    <binding>  
      <security>  
         <message   
                      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
            clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />  
    </security>  
</netMsmqBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3c259-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="3c259-111">Attributes and Elements</span></span>  
 <span data-ttu-id="3c259-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3c259-113">특성</span><span class="sxs-lookup"><span data-stu-id="3c259-113">Attributes</span></span>  
  
|<span data-ttu-id="3c259-114">특성</span><span class="sxs-lookup"><span data-stu-id="3c259-114">Attribute</span></span>|<span data-ttu-id="3c259-115">설명</span><span class="sxs-lookup"><span data-stu-id="3c259-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3c259-116">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="3c259-116">algorithmSuite</span></span>|<span data-ttu-id="3c259-117">MSMQ 전송을 통해 전송되는 메시지에 메시지 기반 보안을 적용하는 데 사용되는 메시지 암호화 및 키 랩 알고리즘을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-117">Sets the message encryption and key-wrap algorithms that are used to achieve message-based security for messages sent over MSMQ transport.</span></span><br /><br /> <span data-ttu-id="3c259-118">기본값은 `Aes256`입니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-118">The default value is `Aes256`.</span></span> <span data-ttu-id="3c259-119">이 특성은 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-119">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span></span>|  
|<span data-ttu-id="3c259-120">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="3c259-120">clientCredentialType</span></span>|<span data-ttu-id="3c259-121">MSMQ 전송을 통해 전송되는 메시지에 대해 클라이언트 인증을 수행할 때 사용되는 자격 증명의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-121">Specifies the type of credential to be used when performing client authentication for messages sent over the MSMQ transport.</span></span> <span data-ttu-id="3c259-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-122">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="3c259-123">-None: 따라서 서비스와 익명 클라이언트가 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-123">-   None: This allows the service to interact with anonymous clients.</span></span> <span data-ttu-id="3c259-124">서비스와 클라이언트 모두 자격 증명이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-124">Neither the service nor the client requires a credential.</span></span><br /><span data-ttu-id="3c259-125">-Windows:이 통해 Windows 자격 증명의 인증 된 컨텍스트에서 SOAP 교환이 이루어지도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-125">-   Windows: This enables the SOAP exchanges to be under the authenticated context of a Windows credential.</span></span> <span data-ttu-id="3c259-126">이 설정은 항상 Kerberos 기반 인증을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-126">This always performs Kerberos-based authentication.</span></span><br /><span data-ttu-id="3c259-127">-UserName:이 통해 필요 하도록 서비스 클라이언트가 UserName 자격 증명을 사용 하 여 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-127">-   UserName: This enables the service to require that the client be authenticated using a UserName credential.</span></span> <span data-ttu-id="3c259-128">자격 증명을 사용 하 여 지정 해야이 경우에 `clientCredentials` 동작 **주의:** 다이제스트 또는 파생 키 암호를 사용 하 여 및에 대 한 이러한 키를 사용 하 여 암호를 보내는 Windows Communication Foundation (WCF) 지원 하지 않습니다 메시지 보안입니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-128">The credential in this case needs to be specified using the `clientCredentials` behavior **Caution:**  Windows Communication Foundation (WCF) does not support sending a password digest or deriving keys using password and using such keys for message security.</span></span> <span data-ttu-id="3c259-129">따라서 WCF 사용자 이름 자격 증명을 사용 하는 경우 교환에 보안을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-129">Therefore, WCF enforces that the exchange is secured when using UserName credentials.</span></span> <span data-ttu-id="3c259-130">이 모드에서는 `clientCredential` 동작 및 `serviceCertificate`를 사용하여 클라이언트에 서비스 인증서를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-130">This mode requires that the service certificate be specified on the client side using `clientCredential` behavior and `serviceCertificate`.</span></span> <br /><br /> <span data-ttu-id="3c259-131">-인증서:이 통해 필요 하도록 서비스 인증서를 사용 하 여 클라이언트 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-131">-   Certificate: This enables the service to require that the client be authenticated using a certificate.</span></span> <span data-ttu-id="3c259-132">이 경우 `clientCredentials` 동작을 사용하여 클라이언트 자격 증명을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-132">The client credential in this case needs to be specified using the `clientCredentials` behavior.</span></span> <span data-ttu-id="3c259-133">이 경우 `clientCredentials`를 지정하여 `serviceCertificate` 동작을 통해 서비스 자격 증명을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-133">The service credential in this case needs to be specified using the `clientCredentials` behavior by specifying the `serviceCertificate`.</span></span><br /><span data-ttu-id="3c259-134">-CardSpace: 이렇게 하면 필요 하도록 서비스를 사용 하는 CardSpace를 사용 하 여 클라이언트를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-134">-   CardSpace: This allows the service to require that the client be authenticated using a CardSpace.</span></span> <span data-ttu-id="3c259-135">`serviceCertiifcate` 동작에 `clientCredential`가 제공되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-135">The `serviceCertiifcate` must be provisioned in the `clientCredential` behavior.</span></span><br /><br /> <span data-ttu-id="3c259-136">기본값은 `Windows`입니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-136">The default value is `Windows`.</span></span> <span data-ttu-id="3c259-137">이 특성은 <xref:System.ServiceModel.MessageCredentialType> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-137">This attribute is of type <xref:System.ServiceModel.MessageCredentialType>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3c259-138">자식 요소</span><span class="sxs-lookup"><span data-stu-id="3c259-138">Child Elements</span></span>  
 <span data-ttu-id="3c259-139">없음</span><span class="sxs-lookup"><span data-stu-id="3c259-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3c259-140">부모 요소</span><span class="sxs-lookup"><span data-stu-id="3c259-140">Parent Elements</span></span>  
  
|<span data-ttu-id="3c259-141">요소</span><span class="sxs-lookup"><span data-stu-id="3c259-141">Element</span></span>|<span data-ttu-id="3c259-142">설명</span><span class="sxs-lookup"><span data-stu-id="3c259-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3c259-143">\<security></span><span class="sxs-lookup"><span data-stu-id="3c259-143">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|<span data-ttu-id="3c259-144">바인딩에 대한 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="3c259-144">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3c259-145">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3c259-145">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>  
 <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Message%2A>  
 <xref:System.ServiceModel.NetMsmqSecurity.Message%2A>  
 <xref:System.ServiceModel.MessageSecurityOverMsmq>  
 [<span data-ttu-id="3c259-146">WCF의 큐</span><span class="sxs-lookup"><span data-stu-id="3c259-146">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [<span data-ttu-id="3c259-147">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="3c259-147">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="3c259-148">바인딩</span><span class="sxs-lookup"><span data-stu-id="3c259-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="3c259-149">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="3c259-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="3c259-150">바인딩을 사용 하 여 Windows Communication Foundation 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="3c259-150">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="3c259-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="3c259-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
