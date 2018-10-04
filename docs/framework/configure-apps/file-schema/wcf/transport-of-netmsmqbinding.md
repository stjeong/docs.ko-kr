---
title: '&lt;netMsmqBinding&gt;의 &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: 72e1b338-39f0-4af1-a5d9-7a2fb79f6a0b
ms.openlocfilehash: 06114990f931eb06d064fcec425e9ab42507c932
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582309"
---
# <a name="lttransportgt-of-ltnetmsmqbindinggt"></a><span data-ttu-id="7f0ae-102">&lt;netMsmqBinding&gt;의 &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="7f0ae-102">&lt;transport&gt; of &lt;netMsmqBinding&gt;</span></span>
<span data-ttu-id="7f0ae-103">전송 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-103">Defines the transport security settings.</span></span>  
  
 <span data-ttu-id="7f0ae-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7f0ae-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7f0ae-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="7f0ae-105">\<bindings></span></span>  
<span data-ttu-id="7f0ae-106">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="7f0ae-106">\<netMsmqBinding></span></span>  
<span data-ttu-id="7f0ae-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="7f0ae-107">\<binding></span></span>  
<span data-ttu-id="7f0ae-108">\<security></span><span class="sxs-lookup"><span data-stu-id="7f0ae-108">\<security></span></span>  
<span data-ttu-id="7f0ae-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="7f0ae-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f0ae-110">구문</span><span class="sxs-lookup"><span data-stu-id="7f0ae-110">Syntax</span></span>  
  
