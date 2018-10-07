---
title: '&lt;nameClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: 17514d95-f0f5-4789-8e28-346640dc227c
author: BrucePerlerMS
ms.openlocfilehash: bd4033b2edea7450b66c25f446669b3ded65e9af
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/07/2018
ms.locfileid: "48847362"
---
# <a name="ltnameclaimtypegt"></a><span data-ttu-id="c882a-102">&lt;nameClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="c882a-102">&lt;nameClaimType&gt;</span></span>
<span data-ttu-id="c882a-103">지정 하는 클레임 형식을 가져오거나 설정 합니다 <xref:System.Security.Principal.IIdentity.Name%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c882a-103">Sets the claim type that specifies the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="c882a-104">클레임 형식에 대 한 검색 되는 <xref:System.Security.Claims.Claim> 의 컬렉션에 있는 <xref:System.Security.Claims.ClaimsIdentity> 반환한 개체는 <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> 이 토큰 처리기의 메서드.</span><span class="sxs-lookup"><span data-stu-id="c882a-104">The claim type is used to search for a <xref:System.Security.Claims.Claim> in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of this token handler.</span></span> <span data-ttu-id="c882a-105">일치 하는 클레임의 값이 이름으로 설정 됩니다는 <xref:System.Security.Principal.IIdentity> 이 토큰 처리기를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c882a-105">The value of the matching claim is then set as the name of the <xref:System.Security.Principal.IIdentity> generated from this token handler.</span></span>  
  
 <span data-ttu-id="c882a-106">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="c882a-106">\<system.identityModel></span></span>  
<span data-ttu-id="c882a-107">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="c882a-107">\<identityConfiguration></span></span>  
<span data-ttu-id="c882a-108">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="c882a-108">\<securityTokenHandlers></span></span>  
<span data-ttu-id="c882a-109">\<add></span><span class="sxs-lookup"><span data-stu-id="c882a-109">\<add></span></span>  
<span data-ttu-id="c882a-110">\<samlSecurityTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="c882a-110">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="c882a-111">\<nameClaimType ></span><span class="sxs-lookup"><span data-stu-id="c882a-111">\<nameClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c882a-112">구문</span><span class="sxs-lookup"><span data-stu-id="c882a-112">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement>  
          <nameClaimType value=xs:string>  
          </nameClaimType>  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c882a-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="c882a-113">Attributes and Elements</span></span>  
 <span data-ttu-id="c882a-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c882a-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c882a-115">특성</span><span class="sxs-lookup"><span data-stu-id="c882a-115">Attributes</span></span>  
  
|<span data-ttu-id="c882a-116">특성</span><span class="sxs-lookup"><span data-stu-id="c882a-116">Attribute</span></span>|<span data-ttu-id="c882a-117">설명</span><span class="sxs-lookup"><span data-stu-id="c882a-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c882a-118">값</span><span class="sxs-lookup"><span data-stu-id="c882a-118">value</span></span>|<span data-ttu-id="c882a-119">에 사용할 클레임의 클레임 형식을 나타내는 URI를 지정 하는 문자열을 <xref:System.Security.Principal.IIdentity.Name%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c882a-119">A string that specifies the URI that represents the claim type of the claim to use for the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="c882a-120">필수.</span><span class="sxs-lookup"><span data-stu-id="c882a-120">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c882a-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="c882a-121">Child Elements</span></span>  
 <span data-ttu-id="c882a-122">없음</span><span class="sxs-lookup"><span data-stu-id="c882a-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c882a-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="c882a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="c882a-124">요소</span><span class="sxs-lookup"><span data-stu-id="c882a-124">Element</span></span>|<span data-ttu-id="c882a-125">설명</span><span class="sxs-lookup"><span data-stu-id="c882a-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c882a-126">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="c882a-126">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="c882a-127">에 대 한 구성을 제공 합니다 <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> 클래스는 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 클래스나 파생된 클래스의 이러한 클래스 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="c882a-127">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c882a-128">설명</span><span class="sxs-lookup"><span data-stu-id="c882a-128">Remarks</span></span>  
 <span data-ttu-id="c882a-129">`<nameClaimType>` 요소 집합을 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> 속성 때를 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> 개체는 구성에서 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c882a-129">The `<nameClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c882a-130">예제</span><span class="sxs-lookup"><span data-stu-id="c882a-130">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <nameClaimType value="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c882a-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c882a-131">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A>
