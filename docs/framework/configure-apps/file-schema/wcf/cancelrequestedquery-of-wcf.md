---
title: WCF의 &lt;cancelRequestedQuery&gt;
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 38d946a213131e8dcb6f4100d0ad67f7c167f342
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49086403"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="31ad5-102">WCF의 &lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="31ad5-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>
<span data-ttu-id="31ad5-103">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="31ad5-104">추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="31ad5-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
 <span data-ttu-id="31ad5-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="31ad5-106">\<system.serviceModel></span></span>  
<span data-ttu-id="31ad5-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="31ad5-107">\<tracking></span></span>  
<span data-ttu-id="31ad5-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="31ad5-108">\<trackingProfile></span></span>  
<span data-ttu-id="31ad5-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="31ad5-109">\<workflow></span></span>  
<span data-ttu-id="31ad5-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="31ad5-110">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="31ad5-111">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="31ad5-111">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31ad5-112">구문</span><span class="sxs-lookup"><span data-stu-id="31ad5-112">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String"
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="31ad5-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="31ad5-113">Attributes and Elements</span></span>  
 <span data-ttu-id="31ad5-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="31ad5-115">특성</span><span class="sxs-lookup"><span data-stu-id="31ad5-115">Attributes</span></span>  
  
|<span data-ttu-id="31ad5-116">특성</span><span class="sxs-lookup"><span data-stu-id="31ad5-116">Attribute</span></span>|<span data-ttu-id="31ad5-117">설명</span><span class="sxs-lookup"><span data-stu-id="31ad5-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="31ad5-118">activityName</span><span class="sxs-lookup"><span data-stu-id="31ad5-118">activityName</span></span>|<span data-ttu-id="31ad5-119">취소를 요청하는 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="31ad5-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="31ad5-120">childActivityName</span></span>|<span data-ttu-id="31ad5-121">취소가 요청된 자식 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="31ad5-122">자식 요소</span><span class="sxs-lookup"><span data-stu-id="31ad5-122">Child Elements</span></span>  
 <span data-ttu-id="31ad5-123">없음</span><span class="sxs-lookup"><span data-stu-id="31ad5-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="31ad5-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="31ad5-124">Parent Elements</span></span>  
  
|<span data-ttu-id="31ad5-125">요소</span><span class="sxs-lookup"><span data-stu-id="31ad5-125">Element</span></span>|<span data-ttu-id="31ad5-126">설명</span><span class="sxs-lookup"><span data-stu-id="31ad5-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="31ad5-127">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="31ad5-127">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="31ad5-128">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 구성 요소의 목록을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-128">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="31ad5-129">추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="31ad5-129">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="31ad5-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="31ad5-130">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>     
 [<span data-ttu-id="31ad5-131">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="31ad5-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="31ad5-132">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="31ad5-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
