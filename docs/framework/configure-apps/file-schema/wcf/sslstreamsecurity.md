---
title: '&lt;sslStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
author: BrucePerlerMS
ms.openlocfilehash: 6eacf1833ecf980696d75c5dbcaaba3ba6403d92
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47196332"
---
# <a name="ltsslstreamsecuritygt"></a><span data-ttu-id="60699-102">&lt;sslStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="60699-102">&lt;sslStreamSecurity&gt;</span></span>
<span data-ttu-id="60699-103">SSL 스트림을 사용한 채널 보안을 지원하는 사용자 지정 바인딩 요소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60699-103">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="60699-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="60699-104">\<system.serviceModel></span></span>  
<span data-ttu-id="60699-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="60699-105">\<bindings></span></span>  
<span data-ttu-id="60699-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="60699-106">\<customBinding></span></span>  
<span data-ttu-id="60699-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="60699-107">\<binding></span></span>  
<span data-ttu-id="60699-108">\<sslStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="60699-108">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60699-109">구문</span><span class="sxs-lookup"><span data-stu-id="60699-109">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"      sslProtocols="Ssl3|Tls|Tls11|Tls12" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="60699-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="60699-110">Attributes and Elements</span></span>  
 <span data-ttu-id="60699-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="60699-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="60699-112">특성</span><span class="sxs-lookup"><span data-stu-id="60699-112">Attributes</span></span>  
  
|<span data-ttu-id="60699-113">특성</span><span class="sxs-lookup"><span data-stu-id="60699-113">Attribute</span></span>|<span data-ttu-id="60699-114">설명</span><span class="sxs-lookup"><span data-stu-id="60699-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="60699-115">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="60699-115">requireClientCertificate</span></span>|<span data-ttu-id="60699-116">이 바인딩에 클라이언트 인증서가 필요한지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="60699-116">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="60699-117">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="60699-117">The default is `false`.</span></span>|  
|<span data-ttu-id="60699-118">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="60699-118">sslProtocols</span></span>|<span data-ttu-id="60699-119">지원되는 SslProtocols를 지정하는 SslProtocols 열거형 플래그 값입니다.</span><span class="sxs-lookup"><span data-stu-id="60699-119">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="60699-120">기본값은 Ssl3&#124;Tls&#124;Tls11&#124;Tls12 합니다.</span><span class="sxs-lookup"><span data-stu-id="60699-120">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="60699-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="60699-121">Child Elements</span></span>  
 <span data-ttu-id="60699-122">없음</span><span class="sxs-lookup"><span data-stu-id="60699-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="60699-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="60699-123">Parent Elements</span></span>  
  
|<span data-ttu-id="60699-124">요소</span><span class="sxs-lookup"><span data-stu-id="60699-124">Element</span></span>|<span data-ttu-id="60699-125">설명</span><span class="sxs-lookup"><span data-stu-id="60699-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="60699-126">\<binding></span><span class="sxs-lookup"><span data-stu-id="60699-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="60699-127">사용자 지정 바인딩의 모든 바인딩 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="60699-127">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="60699-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="60699-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>  
 [<span data-ttu-id="60699-129">바인딩</span><span class="sxs-lookup"><span data-stu-id="60699-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="60699-130">바인딩 확장</span><span class="sxs-lookup"><span data-stu-id="60699-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="60699-131">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="60699-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="60699-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="60699-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
