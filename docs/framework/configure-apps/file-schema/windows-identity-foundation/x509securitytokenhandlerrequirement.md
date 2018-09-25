---
title: '&lt;x509SecurityTokenHandlerRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: aca22c2c-5ae7-42af-9bbd-15c2524692ce
author: BrucePerlerMS
ms.openlocfilehash: 994677904cada71dbc7cce4b6ca0de1d4dc65014
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47085665"
---
# <a name="ltx509securitytokenhandlerrequirementgt"></a><span data-ttu-id="34f2d-102">&lt;x509SecurityTokenHandlerRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="34f2d-102">&lt;x509SecurityTokenHandlerRequirement&gt;</span></span>
<span data-ttu-id="34f2d-103">에 대 한 선택적 구성을 제공 합니다 <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> 클래스나 파생된 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-103">Provides optional configuration for the <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="34f2d-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="34f2d-104">\<system.identityModel></span></span>  
<span data-ttu-id="34f2d-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="34f2d-105">\<identityConfiguration></span></span>  
<span data-ttu-id="34f2d-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="34f2d-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="34f2d-107">\<add></span><span class="sxs-lookup"><span data-stu-id="34f2d-107">\<add></span></span>  
<span data-ttu-id="34f2d-108">\<x509SecurityTokenHandlerRequirement ></span><span class="sxs-lookup"><span data-stu-id="34f2d-108">\<x509SecurityTokenHandlerRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34f2d-109">구문</span><span class="sxs-lookup"><span data-stu-id="34f2d-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
        <x509SecurityTokenHandlerRequirement>  
          mapToWindows=xs:boolean  
          certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
          certificateValidator="Namespace.Class, Assembly"  
          revocationMode="NoCheck||Offline||Online"  
          trustedStoreLocation="CurrentUser||LocalMachine"  
        </x509SecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="34f2d-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="34f2d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="34f2d-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="34f2d-112">특성</span><span class="sxs-lookup"><span data-stu-id="34f2d-112">Attributes</span></span>  
  
|<span data-ttu-id="34f2d-113">특성</span><span class="sxs-lookup"><span data-stu-id="34f2d-113">Attribute</span></span>|<span data-ttu-id="34f2d-114">설명</span><span class="sxs-lookup"><span data-stu-id="34f2d-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="34f2d-115">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="34f2d-115">certificateValidationMode</span></span>|<span data-ttu-id="34f2d-116"><xref:System.ServiceModel.Security.X509CertificateValidationMode> 사용할 X.509 인증서의 유효성 검사 모드를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-116">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="34f2d-117">기본값은 "PeerOrChainTrust"입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-117">The default value is "PeerOrChainTrust".</span></span>|  
|<span data-ttu-id="34f2d-118">mapToWindows</span><span class="sxs-lookup"><span data-stu-id="34f2d-118">mapToWindows</span></span>|<span data-ttu-id="34f2d-119">여부를 토큰 처리기를 매핑해야 유효성 검사 토큰이 Windows 계정에 들어오는 UPN 클레임을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-119">Specifies whether the token handler should map the validating token to a Windows account by using the incoming UPN claim.</span></span> <span data-ttu-id="34f2d-120">기본값은 "false"입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-120">The default is "false".</span></span>|  
|<span data-ttu-id="34f2d-121">revocationMode</span><span class="sxs-lookup"><span data-stu-id="34f2d-121">revocationMode</span></span>|<span data-ttu-id="34f2d-122"><xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 사용할 X.509 인증서의 해지 모드를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-122">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="34f2d-123">기본값은 "Online"입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-123">The default value is "Online".</span></span>|  
|<span data-ttu-id="34f2d-124">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="34f2d-124">trustedStoreLocation</span></span>|<span data-ttu-id="34f2d-125"><xref:System.Security.Cryptography.X509Certificates.StoreLocation> X.509 인증서 저장소를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-125">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="34f2d-126">기본값은 "LocalMachine"입니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-126">The default value is "LocalMachine".</span></span>|  
|<span data-ttu-id="34f2d-127">certificateValidator</span><span class="sxs-lookup"><span data-stu-id="34f2d-127">certificateValidator</span></span>|<span data-ttu-id="34f2d-128">파생 되는 사용자 지정 형식을 <xref:System.IdentityModel.Selectors.X509CertificateValidator>합니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-128">A custom type that derives from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="34f2d-129">경우는 `certificateValidationMode` 특성은 "Custom"을이 형식의 인스턴스는 발급자 인증서 유효성 검사에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-129">If the `certificateValidationMode` attribute is "Custom", an instance of this type is used for issuer certificate validation.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="34f2d-130">자식 요소</span><span class="sxs-lookup"><span data-stu-id="34f2d-130">Child Elements</span></span>  
 <span data-ttu-id="34f2d-131">없음</span><span class="sxs-lookup"><span data-stu-id="34f2d-131">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="34f2d-132">부모 요소</span><span class="sxs-lookup"><span data-stu-id="34f2d-132">Parent Elements</span></span>  
  
|<span data-ttu-id="34f2d-133">요소</span><span class="sxs-lookup"><span data-stu-id="34f2d-133">Element</span></span>|<span data-ttu-id="34f2d-134">설명</span><span class="sxs-lookup"><span data-stu-id="34f2d-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="34f2d-135">\<add></span><span class="sxs-lookup"><span data-stu-id="34f2d-135">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="34f2d-136">토큰 처리기 컬렉션에 지정 된 보안 토큰 처리기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="34f2d-136">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="34f2d-137">예제</span><span class="sxs-lookup"><span data-stu-id="34f2d-137">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
    <x509SecurityTokenHandlerRequirement mapToWindows="true"   
                                         certificateValidationMode="PeerOrChainTrust"   
                                         revocationMode="Online"   
                                         trustedStoreLocation="LocalMachine" />  
</add>  
```
