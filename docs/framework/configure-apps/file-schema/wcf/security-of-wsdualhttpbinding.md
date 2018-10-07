---
title: '&lt;wsDualHttpBinding&gt;의 &lt;security&gt;'
ms.date: 03/30/2017
ms.assetid: 869c05e7-4ebe-467d-95ab-c8f8de4e6b9e
author: BrucePerlerMS
ms.openlocfilehash: 761eb9d111630d64d0fe4450c7a8950a8181366d
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48838290"
---
# <a name="ltsecuritygt-of-ltwsdualhttpbindinggt"></a><span data-ttu-id="965d7-102">&lt;wsDualHttpBinding&gt;의 &lt;security&gt;</span><span class="sxs-lookup"><span data-stu-id="965d7-102">&lt;security&gt; of &lt;wsDualHttpBinding&gt;</span></span>
<span data-ttu-id="965d7-103">보안 기능을 정의 합니다 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-103">Defines the security capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>  
  
 <span data-ttu-id="965d7-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="965d7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="965d7-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="965d7-105">\<bindings></span></span>  
<span data-ttu-id="965d7-106">\<wsDualHttpBinding></span><span class="sxs-lookup"><span data-stu-id="965d7-106">\<wsDualHttpBinding></span></span>  
<span data-ttu-id="965d7-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="965d7-107">\<binding></span></span>  
<span data-ttu-id="965d7-108">\<security></span><span class="sxs-lookup"><span data-stu-id="965d7-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="965d7-109">구문</span><span class="sxs-lookup"><span data-stu-id="965d7-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None">  
   <message  
      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
      clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"  
      negotiateServiceCredential="Boolean"/>  
</security>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="965d7-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="965d7-110">Attributes and Elements</span></span>  
 <span data-ttu-id="965d7-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="965d7-112">특성</span><span class="sxs-lookup"><span data-stu-id="965d7-112">Attributes</span></span>  
  
|<span data-ttu-id="965d7-113">특성</span><span class="sxs-lookup"><span data-stu-id="965d7-113">Attribute</span></span>|<span data-ttu-id="965d7-114">설명</span><span class="sxs-lookup"><span data-stu-id="965d7-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="965d7-115">모드</span><span class="sxs-lookup"><span data-stu-id="965d7-115">mode</span></span>|<span data-ttu-id="965d7-116">-선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-116">-   Optional.</span></span> <span data-ttu-id="965d7-117">적용되는 보안 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-117">Specifies the type of security that is applied.</span></span> <span data-ttu-id="965d7-118">기본값은 `Message`입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-118">The default value is `Message`.</span></span> <span data-ttu-id="965d7-119">이 특성은 <xref:System.ServiceModel.WSDualHttpSecurityMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-119">This attribute is of type <xref:System.ServiceModel.WSDualHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="965d7-120">Mode 특성</span><span class="sxs-lookup"><span data-stu-id="965d7-120">Mode Attribute</span></span>  
  
|<span data-ttu-id="965d7-121">값</span><span class="sxs-lookup"><span data-stu-id="965d7-121">Value</span></span>|<span data-ttu-id="965d7-122">설명</span><span class="sxs-lookup"><span data-stu-id="965d7-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="965d7-123">없음</span><span class="sxs-lookup"><span data-stu-id="965d7-123">None</span></span>|<span data-ttu-id="965d7-124">보안이 해제되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-124">Security is disabled.</span></span>|  
|<span data-ttu-id="965d7-125">메시지</span><span class="sxs-lookup"><span data-stu-id="965d7-125">Message</span></span>|<span data-ttu-id="965d7-126">SOAP 메시지 보안을 사용하여 보안이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-126">Security is provided using SOAP message security.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="965d7-127">자식 요소</span><span class="sxs-lookup"><span data-stu-id="965d7-127">Child Elements</span></span>  
  
|<span data-ttu-id="965d7-128">요소</span><span class="sxs-lookup"><span data-stu-id="965d7-128">Element</span></span>|<span data-ttu-id="965d7-129">설명</span><span class="sxs-lookup"><span data-stu-id="965d7-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="965d7-130">\<message></span><span class="sxs-lookup"><span data-stu-id="965d7-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-wsdualhttpbinding.md)|<span data-ttu-id="965d7-131">메시지 수준 보안 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-131">Defines the settings for the message-level security.</span></span> <span data-ttu-id="965d7-132">이 요소는 <xref:System.ServiceModel.MessageSecurityOverHttp> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-132">This element is of type <xref:System.ServiceModel.MessageSecurityOverHttp>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="965d7-133">부모 요소</span><span class="sxs-lookup"><span data-stu-id="965d7-133">Parent Elements</span></span>  
  
|<span data-ttu-id="965d7-134">요소</span><span class="sxs-lookup"><span data-stu-id="965d7-134">Element</span></span>|<span data-ttu-id="965d7-135">설명</span><span class="sxs-lookup"><span data-stu-id="965d7-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="965d7-136">\<binding></span><span class="sxs-lookup"><span data-stu-id="965d7-136">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="965d7-137">모든 바인딩 기능을 정의 합니다 [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-137">Defines all binding capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="965d7-138">설명</span><span class="sxs-lookup"><span data-stu-id="965d7-138">Remarks</span></span>  
 <span data-ttu-id="965d7-139">이중 바인딩은 클라이언트의 IP 주소를 서비스에 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-139">A dual binding exposes the IP address of the client to the service.</span></span> <span data-ttu-id="965d7-140">클라이언트는 보안을 사용하여 신뢰하는 서비스에만 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-140">The client should use security to ensure that it only connects to services it trusts.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="965d7-141">참고 항목</span><span class="sxs-lookup"><span data-stu-id="965d7-141">See Also</span></span>  
 <xref:System.ServiceModel.WSDualHttpSecurity>  
 <xref:System.ServiceModel.BasicHttpSecurity>  
 [<span data-ttu-id="965d7-142">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="965d7-142">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="965d7-143">바인딩</span><span class="sxs-lookup"><span data-stu-id="965d7-143">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="965d7-144">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="965d7-144">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="965d7-145">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="965d7-145">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="965d7-146">\<binding></span><span class="sxs-lookup"><span data-stu-id="965d7-146">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
