---
title: '&lt;state&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 619414f2-61c2-4427-9977-d05009e343db
ms.openlocfilehash: 8e381671d9282218a4e5bf0ae979bec79c7cfe78
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54523053"
---
# <a name="ltstategt"></a><span data-ttu-id="cc14f-102">&lt;state&gt;</span><span class="sxs-lookup"><span data-stu-id="cc14f-102">&lt;state&gt;</span></span>
<span data-ttu-id="cc14f-103">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="cc14f-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="cc14f-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="cc14f-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="cc14f-105">\<system.serviceModel></span></span>  
<span data-ttu-id="cc14f-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="cc14f-106">\<tracking></span></span>  
<span data-ttu-id="cc14f-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="cc14f-107">\<trackingProfile></span></span>  
<span data-ttu-id="cc14f-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="cc14f-108">\<workflow></span></span>  
<span data-ttu-id="cc14f-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="cc14f-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="cc14f-110">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="cc14f-110">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="cc14f-111">\<states></span><span class="sxs-lookup"><span data-stu-id="cc14f-111">\<states></span></span>  
<span data-ttu-id="cc14f-112">\<state></span><span class="sxs-lookup"><span data-stu-id="cc14f-112">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc14f-113">구문</span><span class="sxs-lookup"><span data-stu-id="cc14f-113">Syntax</span></span>  
  
```xml  
<tracking>
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
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cc14f-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="cc14f-114">Attributes and Elements</span></span>  
 <span data-ttu-id="cc14f-115">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cc14f-116">특성</span><span class="sxs-lookup"><span data-stu-id="cc14f-116">Attributes</span></span>  
  
|<span data-ttu-id="cc14f-117">특성</span><span class="sxs-lookup"><span data-stu-id="cc14f-117">Attribute</span></span>|<span data-ttu-id="cc14f-118">설명</span><span class="sxs-lookup"><span data-stu-id="cc14f-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cc14f-119">name</span><span class="sxs-lookup"><span data-stu-id="cc14f-119">name</span></span>|<span data-ttu-id="cc14f-120">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-120">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cc14f-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="cc14f-121">Child Elements</span></span>  
 <span data-ttu-id="cc14f-122">없음</span><span class="sxs-lookup"><span data-stu-id="cc14f-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cc14f-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="cc14f-123">Parent Elements</span></span>  
  
|<span data-ttu-id="cc14f-124">요소</span><span class="sxs-lookup"><span data-stu-id="cc14f-124">Element</span></span>|<span data-ttu-id="cc14f-125">설명</span><span class="sxs-lookup"><span data-stu-id="cc14f-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cc14f-126">\<states></span><span class="sxs-lookup"><span data-stu-id="cc14f-126">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="cc14f-127">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-127">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cc14f-128">설명</span><span class="sxs-lookup"><span data-stu-id="cc14f-128">Remarks</span></span>  
 <span data-ttu-id="cc14f-129">반환되는 레코드는 이 컬렉션의 상태를 기준으로 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-129">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="cc14f-130">가능한 상태 값은 다음 표에 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-130">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="cc14f-131">상태</span><span class="sxs-lookup"><span data-stu-id="cc14f-131">State</span></span>|<span data-ttu-id="cc14f-132">설명</span><span class="sxs-lookup"><span data-stu-id="cc14f-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="cc14f-133">Aborted</span><span class="sxs-lookup"><span data-stu-id="cc14f-133">Aborted</span></span>|<span data-ttu-id="cc14f-134">워크플로 인스턴스가 중단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-134">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="cc14f-135">Completed</span><span class="sxs-lookup"><span data-stu-id="cc14f-135">Completed</span></span>|<span data-ttu-id="cc14f-136">워크플로 인스턴스가 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-136">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="cc14f-137">삭제됨</span><span class="sxs-lookup"><span data-stu-id="cc14f-137">Deleted</span></span>|<span data-ttu-id="cc14f-138">워크플로 인스턴스가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-138">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="cc14f-139">Idle</span><span class="sxs-lookup"><span data-stu-id="cc14f-139">Idle</span></span>|<span data-ttu-id="cc14f-140">워크플로 인스턴스가 유휴 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-140">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="cc14f-141">Persisted</span><span class="sxs-lookup"><span data-stu-id="cc14f-141">Persisted</span></span>|<span data-ttu-id="cc14f-142">워크플로 인스턴스가 지속되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-142">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="cc14f-143">Resumed</span><span class="sxs-lookup"><span data-stu-id="cc14f-143">Resumed</span></span>|<span data-ttu-id="cc14f-144">워크플로 인스턴스가 다시 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-144">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="cc14f-145">시작됨</span><span class="sxs-lookup"><span data-stu-id="cc14f-145">Started</span></span>|<span data-ttu-id="cc14f-146">워크플로 인스턴스가 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-146">The workflow instance is started.</span></span>|  
|<span data-ttu-id="cc14f-147">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="cc14f-147">UnhandledException</span></span>|<span data-ttu-id="cc14f-148">워크플로 인스턴스에서 처리되지 않은 예외가 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-148">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="cc14f-149">Unloaded</span><span class="sxs-lookup"><span data-stu-id="cc14f-149">Unloaded</span></span>|<span data-ttu-id="cc14f-150">워크플로 인스턴스가 언로드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-150">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="cc14f-151">Canceled</span><span class="sxs-lookup"><span data-stu-id="cc14f-151">Canceled</span></span>|<span data-ttu-id="cc14f-152">워크플로 인스턴스가 취소되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-152">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="cc14f-153">일시 중단됨</span><span class="sxs-lookup"><span data-stu-id="cc14f-153">Suspended</span></span>|<span data-ttu-id="cc14f-154">워크플로 인스턴스가 일시 중단된 경우</span><span class="sxs-lookup"><span data-stu-id="cc14f-154">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="cc14f-155">Terminated</span><span class="sxs-lookup"><span data-stu-id="cc14f-155">Terminated</span></span>|<span data-ttu-id="cc14f-156">워크플로 인스턴스가 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-156">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="cc14f-157">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="cc14f-157">Unsuspended</span></span>|<span data-ttu-id="cc14f-158">워크플로 인스턴스의 일시 중단이 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-158">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="cc14f-159">예제</span><span class="sxs-lookup"><span data-stu-id="cc14f-159">Example</span></span>  
 <span data-ttu-id="cc14f-160">다음 구성은 이 쿼리를 사용하여 `Started` 인스턴스 상태에 대한 워크플로 인스턴스 수준 추적 레코드를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="cc14f-160">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="cc14f-161">참고자료</span><span class="sxs-lookup"><span data-stu-id="cc14f-161">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="cc14f-162">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="cc14f-162">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="cc14f-163">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="cc14f-163">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
