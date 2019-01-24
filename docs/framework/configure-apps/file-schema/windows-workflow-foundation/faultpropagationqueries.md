---
title: '&lt;faultPropagationQueries&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 00ff90ae-ebe0-4c85-a93f-61557288d0a3
ms.openlocfilehash: 546b37279c8ba58f9dd9f07dabacb7af602ff232
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610060"
---
# <a name="ltfaultpropagationqueriesgt"></a><span data-ttu-id="12e9d-102">&lt;faultPropagationQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="12e9d-102">&lt;faultPropagationQueries&gt;</span></span>
<span data-ttu-id="12e9d-103">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="12e9d-104">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="12e9d-105">활동 내에서 발생하는 오류 처리를 추적하려면 이러한 쿼리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="12e9d-106">추적 참가자가 오류 전파 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="12e9d-107">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="12e9d-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="12e9d-108">\<system.serviceModel></span></span>  
<span data-ttu-id="12e9d-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="12e9d-109">\<tracking></span></span>  
<span data-ttu-id="12e9d-110">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="12e9d-110">\<trackingProfile></span></span>  
<span data-ttu-id="12e9d-111">\<workflow></span><span class="sxs-lookup"><span data-stu-id="12e9d-111">\<workflow></span></span>  
<span data-ttu-id="12e9d-112">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="12e9d-112">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12e9d-113">구문</span><span class="sxs-lookup"><span data-stu-id="12e9d-113">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <faultPropagationQueries>
        <faultPropagationQuery activityName="String" 
                               faultHandlerActivityName="String" />
      </faultPropagationQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="12e9d-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="12e9d-114">Attributes and Elements</span></span>  
 <span data-ttu-id="12e9d-115">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="12e9d-116">특성</span><span class="sxs-lookup"><span data-stu-id="12e9d-116">Attributes</span></span>  
 <span data-ttu-id="12e9d-117">없음</span><span class="sxs-lookup"><span data-stu-id="12e9d-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="12e9d-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="12e9d-118">Child Elements</span></span>  
  
|<span data-ttu-id="12e9d-119">요소</span><span class="sxs-lookup"><span data-stu-id="12e9d-119">Element</span></span>|<span data-ttu-id="12e9d-120">설명</span><span class="sxs-lookup"><span data-stu-id="12e9d-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="12e9d-121">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="12e9d-121">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="12e9d-122">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-122">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="12e9d-123">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-123">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="12e9d-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="12e9d-124">Parent Elements</span></span>  
  
|<span data-ttu-id="12e9d-125">요소</span><span class="sxs-lookup"><span data-stu-id="12e9d-125">Element</span></span>|<span data-ttu-id="12e9d-126">설명</span><span class="sxs-lookup"><span data-stu-id="12e9d-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="12e9d-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="12e9d-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="12e9d-128">로 식별 되는 특정 워크플로에 대 한 모든 쿼리를 포함 하는 구성 요소를 **activityDefinitionId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9d-128">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="12e9d-129">참고자료</span><span class="sxs-lookup"><span data-stu-id="12e9d-129">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="12e9d-130">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="12e9d-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="12e9d-131">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="12e9d-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
