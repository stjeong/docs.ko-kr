---
title: WCF의 &lt;activityStateQueries&gt;
ms.date: 10/08/2018
ms.assetid: 9e45db49-ed85-4fdf-bd65-0d5477e31823
ms.openlocfilehash: 081dc297912ed5735dd51111936b85b61f463d2d
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123243"
---
# <a name="ltactivitystatequeriesgt-of-wcf"></a><span data-ttu-id="c6664-102">WCF의 &lt;activityStateQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="c6664-102">&lt;activityStateQueries&gt; of WCF</span></span>

<span data-ttu-id="c6664-103">워크플로 인스턴스를 구성하는 활동의 수명 주기 변경 내용을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-103">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="c6664-104">예를 들어 다음 워크플로 인스턴스 내에 "전자 메일 보내기" 활동이 완료 될 때마다 추적 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="c6664-105">추적 참가자가 활동 상태 레코드 개체를 구독하려면 이 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="c6664-106">구독하기 위해 사용 가능한 상태는 ActivityStates에서 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-106">The available states to subscribe to are specified in ActivityStates.</span></span>

<span data-ttu-id="c6664-107">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>

<span data-ttu-id="c6664-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="c6664-108">\<system.serviceModel></span></span>  
<span data-ttu-id="c6664-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="c6664-109">\<tracking></span></span>  
<span data-ttu-id="c6664-110">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="c6664-110">\<profiles></span></span>  
<span data-ttu-id="c6664-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="c6664-111">\<trackingProfile></span></span>  
<span data-ttu-id="c6664-112">\<workflow></span><span class="sxs-lookup"><span data-stu-id="c6664-112">\<workflow></span></span>  
<span data-ttu-id="c6664-113">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="c6664-113">\<activityStateQueries></span></span>  

## <a name="syntax"></a><span data-ttu-id="c6664-114">구문</span><span class="sxs-lookup"><span data-stu-id="c6664-114">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityStateQueries>
          <activityStateQuery activityName="String">
            <arguments>
              <argument name="String"/>
            </arguments>
            <states>
              <state name="String"/>
            </states>
            <variables>
              <variable name="String"/>
            </variables>
          </activityStateQuery>
        </activityStateQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  

## <a name="attributes-and-elements"></a><span data-ttu-id="c6664-115">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="c6664-115">Attributes and elements</span></span>

<span data-ttu-id="c6664-116">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6664-117">특성</span><span class="sxs-lookup"><span data-stu-id="c6664-117">Attributes</span></span>  

<span data-ttu-id="c6664-118">없음</span><span class="sxs-lookup"><span data-stu-id="c6664-118">None.</span></span>  

### <a name="child-elements"></a><span data-ttu-id="c6664-119">자식 요소</span><span class="sxs-lookup"><span data-stu-id="c6664-119">Child elements</span></span>

|<span data-ttu-id="c6664-120">요소</span><span class="sxs-lookup"><span data-stu-id="c6664-120">Element</span></span>|<span data-ttu-id="c6664-121">설명</span><span class="sxs-lookup"><span data-stu-id="c6664-121">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="c6664-122">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="c6664-122">\<activityStateQuery></span></span>](activitystatequery-of-wcf.md)|<span data-ttu-id="c6664-123">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="c6664-124">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-124">This event occurs each time a FaultHandler processes a fault.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="c6664-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="c6664-125">Parent elements</span></span>

|<span data-ttu-id="c6664-126">요소</span><span class="sxs-lookup"><span data-stu-id="c6664-126">Element</span></span>|<span data-ttu-id="c6664-127">설명</span><span class="sxs-lookup"><span data-stu-id="c6664-127">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="c6664-128">\<workflow></span><span class="sxs-lookup"><span data-stu-id="c6664-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="c6664-129">`activityDefinitionId` 속성에 의해 식별되는 특정 워크플로에 대한 모든 쿼리를 포함하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="c6664-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|

## <a name="see-also"></a><span data-ttu-id="c6664-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="c6664-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection>    
- <xref:System.Activities.Tracking.ActivityStateQuery>    
- [<span data-ttu-id="c6664-131">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="c6664-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="c6664-132">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="c6664-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
