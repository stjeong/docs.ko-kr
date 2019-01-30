---
title: <add>의 <issuerChannelBehaviors>
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: 65c76cba696ae388d6184eaaa70a1f2f5a301e1c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271797"
---
# <a name="add-of-issuerchannelbehaviors"></a><span data-ttu-id="6145e-102">\<추가 >의 \<issuerChannelBehaviors ></span><span class="sxs-lookup"><span data-stu-id="6145e-102">\<add> of \<issuerChannelBehaviors></span></span>
<span data-ttu-id="6145e-103">STS와 통신할 때 사용할 엔드포인트 동작을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-103">Adds an endpoint behavior to be used when communicating with an STS.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6145e-104">끝점 동작을 포함 하는 경우는 [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) 요소에서 예외가 throw 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-104">If any endpoint behavior contains a [\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) element, an exception will be thrown.</span></span>  
  
 <span data-ttu-id="6145e-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="6145e-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="6145e-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="6145e-106">\<behaviors></span></span>  
<span data-ttu-id="6145e-107">endpointBehaviors 섹션</span><span class="sxs-lookup"><span data-stu-id="6145e-107">endpointBehaviors section</span></span>  
<span data-ttu-id="6145e-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="6145e-108">\<behavior></span></span>  
<span data-ttu-id="6145e-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="6145e-109">\<clientCredentials></span></span>  
<span data-ttu-id="6145e-110">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="6145e-110">\<issuedToken></span></span>  
<span data-ttu-id="6145e-111">\<issuerChannelBehaviors > 요소</span><span class="sxs-lookup"><span data-stu-id="6145e-111">\<issuerChannelBehaviors> Element</span></span>  
<span data-ttu-id="6145e-112">\<add></span><span class="sxs-lookup"><span data-stu-id="6145e-112">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6145e-113">구문</span><span class="sxs-lookup"><span data-stu-id="6145e-113">Syntax</span></span>  
  
```xml  
<add issuerAddress="string"
     behaviorConfiguraton="string" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6145e-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="6145e-114">Attributes and Elements</span></span>  
 <span data-ttu-id="6145e-115">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-115">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6145e-116">특성</span><span class="sxs-lookup"><span data-stu-id="6145e-116">Attributes</span></span>  
  
|<span data-ttu-id="6145e-117">특성</span><span class="sxs-lookup"><span data-stu-id="6145e-117">Attribute</span></span>|<span data-ttu-id="6145e-118">설명</span><span class="sxs-lookup"><span data-stu-id="6145e-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6145e-119">issuerAddress</span><span class="sxs-lookup"><span data-stu-id="6145e-119">issuerAddress</span></span>|<span data-ttu-id="6145e-120">통신할 보안 토큰 발급자의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-120">The URI of the security token issuer to communicate with.</span></span>|  
|<span data-ttu-id="6145e-121">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6145e-121">behaviorConfiguration</span></span>|<span data-ttu-id="6145e-122">동일한 구성 파일에 정의된 엔드포인트 동작 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-122">The name of an endpoint behavior defined in the same configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6145e-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="6145e-123">Child Elements</span></span>  
 <span data-ttu-id="6145e-124">없음</span><span class="sxs-lookup"><span data-stu-id="6145e-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6145e-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="6145e-125">Parent Elements</span></span>  
  
|<span data-ttu-id="6145e-126">요소</span><span class="sxs-lookup"><span data-stu-id="6145e-126">Element</span></span>|<span data-ttu-id="6145e-127">설명</span><span class="sxs-lookup"><span data-stu-id="6145e-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6145e-128">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="6145e-128">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|<span data-ttu-id="6145e-129">지정한 서비스 토큰 서비스와 통신할 때 사용 되는 Windows Communication Foundation (WCF) 클라이언트 끝점 동작의 컬렉션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-129">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors to be used when communicating with the specified Service Token Services.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6145e-130">설명</span><span class="sxs-lookup"><span data-stu-id="6145e-130">Remarks</span></span>  
 <span data-ttu-id="6145e-131">`issuerAddress`는 클라이언트가 통신하려는 보안 토큰 서비스의 URI를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-131">`issuerAddress` contains the URI of the Security Token Service that the client wants to communicate with.</span></span> <span data-ttu-id="6145e-132">`behaviorConfiguration` 응용 프로그램 보안 토큰 서비스에서 발급 된 토큰을 가져오기 위해 Windows Communication Foundation (WCF)에서 만든 채널에서 사용 하는 끝점 동작을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="6145e-132">`behaviorConfiguration` points to an endpoint behavior that the application uses in the channels created by Windows Communication Foundation (WCF) to get the issued tokens from the Security Token Services.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6145e-133">참고자료</span><span class="sxs-lookup"><span data-stu-id="6145e-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="6145e-134">서비스 ID 및 인증</span><span class="sxs-lookup"><span data-stu-id="6145e-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="6145e-135">보안 동작</span><span class="sxs-lookup"><span data-stu-id="6145e-135">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="6145e-136">페더레이션 및 발급된 토큰</span><span class="sxs-lookup"><span data-stu-id="6145e-136">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="6145e-137">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="6145e-137">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="6145e-138">클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="6145e-138">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="6145e-139">방법: 페더레이션된 클라이언트 만들기</span><span class="sxs-lookup"><span data-stu-id="6145e-139">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="6145e-140">방법: 로컬 발급자 구성</span><span class="sxs-lookup"><span data-stu-id="6145e-140">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="6145e-141">페더레이션 및 발급된 토큰</span><span class="sxs-lookup"><span data-stu-id="6145e-141">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="6145e-142">\<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="6145e-142">\<issuerChannelBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)
