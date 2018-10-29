---
title: WCF의 &lt;faultPropagationQueries&gt;
ms.date: 03/30/2017
ms.assetid: d85f66a7-e7b0-4dbb-83cc-89fa06fc9161
ms.openlocfilehash: 1db99a8d80fad5c0eca93777d87047b43371d048
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50202122"
---
# <a name="ltfaultpropagationqueriesgt-of-wcf"></a><span data-ttu-id="dbce4-102">WCF의 &lt;faultPropagationQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="dbce4-102">&lt;faultPropagationQueries&gt; of WCF</span></span>

<span data-ttu-id="dbce4-103">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="dbce4-104">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="dbce4-105">활동 내에서 발생하는 오류 처리를 추적하려면 이러한 쿼리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="dbce4-106">추적 참가자가 오류 전파 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="dbce4-107">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="dbce4-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="dbce4-108">\<system.serviceModel></span></span>  
<span data-ttu-id="dbce4-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="dbce4-109">\<tracking></span></span>  
<span data-ttu-id="dbce4-110">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="dbce4-110">\<profiles></span></span>  
<span data-ttu-id="dbce4-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="dbce4-111">\<trackingProfile></span></span>  
<span data-ttu-id="dbce4-112">\<workflow></span><span class="sxs-lookup"><span data-stu-id="dbce4-112">\<workflow></span></span>  
<span data-ttu-id="dbce4-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="dbce4-113">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbce4-114">구문</span><span class="sxs-lookup"><span data-stu-id="dbce4-114">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String"/>
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="dbce4-115">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="dbce4-115">Attributes and elements</span></span>

<span data-ttu-id="dbce4-116">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbce4-117">특성</span><span class="sxs-lookup"><span data-stu-id="dbce4-117">Attributes</span></span>

<span data-ttu-id="dbce4-118">없음</span><span class="sxs-lookup"><span data-stu-id="dbce4-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dbce4-119">자식 요소</span><span class="sxs-lookup"><span data-stu-id="dbce4-119">Child elements</span></span>

|<span data-ttu-id="dbce4-120">요소</span><span class="sxs-lookup"><span data-stu-id="dbce4-120">Element</span></span>|<span data-ttu-id="dbce4-121">설명</span><span class="sxs-lookup"><span data-stu-id="dbce4-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dbce4-122">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="dbce4-122">\<faultPropagationQuery></span></span>](faultpropagationquery-of-wcf.md)|<span data-ttu-id="dbce4-123">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="dbce4-124">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-124">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="dbce4-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="dbce4-125">Parent elements</span></span>  
  
|<span data-ttu-id="dbce4-126">요소</span><span class="sxs-lookup"><span data-stu-id="dbce4-126">Element</span></span>|<span data-ttu-id="dbce4-127">설명</span><span class="sxs-lookup"><span data-stu-id="dbce4-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dbce4-128">\<workflow></span><span class="sxs-lookup"><span data-stu-id="dbce4-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="dbce4-129">`activityDefinitionId` 속성에 의해 식별되는 특정 워크플로에 대한 모든 쿼리를 포함하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="dbce4-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dbce4-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="dbce4-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="dbce4-131">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="dbce4-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="dbce4-132">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="dbce4-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
