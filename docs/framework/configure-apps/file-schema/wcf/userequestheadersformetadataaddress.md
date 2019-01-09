---
title: '&lt;useRequestHeadersForMetadataAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: bcbf1c633e0796c6056759dfbb55014838e0e293
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151412"
---
# <a name="ltuserequestheadersformetadataaddressgt"></a><span data-ttu-id="83682-102">&lt;useRequestHeadersForMetadataAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="83682-102">&lt;useRequestHeadersForMetadataAddress&gt;</span></span>
<span data-ttu-id="83682-103">요청 메시지 헤더에서 메타데이터 주소 정보를 검색할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="83682-103">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="83682-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="83682-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="83682-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="83682-105">\<behaviors></span></span>  
<span data-ttu-id="83682-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="83682-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="83682-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="83682-107">\<behavior></span></span>  
<span data-ttu-id="83682-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="83682-108">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83682-109">구문</span><span class="sxs-lookup"><span data-stu-id="83682-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="83682-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="83682-110">Attributes and Elements</span></span>  
 <span data-ttu-id="83682-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="83682-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="83682-112">특성</span><span class="sxs-lookup"><span data-stu-id="83682-112">Attributes</span></span>  
 <span data-ttu-id="83682-113">없음</span><span class="sxs-lookup"><span data-stu-id="83682-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="83682-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="83682-114">Child Elements</span></span>  
  
|<span data-ttu-id="83682-115">요소</span><span class="sxs-lookup"><span data-stu-id="83682-115">Element</span></span>|<span data-ttu-id="83682-116">설명</span><span class="sxs-lookup"><span data-stu-id="83682-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="83682-117">\<a d d ></span><span class="sxs-lookup"><span data-stu-id="83682-117">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="83682-118">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="83682-118">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="83682-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="83682-119">Parent Elements</span></span>  
  
|<span data-ttu-id="83682-120">요소</span><span class="sxs-lookup"><span data-stu-id="83682-120">Element</span></span>|<span data-ttu-id="83682-121">설명</span><span class="sxs-lookup"><span data-stu-id="83682-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="83682-122">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="83682-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="83682-123">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83682-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="83682-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="83682-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
