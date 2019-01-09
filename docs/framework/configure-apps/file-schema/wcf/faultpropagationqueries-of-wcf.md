---
title: WCF의 &lt;faultPropagationQueries&gt;
ms.date: 03/30/2017
ms.assetid: d85f66a7-e7b0-4dbb-83cc-89fa06fc9161
ms.openlocfilehash: 77a38f8474b5e2ac8634d6ea91bc80c6044ff3ed
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54144966"
---
# <a name="ltfaultpropagationqueriesgt-of-wcf"></a><span data-ttu-id="026e1-102">WCF의 &lt;faultPropagationQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="026e1-102">&lt;faultPropagationQueries&gt; of WCF</span></span>

<span data-ttu-id="026e1-103">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-103">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="026e1-104">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="026e1-105">활동 내에서 발생하는 오류 처리를 추적하려면 이러한 쿼리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="026e1-106">추적 참가자가 오류 전파 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="026e1-107">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="026e1-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="026e1-108">\<system.serviceModel></span></span>  
<span data-ttu-id="026e1-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="026e1-109">\<tracking></span></span>  
<span data-ttu-id="026e1-110">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="026e1-110">\<profiles></span></span>  
<span data-ttu-id="026e1-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="026e1-111">\<trackingProfile></span></span>  
<span data-ttu-id="026e1-112">\<workflow></span><span class="sxs-lookup"><span data-stu-id="026e1-112">\<workflow></span></span>  
<span data-ttu-id="026e1-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="026e1-113">\<faultPropagationQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="026e1-114">구문</span><span class="sxs-lookup"><span data-stu-id="026e1-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="026e1-115">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="026e1-115">Attributes and elements</span></span>

<span data-ttu-id="026e1-116">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="026e1-117">특성</span><span class="sxs-lookup"><span data-stu-id="026e1-117">Attributes</span></span>

<span data-ttu-id="026e1-118">없음</span><span class="sxs-lookup"><span data-stu-id="026e1-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="026e1-119">자식 요소</span><span class="sxs-lookup"><span data-stu-id="026e1-119">Child elements</span></span>

|<span data-ttu-id="026e1-120">요소</span><span class="sxs-lookup"><span data-stu-id="026e1-120">Element</span></span>|<span data-ttu-id="026e1-121">설명</span><span class="sxs-lookup"><span data-stu-id="026e1-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="026e1-122">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="026e1-122">\<faultPropagationQuery></span></span>](faultpropagationquery-of-wcf.md)|<span data-ttu-id="026e1-123">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-123">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="026e1-124">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-124">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="026e1-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="026e1-125">Parent elements</span></span>  
  
|<span data-ttu-id="026e1-126">요소</span><span class="sxs-lookup"><span data-stu-id="026e1-126">Element</span></span>|<span data-ttu-id="026e1-127">설명</span><span class="sxs-lookup"><span data-stu-id="026e1-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="026e1-128">\<workflow></span><span class="sxs-lookup"><span data-stu-id="026e1-128">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="026e1-129">`activityDefinitionId` 속성에 의해 식별되는 특정 워크플로에 대한 모든 쿼리를 포함하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="026e1-129">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="026e1-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="026e1-130">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="026e1-131">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="026e1-131">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="026e1-132">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="026e1-132">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
