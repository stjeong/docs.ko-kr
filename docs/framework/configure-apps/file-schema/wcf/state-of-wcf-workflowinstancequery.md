---
title: WCF의 &lt;state&gt;, &lt;workflowInstanceQuery&gt;
ms.date: 03/30/2017
ms.assetid: 40f21055-766c-4be9-86c4-d1d899007098
ms.openlocfilehash: 168a6980e955f602ee60bff26461f06cb16c836a
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145928"
---
# <a name="ltstategt-of-wcf-ltworkflowinstancequerygt"></a><span data-ttu-id="3a5ba-102">WCF의 &lt;state&gt;, &lt;workflowInstanceQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="3a5ba-102">&lt;state&gt; of WCF, &lt;workflowInstanceQuery&gt;</span></span>
<span data-ttu-id="3a5ba-103">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="3a5ba-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="3a5ba-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="3a5ba-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="3a5ba-105">\<system.serviceModel></span></span>  
<span data-ttu-id="3a5ba-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="3a5ba-106">\<tracking></span></span>  
<span data-ttu-id="3a5ba-107">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="3a5ba-107">\<profiles></span></span>  
<span data-ttu-id="3a5ba-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="3a5ba-108">\<trackingProfile></span></span>  
<span data-ttu-id="3a5ba-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="3a5ba-109">\<workflow></span></span>  
<span data-ttu-id="3a5ba-110">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="3a5ba-110">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="3a5ba-111">\<workflowInstanceQuery ></span><span class="sxs-lookup"><span data-stu-id="3a5ba-111">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="3a5ba-112">\<상태 ></span><span class="sxs-lookup"><span data-stu-id="3a5ba-112">\<states></span></span>  
<span data-ttu-id="3a5ba-113">\<상태 ></span><span class="sxs-lookup"><span data-stu-id="3a5ba-113">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a5ba-114">구문</span><span class="sxs-lookup"><span data-stu-id="3a5ba-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3a5ba-115">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="3a5ba-115">Attributes and elements</span></span>

<span data-ttu-id="3a5ba-116">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a5ba-117">특성</span><span class="sxs-lookup"><span data-stu-id="3a5ba-117">Attributes</span></span>

|<span data-ttu-id="3a5ba-118">특성</span><span class="sxs-lookup"><span data-stu-id="3a5ba-118">Attribute</span></span>|<span data-ttu-id="3a5ba-119">설명</span><span class="sxs-lookup"><span data-stu-id="3a5ba-119">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="3a5ba-120">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3a5ba-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="3a5ba-121">Child elements</span></span>

<span data-ttu-id="3a5ba-122">없음</span><span class="sxs-lookup"><span data-stu-id="3a5ba-122">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="3a5ba-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="3a5ba-123">Parent elements</span></span>

|<span data-ttu-id="3a5ba-124">요소</span><span class="sxs-lookup"><span data-stu-id="3a5ba-124">Element</span></span>|<span data-ttu-id="3a5ba-125">설명</span><span class="sxs-lookup"><span data-stu-id="3a5ba-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3a5ba-126">\<상태 ></span><span class="sxs-lookup"><span data-stu-id="3a5ba-126">\<states></span></span>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="3a5ba-127">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a5ba-128">설명</span><span class="sxs-lookup"><span data-stu-id="3a5ba-128">Remarks</span></span>  

<span data-ttu-id="3a5ba-129">반환되는 레코드는 이 컬렉션의 상태를 기준으로 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-129">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="3a5ba-130">가능한 상태 값은 다음 표에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-130">Possible state values are described in the following table:</span></span>
  
|<span data-ttu-id="3a5ba-131">상태</span><span class="sxs-lookup"><span data-stu-id="3a5ba-131">State</span></span>|<span data-ttu-id="3a5ba-132">설명</span><span class="sxs-lookup"><span data-stu-id="3a5ba-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3a5ba-133">Aborted</span><span class="sxs-lookup"><span data-stu-id="3a5ba-133">Aborted</span></span>|<span data-ttu-id="3a5ba-134">워크플로 인스턴스가 중단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="3a5ba-135">Completed</span><span class="sxs-lookup"><span data-stu-id="3a5ba-135">Completed</span></span>|<span data-ttu-id="3a5ba-136">워크플로 인스턴스가 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="3a5ba-137">삭제됨</span><span class="sxs-lookup"><span data-stu-id="3a5ba-137">Deleted</span></span>|<span data-ttu-id="3a5ba-138">워크플로 인스턴스가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="3a5ba-139">Idle</span><span class="sxs-lookup"><span data-stu-id="3a5ba-139">Idle</span></span>|<span data-ttu-id="3a5ba-140">워크플로 인스턴스가 유휴 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="3a5ba-141">Persisted</span><span class="sxs-lookup"><span data-stu-id="3a5ba-141">Persisted</span></span>|<span data-ttu-id="3a5ba-142">워크플로 인스턴스가 지속되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="3a5ba-143">Resumed</span><span class="sxs-lookup"><span data-stu-id="3a5ba-143">Resumed</span></span>|<span data-ttu-id="3a5ba-144">워크플로 인스턴스가 다시 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="3a5ba-145">시작됨</span><span class="sxs-lookup"><span data-stu-id="3a5ba-145">Started</span></span>|<span data-ttu-id="3a5ba-146">워크플로 인스턴스가 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="3a5ba-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="3a5ba-147">UnhandledException</span></span>|<span data-ttu-id="3a5ba-148">워크플로 인스턴스에서 처리되지 않은 예외가 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="3a5ba-149">Unloaded</span><span class="sxs-lookup"><span data-stu-id="3a5ba-149">Unloaded</span></span>|<span data-ttu-id="3a5ba-150">워크플로 인스턴스가 언로드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="3a5ba-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="3a5ba-151">Canceled</span></span>|<span data-ttu-id="3a5ba-152">워크플로 인스턴스가 취소되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="3a5ba-153">일시 중단됨</span><span class="sxs-lookup"><span data-stu-id="3a5ba-153">Suspended</span></span>|<span data-ttu-id="3a5ba-154">워크플로 인스턴스가 일시 중단된 경우</span><span class="sxs-lookup"><span data-stu-id="3a5ba-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="3a5ba-155">Terminated</span><span class="sxs-lookup"><span data-stu-id="3a5ba-155">Terminated</span></span>|<span data-ttu-id="3a5ba-156">워크플로 인스턴스가 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="3a5ba-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="3a5ba-157">Unsuspended</span></span>|<span data-ttu-id="3a5ba-158">워크플로 인스턴스의 일시 중단이 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="3a5ba-159">예제</span><span class="sxs-lookup"><span data-stu-id="3a5ba-159">Example</span></span>

<span data-ttu-id="3a5ba-160">다음 구성은 이 쿼리를 사용하여 `Started` 인스턴스 상태에 대한 워크플로 인스턴스 수준 추적 레코드를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="3a5ba-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="3a5ba-161">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3a5ba-161">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="3a5ba-162">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="3a5ba-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="3a5ba-163">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="3a5ba-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
