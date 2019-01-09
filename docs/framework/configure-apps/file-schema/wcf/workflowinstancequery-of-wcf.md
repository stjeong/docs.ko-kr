---
title: WCF의 &lt;workflowInstanceQuery&gt;
ms.date: 03/30/2017
ms.assetid: 35c73f9d-474e-42eb-874d-ddc04b1987f3
ms.openlocfilehash: 01867171941db82260d28b0825bdf3453e46e66c
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148177"
---
# <a name="ltworkflowinstancequerygt-of-wcf"></a><span data-ttu-id="fe509-102">WCF의 &lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="fe509-102">&lt;workflowInstanceQuery&gt; of WCF</span></span>

<span data-ttu-id="fe509-103">시작된 이벤트나 완료된 이벤트와 같이 워크플로 인스턴스 수명 주기의 변경 내용을 추적하는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe509-103">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="fe509-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="fe509-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="fe509-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="fe509-105">\<system.serviceModel></span></span>  
<span data-ttu-id="fe509-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="fe509-106">\<tracking></span></span>  
<span data-ttu-id="fe509-107">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="fe509-107">\<profiles></span></span>  
<span data-ttu-id="fe509-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="fe509-108">\<trackingProfile></span></span>  
<span data-ttu-id="fe509-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="fe509-109">\<workflow></span></span>  
<span data-ttu-id="fe509-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="fe509-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="fe509-111">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="fe509-111">\<workflowInstanceQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe509-112">구문</span><span class="sxs-lookup"><span data-stu-id="fe509-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fe509-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="fe509-113">Attributes and elements</span></span>  

<span data-ttu-id="fe509-114">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="fe509-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fe509-115">특성</span><span class="sxs-lookup"><span data-stu-id="fe509-115">Attributes</span></span>  

<span data-ttu-id="fe509-116">없음</span><span class="sxs-lookup"><span data-stu-id="fe509-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fe509-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="fe509-117">Child elements</span></span>  
  
|<span data-ttu-id="fe509-118">요소</span><span class="sxs-lookup"><span data-stu-id="fe509-118">Element</span></span>|<span data-ttu-id="fe509-119">설명</span><span class="sxs-lookup"><span data-stu-id="fe509-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fe509-120">\<상태 ></span><span class="sxs-lookup"><span data-stu-id="fe509-120">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="fe509-121">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="fe509-121">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fe509-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="fe509-122">Parent elements</span></span>  
  
|<span data-ttu-id="fe509-123">요소</span><span class="sxs-lookup"><span data-stu-id="fe509-123">Element</span></span>|<span data-ttu-id="fe509-124">설명</span><span class="sxs-lookup"><span data-stu-id="fe509-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fe509-125">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="fe509-125">\<workflowInstanceQueries></span></span>](workflowinstancequeries-of-wcf.md)|<span data-ttu-id="fe509-126">시작된 이벤트나 완료된 이벤트와 같이 워크플로 인스턴스 수명 주기의 변경 내용을 추적하는 구성 요소의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe509-126">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe509-127">설명</span><span class="sxs-lookup"><span data-stu-id="fe509-127">Remarks</span></span>  

<span data-ttu-id="fe509-128"><xref:System.Activities.Tracking.WorkflowInstanceQuery>는 다음 <xref:System.Activities.Tracking.TrackingRecord> 개체를 구독하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe509-128">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="fe509-129">예제</span><span class="sxs-lookup"><span data-stu-id="fe509-129">Example</span></span>  

<span data-ttu-id="fe509-130">다음 구성은 이 쿼리를 사용하여 `Started` 인스턴스 상태에 대한 워크플로 인스턴스 수준 추적 레코드를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="fe509-130">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="fe509-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fe509-131">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="fe509-132">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="fe509-132">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="fe509-133">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="fe509-133">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
