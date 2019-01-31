---
title: <certificateValidation>
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
ms.openlocfilehash: 7b8823d792e3f15846a9483d670994be4b368980
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273899"
---
# <a name="certificatevalidation"></a><span data-ttu-id="5a548-101">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="5a548-101">\<certificateValidation></span></span>
<span data-ttu-id="5a548-102">토큰 처리기 인증서의 유효성을 검사 하는 데 사용 되는 설정을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-102">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="5a548-103">특정 처리기를 자체 유효성 검사기를 사용 하 여 구성 된 경우이 설정은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-103">These settings are overridden if a specific handler is configured with its own validator.</span></span>  
  
 <span data-ttu-id="5a548-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="5a548-104">\<system.identityModel></span></span>  
<span data-ttu-id="5a548-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="5a548-105">\<identityConfiguration></span></span>  
<span data-ttu-id="5a548-106">\<certificateValidation></span><span class="sxs-lookup"><span data-stu-id="5a548-106">\<certificateValidation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a548-107">구문</span><span class="sxs-lookup"><span data-stu-id="5a548-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation  
      certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
      revocationMode="NoCheck||Offline||Online"  
      trustedStoreLocation="CurrentLocation||LocalMachine" >  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5a548-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="5a548-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5a548-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5a548-110">특성</span><span class="sxs-lookup"><span data-stu-id="5a548-110">Attributes</span></span>  
  
|<span data-ttu-id="5a548-111">특성</span><span class="sxs-lookup"><span data-stu-id="5a548-111">Attribute</span></span>|<span data-ttu-id="5a548-112">설명</span><span class="sxs-lookup"><span data-stu-id="5a548-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5a548-113">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="5a548-113">certificateValidationMode</span></span>|<span data-ttu-id="5a548-114"><xref:System.ServiceModel.Security.X509CertificateValidationMode> 사용할 X.509 인증서의 유효성 검사 모드를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-114">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="5a548-115">기본값은 "PeerOrChainTrust"입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-115">The default value is "PeerOrChainTrust".</span></span> <span data-ttu-id="5a548-116">사용자 지정 유효성 검사기를 지정 하려면이 특성을 "Custom"으로 설정 하 고 사용 하 여 유효성 검사기를 지정 합니다 [ \<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-116">To specify a custom validator, set this attribute to "Custom" and specify the validator using the [\<certificateValidator>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) element.</span></span> <span data-ttu-id="5a548-117">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-117">Optional.</span></span>|  
|<span data-ttu-id="5a548-118">revocationMode</span><span class="sxs-lookup"><span data-stu-id="5a548-118">revocationMode</span></span>|<span data-ttu-id="5a548-119"><xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 사용할 X.509 인증서의 해지 모드를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-119">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="5a548-120">기본값은 "Online"입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-120">The default value is "Online".</span></span> <span data-ttu-id="5a548-121">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-121">Optional.</span></span>|  
|<span data-ttu-id="5a548-122">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="5a548-122">trustedStoreLocation</span></span>|<span data-ttu-id="5a548-123"><xref:System.Security.Cryptography.X509Certificates.StoreLocation> X.509 인증서 저장소를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-123">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="5a548-124">기본값은 "LocalMachine"입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-124">The default value is "LocalMachine".</span></span> <span data-ttu-id="5a548-125">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-125">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5a548-126">자식 요소</span><span class="sxs-lookup"><span data-stu-id="5a548-126">Child Elements</span></span>  
  
|<span data-ttu-id="5a548-127">요소</span><span class="sxs-lookup"><span data-stu-id="5a548-127">Element</span></span>|<span data-ttu-id="5a548-128">설명</span><span class="sxs-lookup"><span data-stu-id="5a548-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5a548-129">\<certificateValidator></span><span class="sxs-lookup"><span data-stu-id="5a548-129">\<certificateValidator></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md)|<span data-ttu-id="5a548-130">인증서 유효성 검사에 대 한 사용자 지정 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-130">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="5a548-131">이 이와 같은 경우에 사용 됩니다 합니다 `certificateValidationMode` 특성을 [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) 요소 "Custom"으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-131">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5a548-132">부모 요소</span><span class="sxs-lookup"><span data-stu-id="5a548-132">Parent Elements</span></span>  
  
|<span data-ttu-id="5a548-133">요소</span><span class="sxs-lookup"><span data-stu-id="5a548-133">Element</span></span>|<span data-ttu-id="5a548-134">설명</span><span class="sxs-lookup"><span data-stu-id="5a548-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5a548-135">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="5a548-135">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="5a548-136">서비스 수준 id 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-136">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="5a548-137">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="5a548-137">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="5a548-138">구성 컬렉션의 보안 토큰 처리기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-138">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5a548-139">설명</span><span class="sxs-lookup"><span data-stu-id="5a548-139">Remarks</span></span>  
 <span data-ttu-id="5a548-140">`<certificateValidation>` 요소 아래에 있는 서비스 수준에서 지정할 수 있습니다 합니다 `<identityConfiguration>` 요소 또는 보안 토큰 처리기 컬렉션 수준에서는 `<securityTokenHandlerConfiguration>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-140">A `<certificateValidation>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="5a548-141">서비스에 지정 된 토큰 처리기 컬렉션의 설정을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-141">Settings on a token handler collection override those specified on the service.</span></span> <span data-ttu-id="5a548-142">일부 토큰 처리기를 사용 하면 구성에서 인증서 유효성 검사 설정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-142">Some token handlers allow you to specify certificate validation settings in configuration.</span></span> <span data-ttu-id="5a548-143">서비스 수준 및 보안 토큰 처리기 컬렉션의 개별 토큰 처리기의 설정을 지정 된 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="5a548-143">Settings on individual token handlers override those specified both at the service level and on the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5a548-144">예제</span><span class="sxs-lookup"><span data-stu-id="5a548-144">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
