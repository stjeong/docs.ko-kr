---
title: <xmlElement>
ms.date: 03/30/2017
ms.assetid: 395205c2-d8c0-4a5e-90f3-7ce3c085fccd
ms.openlocfilehash: 648147a7e3977648ac3c26c9dfc469629f3b70c3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278293"
---
# <a name="xmlelement"></a><span data-ttu-id="5084c-101">\<xmlElement></span><span class="sxs-lookup"><span data-stu-id="5084c-101">\<xmlElement></span></span>
<span data-ttu-id="5084c-102">토큰을 요청할 때 메시지 본문에서 보안 토큰 서비스로 보낼 XML 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5084c-102">Specifies an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>  
  
 <span data-ttu-id="5084c-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5084c-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="5084c-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="5084c-104">\<bindings></span></span>  
<span data-ttu-id="5084c-105">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="5084c-105">\<wsFederatedBinding></span></span>  
<span data-ttu-id="5084c-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="5084c-106">\<binding></span></span>  
<span data-ttu-id="5084c-107">\<security></span><span class="sxs-lookup"><span data-stu-id="5084c-107">\<security></span></span>  
<span data-ttu-id="5084c-108">\<message></span><span class="sxs-lookup"><span data-stu-id="5084c-108">\<message></span></span>  
<span data-ttu-id="5084c-109">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="5084c-109">\<tokenRequestParameters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5084c-110">구문</span><span class="sxs-lookup"><span data-stu-id="5084c-110">Syntax</span></span>  
  
```xml  
<tokenRequestParameters>
  <xmlElement xmlElement="String" />
</tokenRequestParameters>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5084c-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="5084c-111">Attributes and Elements</span></span>  
 <span data-ttu-id="5084c-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5084c-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5084c-113">특성</span><span class="sxs-lookup"><span data-stu-id="5084c-113">Attributes</span></span>  
  
|<span data-ttu-id="5084c-114">특성</span><span class="sxs-lookup"><span data-stu-id="5084c-114">Attribute</span></span>|<span data-ttu-id="5084c-115">설명</span><span class="sxs-lookup"><span data-stu-id="5084c-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5084c-116">xmlElement</span><span class="sxs-lookup"><span data-stu-id="5084c-116">xmlElement</span></span>|<span data-ttu-id="5084c-117">토큰을 요청할 때 메시지 본문에서 보안 토큰 서비스로 보낼 XML 요소를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5084c-117">A string specifying an XML element that is sent in the message body to the Security Token Service when requesting a token.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5084c-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="5084c-118">Child Elements</span></span>  
 <span data-ttu-id="5084c-119">없음</span><span class="sxs-lookup"><span data-stu-id="5084c-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5084c-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="5084c-120">Parent Elements</span></span>  
  
|<span data-ttu-id="5084c-121">요소</span><span class="sxs-lookup"><span data-stu-id="5084c-121">Element</span></span>|<span data-ttu-id="5084c-122">설명</span><span class="sxs-lookup"><span data-stu-id="5084c-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5084c-123">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="5084c-123">\<tokenRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/tokenrequestparameters.md)|<span data-ttu-id="5084c-124">토큰 요청 매개 변수 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="5084c-124">A collection of token request parameters.</span></span> <span data-ttu-id="5084c-125">각 매개 변수는 XML 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="5084c-125">Each parameter is an XML element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5084c-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="5084c-126">See also</span></span>
- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.TokenRequestParameters%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.TokenRequestParameters%2A>
- [<span data-ttu-id="5084c-127">서비스 ID 및 인증</span><span class="sxs-lookup"><span data-stu-id="5084c-127">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="5084c-128">페더레이션 및 발급된 토큰</span><span class="sxs-lookup"><span data-stu-id="5084c-128">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="5084c-129">사용자 지정 바인딩을 사용하는 보안 기능</span><span class="sxs-lookup"><span data-stu-id="5084c-129">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="5084c-130">페더레이션 및 발급된 토큰</span><span class="sxs-lookup"><span data-stu-id="5084c-130">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="5084c-131">바인딩</span><span class="sxs-lookup"><span data-stu-id="5084c-131">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
