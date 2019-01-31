---
title: <webScriptEndpoint>
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: 3d95624c82388ed6219fc567dd2d3c17bedad7a1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255291"
---
# <a name="webscriptendpoint"></a><span data-ttu-id="99b42-101">\<webScriptEndpoint></span><span class="sxs-lookup"><span data-stu-id="99b42-101">\<webScriptEndpoint></span></span>
<span data-ttu-id="99b42-102">이 구성 요소에는 고정 된 표준 끝점을 정의 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) 자동으로 바인딩을 추가 합니다 [ \<enableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) 동작 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b42-102">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) behavior.</span></span> <span data-ttu-id="99b42-103">ASP.NET AJAX 응용 프로그램에서 호출되는 서비스를 기록할 때 이 엔드포인트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="99b42-103">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
<span data-ttu-id="99b42-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="99b42-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="99b42-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="99b42-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99b42-106">구문</span><span class="sxs-lookup"><span data-stu-id="99b42-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="99b42-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="99b42-107">Attributes and Elements</span></span>  
 <span data-ttu-id="99b42-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="99b42-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="99b42-109">특성</span><span class="sxs-lookup"><span data-stu-id="99b42-109">Attributes</span></span>  
  
|<span data-ttu-id="99b42-110">특성</span><span class="sxs-lookup"><span data-stu-id="99b42-110">Attribute</span></span>|<span data-ttu-id="99b42-111">설명</span><span class="sxs-lookup"><span data-stu-id="99b42-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="99b42-112">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="99b42-112">webEndpointType</span></span>|<span data-ttu-id="99b42-113">엔드포인트의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="99b42-113">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="99b42-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="99b42-114">Child Elements</span></span>  
 <span data-ttu-id="99b42-115">없음</span><span class="sxs-lookup"><span data-stu-id="99b42-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="99b42-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="99b42-116">Parent Elements</span></span>  
  
|<span data-ttu-id="99b42-117">요소</span><span class="sxs-lookup"><span data-stu-id="99b42-117">Element</span></span>|<span data-ttu-id="99b42-118">설명</span><span class="sxs-lookup"><span data-stu-id="99b42-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="99b42-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="99b42-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="99b42-120">하나 이상의 속성(주소, 바인딩, 계약)이 고정된 미리 정의된 엔드포인트인 표준 엔드포인트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="99b42-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="99b42-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="99b42-121">See also</span></span>
- <xref:System.ServiceModel.Description.WebScriptEndpoint>
- <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
