---
title: '&lt;messageSenderAuthentication&gt; 요소'
ms.date: 03/30/2017
ms.assetid: 8d979dfc-a6f9-42ec-96d5-7fbc13a48118
ms.openlocfilehash: 9b5155e579973555db1fefb6b22bd6c1ff38ea70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54579903"
---
# <a name="ltmessagesenderauthenticationgt-element"></a><span data-ttu-id="4d08f-102">&lt;messageSenderAuthentication&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="4d08f-102">&lt;messageSenderAuthentication&gt; element</span></span>
<span data-ttu-id="4d08f-103">피어 투 피어 메시지 발신자에 대한 인증 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-103">Specifies authentication options for peer-to-peer message senders.</span></span>  
  
 <span data-ttu-id="4d08f-104">피어 투 피어 프로그래밍에 대 한 자세한 내용은 참조 하세요. [피어-투-피어 네트워킹](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-104">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
 <span data-ttu-id="4d08f-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4d08f-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="4d08f-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="4d08f-106">\<behaviors></span></span>  
<span data-ttu-id="4d08f-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="4d08f-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="4d08f-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4d08f-108">\<behavior></span></span>  
<span data-ttu-id="4d08f-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="4d08f-109">\<clientCredentials></span></span>  
<span data-ttu-id="4d08f-110">\<peer></span><span class="sxs-lookup"><span data-stu-id="4d08f-110">\<peer></span></span>  
<span data-ttu-id="4d08f-111">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="4d08f-111">\<messageSenderAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d08f-112">구문</span><span class="sxs-lookup"><span data-stu-id="4d08f-112">Syntax</span></span>  
  
```xml  
<messageSenderAuthentication customCertificateValidatorType= "namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"
                             certificateValidationMode = "ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"
                             revocationMode="NoCheck/Online/Offline"
                             trustedStoreLocation="CurrentUser/LocalMachine" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4d08f-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4d08f-113">Attributes and Elements</span></span>  
 <span data-ttu-id="4d08f-114">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-114">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4d08f-115">특성</span><span class="sxs-lookup"><span data-stu-id="4d08f-115">Attributes</span></span>  
  
|<span data-ttu-id="4d08f-116">특성</span><span class="sxs-lookup"><span data-stu-id="4d08f-116">Attribute</span></span>|<span data-ttu-id="4d08f-117">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4d08f-118">customCertificateValidatorType</span><span class="sxs-lookup"><span data-stu-id="4d08f-118">customCertificateValidatorType</span></span>|<span data-ttu-id="4d08f-119">사용자 지정 형식의 유효성을 검사하는 데 사용되는 형식 및 어셈블리입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-119">A type and assembly used to validate a custom type.</span></span> <span data-ttu-id="4d08f-120">이 특성은 `certificateValidationMode`가 `Custom`으로 설정되어 있을 때 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-120">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span>|  
|<span data-ttu-id="4d08f-121">certifcateValidationMode</span><span class="sxs-lookup"><span data-stu-id="4d08f-121">certifcateValidationMode</span></span>|<span data-ttu-id="4d08f-122">자격 증명의 유효성을 검사하는 데 사용되는 세 가지 모드 중 하나를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-122">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="4d08f-123">`Custom`으로 설정되면 `customCertificateValidator`도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-123">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|<span data-ttu-id="4d08f-124">revocationMode</span><span class="sxs-lookup"><span data-stu-id="4d08f-124">revocationMode</span></span>|<span data-ttu-id="4d08f-125">CRL(해지된 인증서 목록)을 검사하는 데 사용되는 모드 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-125">One of the modes used to check for a revoked certificate lists (CRL).</span></span>|  
|<span data-ttu-id="4d08f-126">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="4d08f-126">trustedStoreLocation</span></span>|<span data-ttu-id="4d08f-127">시스템 저장소 위치 `LocalMachine` 또는 `CurrentUser` 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-127">One of the two system store locations: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="4d08f-128">서비스 인증서가 클라이언트와 협상될 때 이 값이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-128">This value is used when a service certificate is negotiated to the client.</span></span> <span data-ttu-id="4d08f-129">에 대 한 유효성 검사를 수행 합니다 **신뢰할 수 있는 사용자** 지정한 저장소 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-129">Validation is performed against the **Trusted People** store in the specified store location.</span></span>|  
  
## <a name="customcertificatevalidatortype-attribute"></a><span data-ttu-id="4d08f-130">customCertificateValidatorType 특성</span><span class="sxs-lookup"><span data-stu-id="4d08f-130">customCertificateValidatorType Attribute</span></span>  
  
|<span data-ttu-id="4d08f-131">값</span><span class="sxs-lookup"><span data-stu-id="4d08f-131">Value</span></span>|<span data-ttu-id="4d08f-132">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4d08f-133">문자열</span><span class="sxs-lookup"><span data-stu-id="4d08f-133">String</span></span>|<span data-ttu-id="4d08f-134">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-134">Optional.</span></span> <span data-ttu-id="4d08f-135">형식 이름 및 어셈블리와 형식을 찾는 데 사용되는 기타 데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-135">Specifies the type name and assembly and other data used to find the type.</span></span> <span data-ttu-id="4d08f-136">적어도 네임스페이스 및 형식 이름이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-136">At minimum, a namespace and type name are required.</span></span> <span data-ttu-id="4d08f-137">선택적 정보로는 어셈블리 이름, 버전 번호, 문화권 및 공개 키 토큰이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-137">Optional information includes: assembly name, version number, culture, and public key token.</span></span>|  
  
## <a name="certificatevalidationmode-attribute"></a><span data-ttu-id="4d08f-138">certificateValidationMode 특성</span><span class="sxs-lookup"><span data-stu-id="4d08f-138">certificateValidationMode Attribute</span></span>  
  
|<span data-ttu-id="4d08f-139">값</span><span class="sxs-lookup"><span data-stu-id="4d08f-139">Value</span></span>|<span data-ttu-id="4d08f-140">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-140">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4d08f-141">열거형</span><span class="sxs-lookup"><span data-stu-id="4d08f-141">Enumeration</span></span>|<span data-ttu-id="4d08f-142">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-142">Optional.</span></span> <span data-ttu-id="4d08f-143">`None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust`, `Custom` 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-143">One of the following values: `None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust`, `Custom`.</span></span> <span data-ttu-id="4d08f-144">기본값은 `ChainTrust`입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-144">The default is `ChainTrust`.</span></span> <span data-ttu-id="4d08f-145">기본값은 `ChainTrust`입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-145">The default is `ChainTrust`.</span></span><br /><br /> <span data-ttu-id="4d08f-146">자세한 내용은 [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-146">For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="revocationmode-attribute"></a><span data-ttu-id="4d08f-147">revocationMode 특성</span><span class="sxs-lookup"><span data-stu-id="4d08f-147">revocationMode Attribute</span></span>  
  
|<span data-ttu-id="4d08f-148">값</span><span class="sxs-lookup"><span data-stu-id="4d08f-148">Value</span></span>|<span data-ttu-id="4d08f-149">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-149">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4d08f-150">열거형</span><span class="sxs-lookup"><span data-stu-id="4d08f-150">Enumeration</span></span>|<span data-ttu-id="4d08f-151">`NoCheck`, `Online`, `Offline` 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-151">One of the following values: `NoCheck`, `Online`, `Offline`.</span></span> <span data-ttu-id="4d08f-152">기본값은 `Online`입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-152">The default is `Online`.</span></span><br /><br /> <span data-ttu-id="4d08f-153">자세한 내용은 [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-153">For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="trustedstorelocation-attribute"></a><span data-ttu-id="4d08f-154">trustedStoreLocation 특성</span><span class="sxs-lookup"><span data-stu-id="4d08f-154">trustedStoreLocation Attribute</span></span>  
  
|<span data-ttu-id="4d08f-155">값</span><span class="sxs-lookup"><span data-stu-id="4d08f-155">Value</span></span>|<span data-ttu-id="4d08f-156">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-156">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4d08f-157">열거형</span><span class="sxs-lookup"><span data-stu-id="4d08f-157">Enumeration</span></span>|<span data-ttu-id="4d08f-158">`LocalMachine` 또는 `CurrentUser` 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-158">One of the following values: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="4d08f-159">기본값은 `CurrentUser`입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-159">The default is `CurrentUser`.</span></span> <span data-ttu-id="4d08f-160">시스템 계정으로 클라이언트 응용 프로그램을 실행하는 경우 인증서는 대개 `LocalMachine`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-160">If the client application is running under a system account then the certificate is typically under `LocalMachine`.</span></span> <span data-ttu-id="4d08f-161">사용자 계정으로 클라이언트 응용 프로그램을 실행하는 경우 인증서는 대개 `CurrentUser`에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-161">If the client application is running under a user account then the certificate is typically in `CurrentUser`.</span></span> <span data-ttu-id="4d08f-162">기본값은 `CurrentUser`입니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-162">The default is `CurrentUser`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4d08f-163">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4d08f-163">Child Elements</span></span>  
 <span data-ttu-id="4d08f-164">없음</span><span class="sxs-lookup"><span data-stu-id="4d08f-164">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4d08f-165">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4d08f-165">Parent Elements</span></span>  
  
|<span data-ttu-id="4d08f-166">요소</span><span class="sxs-lookup"><span data-stu-id="4d08f-166">Element</span></span>|<span data-ttu-id="4d08f-167">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-167">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4d08f-168">\<peer></span><span class="sxs-lookup"><span data-stu-id="4d08f-168">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="4d08f-169">피어 서비스에 대해 클라이언트를 인증하는 데 사용되는 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-169">Specifies a credential used for authenticating the client to a peer service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4d08f-170">설명</span><span class="sxs-lookup"><span data-stu-id="4d08f-170">Remarks</span></span>  
 <span data-ttu-id="4d08f-171">메시지 인증을 선택하면 이 요소를 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-171">This element must be configured if message authentication is chosen.</span></span> <span data-ttu-id="4d08f-172">제공한 인증서를 사용 하 여 각 메시지는 서명 하는 출력 채널의 경우 [ \<인증서 >](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-172">For output channels, each message is signed using the certificate provided by [\<certificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md).</span></span> <span data-ttu-id="4d08f-173">모든 메시지는 응용 프로그램에 배달되기 전에 이 요소의 `customCertificateValidatorType` 특성에 지정된 유효성 검사기를 사용하여 메시지 자격 증명과 비교하여 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-173">All messages, before delivered to the application, are checked against the message credential using the validator specified by the `customCertificateValidatorType` attribute of this element.</span></span> <span data-ttu-id="4d08f-174">유효성 검사기는 자격 증명을 수락하거나 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-174">The validator can either accept or reject the credential.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4d08f-175">예제</span><span class="sxs-lookup"><span data-stu-id="4d08f-175">Example</span></span>  
 <span data-ttu-id="4d08f-176">다음 코드에서는 메시지 발신자 유효성 검사 모드를 `PeerOrChainTrust`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d08f-176">The following code sets the message sender validation mode to `PeerOrChainTrust`.</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <peer>
          <certificate findValue="www.contoso.com"
                       storeLocation="LocalMachine"
                       x509FindType="FindByIssuerName" />
          <messageSenderAuthentication certificateValidationMode="PeerOrChainTrust" />
          <messageSenderAuthentication certificateValidationMode="None" />
        </peer>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="4d08f-177">참고자료</span><span class="sxs-lookup"><span data-stu-id="4d08f-177">See also</span></span>
- <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>
- <xref:System.ServiceModel.Security.PeerCredential.MessageSenderAuthentication%2A>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.MessageSenderAuthentication%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>
- [<span data-ttu-id="4d08f-178">인증서 작업</span><span class="sxs-lookup"><span data-stu-id="4d08f-178">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="4d08f-179">피어 투 피어 네트워킹</span><span class="sxs-lookup"><span data-stu-id="4d08f-179">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="4d08f-180">피어 채널 메시지 인증</span><span class="sxs-lookup"><span data-stu-id="4d08f-180">Peer Channel Message Authentication</span></span>](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [<span data-ttu-id="4d08f-181">피어 채널 사용자 지정 인증</span><span class="sxs-lookup"><span data-stu-id="4d08f-181">Peer Channel Custom Authentication</span></span>](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [<span data-ttu-id="4d08f-182">피어 채널 애플리케이션 보안</span><span class="sxs-lookup"><span data-stu-id="4d08f-182">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
