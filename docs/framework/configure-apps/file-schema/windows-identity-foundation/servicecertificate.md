---
title: '&lt;ServiceCertificate&gt;'
ms.date: 03/30/2017
ms.assetid: 42c7f291-2ec3-43c5-8872-35897ff3c660
author: BrucePerlerMS
ms.openlocfilehash: 008d2269a72759117658e27ec130cc8cf62cfdfa
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084308"
---
# <a name="ltservicecertificategt"></a><span data-ttu-id="b7569-102">&lt;ServiceCertificate&gt;</span><span class="sxs-lookup"><span data-stu-id="b7569-102">&lt;serviceCertificate&gt;</span></span>
<span data-ttu-id="b7569-103">암호화 및 토큰 암호 해독에 사용 되는 X.509 인증서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7569-103">Configures the X.509 certificate that is used to encrypt and decrypt tokens.</span></span>  
  
 <span data-ttu-id="b7569-104">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="b7569-104">\<system.identityModel.services></span></span>  
<span data-ttu-id="b7569-105">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="b7569-105">\<federationConfiguration></span></span>  
<span data-ttu-id="b7569-106">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="b7569-106">\<serviceCertificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7569-107">구문</span><span class="sxs-lookup"><span data-stu-id="b7569-107">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b7569-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="b7569-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b7569-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b7569-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b7569-110">특성</span><span class="sxs-lookup"><span data-stu-id="b7569-110">Attributes</span></span>  
 <span data-ttu-id="b7569-111">없음</span><span class="sxs-lookup"><span data-stu-id="b7569-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b7569-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="b7569-112">Child Elements</span></span>  
  
|<span data-ttu-id="b7569-113">요소</span><span class="sxs-lookup"><span data-stu-id="b7569-113">Element</span></span>|<span data-ttu-id="b7569-114">설명</span><span class="sxs-lookup"><span data-stu-id="b7569-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b7569-115">\<certificateReference ></span><span class="sxs-lookup"><span data-stu-id="b7569-115">\<certificateReference></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatereference.md)|<span data-ttu-id="b7569-116">찾기 및 인증서 저장소에서 X.509 인증서의 유효성을 검사 하는 데 사용 되는 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7569-116">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b7569-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="b7569-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b7569-118">요소</span><span class="sxs-lookup"><span data-stu-id="b7569-118">Element</span></span>|<span data-ttu-id="b7569-119">설명</span><span class="sxs-lookup"><span data-stu-id="b7569-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b7569-120">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="b7569-120">\<federationConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|<span data-ttu-id="b7569-121">구성 설정이 포함 된 <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) 및 <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span><span class="sxs-lookup"><span data-stu-id="b7569-121">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b7569-122">예제</span><span class="sxs-lookup"><span data-stu-id="b7569-122">Example</span></span>  
 <span data-ttu-id="b7569-123">다음 XML의 사용을 보여 줍니다.는 \<serviceCertificate > 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b7569-123">The following XML shows the use of the \<serviceCertificate> element.</span></span> <span data-ttu-id="b7569-124">XML에서 가져온 것은 `CustomToken` 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="b7569-124">The XML is taken from the `CustomToken` sample.</span></span>  
  
```xml  
<serviceCertificate>  
  <certificateReference x509FindType="FindBySubjectName" findValue="localhost" storeLocation="LocalMachine" storeName="My"/>  
</serviceCertificate>  
```
