---
title: <enableWebScript>
ms.date: 03/30/2017
ms.assetid: 9c7e96e1-af70-4e6e-ac5c-d67929dddbaa
ms.openlocfilehash: 9c9bbb9ccc7879510ae3e2bee2fabd604fd52f65
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266652"
---
# <a name="enablewebscript"></a><span data-ttu-id="ead15-101">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="ead15-101">\<enableWebScript></span></span>
<span data-ttu-id="ead15-102">이 요소는 ASP.NET AJAX 웹 페이지에서 서비스를 사용할 수 있게 하는 엔드포인트 동작을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ead15-102">This element enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span>  
  
 <span data-ttu-id="ead15-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ead15-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="ead15-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="ead15-104">\<behaviors></span></span>  
<span data-ttu-id="ead15-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="ead15-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="ead15-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="ead15-106">\<behavior></span></span>  
<span data-ttu-id="ead15-107">\<enableWebScript></span><span class="sxs-lookup"><span data-stu-id="ead15-107">\<enableWebScript></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ead15-108">구문</span><span class="sxs-lookup"><span data-stu-id="ead15-108">Syntax</span></span>  
  
```xml  
<enableWebScript />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ead15-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ead15-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ead15-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ead15-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ead15-111">특성</span><span class="sxs-lookup"><span data-stu-id="ead15-111">Attributes</span></span>  
 <span data-ttu-id="ead15-112">없음</span><span class="sxs-lookup"><span data-stu-id="ead15-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ead15-113">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ead15-113">Child Elements</span></span>  
 <span data-ttu-id="ead15-114">없음</span><span class="sxs-lookup"><span data-stu-id="ead15-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ead15-115">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ead15-115">Parent Elements</span></span>  
  
|<span data-ttu-id="ead15-116">요소</span><span class="sxs-lookup"><span data-stu-id="ead15-116">Element</span></span>|<span data-ttu-id="ead15-117">설명</span><span class="sxs-lookup"><span data-stu-id="ead15-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ead15-118">\<behavior></span><span class="sxs-lookup"><span data-stu-id="ead15-118">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="ead15-119">엔드포인트 동작 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ead15-119">Specifies the set of endpoint behaviors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ead15-120">설명</span><span class="sxs-lookup"><span data-stu-id="ead15-120">Remarks</span></span>  
 <span data-ttu-id="ead15-121">이 동작을 사용 하 여 함께에서 해야 합니다 [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) 표준 바인딩 또는 [ \<webMessageEncoding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) 바인딩 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="ead15-121">This behavior should only be used in conjunction with either the [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) standard binding, or the [\<webMessageEncoding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webmessageencoding.md) binding element.</span></span>  <span data-ttu-id="ead15-122">이 동작에 대한 자세한 내용은 <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ead15-122">For more information on this behavior, see <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ead15-123">참고자료</span><span class="sxs-lookup"><span data-stu-id="ead15-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.WebScriptEnablingElement>
- <xref:System.ServiceModel.Description.WebScriptEnablingBehavior>
- [<span data-ttu-id="ead15-124">AJAX 통합 및 JSON 지원</span><span class="sxs-lookup"><span data-stu-id="ead15-124">AJAX Integration and JSON Support</span></span>](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [<span data-ttu-id="ead15-125">\<webHttp></span><span class="sxs-lookup"><span data-stu-id="ead15-125">\<webHttp></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)
