---
title: <clientCredentials>
ms.date: 03/30/2017
ms.assetid: 1e6eef0d-a34e-4d74-b0f7-f65d2181858d
ms.openlocfilehash: 7ee49d6960864826dc74fbff629f502fcc70b4bf
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254810"
---
# <a name="clientcredentials"></a><span data-ttu-id="bb6a2-101">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="bb6a2-101">\<clientCredentials></span></span>
<span data-ttu-id="bb6a2-102">클라이언트를 서비스에 인증하는 데 사용되는 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-102">Specifies the credentials used to authenticate the client to a service.</span></span>  
  
 <span data-ttu-id="bb6a2-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="bb6a2-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="bb6a2-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="bb6a2-104">\<behaviors></span></span>  
<span data-ttu-id="bb6a2-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="bb6a2-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="bb6a2-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="bb6a2-106">\<behavior></span></span>  
<span data-ttu-id="bb6a2-107">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="bb6a2-107">\<clientCredentials></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb6a2-108">구문</span><span class="sxs-lookup"><span data-stu-id="bb6a2-108">Syntax</span></span>  
  
```xml  
<clientCredentials type="String"
                   supportInteractive="Boolean" >
  <clientCertificate>
  </clientCertificate>
  <digest>
  </digest>
  <isuedToken>
  </isuedToken>
  <peer>
  </peer>
  <serviceCertificate>
  </serviceCertificate>
  <windowsAuthentication>
  </windowsAuthentication>
</clientCredentials>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bb6a2-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="bb6a2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="bb6a2-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bb6a2-111">특성</span><span class="sxs-lookup"><span data-stu-id="bb6a2-111">Attributes</span></span>  
  
|<span data-ttu-id="bb6a2-112">특성</span><span class="sxs-lookup"><span data-stu-id="bb6a2-112">Attribute</span></span>|<span data-ttu-id="bb6a2-113">설명</span><span class="sxs-lookup"><span data-stu-id="bb6a2-113">Description</span></span>|  
|---------------|-----------------|  
|`supportInteractive`|<span data-ttu-id="bb6a2-114">런타임에 클라이언트 자격 증명을 선택할 때 대화형 사용자가 포함될 수 있는지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-114">A Boolean value that specifies whether an interactive user can be involved in selecting a client credential at runtime.</span></span> <span data-ttu-id="bb6a2-115">기본값은 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-115">The default value is `true`.</span></span>|  
|`type`|<span data-ttu-id="bb6a2-116">이 구성 요소의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-116">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bb6a2-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="bb6a2-117">Child Elements</span></span>  
  
|<span data-ttu-id="bb6a2-118">요소</span><span class="sxs-lookup"><span data-stu-id="bb6a2-118">Element</span></span>|<span data-ttu-id="bb6a2-119">설명</span><span class="sxs-lookup"><span data-stu-id="bb6a2-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bb6a2-120">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="bb6a2-120">\<clientCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md)|<span data-ttu-id="bb6a2-121">클라이언트를 서비스에 인증하는 데 사용되는 인증서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-121">Specifies the certificate used to authenticate the client to the service.</span></span> <span data-ttu-id="bb6a2-122">이 요소는 <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-122">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="bb6a2-123">\<httpDigest></span><span class="sxs-lookup"><span data-stu-id="bb6a2-123">\<httpDigest></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/httpdigest-element.md)|<span data-ttu-id="bb6a2-124">클라이언트를 서비스에 인증하는 데 사용되는 다이제스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-124">Specifies a digest used to authenticate the client to the service.</span></span> <span data-ttu-id="bb6a2-125">이 요소는 <xref:System.ServiceModel.Configuration.HttpDigestClientElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-125">This element is of type <xref:System.ServiceModel.Configuration.HttpDigestClientElement>.</span></span>|  
|[<span data-ttu-id="bb6a2-126">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="bb6a2-126">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="bb6a2-127">클라이언트를 STS(보안 토큰 서비스)에 인증하는 데 사용되는 사용자 지정 토큰 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-127">Specifies a custom token type used to authenticate the client to a Secure Token Service (STS).</span></span> <span data-ttu-id="bb6a2-128">이 요소는 <xref:System.ServiceModel.Configuration.IssuedTokenClientElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-128">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenClientElement>.</span></span>|  
|[<span data-ttu-id="bb6a2-129">\<peer></span><span class="sxs-lookup"><span data-stu-id="bb6a2-129">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="bb6a2-130">현재 피어 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-130">Specifies a current peer credential.</span></span> <span data-ttu-id="bb6a2-131">이 요소는 <xref:System.ServiceModel.Configuration.PeerCredentialElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-131">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[<span data-ttu-id="bb6a2-132">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="bb6a2-132">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md)|<span data-ttu-id="bb6a2-133">서비스를 클라이언트에 인증하는 데 사용되는 인증서를 지정하고 인증서 옵션을 설정하기 위한 구조를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-133">Specifies the certificate used to authenticate the service to the client and provides a structure for setting certificate options.</span></span> <span data-ttu-id="bb6a2-134">이 인증서는 서비스로부터 클라이언트에게 out-of-band로 제공되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-134">This certificate must be supplied out-of-band from the service to the client.</span></span> <span data-ttu-id="bb6a2-135">이 요소는 <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-135">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>.</span></span>|  
|[<span data-ttu-id="bb6a2-136">\<windows></span><span class="sxs-lookup"><span data-stu-id="bb6a2-136">\<windows></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/windows-of-clientcredentials-element.md)|<span data-ttu-id="bb6a2-137">Windows 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-137">Specifies a Windows credential.</span></span> <span data-ttu-id="bb6a2-138">기본값은 현재 스레드의 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-138">The default is the credential of the current thread.</span></span> <span data-ttu-id="bb6a2-139">이 요소는 <xref:System.ServiceModel.Configuration.WindowsClientElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-139">This element is of type <xref:System.ServiceModel.Configuration.WindowsClientElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bb6a2-140">부모 요소</span><span class="sxs-lookup"><span data-stu-id="bb6a2-140">Parent Elements</span></span>  
  
|<span data-ttu-id="bb6a2-141">요소</span><span class="sxs-lookup"><span data-stu-id="bb6a2-141">Element</span></span>|<span data-ttu-id="bb6a2-142">설명</span><span class="sxs-lookup"><span data-stu-id="bb6a2-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bb6a2-143">\<behavior></span><span class="sxs-lookup"><span data-stu-id="bb6a2-143">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="bb6a2-144">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-144">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bb6a2-145">설명</span><span class="sxs-lookup"><span data-stu-id="bb6a2-145">Remarks</span></span>  
 <span data-ttu-id="bb6a2-146">클라이언트 자격 증명은 상호 인증이 필요한 경우 서비스에 대해 클라이언트를 인증하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-146">Client credentials are used to authenticate the client to services in cases where mutual authentication is required.</span></span> <span data-ttu-id="bb6a2-147">또한 이 구성 섹션은 클라이언트가 서비스 인증서를 사용하여 서비스에 대한 메시지 보안을 유지해야 하는 경우 서비스 인증서를 지정하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-147">This configuration section can also be used to specify service certificates for scenarios where the client must secure messages to a service with the service's certificate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb6a2-148">참고자료</span><span class="sxs-lookup"><span data-stu-id="bb6a2-148">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- [<span data-ttu-id="bb6a2-149">보안 동작</span><span class="sxs-lookup"><span data-stu-id="bb6a2-149">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="bb6a2-150">클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="bb6a2-150">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
