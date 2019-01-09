---
title: '&lt;enableWebScript&gt;'
ms.date: 03/30/2017
ms.assetid: 9c7e96e1-af70-4e6e-ac5c-d67929dddbaa
ms.openlocfilehash: 34100ce17e67e12574ec0cdd677991949d0b9214
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150801"
---
# <a name="ltenablewebscriptgt"></a><span data-ttu-id="268f0-102">&lt;enableWebScript&gt;</span><span class="sxs-lookup"><span data-stu-id="268f0-102">&lt;enableWebScript&gt;</span></span>
<span data-ttu-id="268f0-103">이 요소는 ASP.NET AJAX 웹 페이지에서 서비스를 사용할 수 있게 하는 엔드포인트 동작을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="268f0-103">This element enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span>  
  
 <span data-ttu-id="268f0-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="268f0-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="268f0-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="268f0-105">\<behaviors></span></span>  
<span data-ttu-id="268f0-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="268f0-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="268f0-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="268f0-107">\<behavior></span></span>  
<span data-ttu-id="268f0-108">\<enableWebScript ></span><span class="sxs-lookup"><span data-stu-id="268f0-108">\<enableWebScript></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="268f0-109">구문</span><span class="sxs-lookup"><span data-stu-id="268f0-109">Syntax</span></span>  
  
```xml  
<enableWebScript />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="268f0-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="268f0-110">Attributes and Elements</span></span>  
 <span data-ttu-id="268f0-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="268f0-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="268f0-112">특성</span><span class="sxs-lookup"><span data-stu-id="268f0-112">Attributes</span></span>  
 <span data-ttu-id="268f0-113">없음</span><span class="sxs-lookup"><span data-stu-id="268f0-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="268f0-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="268f0-114">Child Elements</span></span>  
 <span data-ttu-id="268f0-115">없음</span><span class="sxs-lookup"><span data-stu-id="268f0-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="268f0-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="268f0-116">Parent Elements</span></span>  
  
|<span data-ttu-id="268f0-117">요소</span><span class="sxs-lookup"><span data-stu-id="268f0-117">Element</span></span>|<span data-ttu-id="268f0-118">설명</span><span class="sxs-lookup"><span data-stu-id="268f0-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="268f0-119">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="268f0-119">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="268f0-120">엔드포인트 동작 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="268f0-120">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="268f0-121">설명</span><span class="sxs-lookup"><span data-stu-id="268f0-121">Remarks</span></span>  
 <span data-ttu-id="268f0-122">이 동작을 사용 하 여 함께에서 해야 합니다 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) 표준 바인딩 또는 [ \<webMessageEncoding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) 바인딩 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="268f0-122">This behavior should only be used in conjunction with either the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, or the [\<webMessageEncoding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) binding element.</span></span>  <span data-ttu-id="268f0-123">이 동작에 대한 자세한 내용은 <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="268f0-123">For more information on this behavior, see <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="268f0-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="268f0-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WebScriptEnablingElement>  
 <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>  
 [<span data-ttu-id="268f0-125">AJAX 통합 및 JSON 지원</span><span class="sxs-lookup"><span data-stu-id="268f0-125">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)  
 [<span data-ttu-id="268f0-126">\<webHttp ></span><span class="sxs-lookup"><span data-stu-id="268f0-126">\<webHttp></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)
