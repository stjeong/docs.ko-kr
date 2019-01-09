---
title: '&lt;ServiceCredentials&gt;'
ms.date: 03/30/2017
ms.assetid: 96db336c-4f7a-4193-81a5-910b8ffd804f
ms.openlocfilehash: b9e32509a5e182301455eaf0e602a03c51fbc23a
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150775"
---
# <a name="ltservicecredentialsgt"></a><span data-ttu-id="5771f-102">&lt;ServiceCredentials&gt;</span><span class="sxs-lookup"><span data-stu-id="5771f-102">&lt;serviceCredentials&gt;</span></span>
<span data-ttu-id="5771f-103">서비스를 인증하는 데 사용되는 자격 증명 및 클라이언트 자격 증명 유효성 검사 관련 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-103">Specifies the credential to be used in authenticating the service and the client credential validation-related settings.</span></span>  
  
 <span data-ttu-id="5771f-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5771f-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5771f-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="5771f-105">\<behaviors></span></span>  
<span data-ttu-id="5771f-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="5771f-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="5771f-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="5771f-107">\<behavior></span></span>  
<span data-ttu-id="5771f-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="5771f-108">\<serviceCredentials></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5771f-109">구문</span><span class="sxs-lookup"><span data-stu-id="5771f-109">Syntax</span></span>  
  
```xml  
<serviceCredentials type="String">
  <clientCertificate>
  </clientCertificate>
  <issuedTokenAuthentication>
  </issuedTokenAuthentication>
  <peer>
  </peer>
  <secureConversationAuthentication>
  </secureConversationAuthentication>
  <serviceCertificate>
  </serviceCertificate>
  <userNameAuthentication>
  </userNameAuthentication>
  <windowsAuthentication>
  </windowsAuthentication>
</serviceCredentials>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5771f-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="5771f-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5771f-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5771f-112">특성</span><span class="sxs-lookup"><span data-stu-id="5771f-112">Attributes</span></span>  
  
|<span data-ttu-id="5771f-113">특성</span><span class="sxs-lookup"><span data-stu-id="5771f-113">Attribute</span></span>|<span data-ttu-id="5771f-114">설명</span><span class="sxs-lookup"><span data-stu-id="5771f-114">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="5771f-115">이 구성 요소의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-115">A string that specifies the type of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5771f-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="5771f-116">Child Elements</span></span>  
  
|<span data-ttu-id="5771f-117">요소</span><span class="sxs-lookup"><span data-stu-id="5771f-117">Element</span></span>|<span data-ttu-id="5771f-118">설명</span><span class="sxs-lookup"><span data-stu-id="5771f-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5771f-119">\<clientCertificate ></span><span class="sxs-lookup"><span data-stu-id="5771f-119">\<clientCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md)|<span data-ttu-id="5771f-120">클라이언트 인증서가 out-of-band 방식으로 제공될 때 사용할 인증서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-120">Specifies the certificate to be used when the client certificate is available out-of-band.</span></span> <span data-ttu-id="5771f-121">이 요소는 클라이언트 인증서 유효성 검사 설정도 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-121">This element also specifies client certificate validation settings.</span></span> <span data-ttu-id="5771f-122">이 요소는 <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-122">This element is of type <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>.</span></span>|  
|[<span data-ttu-id="5771f-123">\<issuedTokenAuthentication ></span><span class="sxs-lookup"><span data-stu-id="5771f-123">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)|<span data-ttu-id="5771f-124">이 서비스에 대해 현재 발급된 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-124">Specifies the current issued token for this service.</span></span> <span data-ttu-id="5771f-125">이 요소는 <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-125">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement>.</span></span>|  
|[<span data-ttu-id="5771f-126">\<peer></span><span class="sxs-lookup"><span data-stu-id="5771f-126">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-servicecredentials.md)|<span data-ttu-id="5771f-127">피어 노드에 대한 현재 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-127">Specifies the current credentials for a peer node.</span></span> <span data-ttu-id="5771f-128">이 요소는 <xref:System.ServiceModel.Configuration.PeerCredentialElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-128">This element is of type <xref:System.ServiceModel.Configuration.PeerCredentialElement>.</span></span>|  
|[<span data-ttu-id="5771f-129">\<secureConversationAuthentication ></span><span class="sxs-lookup"><span data-stu-id="5771f-129">\<secureConversationAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationauthentication-of-servicecredential.md)|<span data-ttu-id="5771f-130">보안 대화에 대한 현재 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-130">Specifies the current credentials for a secure conversation.</span></span> <span data-ttu-id="5771f-131">이 요소는 <xref:System.ServiceModel.Configuration.SecureConversationServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-131">This element is of type <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>.</span></span>|  
|[<span data-ttu-id="5771f-132">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="5771f-132">\<serviceCertificate></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md)|<span data-ttu-id="5771f-133">자체 식별을 위해 서비스에서 사용되는 인증서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-133">Specifies a certificate used by a service to identify itself.</span></span> <span data-ttu-id="5771f-134">이 요소는 <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-134">This element is of type <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>.</span></span>|  
|[<span data-ttu-id="5771f-135">\<userNameAuthentication ></span><span class="sxs-lookup"><span data-stu-id="5771f-135">\<userNameAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/usernameauthentication.md)|<span data-ttu-id="5771f-136">사용자 이름 암호 유효성 검사의 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-136">Specifies the settings for username password validation.</span></span> <span data-ttu-id="5771f-137">이 요소는 <xref:System.ServiceModel.Configuration.UserNameServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-137">This element is of type <xref:System.ServiceModel.Configuration.UserNameServiceElement>.</span></span>|  
|[<span data-ttu-id="5771f-138">\<windowsAuthentication ></span><span class="sxs-lookup"><span data-stu-id="5771f-138">\<windowsAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/windowsauthentication-of-servicecredentials.md)|<span data-ttu-id="5771f-139">Windows 자격 증명 유효성 검사의 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-139">Specifies the settings for Windows credential validation.</span></span> <span data-ttu-id="5771f-140">이 요소는 <xref:System.ServiceModel.Configuration.WindowsServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-140">This element is of type <xref:System.ServiceModel.Configuration.WindowsServiceElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5771f-141">부모 요소</span><span class="sxs-lookup"><span data-stu-id="5771f-141">Parent Elements</span></span>  
  
|<span data-ttu-id="5771f-142">요소</span><span class="sxs-lookup"><span data-stu-id="5771f-142">Element</span></span>|<span data-ttu-id="5771f-143">설명</span><span class="sxs-lookup"><span data-stu-id="5771f-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5771f-144">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="5771f-144">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="5771f-145">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5771f-145">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5771f-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5771f-146">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceCredentialsElement>  
 <xref:System.ServiceModel.Description.ServiceCredentials>  
 [<span data-ttu-id="5771f-147">보안 동작</span><span class="sxs-lookup"><span data-stu-id="5771f-147">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
