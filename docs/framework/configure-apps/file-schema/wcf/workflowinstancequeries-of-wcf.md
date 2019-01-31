---
title: <workflowInstanceQueries> WCF의
ms.date: 03/30/2017
ms.assetid: b0852f77-16e4-4d55-8eb7-a19feb0e8fc4
ms.openlocfilehash: 544ca868485a409554ece9d9b000beb1a472d344
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255304"
---
# <a name="workflowinstancequeries-of-wcf"></a><span data-ttu-id="136b3-102">\<workflowInstanceQueries > WCF의</span><span class="sxs-lookup"><span data-stu-id="136b3-102">\<workflowInstanceQueries> of WCF</span></span>

<span data-ttu-id="136b3-103">시작된 이벤트나 완료된 이벤트와 같이 워크플로 인스턴스 수명 주기의 변경 내용을 추적하는 구성 요소의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="136b3-103">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="136b3-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="136b3-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="136b3-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="136b3-105">\<system.serviceModel></span></span>  
<span data-ttu-id="136b3-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="136b3-106">\<tracking></span></span>  
<span data-ttu-id="136b3-107">\<profiles></span><span class="sxs-lookup"><span data-stu-id="136b3-107">\<profiles></span></span>  
<span data-ttu-id="136b3-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="136b3-108">\<trackingProfile></span></span>  
<span data-ttu-id="136b3-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="136b3-109">\<workflow></span></span>  
<span data-ttu-id="136b3-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="136b3-110">\<workflowInstanceQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="136b3-111">구문</span><span class="sxs-lookup"><span data-stu-id="136b3-111">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <workflowInstanceQueries>
          <workflowInstanceQuery>
            <states>
              <state name="Name" />
            </states>
          </workflowInstanceQuery>
        </workflowInstanceQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="136b3-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="136b3-112">Attributes and elements</span></span>

<span data-ttu-id="136b3-113">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="136b3-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="136b3-114">특성</span><span class="sxs-lookup"><span data-stu-id="136b3-114">Attributes</span></span>  

<span data-ttu-id="136b3-115">없음</span><span class="sxs-lookup"><span data-stu-id="136b3-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="136b3-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="136b3-116">Child elements</span></span>  
  
|<span data-ttu-id="136b3-117">요소</span><span class="sxs-lookup"><span data-stu-id="136b3-117">Element</span></span>|<span data-ttu-id="136b3-118">설명</span><span class="sxs-lookup"><span data-stu-id="136b3-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="136b3-119">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="136b3-119">\<workflowInstanceQuery></span></span>](workflowinstancequery-of-wcf.md)|<span data-ttu-id="136b3-120">워크플로 인스턴스 수명 주기 변경 내용을 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="136b3-120">A query that is used to track workflow instance life cycle changes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="136b3-121">부모 요소</span><span class="sxs-lookup"><span data-stu-id="136b3-121">Parent elements</span></span>  
  
|<span data-ttu-id="136b3-122">요소</span><span class="sxs-lookup"><span data-stu-id="136b3-122">Element</span></span>|<span data-ttu-id="136b3-123">설명</span><span class="sxs-lookup"><span data-stu-id="136b3-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="136b3-124">\<workflow></span><span class="sxs-lookup"><span data-stu-id="136b3-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="136b3-125">로 식별 되는 특정 워크플로에 대 한 모든 쿼리를 포함 하는 구성 요소를 [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="136b3-125">A configuration element that contains all queries for a specific workflow identified by the [activityDefinitionId](https://msdn.microsoft.com/library/system.servicemodel.activities.tracking.configuration.profileworkflowelement.activitydefinitionid(VS.100).aspx) property.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="136b3-126">설명</span><span class="sxs-lookup"><span data-stu-id="136b3-126">Remarks</span></span>

<span data-ttu-id="136b3-127"><xref:System.Activities.Tracking.WorkflowInstanceQuery>는 다음 <xref:System.Activities.Tracking.TrackingRecord> 개체를 구독하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="136b3-127">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="136b3-128">예제</span><span class="sxs-lookup"><span data-stu-id="136b3-128">Example</span></span>  

<span data-ttu-id="136b3-129">다음 구성은 이 쿼리를 사용하여 `Started` 인스턴스 상태에 대한 워크플로 인스턴스 수준 추적 레코드를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="136b3-129">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="136b3-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="136b3-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="136b3-131">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="136b3-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="136b3-132">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="136b3-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
