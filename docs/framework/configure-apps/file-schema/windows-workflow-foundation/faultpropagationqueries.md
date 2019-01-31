---
title: <faultPropagationQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 00ff90ae-ebe0-4c85-a93f-61557288d0a3
ms.openlocfilehash: 0424c01397a95803b9e8502d90a55d1bd4c3b5e6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269395"
---
# <a name="faultpropagationqueries"></a><span data-ttu-id="3f696-101">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="3f696-101">\<faultPropagationQueries></span></span>
<span data-ttu-id="3f696-102">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-102">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="3f696-103">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-103">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="3f696-104">활동 내에서 발생하는 오류 처리를 추적하려면 이러한 쿼리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-104">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="3f696-105">추적 참가자가 오류 전파 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-105">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="3f696-106">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-106">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="3f696-107">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="3f696-107">\<system.serviceModel></span></span>  
<span data-ttu-id="3f696-108">\<tracking></span><span class="sxs-lookup"><span data-stu-id="3f696-108">\<tracking></span></span>  
<span data-ttu-id="3f696-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="3f696-109">\<trackingProfile></span></span>  
<span data-ttu-id="3f696-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="3f696-110">\<workflow></span></span>  
<span data-ttu-id="3f696-111">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="3f696-111">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f696-112">구문</span><span class="sxs-lookup"><span data-stu-id="3f696-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3f696-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="3f696-113">Attributes and Elements</span></span>  
 <span data-ttu-id="3f696-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3f696-115">특성</span><span class="sxs-lookup"><span data-stu-id="3f696-115">Attributes</span></span>  
 <span data-ttu-id="3f696-116">없음</span><span class="sxs-lookup"><span data-stu-id="3f696-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="3f696-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="3f696-117">Child Elements</span></span>  
  
|<span data-ttu-id="3f696-118">요소</span><span class="sxs-lookup"><span data-stu-id="3f696-118">Element</span></span>|<span data-ttu-id="3f696-119">설명</span><span class="sxs-lookup"><span data-stu-id="3f696-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3f696-120">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="3f696-120">\<faultPropagationQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationquery.md)|<span data-ttu-id="3f696-121">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-121">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="3f696-122">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-122">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3f696-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="3f696-123">Parent Elements</span></span>  
  
|<span data-ttu-id="3f696-124">요소</span><span class="sxs-lookup"><span data-stu-id="3f696-124">Element</span></span>|<span data-ttu-id="3f696-125">설명</span><span class="sxs-lookup"><span data-stu-id="3f696-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3f696-126">\<workflow></span><span class="sxs-lookup"><span data-stu-id="3f696-126">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="3f696-127">로 식별 되는 특정 워크플로에 대 한 모든 쿼리를 포함 하는 구성 요소를 **activityDefinitionId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="3f696-127">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3f696-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="3f696-128">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="3f696-129">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="3f696-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="3f696-130">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="3f696-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
