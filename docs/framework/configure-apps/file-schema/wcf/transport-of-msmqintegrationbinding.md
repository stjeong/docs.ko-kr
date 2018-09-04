---
title: '&lt;msmqIntegrationBinding&gt;의 &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: 054579e3-7fdd-47df-99ca-952706ba5c8e
ms.openlocfilehash: eb992a79a4a5a65404aec99cc84e9f1d78cb3f4b
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43535125"
---
# <a name="lttransportgt-of-ltmsmqintegrationbindinggt"></a><span data-ttu-id="a4a58-102">&lt;msmqIntegrationBinding&gt;의 &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="a4a58-102">&lt;transport&gt; of &lt;msmqIntegrationBinding&gt;</span></span>
<span data-ttu-id="a4a58-103">메시지 큐 통합 전송을 위한 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-103">Defines the security settings for the Message Queuing integration transport.</span></span>  
  
 <span data-ttu-id="a4a58-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a4a58-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a4a58-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="a4a58-105">\<bindings></span></span>  
<span data-ttu-id="a4a58-106">msmqIntegrationBinding</span><span class="sxs-lookup"><span data-stu-id="a4a58-106">msmqIntegrationBinding</span></span>  
<span data-ttu-id="a4a58-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="a4a58-107">\<binding></span></span>  
<span data-ttu-id="a4a58-108">\<security></span><span class="sxs-lookup"><span data-stu-id="a4a58-108">\<security></span></span>  
<span data-ttu-id="a4a58-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="a4a58-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4a58-110">구문</span><span class="sxs-lookup"><span data-stu-id="a4a58-110">Syntax</span></span>  
  
