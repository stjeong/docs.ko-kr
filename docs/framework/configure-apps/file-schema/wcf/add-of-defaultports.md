---
title: '&lt;defaultPorts&gt;의 &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: f162ce42-963b-4779-96a7-d6d8b4ea0d2f
ms.openlocfilehash: 0932ef9afacb6278c4857dcfd6ba545595ff8f9d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147722"
---
# <a name="ltaddgt-of-ltdefaultportsgt"></a><span data-ttu-id="4201d-102">&lt;defaultPorts&gt;의 &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="4201d-102">&lt;add&gt; of &lt;defaultPorts&gt;</span></span>
<span data-ttu-id="4201d-103">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="4201d-103">A default communications endpoint that the client application listens to.</span></span>  
  
 <span data-ttu-id="4201d-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4201d-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4201d-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="4201d-105">\<behaviors></span></span>  
<span data-ttu-id="4201d-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="4201d-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="4201d-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="4201d-107">\<behavior></span></span>  
<span data-ttu-id="4201d-108">\<useRequestHeadersForMetadataAddress ></span><span class="sxs-lookup"><span data-stu-id="4201d-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="4201d-109">\<a d d ></span><span class="sxs-lookup"><span data-stu-id="4201d-109">\<defaultPorts></span></span>  
<span data-ttu-id="4201d-110">\<add></span><span class="sxs-lookup"><span data-stu-id="4201d-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4201d-111">구문</span><span class="sxs-lookup"><span data-stu-id="4201d-111">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add port="Integer"
         scheme="String" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4201d-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4201d-112">Attributes and Elements</span></span>  
 <span data-ttu-id="4201d-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4201d-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4201d-114">특성</span><span class="sxs-lookup"><span data-stu-id="4201d-114">Attributes</span></span>  
  
|<span data-ttu-id="4201d-115">특성</span><span class="sxs-lookup"><span data-stu-id="4201d-115">Attribute</span></span>|<span data-ttu-id="4201d-116">설명</span><span class="sxs-lookup"><span data-stu-id="4201d-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4201d-117">포트</span><span class="sxs-lookup"><span data-stu-id="4201d-117">port</span></span>|<span data-ttu-id="4201d-118">기본 통신 포트 번호를 지정하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="4201d-118">An integer that specifies the default communications port number</span></span>|  
|<span data-ttu-id="4201d-119">scheme</span><span class="sxs-lookup"><span data-stu-id="4201d-119">scheme</span></span>|<span data-ttu-id="4201d-120">통신 포트와 연결된 프로토콜 설정 그룹을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="4201d-120">A string that specifies the group of protocol settings associated with a communications port.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4201d-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4201d-121">Child Elements</span></span>  
 <span data-ttu-id="4201d-122">없음</span><span class="sxs-lookup"><span data-stu-id="4201d-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4201d-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4201d-123">Parent Elements</span></span>  
  
|<span data-ttu-id="4201d-124">요소</span><span class="sxs-lookup"><span data-stu-id="4201d-124">Element</span></span>|<span data-ttu-id="4201d-125">설명</span><span class="sxs-lookup"><span data-stu-id="4201d-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4201d-126">\<a d d ></span><span class="sxs-lookup"><span data-stu-id="4201d-126">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="4201d-127">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="4201d-127">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4201d-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4201d-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.DefaultPortElement>
