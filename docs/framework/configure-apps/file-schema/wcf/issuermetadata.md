---
title: '&lt;issuerMetadata&gt;'
ms.date: 03/30/2017
ms.assetid: e7eae2c0-cc17-4281-af59-e4eb8d54f92a
ms.openlocfilehash: 38fa373212464a7dc919c2f364524a391db17d43
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149360"
---
# <a name="ltissuermetadatagt"></a><span data-ttu-id="55693-102">&lt;issuerMetadata&gt;</span><span class="sxs-lookup"><span data-stu-id="55693-102">&lt;issuerMetadata&gt;</span></span>
<span data-ttu-id="55693-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="55693-103">\<system.serviceModel></span></span>  
<span data-ttu-id="55693-104">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="55693-104">\<bindings></span></span>  
<span data-ttu-id="55693-105">\<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="55693-105">\<wsFederationHttpBinding></span></span>  
<span data-ttu-id="55693-106">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="55693-106">\<binding></span></span>  
<span data-ttu-id="55693-107">\<security></span><span class="sxs-lookup"><span data-stu-id="55693-107">\<security></span></span>  
<span data-ttu-id="55693-108">\<message></span><span class="sxs-lookup"><span data-stu-id="55693-108">\<message></span></span>  
<span data-ttu-id="55693-109">\<issuerMetadata ></span><span class="sxs-lookup"><span data-stu-id="55693-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55693-110">구문</span><span class="sxs-lookup"><span data-stu-id="55693-110">Syntax</span></span>  
  
```xml  
<issuerMetadata address="String">
  <headers>
    <add name="String"
         namespace="String" />
  </headers>
  <identity>
    <certificate encodedValue="String" />
    <certificateReference findValue="String"
                          isChainIncluded="Boolean"
                          storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                          storeLocation="LocalMachine/CurrentUser"
                          x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
    <dns value="String" />
    <rsa value="String" />
    <servicePrincipalName value="String" />
    <usePrincipalName value="String" />
  </identity>
</issuerMetadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="55693-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="55693-111">Attributes and Elements</span></span>  
 <span data-ttu-id="55693-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="55693-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="55693-113">특성</span><span class="sxs-lookup"><span data-stu-id="55693-113">Attributes</span></span>  
  
|<span data-ttu-id="55693-114">특성</span><span class="sxs-lookup"><span data-stu-id="55693-114">Attribute</span></span>|<span data-ttu-id="55693-115">설명</span><span class="sxs-lookup"><span data-stu-id="55693-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="55693-116">address</span><span class="sxs-lookup"><span data-stu-id="55693-116">address</span></span>|<span data-ttu-id="55693-117">필수 `string` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="55693-117">Required `string` attribute.</span></span><br /><br /> <span data-ttu-id="55693-118">끝점의 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="55693-118">Specifies the address of the endpoint.</span></span> <span data-ttu-id="55693-119">주소는 절대 URI이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="55693-119">The address must be an absolute URI.</span></span> <span data-ttu-id="55693-120">기본값은 빈 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="55693-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="55693-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="55693-121">Child Elements</span></span>  
  
|<span data-ttu-id="55693-122">요소</span><span class="sxs-lookup"><span data-stu-id="55693-122">Element</span></span>|<span data-ttu-id="55693-123">설명</span><span class="sxs-lookup"><span data-stu-id="55693-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="55693-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="55693-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="55693-125">주소 헤더 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="55693-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="55693-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="55693-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="55693-127">한 엔드포인트에서 다른 엔드포인트와 메시지를 교환할 때 상대 엔드포인트를 인증할 수 있도록 하는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="55693-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="55693-128">부모 요소</span><span class="sxs-lookup"><span data-stu-id="55693-128">Parent Elements</span></span>  
  
|<span data-ttu-id="55693-129">요소</span><span class="sxs-lookup"><span data-stu-id="55693-129">Element</span></span>|<span data-ttu-id="55693-130">설명</span><span class="sxs-lookup"><span data-stu-id="55693-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="55693-131">\<message></span><span class="sxs-lookup"><span data-stu-id="55693-131">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="55693-132">에 대 한 메시지 수준 보안 설정을 정의 합니다 [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="55693-132">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="55693-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="55693-133">See Also</span></span>  
 <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A>  
 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.IssuerMetadata%2A>  
 [<span data-ttu-id="55693-134">서비스 ID 및 인증</span><span class="sxs-lookup"><span data-stu-id="55693-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="55693-135">페더레이션 및 발급된 토큰</span><span class="sxs-lookup"><span data-stu-id="55693-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="55693-136">사용자 지정 바인딩을 사용하는 보안 기능</span><span class="sxs-lookup"><span data-stu-id="55693-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="55693-137">페더레이션 및 발급된 토큰</span><span class="sxs-lookup"><span data-stu-id="55693-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