```xml  
<security>  
    <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"  
        msmqEncryptionAlgorithm="RC4Stream/AES"  
        msmqProtectionLevel="None/Sign/EncryptAndSign"  
        msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a4a58-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a4a58-111">Attributes and Elements</span></span>  
 <span data-ttu-id="a4a58-112">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a4a58-113">특성</span><span class="sxs-lookup"><span data-stu-id="a4a58-113">Attributes</span></span>  
  
|<span data-ttu-id="a4a58-114">특성</span><span class="sxs-lookup"><span data-stu-id="a4a58-114">Attribute</span></span>|<span data-ttu-id="a4a58-115">설명</span><span class="sxs-lookup"><span data-stu-id="a4a58-115">Description</span></span>|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|<span data-ttu-id="a4a58-116">메시지가 MSMQ 전송에 의해 인증되는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-116">Specifies how the message must be authenticated by the MSMQ transport.</span></span> <span data-ttu-id="a4a58-117">이 특성이 `None`으로 설정되면 `msmqProtectionLevel` 특성 값도 `None`으로 설정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-117">If this is set to `None`, the value of the `msmqProtectionLevel` attribute must also be set to `None`.</span></span><br /><br /> <span data-ttu-id="a4a58-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a4a58-119">-None: 인증 안 함.</span><span class="sxs-lookup"><span data-stu-id="a4a58-119">-   None: No authentication.</span></span><br /><span data-ttu-id="a4a58-120">-WindowsDomain: 인증 메커니즘은 메시지와 연결 된 SID에 대 한 X.509 인증서를 가져오는 Active Directory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-120">-   WindowsDomain: The authentication mechanism uses Active Directory to get the X.509 certificate for the SID associated with the message.</span></span> <span data-ttu-id="a4a58-121">그런 다음 이 인증서는 사용자에게 큐에 대한 쓰기 권한이 있는지 확인하기 위해 큐의 ACL을 검사하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-121">This is then used to check the ACL of the queue to ensure the user has permission to write to the queue.</span></span><br /><span data-ttu-id="a4a58-122">-채널 인증서를: 인증서 저장소에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-122">-   Certificate: The channel gets the certificate from the certificate store.</span></span><br /><br /> <span data-ttu-id="a4a58-123">기본값은 WindowsDomain입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-123">The default value is WindowsDomain.</span></span> <span data-ttu-id="a4a58-124">이 특성은 <xref:System.ServiceModel.MsmqAuthenticationMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-124">This attribute is of type <xref:System.ServiceModel.MsmqAuthenticationMode>.</span></span>|  
|`msmqEncryptionAlgorithm`|<span data-ttu-id="a4a58-125">메시지 큐 관리자 간에 메시지를 전송할 때 통신 중에 메시지 암호화에 사용할 알고리즘을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-125">Specifies the algorithm to be used for message encryption on the wire when transferring messages between message queue managers.</span></span> <span data-ttu-id="a4a58-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-126">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="a4a58-127">-RC4Stream</span><span class="sxs-lookup"><span data-stu-id="a4a58-127">-   RC4Stream</span></span><br /><span data-ttu-id="a4a58-128">-   AES</span><span class="sxs-lookup"><span data-stu-id="a4a58-128">-   AES</span></span><br /><br /> <span data-ttu-id="a4a58-129">기본값은 RC4Stream입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-129">The default value is RC4Stream.</span></span> <span data-ttu-id="a4a58-130">이 특성은 <xref:System.ServiceModel.MsmqEncryptionAlgorithm> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-130">This attribute is of type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.</span></span>|  
|`msmqProtectionLevel`|<span data-ttu-id="a4a58-131">메시지가 MSMQ 전송 수준에서 보호되는 방식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-131">Specifies how the message is secured at the level of the MSMQ transport.</span></span> <span data-ttu-id="a4a58-132">EncryptAndSign이 메시지 무결성 및 비부인을 보장하는 반면 암호화는 메시지 무결성을 보장합니다. 즉, 메시지는 실제로 보낸 사람으로부터 나오고 보낸 사람은 보낸 사람임을 밝히는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-132">Encryption ensures message integrity while EncryptAndSign ensures both message integrity and non-repudiation; that is, the message indeed comes from the sender and the sender is who he says he is.</span></span><br /><br /> <span data-ttu-id="a4a58-133">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-133">-   Valid values include the following:</span></span><br /><span data-ttu-id="a4a58-134">-None: 보호 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-134">-   None: No protection.</span></span><br /><span data-ttu-id="a4a58-135">-Sign: 메시지가 서명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-135">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="a4a58-136">-EncryptAndSign: 메시지가 암호화 되 고 서명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-136">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><br /> <span data-ttu-id="a4a58-137">기본값은 Sign입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-137">The default value is Sign.</span></span> <span data-ttu-id="a4a58-138">이 특성은 ProtectionLevel 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-138">This attribute is of type ProtectionLevel.</span></span>|  
|`msmqSecureHashAlgorithm`|<span data-ttu-id="a4a58-139">-서명의 일부로 다이제스트를 계산 하는 데 사용할 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-139">-   Specifies the algorithm to be used in computing the digest as part of signatures.</span></span> <span data-ttu-id="a4a58-140">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-140">Valid values include the following:</span></span><br /><span data-ttu-id="a4a58-141">-   MD5</span><span class="sxs-lookup"><span data-stu-id="a4a58-141">-   MD5</span></span><br /><span data-ttu-id="a4a58-142">-   SHA1</span><span class="sxs-lookup"><span data-stu-id="a4a58-142">-   SHA1</span></span><br /><span data-ttu-id="a4a58-143">-   SHA256</span><span class="sxs-lookup"><span data-stu-id="a4a58-143">-   SHA256</span></span><br /><span data-ttu-id="a4a58-144">-   SHA512</span><span class="sxs-lookup"><span data-stu-id="a4a58-144">-   SHA512</span></span><br /><br /> <span data-ttu-id="a4a58-145">기본값은 SHA1입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-145">The default value is SHA1.</span></span> <span data-ttu-id="a4a58-146">이 특성은 <xref:System.ServiceModel.MsmqSecureHashAlgorithm> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-146">This attribute is of type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a4a58-147">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a4a58-147">Child Elements</span></span>  
 <span data-ttu-id="a4a58-148">없음</span><span class="sxs-lookup"><span data-stu-id="a4a58-148">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a4a58-149">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a4a58-149">Parent Elements</span></span>  
  
|<span data-ttu-id="a4a58-150">요소</span><span class="sxs-lookup"><span data-stu-id="a4a58-150">Element</span></span>|<span data-ttu-id="a4a58-151">설명</span><span class="sxs-lookup"><span data-stu-id="a4a58-151">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a4a58-152">\<security></span><span class="sxs-lookup"><span data-stu-id="a4a58-152">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|<span data-ttu-id="a4a58-153">MSMQ 바인딩에 대한 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-153">Defines the security settings for a MSMQ binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a4a58-154">설명</span><span class="sxs-lookup"><span data-stu-id="a4a58-154">Remarks</span></span>  
 <span data-ttu-id="a4a58-155">이 요소는 메시지 큐 통합 전송을 위한 보안 설정을 캡슐화합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-155">This element encapsulates the security settings for the Message Queuing integration transport.</span></span> <span data-ttu-id="a4a58-156">설정은 메시지 큐 통합 및 대기 중인 전송에서 모두 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-156">The settings are the same for both the Message Queuing integration and queued transports.</span></span> <span data-ttu-id="a4a58-157">이 요소를 사용하여 인증 모드, 암호화 알고리즘, 보안 해시 알고리즘 및 보호 수준을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4a58-157">It enables you to set the Authentication Mode, Encryption Algorithm, Secure Hash Algorithm, and Protection Level.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4a58-158">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a4a58-158">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.MsmqIntegrationSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.MsmqTransportSecurity>  
 [<span data-ttu-id="a4a58-159">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="a4a58-159">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="a4a58-160">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="a4a58-160">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="a4a58-161">바인딩</span><span class="sxs-lookup"><span data-stu-id="a4a58-161">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="a4a58-162">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="a4a58-162">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="a4a58-163">바인딩을 사용 하 여 Windows Communication Foundation 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="a4a58-163">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="a4a58-164">\<binding></span><span class="sxs-lookup"><span data-stu-id="a4a58-164">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
