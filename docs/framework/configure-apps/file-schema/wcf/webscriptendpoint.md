---
title: '&lt;webScriptEndpoint&gt;'
ms.date: 03/30/2017
ms.assetid: 85cb5ecf-351b-45f3-aa29-aa2e4b64bcdd
ms.openlocfilehash: beb17d4ccc39bcca30e97d4f0df47c797cde6216
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148775"
---
# <a name="ltwebscriptendpointgt"></a><span data-ttu-id="a0ea4-102">&lt;webScriptEndpoint&gt;</span><span class="sxs-lookup"><span data-stu-id="a0ea4-102">&lt;webScriptEndpoint&gt;</span></span>
<span data-ttu-id="a0ea4-103">이 구성 요소에는 고정 된 표준 끝점을 정의 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) 자동으로 바인딩을 추가 합니다 [ \<enableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) 동작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ea4-103">This configuration element defines a standard endpoint with a fixed [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) binding that automatically adds the [\<enableWebScript>](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md) behavior.</span></span> <span data-ttu-id="a0ea4-104">ASP.NET AJAX 응용 프로그램에서 호출되는 서비스를 기록할 때 이 엔드포인트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ea4-104">Use this endpoint when you are writing a service that is called from an ASP.NET AJAX application.</span></span>  
  
<span data-ttu-id="a0ea4-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a0ea4-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="a0ea4-106">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="a0ea4-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0ea4-107">구문</span><span class="sxs-lookup"><span data-stu-id="a0ea4-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <webScriptEndpoint>
      <standardEndpoint webEndpointType="String" />
    </webScriptEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a0ea4-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a0ea4-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a0ea4-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ea4-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a0ea4-110">특성</span><span class="sxs-lookup"><span data-stu-id="a0ea4-110">Attributes</span></span>  
  
|<span data-ttu-id="a0ea4-111">특성</span><span class="sxs-lookup"><span data-stu-id="a0ea4-111">Attribute</span></span>|<span data-ttu-id="a0ea4-112">설명</span><span class="sxs-lookup"><span data-stu-id="a0ea4-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a0ea4-113">webEndpointType</span><span class="sxs-lookup"><span data-stu-id="a0ea4-113">webEndpointType</span></span>|<span data-ttu-id="a0ea4-114">엔드포인트의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a0ea4-114">A string that specifies the type of the endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a0ea4-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a0ea4-115">Child Elements</span></span>  
 <span data-ttu-id="a0ea4-116">없음</span><span class="sxs-lookup"><span data-stu-id="a0ea4-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a0ea4-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a0ea4-117">Parent Elements</span></span>  
  
|<span data-ttu-id="a0ea4-118">요소</span><span class="sxs-lookup"><span data-stu-id="a0ea4-118">Element</span></span>|<span data-ttu-id="a0ea4-119">설명</span><span class="sxs-lookup"><span data-stu-id="a0ea4-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a0ea4-120">\<standardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="a0ea4-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="a0ea4-121">하나 이상의 속성(주소, 바인딩, 계약)이 고정된 미리 정의된 엔드포인트인 표준 엔드포인트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a0ea4-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a0ea4-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a0ea4-122">See Also</span></span>  
 <xref:System.ServiceModel.Description.WebScriptEndpoint>  
 <xref:System.ServiceModel.Configuration.WebScriptEndpointElement>