```xml  
<netMsmqBinding>  
    <binding>  
    <security>  
         <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"  
            msmqEncryptionAlgorithm="RC4Stream/AES"  
            msmqProtectionLevel="None/Sign/EncryptAndSign"  
            msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
    </security>  
   </binding>  
</netMsmqBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7f0ae-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="7f0ae-111">Attributes and Elements</span></span>  
 <span data-ttu-id="7f0ae-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7f0ae-113">특성</span><span class="sxs-lookup"><span data-stu-id="7f0ae-113">Attributes</span></span>  
  
|<span data-ttu-id="7f0ae-114">특성</span><span class="sxs-lookup"><span data-stu-id="7f0ae-114">Attribute</span></span>|<span data-ttu-id="7f0ae-115">설명</span><span class="sxs-lookup"><span data-stu-id="7f0ae-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7f0ae-116">msmqAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="7f0ae-116">msmqAuthenticationMode</span></span>|<span data-ttu-id="7f0ae-117">메시지가 MSMQ 전송에 의해 인증되는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-117">Specifies how the message must be authenticated by the MSMQ transport.</span></span> <span data-ttu-id="7f0ae-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7f0ae-119">-None: 인증 안 함.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-119">-   None: No authentication.</span></span><br /><span data-ttu-id="7f0ae-120">-WindowsDomain: 인증 메커니즘 메시지에 연결 된 보안 식별자에 대 한 X.509 인증서를 검색할 Active Directory를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-120">-   WindowsDomain: The authentication mechanism uses Active Directory to retrieve the X.509 certificate for the security identifier associated with the message.</span></span> <span data-ttu-id="7f0ae-121">그런 다음 이 인증서는 사용자에게 큐에 대한 쓰기 권한이 있는지 확인하기 위해 큐의 ACL을 검사하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-121">This is then used to check the ACL of the queue to ensure the user has write permission for the queue.</span></span><br /><span data-ttu-id="7f0ae-122">-채널 인증서: 인증서 저장소에서 인증서를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-122">-   Certificate: The channel retrieves the certificate from the certificate store.</span></span><br /><br /> <span data-ttu-id="7f0ae-123">기본값은 `WindowsDomain`입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-123">The default is `WindowsDomain`.</span></span><br /><br /> <span data-ttu-id="7f0ae-124">이 특성이 `None`으로 설정되면 `msmqProtectionLevel` 특성도 `None`으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-124">If this attribute is set to `None`, the `msmqProtectionLevel` attribute must also be set to `None`.</span></span> <span data-ttu-id="7f0ae-125">이 특성은 <xref:System.ServiceModel.MsmqAuthenticationMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-125">This attribute is of type <xref:System.ServiceModel.MsmqAuthenticationMode></span></span>|  
|<span data-ttu-id="7f0ae-126">msmqEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7f0ae-126">msmqEncryptionAlgorithm</span></span>|<span data-ttu-id="7f0ae-127">메시지 큐 관리자 간에 메시지를 전송할 때 통신 중에 메시지 암호화에 사용할 알고리즘을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-127">Specifies the algorithm to be used for message encryption on the wire when transferring messages between message queue managers.</span></span> <span data-ttu-id="7f0ae-128">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-128">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7f0ae-129">-RC4Stream</span><span class="sxs-lookup"><span data-stu-id="7f0ae-129">-   RC4Stream</span></span><br /><span data-ttu-id="7f0ae-130">-   AES</span><span class="sxs-lookup"><span data-stu-id="7f0ae-130">-   AES</span></span><br /><span data-ttu-id="7f0ae-131">-기본값은 `RC4Stream`합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-131">-   The default value is `RC4Stream`.</span></span> <span data-ttu-id="7f0ae-132">이 특성은 <xref:System.ServiceModel.MsmqEncryptionAlgorithm> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-132">This attribute is of type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.</span></span>|  
|<span data-ttu-id="7f0ae-133">msmqProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="7f0ae-133">msmqProtectionLevel</span></span>|<span data-ttu-id="7f0ae-134">메시지가 MSMQ 전송 수준에서 보호되는 방식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-134">Specifies the way messages are secured at the level of the MSMQ transport.</span></span> <span data-ttu-id="7f0ae-135">암호화는 메시지 무결성을 보장하지만 서명 및 암호화는 메시지 무결성 및 부인 없음을 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-135">Encryption ensures message integrity, while sign and encrypt ensures both message integrity and non-repudiation.</span></span> <span data-ttu-id="7f0ae-136">즉 메시지는 실제로 해당 보낸 사람이 보낸 것이며 보낸 사람은 본인이 보낸 사람이라고 밝힌 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-136">That is, the message indeed came from the sender and the sender is who he says he is.</span></span> <span data-ttu-id="7f0ae-137">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-137">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7f0ae-138">-None: 보호 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-138">-   None: No protection.</span></span><br /><span data-ttu-id="7f0ae-139">-Sign: 메시지가 서명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-139">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="7f0ae-140">-EncryptAndSign: 메시지가 암호화 되 고 서명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-140">-   EncryptAndSign: Messages are encrypted and signed.</span></span><br /><span data-ttu-id="7f0ae-141">-기본값은 `Sign`합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-141">-   The default is `Sign`.</span></span>|  
|<span data-ttu-id="7f0ae-142">msmqSecureHashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7f0ae-142">msmqSecureHashAlgorithm</span></span>|<span data-ttu-id="7f0ae-143">메시지 다이제스트를 계산하는 데 사용할 해시 알고리즘을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-143">Specifies the hash algorithm to be used for computing the message digest.</span></span> <span data-ttu-id="7f0ae-144">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-144">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7f0ae-145">-   MD5</span><span class="sxs-lookup"><span data-stu-id="7f0ae-145">-   MD5</span></span><br /><span data-ttu-id="7f0ae-146">-   SHA1</span><span class="sxs-lookup"><span data-stu-id="7f0ae-146">-   SHA1</span></span><br /><span data-ttu-id="7f0ae-147">-   SHA256</span><span class="sxs-lookup"><span data-stu-id="7f0ae-147">-   SHA256</span></span><br /><span data-ttu-id="7f0ae-148">-   SHA512</span><span class="sxs-lookup"><span data-stu-id="7f0ae-148">-   SHA512</span></span><br /><br /> <span data-ttu-id="7f0ae-149">기본값은 `SHA1`입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-149">The default is `SHA1`.</span></span> <span data-ttu-id="7f0ae-150">이 특성은 <xref:System.ServiceModel.MsmqSecureHashAlgorithm> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-150">This attribute is of type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7f0ae-151">자식 요소</span><span class="sxs-lookup"><span data-stu-id="7f0ae-151">Child Elements</span></span>  
 <span data-ttu-id="7f0ae-152">없음</span><span class="sxs-lookup"><span data-stu-id="7f0ae-152">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7f0ae-153">부모 요소</span><span class="sxs-lookup"><span data-stu-id="7f0ae-153">Parent Elements</span></span>  
  
|<span data-ttu-id="7f0ae-154">요소</span><span class="sxs-lookup"><span data-stu-id="7f0ae-154">Element</span></span>|<span data-ttu-id="7f0ae-155">설명</span><span class="sxs-lookup"><span data-stu-id="7f0ae-155">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7f0ae-156">\<security></span><span class="sxs-lookup"><span data-stu-id="7f0ae-156">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|<span data-ttu-id="7f0ae-157">대기 중인 전송에 대한 전송 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0ae-157">Defines the transport security settings for queued transports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7f0ae-158">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7f0ae-158">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>  
 <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.NetMsmqSecurity.Transport%2A>  
 <xref:System.ServiceModel.MsmqTransportSecurity>  
 [<span data-ttu-id="7f0ae-159">WCF의 큐</span><span class="sxs-lookup"><span data-stu-id="7f0ae-159">Queues in WCF</span></span>](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [<span data-ttu-id="7f0ae-160">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="7f0ae-160">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="7f0ae-161">바인딩</span><span class="sxs-lookup"><span data-stu-id="7f0ae-161">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="7f0ae-162">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="7f0ae-162">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="7f0ae-163">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="7f0ae-163">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="7f0ae-164">\<binding></span><span class="sxs-lookup"><span data-stu-id="7f0ae-164">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
