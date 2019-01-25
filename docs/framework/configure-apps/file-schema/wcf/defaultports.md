---
title: '&lt;defaultPorts&gt;'
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 2c742f98315c0e497ac4117953424bae913cb5b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614499"
---
# <a name="ltdefaultportsgt"></a><span data-ttu-id="f80cd-102">&lt;defaultPorts&gt;</span><span class="sxs-lookup"><span data-stu-id="f80cd-102">&lt;defaultPorts&gt;</span></span>
<span data-ttu-id="f80cd-103">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="f80cd-103">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="f80cd-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f80cd-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f80cd-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="f80cd-105">\<behaviors></span></span>  
<span data-ttu-id="f80cd-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="f80cd-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="f80cd-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="f80cd-107">\<behavior></span></span>  
<span data-ttu-id="f80cd-108">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="f80cd-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="f80cd-109">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="f80cd-109">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f80cd-110">구문</span><span class="sxs-lookup"><span data-stu-id="f80cd-110">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f80cd-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="f80cd-111">Attributes and Elements</span></span>  
 <span data-ttu-id="f80cd-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f80cd-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f80cd-113">특성</span><span class="sxs-lookup"><span data-stu-id="f80cd-113">Attributes</span></span>  
 <span data-ttu-id="f80cd-114">없음</span><span class="sxs-lookup"><span data-stu-id="f80cd-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="f80cd-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="f80cd-115">Child Elements</span></span>  
  
|<span data-ttu-id="f80cd-116">요소</span><span class="sxs-lookup"><span data-stu-id="f80cd-116">Element</span></span>|<span data-ttu-id="f80cd-117">설명</span><span class="sxs-lookup"><span data-stu-id="f80cd-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f80cd-118">\<추가 >의 \<a d d ></span><span class="sxs-lookup"><span data-stu-id="f80cd-118">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="f80cd-119">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="f80cd-119">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f80cd-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="f80cd-120">Parent Elements</span></span>  
  
|<span data-ttu-id="f80cd-121">요소</span><span class="sxs-lookup"><span data-stu-id="f80cd-121">Element</span></span>|<span data-ttu-id="f80cd-122">설명</span><span class="sxs-lookup"><span data-stu-id="f80cd-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f80cd-123">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="f80cd-123">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="f80cd-124">기본 포트의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f80cd-124">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f80cd-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="f80cd-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
