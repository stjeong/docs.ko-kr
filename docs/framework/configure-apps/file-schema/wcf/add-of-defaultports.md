---
title: <add>의 <defaultPorts>
ms.date: 03/30/2017
ms.assetid: f162ce42-963b-4779-96a7-d6d8b4ea0d2f
ms.openlocfilehash: 799715ef008274ead6b745e8ab97e769cb59e6b5
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261602"
---
# <a name="add-of-defaultports"></a><span data-ttu-id="4103b-102">\<추가 >의 \<a d d ></span><span class="sxs-lookup"><span data-stu-id="4103b-102">\<add> of \<defaultPorts></span></span>
<span data-ttu-id="4103b-103">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="4103b-103">A default communications endpoint that the client application listens to.</span></span>  
  
 <span data-ttu-id="4103b-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4103b-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4103b-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="4103b-105">\<behaviors></span></span>  
<span data-ttu-id="4103b-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="4103b-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="4103b-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4103b-107">\<behavior></span></span>  
<span data-ttu-id="4103b-108">\<useRequestHeadersForMetadataAddress></span><span class="sxs-lookup"><span data-stu-id="4103b-108">\<useRequestHeadersForMetadataAddress></span></span>  
<span data-ttu-id="4103b-109">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="4103b-109">\<defaultPorts></span></span>  
<span data-ttu-id="4103b-110">\<add></span><span class="sxs-lookup"><span data-stu-id="4103b-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4103b-111">구문</span><span class="sxs-lookup"><span data-stu-id="4103b-111">Syntax</span></span>  
  
```xml  
<useRequestHeadersForMetadataAddress>
  <defaultPorts>
    <add port="Integer"
         scheme="String" />
  </defaultPorts>
</useRequestHeadersForMetadataAddress>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4103b-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4103b-112">Attributes and Elements</span></span>  
 <span data-ttu-id="4103b-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4103b-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4103b-114">특성</span><span class="sxs-lookup"><span data-stu-id="4103b-114">Attributes</span></span>  
  
|<span data-ttu-id="4103b-115">특성</span><span class="sxs-lookup"><span data-stu-id="4103b-115">Attribute</span></span>|<span data-ttu-id="4103b-116">설명</span><span class="sxs-lookup"><span data-stu-id="4103b-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4103b-117">포트</span><span class="sxs-lookup"><span data-stu-id="4103b-117">port</span></span>|<span data-ttu-id="4103b-118">기본 통신 포트 번호를 지정하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="4103b-118">An integer that specifies the default communications port number</span></span>|  
|<span data-ttu-id="4103b-119">scheme</span><span class="sxs-lookup"><span data-stu-id="4103b-119">scheme</span></span>|<span data-ttu-id="4103b-120">통신 포트와 연결된 프로토콜 설정 그룹을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="4103b-120">A string that specifies the group of protocol settings associated with a communications port.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4103b-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4103b-121">Child Elements</span></span>  
 <span data-ttu-id="4103b-122">없음</span><span class="sxs-lookup"><span data-stu-id="4103b-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4103b-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4103b-123">Parent Elements</span></span>  
  
|<span data-ttu-id="4103b-124">요소</span><span class="sxs-lookup"><span data-stu-id="4103b-124">Element</span></span>|<span data-ttu-id="4103b-125">설명</span><span class="sxs-lookup"><span data-stu-id="4103b-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4103b-126">\<defaultPorts></span><span class="sxs-lookup"><span data-stu-id="4103b-126">\<defaultPorts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultports.md)|<span data-ttu-id="4103b-127">클라이언트 응용 프로그램에서 수신하는 기본 통신 엔드포인트를 나열하는 기본 포트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="4103b-127">A collection of default ports listing the default communications endpoints that the client application listens to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4103b-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="4103b-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.DefaultPortElement>
