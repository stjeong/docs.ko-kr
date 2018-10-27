---
title: WCF의 &lt;activityScheduledQueries&gt;
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: 35bcb0dc0c33d30eee566869579edb32f131f495
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452698"
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="171b8-102">WCF의 &lt;activityScheduledQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="171b8-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="171b8-103">부모 활동에 의해 실행이 예약된 활동을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="171b8-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="171b8-104">추적 참가자가 활동 예약 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="171b8-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="171b8-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="171b8-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="171b8-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="171b8-106">\<system.serviceModel></span></span>  
<span data-ttu-id="171b8-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="171b8-107">\<tracking></span></span>  
<span data-ttu-id="171b8-108">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="171b8-108">\<profiles></span></span>  
<span data-ttu-id="171b8-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="171b8-109">\<trackingProfile></span></span>  
<span data-ttu-id="171b8-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="171b8-110">\<workflow></span></span>  
<span data-ttu-id="171b8-111">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="171b8-111">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="171b8-112">구문</span><span class="sxs-lookup"><span data-stu-id="171b8-112">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"   
                                  childActivityName="String"/>
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="171b8-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="171b8-113">Attributes and elements</span></span>  

<span data-ttu-id="171b8-114">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="171b8-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="171b8-115">특성</span><span class="sxs-lookup"><span data-stu-id="171b8-115">Attributes</span></span>  

<span data-ttu-id="171b8-116">없음</span><span class="sxs-lookup"><span data-stu-id="171b8-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="171b8-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="171b8-117">Child elements</span></span>  
  
|<span data-ttu-id="171b8-118">요소</span><span class="sxs-lookup"><span data-stu-id="171b8-118">Element</span></span>|<span data-ttu-id="171b8-119">설명</span><span class="sxs-lookup"><span data-stu-id="171b8-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="171b8-120">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="171b8-120">\<activityScheduledQuery></span></span>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="171b8-121">부모 활동에 의해 실행이 예약된 활동을 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="171b8-121">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="171b8-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="171b8-122">Parent elements</span></span>  
  
|<span data-ttu-id="171b8-123">요소</span><span class="sxs-lookup"><span data-stu-id="171b8-123">Element</span></span>|<span data-ttu-id="171b8-124">설명</span><span class="sxs-lookup"><span data-stu-id="171b8-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="171b8-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="171b8-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="171b8-126">`activityDefinitionId` 속성에 의해 식별되는 특정 워크플로에 대한 모든 쿼리를 포함하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="171b8-126">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="171b8-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="171b8-127">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="171b8-128">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="171b8-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="171b8-129">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="171b8-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
