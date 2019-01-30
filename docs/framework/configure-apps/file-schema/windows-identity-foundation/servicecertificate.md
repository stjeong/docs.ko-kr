---
title: <serviceCertificate>
ms.date: 03/30/2017
ms.assetid: 42c7f291-2ec3-43c5-8872-35897ff3c660
author: BrucePerlerMS
ms.openlocfilehash: 328d074f9edc5ddf871308a7e3d694bf94adea78
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261605"
---
# <a name="servicecertificate"></a><span data-ttu-id="57062-101">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="57062-101">\<serviceCertificate></span></span>
<span data-ttu-id="57062-102">암호화 및 토큰 암호 해독에 사용 되는 X.509 인증서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57062-102">Configures the X.509 certificate that is used to encrypt and decrypt tokens.</span></span>  
  
 <span data-ttu-id="57062-103">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="57062-103">\<system.identityModel.services></span></span>  
<span data-ttu-id="57062-104">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="57062-104">\<federationConfiguration></span></span>  
<span data-ttu-id="57062-105">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="57062-105">\<serviceCertificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57062-106">구문</span><span class="sxs-lookup"><span data-stu-id="57062-106">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="57062-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="57062-107">Attributes and Elements</span></span>  
 <span data-ttu-id="57062-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="57062-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="57062-109">특성</span><span class="sxs-lookup"><span data-stu-id="57062-109">Attributes</span></span>  
 <span data-ttu-id="57062-110">없음</span><span class="sxs-lookup"><span data-stu-id="57062-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="57062-111">자식 요소</span><span class="sxs-lookup"><span data-stu-id="57062-111">Child Elements</span></span>  
  
|<span data-ttu-id="57062-112">요소</span><span class="sxs-lookup"><span data-stu-id="57062-112">Element</span></span>|<span data-ttu-id="57062-113">설명</span><span class="sxs-lookup"><span data-stu-id="57062-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="57062-114">\<certificateReference></span><span class="sxs-lookup"><span data-stu-id="57062-114">\<certificateReference></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatereference.md)|<span data-ttu-id="57062-115">찾기 및 인증서 저장소에서 X.509 인증서의 유효성을 검사 하는 데 사용 되는 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57062-115">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="57062-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="57062-116">Parent Elements</span></span>  
  
|<span data-ttu-id="57062-117">요소</span><span class="sxs-lookup"><span data-stu-id="57062-117">Element</span></span>|<span data-ttu-id="57062-118">설명</span><span class="sxs-lookup"><span data-stu-id="57062-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="57062-119">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="57062-119">\<federationConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|<span data-ttu-id="57062-120">구성 설정이 포함 된 <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) 및 <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span><span class="sxs-lookup"><span data-stu-id="57062-120">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="57062-121">예제</span><span class="sxs-lookup"><span data-stu-id="57062-121">Example</span></span>  
 <span data-ttu-id="57062-122">다음 XML의 사용을 보여 줍니다.는 \<serviceCertificate > 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="57062-122">The following XML shows the use of the \<serviceCertificate> element.</span></span> <span data-ttu-id="57062-123">XML에서 가져온 것은 `CustomToken` 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="57062-123">The XML is taken from the `CustomToken` sample.</span></span>  
  
```xml  
<serviceCertificate>  
  <certificateReference x509FindType="FindBySubjectName" findValue="localhost" storeLocation="LocalMachine" storeName="My"/>  
</serviceCertificate>  
```
