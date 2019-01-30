---
title: <webHttpEndpoint>
ms.date: 03/30/2017
ms.assetid: ecaaeb6f-ebd0-411d-8b53-92477cd45347
ms.openlocfilehash: 9b4dd3a61a9b5ad1b35cce4025a50ac4220fd77e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55256436"
---
# <a name="webhttpendpoint"></a><span data-ttu-id="dcade-101">\<webHttpEndpoint></span><span class="sxs-lookup"><span data-stu-id="dcade-101">\<webHttpEndpoint></span></span>
<span data-ttu-id="dcade-102">이 구성 요소에는 고정 된 표준 끝점을 정의 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) 자동으로 바인딩을 추가 합니다 [ \<webHttp >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) 동작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<webHttp>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) behavior.</span></span> <span data-ttu-id="dcade-103">REST 서비스를 작성할 때는 이 엔드포인트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-103">Use this endpoint when writing a REST service.</span></span>  
  
<span data-ttu-id="dcade-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="dcade-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="dcade-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="dcade-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcade-106">구문</span><span class="sxs-lookup"><span data-stu-id="dcade-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webHttpEndpoint>
      <standardEndpoint automaticFormatSelectionEnabled="String"
                        defaultOutgoingResponseFormat="Xml/Json"
                        helpEnabled="Boolean"
                        webEndpointType="String" />
    </webHttpEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dcade-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="dcade-107">Attributes and Elements</span></span>  
 <span data-ttu-id="dcade-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dcade-109">특성</span><span class="sxs-lookup"><span data-stu-id="dcade-109">Attributes</span></span>  
  
|<span data-ttu-id="dcade-110">특성</span><span class="sxs-lookup"><span data-stu-id="dcade-110">Attribute</span></span>|<span data-ttu-id="dcade-111">설명</span><span class="sxs-lookup"><span data-stu-id="dcade-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dcade-112">automaticFormatSelectionEnabled</span><span class="sxs-lookup"><span data-stu-id="dcade-112">automaticFormatSelectionEnabled</span></span>|<span data-ttu-id="dcade-113">자동 서식 선택을 사용하는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-113">A Boolean value that indicates whether automatic format selection is enabled.</span></span><br /><br /> <span data-ttu-id="dcade-114">자동 서식 선택을 사용하면 인프라에서 요청 메시지의 `Accept` 헤더를 구문 분석하여 가장 적합한 응답 형식을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-114">When automatic format selection is enabled, the infrastructure parses the `Accept` header of the request message and determines the most appropriate response format.</span></span> <span data-ttu-id="dcade-115">`Accept` 헤더에서 적합한 응답 형식을 지정하지 않는 경우 인프라에서 요청 메시지의 `Content-Type`이나 작업의 기본 응답 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-115">If the `Accept` header does not specify a suitable response format, the infrastructure uses the `Content-Type` of the request message or the default response format of the operation.</span></span>|  
|<span data-ttu-id="dcade-116">defaultOutgoingResponseFormat</span><span class="sxs-lookup"><span data-stu-id="dcade-116">defaultOutgoingResponseFormat</span></span>|<span data-ttu-id="dcade-117">나가는 응답의 기본 형식을 지정하는 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-117">An attribute that specifies the default outgoing response format.</span></span> <span data-ttu-id="dcade-118">이 특성은 <xref:System.ServiceModel.Web.WebMessageFormat> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-118">This attribute is of the <xref:System.ServiceModel.Web.WebMessageFormat> type</span></span>|  
|<span data-ttu-id="dcade-119">helpEnabled</span><span class="sxs-lookup"><span data-stu-id="dcade-119">helpEnabled</span></span>|<span data-ttu-id="dcade-120">엔드포인트에 대해 HTTP 도움말 페이지가 사용되는지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-120">A Boolean value that indicates whether the HTTP help page is enabled for the endpoint.</span></span>|  
|<span data-ttu-id="dcade-121">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="dcade-121">webEndpointType</span></span>|<span data-ttu-id="dcade-122">엔드포인트의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-122">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dcade-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="dcade-123">Child Elements</span></span>  
 <span data-ttu-id="dcade-124">없음</span><span class="sxs-lookup"><span data-stu-id="dcade-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dcade-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="dcade-125">Parent Elements</span></span>  
  
|<span data-ttu-id="dcade-126">요소</span><span class="sxs-lookup"><span data-stu-id="dcade-126">Element</span></span>|<span data-ttu-id="dcade-127">설명</span><span class="sxs-lookup"><span data-stu-id="dcade-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dcade-128">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="dcade-128">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="dcade-129">하나 이상의 속성(주소, 바인딩, 계약)이 고정된 미리 정의된 엔드포인트인 표준 엔드포인트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="dcade-129">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dcade-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="dcade-130">See also</span></span>
- <xref:System.ServiceModel.Description.WebHttpEndpoint>
- <xref:System.ServiceModel.Configuration.WebHttpEndpointElement>
