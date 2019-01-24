---
title: '&lt;activityStateQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: bdd3c8ae-a13f-4df1-9b3c-a9d6c4bb1b5f
ms.openlocfilehash: bfd19e00e79a95eb717ca9131e92b5ff5c600d5b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511984"
---
# <a name="ltactivitystatequeriesgt"></a><span data-ttu-id="a56c0-102">&lt;activityStateQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="a56c0-102">&lt;activityStateQueries&gt;</span></span>
<span data-ttu-id="a56c0-103">워크플로 인스턴스를 구성하는 활동의 수명 주기 변경 내용을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-103">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="a56c0-104">예를 들어 다음 워크플로 인스턴스 내에 "전자 메일 보내기" 활동이 완료 될 때마다 추적 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="a56c0-105">추적 참가자가 활동 상태 레코드 개체를 구독하려면 이 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="a56c0-106">구독하기 위해 사용 가능한 상태는 ActivityStates에서 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-106">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
 <span data-ttu-id="a56c0-107">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="a56c0-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a56c0-108">\<system.serviceModel></span></span>  
<span data-ttu-id="a56c0-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="a56c0-109">\<tracking></span></span>  
<span data-ttu-id="a56c0-110">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="a56c0-110">\<trackingProfile></span></span>  
<span data-ttu-id="a56c0-111">\<workflow></span><span class="sxs-lookup"><span data-stu-id="a56c0-111">\<workflow></span></span>  
<span data-ttu-id="a56c0-112">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="a56c0-112">\<activityStateQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a56c0-113">구문</span><span class="sxs-lookup"><span data-stu-id="a56c0-113">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String" />
        </arguments>
        <states>
          <state name="String" />
        </states>
        <variables>
         <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a56c0-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a56c0-114">Attributes and Elements</span></span>  
 <span data-ttu-id="a56c0-115">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a56c0-116">특성</span><span class="sxs-lookup"><span data-stu-id="a56c0-116">Attributes</span></span>  
 <span data-ttu-id="a56c0-117">없음</span><span class="sxs-lookup"><span data-stu-id="a56c0-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a56c0-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a56c0-118">Child Elements</span></span>  
  
|<span data-ttu-id="a56c0-119">요소</span><span class="sxs-lookup"><span data-stu-id="a56c0-119">Element</span></span>|<span data-ttu-id="a56c0-120">설명</span><span class="sxs-lookup"><span data-stu-id="a56c0-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a56c0-121">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="a56c0-121">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="a56c0-122">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-122">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="a56c0-123">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-123">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a56c0-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a56c0-124">Parent Elements</span></span>  
  
|<span data-ttu-id="a56c0-125">요소</span><span class="sxs-lookup"><span data-stu-id="a56c0-125">Element</span></span>|<span data-ttu-id="a56c0-126">설명</span><span class="sxs-lookup"><span data-stu-id="a56c0-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a56c0-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="a56c0-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="a56c0-128">로 식별 되는 특정 워크플로에 대 한 모든 쿼리를 포함 하는 구성 요소를 **activityDefinitionId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="a56c0-128">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a56c0-129">참고자료</span><span class="sxs-lookup"><span data-stu-id="a56c0-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="a56c0-130">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="a56c0-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a56c0-131">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="a56c0-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
