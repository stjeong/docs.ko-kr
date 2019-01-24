---
title: '&lt;useRequestHeadersForMetadataAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 679f0eae-f353-44d1-b42d-a9e247509774
ms.openlocfilehash: 6c03057fca23b037702c702b9a574045ebb302b4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656630"
---
# <a name="ltuserequestheadersformetadataaddressgt"></a><span data-ttu-id="ff2b8-102">&lt;useRequestHeadersForMetadataAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="ff2b8-102">&lt;useRequestHeadersForMetadataAddress&gt;</span></span>
<span data-ttu-id="ff2b8-103">요청 메시지 헤더에서 메타데이터 주소 정보를 검색할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b8-103">Enables the retrieval of metadata address information from the request message headers.</span></span>  
  
<span data-ttu-id="ff2b8-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ff2b8-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ff2b8-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="ff2b8-105">\<behaviors></span></span>  
<span data-ttu-id="ff2b8-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="ff2b8-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="ff2b8-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="ff2b8-107">\<behavior></span></span>  
<span data-ttu-id="ff2b8-108">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="ff2b8-108">\<useRequestHeadersForMetadataAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff2b8-109">구문</span><span class="sxs-lookup"><span data-stu-id="ff2b8-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ff2b8-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ff2b8-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ff2b8-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b8-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ff2b8-112">특성</span><span class="sxs-lookup"><span data-stu-id="ff2b8-112">Attributes</span></span>  
 <span data-ttu-id="ff2b8-113">없음</span><span class="sxs-lookup"><span data-stu-id="ff2b8-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ff2b8-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ff2b8-114">Child Elements</span></span>  
  
|<span data-ttu-id="ff2b8-115">요소</span><span class="sxs-lookup"><span data-stu-id="ff2b8-115">Element</span></span>|<span data-ttu-id="ff2b8-116">설명</span><span class="sxs-lookup"><span data-stu-id="ff2b8-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ff2b8-117">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="ff2b8-117">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="ff2b8-118">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b8-118">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ff2b8-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ff2b8-119">Parent Elements</span></span>  
  
|<span data-ttu-id="ff2b8-120">요소</span><span class="sxs-lookup"><span data-stu-id="ff2b8-120">Element</span></span>|<span data-ttu-id="ff2b8-121">설명</span><span class="sxs-lookup"><span data-stu-id="ff2b8-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ff2b8-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="ff2b8-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="ff2b8-123">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b8-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ff2b8-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="ff2b8-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.UseRequestHeadersForMetadataAddressElement>
