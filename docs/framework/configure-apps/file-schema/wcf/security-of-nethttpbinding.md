---
title: '&lt;netHttpBinding&gt;의 &lt;security'
ms.date: 03/30/2017
ms.assetid: dc41f6f7-cabc-4a64-9fa0-ceabf861b348
ms.openlocfilehash: 912f53a9e0a5d1d145c308dd6f427df05b27c077
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48838535"
---
# <a name="ltsecuritygt-of-ltnethttpbinding"></a><span data-ttu-id="b8ad3-102">&lt;netHttpBinding&gt;의 &lt;security</span><span class="sxs-lookup"><span data-stu-id="b8ad3-102">&lt;security&gt; of &lt;netHttpBinding</span></span>
<span data-ttu-id="b8ad3-103">보안 기능을 정의 합니다 [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-103">Defines the security capabilities of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>  
  
 <span data-ttu-id="b8ad3-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b8ad3-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b8ad3-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="b8ad3-105">\<bindings></span></span>  
<span data-ttu-id="b8ad3-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="b8ad3-106">\<netHttpBinding></span></span>  
<span data-ttu-id="b8ad3-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="b8ad3-107">\<binding></span></span>  
<span data-ttu-id="b8ad3-108">\<security></span><span class="sxs-lookup"><span data-stu-id="b8ad3-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8ad3-109">구문</span><span class="sxs-lookup"><span data-stu-id="b8ad3-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None/Transport/TransportWithCredential">  
   <transport  
      clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"  
      proxyCredentialType="Basic/Digest/None/Ntlm/Windows"  
      realm="string" />  
   <message  
      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
            clientCredentialType="Certificate/IssuedToken/None/UserName/Windows" />  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b8ad3-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="b8ad3-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b8ad3-111">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-111">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b8ad3-112">특성</span><span class="sxs-lookup"><span data-stu-id="b8ad3-112">Attributes</span></span>  
  
|<span data-ttu-id="b8ad3-113">특성</span><span class="sxs-lookup"><span data-stu-id="b8ad3-113">Attribute</span></span>|<span data-ttu-id="b8ad3-114">설명</span><span class="sxs-lookup"><span data-stu-id="b8ad3-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b8ad3-115">모드</span><span class="sxs-lookup"><span data-stu-id="b8ad3-115">mode</span></span>|<span data-ttu-id="b8ad3-116">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-116">Optional.</span></span> <span data-ttu-id="b8ad3-117">사용되는 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-117">Specifies the type of security that is used.</span></span> <span data-ttu-id="b8ad3-118">기본값은 `None`입니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-118">The default is `None`.</span></span> <span data-ttu-id="b8ad3-119">이 특성은 형식 <!--zz <xref:System.ServiceModel.NetHttpSecurityMode> --> `System.ServiceModel.NetHttpSecurityMode`합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-119">This attribute is of type <!--zz <xref:System.ServiceModel.NetHttpSecurityMode> -->`System.ServiceModel.NetHttpSecurityMode`.</span></span>|
  
## <a name="mode-attribute"></a><span data-ttu-id="b8ad3-120">mode 특성</span><span class="sxs-lookup"><span data-stu-id="b8ad3-120">mode Attribute</span></span>  
  
|<span data-ttu-id="b8ad3-121">값</span><span class="sxs-lookup"><span data-stu-id="b8ad3-121">Value</span></span>|<span data-ttu-id="b8ad3-122">설명</span><span class="sxs-lookup"><span data-stu-id="b8ad3-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b8ad3-123">없음</span><span class="sxs-lookup"><span data-stu-id="b8ad3-123">None</span></span>|<span data-ttu-id="b8ad3-124">-메시지 전송 하는 동안 보안이 유지 되지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-124">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="b8ad3-125">전송</span><span class="sxs-lookup"><span data-stu-id="b8ad3-125">Transport</span></span>|<span data-ttu-id="b8ad3-126">HTTPS 전송을 사용하여 보안이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-126">Security is provided using HTTPS transport.</span></span> <span data-ttu-id="b8ad3-127">SOAP 메시지는 HTTPS를 사용하여 보호됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-127">The SOAP messages are secured using HTTPS.</span></span> <span data-ttu-id="b8ad3-128">이 서비스는 서비스의 X.509 인증서를 사용하여 클라이언트에 인증됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-128">The service is authenticated to the client using the service's X.509 certificate.</span></span> <span data-ttu-id="b8ad3-129">클라이언트는 제공된 ClientCredentialType을 사용하여 인증됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-129">The client is authenticated using the ClientCredentialType supplied.</span></span>|  
|<span data-ttu-id="b8ad3-130">메시지</span><span class="sxs-lookup"><span data-stu-id="b8ad3-130">Message</span></span>|<span data-ttu-id="b8ad3-131">SOAP 메시지 보안을 사용하여 보안이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-131">Security is provided using SOAP message security.</span></span> <span data-ttu-id="b8ad3-132">기본적으로 본문에는 암호화 및 서명이 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-132">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="b8ad3-133">이 바인딩에서는 클라이언트에 out of band 방식으로 서버 인증서가 제공되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-133">For this binding, the system requires that the server certificate be provided to the client out of band.</span></span> <span data-ttu-id="b8ad3-134">이 바인딩의 유효한 `ClientCredentialType`은 `Certificate`뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-134">The only valid `ClientCredentialType` for this binding is `Certificate`.</span></span>|  
|<span data-ttu-id="b8ad3-135">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="b8ad3-135">TransportWithMessageCredential</span></span>|<span data-ttu-id="b8ad3-136">전송 보안에 의해 무결성, 기밀성 및 서버 인증이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-136">Integrity, confidentiality and server authentication are provided by transport security.</span></span> <span data-ttu-id="b8ad3-137">클라이언트 인증은 SOAP 메시지 보안에 의해 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-137">Client authentication is provided by means of SOAP message security.</span></span> <span data-ttu-id="b8ad3-138">이 모드는 사용자가 사용자 이름/암호를 사용하여 인증되며 메시지 전송 보호를 위한 기존의 HTTP 배포가 있는 경우에 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-138">This mode is relevant when the user is authenticating using username/password and there is an existing HTTP deployment for securing message transfer.</span></span>|  
|<span data-ttu-id="b8ad3-139">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="b8ad3-139">TransportCredentialOnly</span></span>|<span data-ttu-id="b8ad3-140">이 모드는 메시지 무결성 및 기밀성을 제공하지 않으나</span><span class="sxs-lookup"><span data-stu-id="b8ad3-140">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="b8ad3-141">http 기반 클라이언트 인증을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-141">It provides http-based client authentication.</span></span> <span data-ttu-id="b8ad3-142">이 모드는 주의해서 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-142">This mode should be used with caution.</span></span> <span data-ttu-id="b8ad3-143">전송 보안 (예: IPSec) 다른 방법으로 제공 되 고 WCF 인프라에서 클라이언트 인증만 제공 하는 환경에서는 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-143">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b8ad3-144">자식 요소</span><span class="sxs-lookup"><span data-stu-id="b8ad3-144">Child Elements</span></span>  
  
|<span data-ttu-id="b8ad3-145">요소</span><span class="sxs-lookup"><span data-stu-id="b8ad3-145">Element</span></span>|<span data-ttu-id="b8ad3-146">설명</span><span class="sxs-lookup"><span data-stu-id="b8ad3-146">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b8ad3-147">\<transport></span><span class="sxs-lookup"><span data-stu-id="b8ad3-147">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-nethttpbinding.md)|<span data-ttu-id="b8ad3-148">기본 HTTP 서비스에 대한 전송 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-148">Defines the transport security settings for a basic HTTP service.</span></span> <span data-ttu-id="b8ad3-149">이 요소는 <xref:System.ServiceModel.HttpTransportSecurity>에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-149">This element corresponds to <xref:System.ServiceModel.HttpTransportSecurity>.</span></span>|  
|[<span data-ttu-id="b8ad3-150">\<message></span><span class="sxs-lookup"><span data-stu-id="b8ad3-150">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-nethttpbinding.md)|<span data-ttu-id="b8ad3-151">기본 HTTP 서비스에 대한 메시지 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-151">Defines the message security settings for a basic HTTP service.</span></span> <span data-ttu-id="b8ad3-152">이 요소에 해당 <!--zz <xref:System.ServiceModel.NetHttpMessageSecurity> --> `System.ServiceModel.NetHttpMessageSecurity`합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-152">This element corresponds to <!--zz <xref:System.ServiceModel.NetHttpMessageSecurity> --> `System.ServiceModel.NetHttpMessageSecurity`.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b8ad3-153">부모 요소</span><span class="sxs-lookup"><span data-stu-id="b8ad3-153">Parent Elements</span></span>  
  
|<span data-ttu-id="b8ad3-154">요소</span><span class="sxs-lookup"><span data-stu-id="b8ad3-154">Element</span></span>|<span data-ttu-id="b8ad3-155">설명</span><span class="sxs-lookup"><span data-stu-id="b8ad3-155">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b8ad3-156">바인딩</span><span class="sxs-lookup"><span data-stu-id="b8ad3-156">binding</span></span>|<span data-ttu-id="b8ad3-157">바인딩 요소를 [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-157">The binding element of the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b8ad3-158">설명</span><span class="sxs-lookup"><span data-stu-id="b8ad3-158">Remarks</span></span>  
 <span data-ttu-id="b8ad3-159">기본적으로 SOAP 메시지의 보안이 유지되지 않고 클라이언트가 인증되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-159">By default, the SOAP message is not secured and the client is not authenticated.</span></span> <span data-ttu-id="b8ad3-160">이 요소를 사용하면 `netHttpBinding` 요소에 대한 추가 보안 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8ad3-160">This element enables you to configure additional security settings for the `netHttpBinding` element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8ad3-161">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b8ad3-161">See Also</span></span>  
 <xref:System.ServiceModel.NetHttpBinding.Security%2A>  
 <xref:System.ServiceModel.Configuration.NetHttpBindingElement.Security%2A>    
 [<span data-ttu-id="b8ad3-162">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="b8ad3-162">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="b8ad3-163">자격 증명 형식 선택</span><span class="sxs-lookup"><span data-stu-id="b8ad3-163">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)  
 [<span data-ttu-id="b8ad3-164">바인딩</span><span class="sxs-lookup"><span data-stu-id="b8ad3-164">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="b8ad3-165">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="b8ad3-165">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="b8ad3-166">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="b8ad3-166">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="b8ad3-167">\<binding></span><span class="sxs-lookup"><span data-stu-id="b8ad3-167">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
