---
title: '&lt;defaultPorts&gt;'
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 7ddfddaa13778ce98bd93b6d8029438377fc7e94
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145187"
---
# <a name="ltdefaultportsgt"></a><span data-ttu-id="2f1c4-102">&lt;defaultPorts&gt;</span><span class="sxs-lookup"><span data-stu-id="2f1c4-102">&lt;defaultPorts&gt;</span></span>
<span data-ttu-id="2f1c4-103">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1c4-103">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="2f1c4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2f1c4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2f1c4-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="2f1c4-105">\<behaviors></span></span>  
<span data-ttu-id="2f1c4-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="2f1c4-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="2f1c4-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="2f1c4-107">\<behavior></span></span>  
<span data-ttu-id="2f1c4-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="2f1c4-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="2f1c4-109">\<a d d ></span><span class="sxs-lookup"><span data-stu-id="2f1c4-109">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f1c4-110">구문</span><span class="sxs-lookup"><span data-stu-id="2f1c4-110">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2f1c4-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="2f1c4-111">Attributes and Elements</span></span>  
 <span data-ttu-id="2f1c4-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2f1c4-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2f1c4-113">특성</span><span class="sxs-lookup"><span data-stu-id="2f1c4-113">Attributes</span></span>  
 <span data-ttu-id="2f1c4-114">없음</span><span class="sxs-lookup"><span data-stu-id="2f1c4-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2f1c4-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="2f1c4-115">Child Elements</span></span>  
  
|<span data-ttu-id="2f1c4-116">요소</span><span class="sxs-lookup"><span data-stu-id="2f1c4-116">Element</span></span>|<span data-ttu-id="2f1c4-117">설명</span><span class="sxs-lookup"><span data-stu-id="2f1c4-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2f1c4-118">\<추가 >의 \<a d d ></span><span class="sxs-lookup"><span data-stu-id="2f1c4-118">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="2f1c4-119">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1c4-119">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2f1c4-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="2f1c4-120">Parent Elements</span></span>  
  
|<span data-ttu-id="2f1c4-121">요소</span><span class="sxs-lookup"><span data-stu-id="2f1c4-121">Element</span></span>|<span data-ttu-id="2f1c4-122">설명</span><span class="sxs-lookup"><span data-stu-id="2f1c4-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2f1c4-123">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="2f1c4-123">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="2f1c4-124">기본 포트의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1c4-124">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2f1c4-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2f1c4-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
