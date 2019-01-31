---
title: <nameClaimType>
ms.date: 03/30/2017
ms.assetid: 17514d95-f0f5-4789-8e28-346640dc227c
author: BrucePerlerMS
ms.openlocfilehash: aab76949d9c31ac003b8afd519c2ad66529cbf26
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254863"
---
# <a name="nameclaimtype"></a><span data-ttu-id="ab595-101">\<nameClaimType></span><span class="sxs-lookup"><span data-stu-id="ab595-101">\<nameClaimType></span></span>
<span data-ttu-id="ab595-102">지정 하는 클레임 형식을 가져오거나 설정 합니다 <xref:System.Security.Principal.IIdentity.Name%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="ab595-102">Sets the claim type that specifies the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="ab595-103">클레임 형식에 대 한 검색 되는 <xref:System.Security.Claims.Claim> 의 컬렉션에 있는 <xref:System.Security.Claims.ClaimsIdentity> 반환한 개체는 <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> 이 토큰 처리기의 메서드.</span><span class="sxs-lookup"><span data-stu-id="ab595-103">The claim type is used to search for a <xref:System.Security.Claims.Claim> in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of this token handler.</span></span> <span data-ttu-id="ab595-104">일치 하는 클레임의 값이 이름으로 설정 됩니다는 <xref:System.Security.Principal.IIdentity> 이 토큰 처리기를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab595-104">The value of the matching claim is then set as the name of the <xref:System.Security.Principal.IIdentity> generated from this token handler.</span></span>  
  
 <span data-ttu-id="ab595-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="ab595-105">\<system.identityModel></span></span>  
<span data-ttu-id="ab595-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="ab595-106">\<identityConfiguration></span></span>  
<span data-ttu-id="ab595-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="ab595-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="ab595-108">\<add></span><span class="sxs-lookup"><span data-stu-id="ab595-108">\<add></span></span>  
<span data-ttu-id="ab595-109">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="ab595-109">\<samlSecurityTokenRequirement></span></span>  
<span data-ttu-id="ab595-110">\<nameClaimType></span><span class="sxs-lookup"><span data-stu-id="ab595-110">\<nameClaimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab595-111">구문</span><span class="sxs-lookup"><span data-stu-id="ab595-111">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ab595-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ab595-112">Attributes and Elements</span></span>  
 <span data-ttu-id="ab595-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ab595-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ab595-114">특성</span><span class="sxs-lookup"><span data-stu-id="ab595-114">Attributes</span></span>  
  
|<span data-ttu-id="ab595-115">특성</span><span class="sxs-lookup"><span data-stu-id="ab595-115">Attribute</span></span>|<span data-ttu-id="ab595-116">설명</span><span class="sxs-lookup"><span data-stu-id="ab595-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ab595-117">값</span><span class="sxs-lookup"><span data-stu-id="ab595-117">value</span></span>|<span data-ttu-id="ab595-118">에 사용할 클레임의 클레임 형식을 나타내는 URI를 지정 하는 문자열을 <xref:System.Security.Principal.IIdentity.Name%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="ab595-118">A string that specifies the URI that represents the claim type of the claim to use for the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span> <span data-ttu-id="ab595-119">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="ab595-119">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ab595-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ab595-120">Child Elements</span></span>  
 <span data-ttu-id="ab595-121">없음</span><span class="sxs-lookup"><span data-stu-id="ab595-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ab595-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ab595-122">Parent Elements</span></span>  
  
|<span data-ttu-id="ab595-123">요소</span><span class="sxs-lookup"><span data-stu-id="ab595-123">Element</span></span>|<span data-ttu-id="ab595-124">설명</span><span class="sxs-lookup"><span data-stu-id="ab595-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ab595-125">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="ab595-125">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="ab595-126">에 대 한 구성을 제공 합니다 <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> 클래스는 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 클래스나 파생된 클래스의 이러한 클래스 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ab595-126">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ab595-127">설명</span><span class="sxs-lookup"><span data-stu-id="ab595-127">Remarks</span></span>  
 <span data-ttu-id="ab595-128">`<nameClaimType>` 요소 집합을 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> 속성 때를 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> 개체는 구성에서 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab595-128">The `<nameClaimType>` element sets the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A> property when a <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ab595-129">예제</span><span class="sxs-lookup"><span data-stu-id="ab595-129">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement>  
        <nameClaimType value="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" />  
    </samlSecurityTokenRequirement>  
</add>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ab595-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="ab595-130">See also</span></span>
- <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement.NameClaimType%2A>
