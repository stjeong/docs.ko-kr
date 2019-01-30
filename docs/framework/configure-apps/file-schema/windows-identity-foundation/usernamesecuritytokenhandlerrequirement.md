---
title: <userNameSecurityTokenHandlerRequirement>
ms.date: 03/30/2017
ms.assetid: 6ec3bac1-b014-49ae-843c-c54518cb709a
author: BrucePerlerMS
ms.openlocfilehash: 18769794da8528f085c567264827db5aa6b214f1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271891"
---
# <a name="usernamesecuritytokenhandlerrequirement"></a><span data-ttu-id="2d5f2-101">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="2d5f2-101">\<userNameSecurityTokenHandlerRequirement></span></span>
<span data-ttu-id="2d5f2-102">에 대 한 구성을 제공 합니다 <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> 클래스나 파생된 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="2d5f2-102">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="2d5f2-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="2d5f2-103">\<system.identityModel></span></span>  
<span data-ttu-id="2d5f2-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="2d5f2-104">\<identityConfiguration></span></span>  
<span data-ttu-id="2d5f2-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="2d5f2-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="2d5f2-106">\<add></span><span class="sxs-lookup"><span data-stu-id="2d5f2-106">\<add></span></span>  
<span data-ttu-id="2d5f2-107">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="2d5f2-107">\<userNameSecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d5f2-108">구문</span><span class="sxs-lookup"><span data-stu-id="2d5f2-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
        <userNameSecurityTokenHandlerRequirement membershipProviderName=xs:string >  
        </userNameSecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2d5f2-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="2d5f2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="2d5f2-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2d5f2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2d5f2-111">특성</span><span class="sxs-lookup"><span data-stu-id="2d5f2-111">Attributes</span></span>  
  
|<span data-ttu-id="2d5f2-112">특성</span><span class="sxs-lookup"><span data-stu-id="2d5f2-112">Attribute</span></span>|<span data-ttu-id="2d5f2-113">설명</span><span class="sxs-lookup"><span data-stu-id="2d5f2-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2d5f2-114">membershipProviderName</span><span class="sxs-lookup"><span data-stu-id="2d5f2-114">membershipProviderName</span></span>|<span data-ttu-id="2d5f2-115">지정 된 <xref:System.Web.Security.MembershipProvider> 는 보안 토큰 처리기를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d5f2-115">Specifies the <xref:System.Web.Security.MembershipProvider> that should be used by the security token handler.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2d5f2-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="2d5f2-116">Child Elements</span></span>  
 <span data-ttu-id="2d5f2-117">없음</span><span class="sxs-lookup"><span data-stu-id="2d5f2-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2d5f2-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="2d5f2-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2d5f2-119">요소</span><span class="sxs-lookup"><span data-stu-id="2d5f2-119">Element</span></span>|<span data-ttu-id="2d5f2-120">설명</span><span class="sxs-lookup"><span data-stu-id="2d5f2-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2d5f2-121">\<add></span><span class="sxs-lookup"><span data-stu-id="2d5f2-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="2d5f2-122">토큰 처리기 컬렉션에 지정 된 보안 토큰 처리기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2d5f2-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2d5f2-123">설명</span><span class="sxs-lookup"><span data-stu-id="2d5f2-123">Remarks</span></span>  
 <span data-ttu-id="2d5f2-124">`<userNameSecurityTokenHandlerRequirement>` 요소 집합을 <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> 속성 때를 <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> 개체는 구성에서 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d5f2-124">The `<userNameSecurityTokenHandlerRequirement>` element sets the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler.MembershipProvider%2A> property when a <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> object is initialized from configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2d5f2-125">예제</span><span class="sxs-lookup"><span data-stu-id="2d5f2-125">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler, System.IdentityModel.Services">  
    <userNameSecurityTokenHandlerRequirement membershipProviderName="AspNetSqlProvider/>  
</add>  
```
