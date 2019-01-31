---
title: <defaultPorts>
ms.date: 03/30/2017
ms.assetid: 725d4ee5-bd46-4f0e-9c20-30ba75d6eb2c
ms.openlocfilehash: 595970a56e05c4fc1c9b2c0eb669ec3b3a120fe1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262389"
---
# <a name="defaultports"></a><span data-ttu-id="53782-101">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="53782-101">\<defaultPorts></span></span>
<span data-ttu-id="53782-102">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="53782-102">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>  
  
<span data-ttu-id="53782-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="53782-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="53782-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="53782-104">\<behaviors></span></span>  
<span data-ttu-id="53782-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="53782-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="53782-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="53782-106">\<behavior></span></span>  
<span data-ttu-id="53782-107">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="53782-107">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="53782-108">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="53782-108">\<defaultPorts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53782-109">구문</span><span class="sxs-lookup"><span data-stu-id="53782-109">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add scheme="http"
         port="integer" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="53782-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="53782-110">Attributes and Elements</span></span>  
 <span data-ttu-id="53782-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="53782-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="53782-112">특성</span><span class="sxs-lookup"><span data-stu-id="53782-112">Attributes</span></span>  
 <span data-ttu-id="53782-113">없음</span><span class="sxs-lookup"><span data-stu-id="53782-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="53782-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="53782-114">Child Elements</span></span>  
  
|<span data-ttu-id="53782-115">요소</span><span class="sxs-lookup"><span data-stu-id="53782-115">Element</span></span>|<span data-ttu-id="53782-116">설명</span><span class="sxs-lookup"><span data-stu-id="53782-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="53782-117">\<추가 >의 \<a d d ></span><span class="sxs-lookup"><span data-stu-id="53782-117">\<add> of \<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-defaultports.md)|<span data-ttu-id="53782-118">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="53782-118">A default communications endpoint that the client application listens to.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="53782-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="53782-119">Parent Elements</span></span>  
  
|<span data-ttu-id="53782-120">요소</span><span class="sxs-lookup"><span data-stu-id="53782-120">Element</span></span>|<span data-ttu-id="53782-121">설명</span><span class="sxs-lookup"><span data-stu-id="53782-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="53782-122">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="53782-122">\<useRequestHeadersForMetadataAddress></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|<span data-ttu-id="53782-123">기본 포트의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="53782-123">A list of default ports.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="53782-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="53782-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElementCollection>
