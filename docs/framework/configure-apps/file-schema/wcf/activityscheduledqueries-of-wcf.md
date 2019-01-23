---
title: WCF의 &lt;activityScheduledQueries&gt;
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: 5430058049e8a09c1e2a289e1f997338c23b9d94
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492158"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="001ea-102">WCF의 &lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="001ea-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="001ea-103">부모 활동에 의해 실행이 예약된 활동을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="001ea-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="001ea-104">추적 참가자가 활동 예약 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="001ea-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="001ea-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="001ea-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="001ea-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="001ea-106">\<system.serviceModel></span></span>  
<span data-ttu-id="001ea-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="001ea-107">\<tracking></span></span>  
<span data-ttu-id="001ea-108">\<profiles></span><span class="sxs-lookup"><span data-stu-id="001ea-108">\<profiles></span></span>  
<span data-ttu-id="001ea-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="001ea-109">\<trackingProfile></span></span>  
<span data-ttu-id="001ea-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="001ea-110">\<workflow></span></span>  
<span data-ttu-id="001ea-111">\<activityScheduledQueries></span><span class="sxs-lookup"><span data-stu-id="001ea-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="001ea-112">구문</span><span class="sxs-lookup"><span data-stu-id="001ea-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"
                                  childActivityName="String" />
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="001ea-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="001ea-113">Attributes and elements</span></span>  

<span data-ttu-id="001ea-114">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="001ea-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="001ea-115">특성</span><span class="sxs-lookup"><span data-stu-id="001ea-115">Attributes</span></span>  

<span data-ttu-id="001ea-116">없음</span><span class="sxs-lookup"><span data-stu-id="001ea-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="001ea-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="001ea-117">Child elements</span></span>  
  
|<span data-ttu-id="001ea-118">요소</span><span class="sxs-lookup"><span data-stu-id="001ea-118">Element</span></span>|<span data-ttu-id="001ea-119">설명</span><span class="sxs-lookup"><span data-stu-id="001ea-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="001ea-120">\<activityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="001ea-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="001ea-121">부모 활동에 의해 실행이 예약된 활동을 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="001ea-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="001ea-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="001ea-122">Parent elements</span></span>  
  
|<span data-ttu-id="001ea-123">요소</span><span class="sxs-lookup"><span data-stu-id="001ea-123">Element</span></span>|<span data-ttu-id="001ea-124">설명</span><span class="sxs-lookup"><span data-stu-id="001ea-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="001ea-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="001ea-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="001ea-126">`activityDefinitionId` 속성에 의해 식별되는 특정 워크플로에 대한 모든 쿼리를 포함하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="001ea-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="001ea-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="001ea-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="001ea-128">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="001ea-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="001ea-129">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="001ea-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
