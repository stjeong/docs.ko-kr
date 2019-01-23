---
title: '&lt;cancelRequestedQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8da9b1c4-338a-4f23-9830-6d257772d340
ms.openlocfilehash: a3d24536589288ce9585901f3d955075bc856c97
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520310"
---
# <a name="ltcancelrequestedquerygt"></a><span data-ttu-id="a9b1e-102">&lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="a9b1e-102">&lt;cancelRequestedQuery&gt;</span></span>
<span data-ttu-id="a9b1e-103">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="a9b1e-104">추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="a9b1e-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="a9b1e-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a9b1e-106">\<system.serviceModel></span></span>  
<span data-ttu-id="a9b1e-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="a9b1e-107">\<tracking></span></span>  
<span data-ttu-id="a9b1e-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="a9b1e-108">\<trackingProfile></span></span>  
<span data-ttu-id="a9b1e-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="a9b1e-109">\<workflow></span></span>  
<span data-ttu-id="a9b1e-110">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="a9b1e-110">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="a9b1e-111">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="a9b1e-111">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9b1e-112">구문</span><span class="sxs-lookup"><span data-stu-id="a9b1e-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a9b1e-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a9b1e-113">Attributes and Elements</span></span>  
 <span data-ttu-id="a9b1e-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a9b1e-115">특성</span><span class="sxs-lookup"><span data-stu-id="a9b1e-115">Attributes</span></span>  
  
|<span data-ttu-id="a9b1e-116">특성</span><span class="sxs-lookup"><span data-stu-id="a9b1e-116">Attribute</span></span>|<span data-ttu-id="a9b1e-117">설명</span><span class="sxs-lookup"><span data-stu-id="a9b1e-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b1e-118">activityName</span><span class="sxs-lookup"><span data-stu-id="a9b1e-118">activityName</span></span>|<span data-ttu-id="a9b1e-119">취소를 요청하는 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="a9b1e-120">childActivityName</span><span class="sxs-lookup"><span data-stu-id="a9b1e-120">childActivityName</span></span>|<span data-ttu-id="a9b1e-121">취소가 요청된 자식 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-121">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a9b1e-122">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a9b1e-122">Child Elements</span></span>  
 <span data-ttu-id="a9b1e-123">없음</span><span class="sxs-lookup"><span data-stu-id="a9b1e-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a9b1e-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a9b1e-124">Parent Elements</span></span>  
  
|<span data-ttu-id="a9b1e-125">요소</span><span class="sxs-lookup"><span data-stu-id="a9b1e-125">Element</span></span>|<span data-ttu-id="a9b1e-126">설명</span><span class="sxs-lookup"><span data-stu-id="a9b1e-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a9b1e-127">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="a9b1e-127">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="a9b1e-128">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 구성 요소의 목록을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-128">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="a9b1e-129">추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b1e-129">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a9b1e-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="a9b1e-130">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="a9b1e-131">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="a9b1e-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a9b1e-132">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="a9b1e-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
