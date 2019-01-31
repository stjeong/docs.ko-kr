---
title: <state>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 619414f2-61c2-4427-9977-d05009e343db
ms.openlocfilehash: 38b0522b93c051473d7cdc28ae955cc3b7b58efe
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55287237"
---
# <a name="state"></a><span data-ttu-id="5e209-101">\<state></span><span class="sxs-lookup"><span data-stu-id="5e209-101">\<state></span></span>
<span data-ttu-id="5e209-102">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-102">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="5e209-103">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="5e209-103">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="5e209-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5e209-104">\<system.serviceModel></span></span>  
<span data-ttu-id="5e209-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="5e209-105">\<tracking></span></span>  
<span data-ttu-id="5e209-106">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="5e209-106">\<trackingProfile></span></span>  
<span data-ttu-id="5e209-107">\<workflow></span><span class="sxs-lookup"><span data-stu-id="5e209-107">\<workflow></span></span>  
<span data-ttu-id="5e209-108">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="5e209-108">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="5e209-109">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="5e209-109">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="5e209-110">\<states></span><span class="sxs-lookup"><span data-stu-id="5e209-110">\<states></span></span>  
<span data-ttu-id="5e209-111">\<state></span><span class="sxs-lookup"><span data-stu-id="5e209-111">\<state></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e209-112">구문</span><span class="sxs-lookup"><span data-stu-id="5e209-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e209-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="5e209-113">Attributes and Elements</span></span>  
 <span data-ttu-id="5e209-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e209-115">특성</span><span class="sxs-lookup"><span data-stu-id="5e209-115">Attributes</span></span>  
  
|<span data-ttu-id="5e209-116">특성</span><span class="sxs-lookup"><span data-stu-id="5e209-116">Attribute</span></span>|<span data-ttu-id="5e209-117">설명</span><span class="sxs-lookup"><span data-stu-id="5e209-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e209-118">name</span><span class="sxs-lookup"><span data-stu-id="5e209-118">name</span></span>|<span data-ttu-id="5e209-119">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-119">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e209-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="5e209-120">Child Elements</span></span>  
 <span data-ttu-id="5e209-121">없음</span><span class="sxs-lookup"><span data-stu-id="5e209-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5e209-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="5e209-122">Parent Elements</span></span>  
  
|<span data-ttu-id="5e209-123">요소</span><span class="sxs-lookup"><span data-stu-id="5e209-123">Element</span></span>|<span data-ttu-id="5e209-124">설명</span><span class="sxs-lookup"><span data-stu-id="5e209-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e209-125">\<states></span><span class="sxs-lookup"><span data-stu-id="5e209-125">\<states></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="5e209-126">추적 레코드가 만들어질 때 추적된 워크플로 인스턴스에서 구독된 상태의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-126">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5e209-127">설명</span><span class="sxs-lookup"><span data-stu-id="5e209-127">Remarks</span></span>  
 <span data-ttu-id="5e209-128">반환되는 레코드는 이 컬렉션의 상태를 기준으로 필터링됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-128">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="5e209-129">가능한 상태 값은 다음 표에 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-129">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="5e209-130">상태</span><span class="sxs-lookup"><span data-stu-id="5e209-130">State</span></span>|<span data-ttu-id="5e209-131">설명</span><span class="sxs-lookup"><span data-stu-id="5e209-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="5e209-132">Aborted</span><span class="sxs-lookup"><span data-stu-id="5e209-132">Aborted</span></span>|<span data-ttu-id="5e209-133">워크플로 인스턴스가 중단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-133">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="5e209-134">Completed</span><span class="sxs-lookup"><span data-stu-id="5e209-134">Completed</span></span>|<span data-ttu-id="5e209-135">워크플로 인스턴스가 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-135">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="5e209-136">삭제됨</span><span class="sxs-lookup"><span data-stu-id="5e209-136">Deleted</span></span>|<span data-ttu-id="5e209-137">워크플로 인스턴스가 삭제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-137">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="5e209-138">Idle</span><span class="sxs-lookup"><span data-stu-id="5e209-138">Idle</span></span>|<span data-ttu-id="5e209-139">워크플로 인스턴스가 유휴 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-139">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="5e209-140">Persisted</span><span class="sxs-lookup"><span data-stu-id="5e209-140">Persisted</span></span>|<span data-ttu-id="5e209-141">워크플로 인스턴스가 지속되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-141">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="5e209-142">Resumed</span><span class="sxs-lookup"><span data-stu-id="5e209-142">Resumed</span></span>|<span data-ttu-id="5e209-143">워크플로 인스턴스가 다시 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-143">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="5e209-144">시작됨</span><span class="sxs-lookup"><span data-stu-id="5e209-144">Started</span></span>|<span data-ttu-id="5e209-145">워크플로 인스턴스가 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-145">The workflow instance is started.</span></span>|  
|<span data-ttu-id="5e209-146">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="5e209-146">UnhandledException</span></span>|<span data-ttu-id="5e209-147">워크플로 인스턴스에서 처리되지 않은 예외가 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-147">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="5e209-148">Unloaded</span><span class="sxs-lookup"><span data-stu-id="5e209-148">Unloaded</span></span>|<span data-ttu-id="5e209-149">워크플로 인스턴스가 언로드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-149">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="5e209-150">Canceled</span><span class="sxs-lookup"><span data-stu-id="5e209-150">Canceled</span></span>|<span data-ttu-id="5e209-151">워크플로 인스턴스가 취소되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-151">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="5e209-152">일시 중단됨</span><span class="sxs-lookup"><span data-stu-id="5e209-152">Suspended</span></span>|<span data-ttu-id="5e209-153">워크플로 인스턴스가 일시 중단된 경우</span><span class="sxs-lookup"><span data-stu-id="5e209-153">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="5e209-154">Terminated</span><span class="sxs-lookup"><span data-stu-id="5e209-154">Terminated</span></span>|<span data-ttu-id="5e209-155">워크플로 인스턴스가 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-155">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="5e209-156">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="5e209-156">Unsuspended</span></span>|<span data-ttu-id="5e209-157">워크플로 인스턴스의 일시 중단이 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-157">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="5e209-158">예제</span><span class="sxs-lookup"><span data-stu-id="5e209-158">Example</span></span>  
 <span data-ttu-id="5e209-159">다음 구성은 이 쿼리를 사용하여 `Started` 인스턴스 상태에 대한 워크플로 인스턴스 수준 추적 레코드를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="5e209-159">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5e209-160">참고자료</span><span class="sxs-lookup"><span data-stu-id="5e209-160">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="5e209-161">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="5e209-161">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="5e209-162">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="5e209-162">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
