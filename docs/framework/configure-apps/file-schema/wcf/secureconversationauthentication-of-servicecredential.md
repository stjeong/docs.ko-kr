---
title: '&lt;serviceCredential&gt;의 &lt;secureConversationAuthentication&gt;'
ms.date: 03/30/2017
ms.assetid: 0bd3fac7-befd-4a45-ba51-c200b33be0fd
ms.openlocfilehash: 8433ac8f698f3e5569802a8d76f7dedaf22f53c3
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180379"
---
# <a name="ltsecureconversationauthenticationgt-of-ltservicecredentialgt"></a><span data-ttu-id="35ef3-102">&lt;serviceCredential&gt;의 &lt;secureConversationAuthentication&gt;</span><span class="sxs-lookup"><span data-stu-id="35ef3-102">&lt;secureConversationAuthentication&gt; of &lt;serviceCredential&gt;</span></span>
<span data-ttu-id="35ef3-103">보안 대화 서비스 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35ef3-103">Specifies the settings for a secure conversation service.</span></span>  
  
 <span data-ttu-id="35ef3-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="35ef3-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="35ef3-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="35ef3-105">\<behaviors></span></span>  
<span data-ttu-id="35ef3-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="35ef3-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="35ef3-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="35ef3-107">\<behavior></span></span>  
<span data-ttu-id="35ef3-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="35ef3-108">\<serviceCredentials></span></span>  
<span data-ttu-id="35ef3-109">\<secureConversationAuthentication ></span><span class="sxs-lookup"><span data-stu-id="35ef3-109">\<secureConversationAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35ef3-110">구문</span><span class="sxs-lookup"><span data-stu-id="35ef3-110">Syntax</span></span>  
  
```xml  
<secureConversationAuthentication securityStateEncoderType="String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="35ef3-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="35ef3-111">Attributes and Elements</span></span>  
 <span data-ttu-id="35ef3-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="35ef3-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="35ef3-113">특성</span><span class="sxs-lookup"><span data-stu-id="35ef3-113">Attributes</span></span>  
  
|<span data-ttu-id="35ef3-114">특성</span><span class="sxs-lookup"><span data-stu-id="35ef3-114">Attribute</span></span>|<span data-ttu-id="35ef3-115">설명</span><span class="sxs-lookup"><span data-stu-id="35ef3-115">Description</span></span>|  
|---------------|-----------------|  
|`securityStateEncoderType`|<span data-ttu-id="35ef3-116">사용할 <xref:System.ServiceModel.Security.SecurityStateEncoder> 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="35ef3-116">A string that specifies the type of <xref:System.ServiceModel.Security.SecurityStateEncoder> to be used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="35ef3-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="35ef3-117">Child Elements</span></span>  
 <span data-ttu-id="35ef3-118">없음</span><span class="sxs-lookup"><span data-stu-id="35ef3-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="35ef3-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="35ef3-119">Parent Elements</span></span>  
  
|<span data-ttu-id="35ef3-120">요소</span><span class="sxs-lookup"><span data-stu-id="35ef3-120">Element</span></span>|<span data-ttu-id="35ef3-121">설명</span><span class="sxs-lookup"><span data-stu-id="35ef3-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="35ef3-122">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="35ef3-122">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="35ef3-123">서비스를 인증하는 데 사용되는 자격 증명 및 클라이언트 자격 증명 유효성 검사 관련 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="35ef3-123">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="35ef3-124">설명</span><span class="sxs-lookup"><span data-stu-id="35ef3-124">Remarks</span></span>  
 <span data-ttu-id="35ef3-125">SCT(보안 컨텍스트 토큰) 쿠키 serialization을 위한 알려진 클레임 형식 목록과 쿠키 정보를 인코딩 및 보안할 인코더를 지정하려면 이 구성 요소를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="35ef3-125">Use this configuration element to specify a list of known claim types for the Security Context Token (SCT) cookies serialization, as well as an encoder to encode and secure cookies information.</span></span> <span data-ttu-id="35ef3-126">SCT에 대한 자세한 내용은 <xref:System.ServiceModel.Security.SecureConversationServiceCredential>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35ef3-126">For more information on SCT, see <xref:System.ServiceModel.Security.SecureConversationServiceCredential>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35ef3-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="35ef3-127">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>  
 <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.SecureConversationAuthentication%2A>  
 <xref:System.ServiceModel.Description.ServiceCredentials.SecureConversationAuthentication%2A>  
 <xref:System.ServiceModel.Security.SecureConversationServiceCredential>
