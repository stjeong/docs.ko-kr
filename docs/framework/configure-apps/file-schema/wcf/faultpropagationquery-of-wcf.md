---
title: WCF의 &lt;faultPropagationQuery&gt;
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: cf582fce4e899e62daa4f34f193a0232ec19a135
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149035"
---
# <a name="ltfaultpropagationquerygt-of-wcf"></a><span data-ttu-id="20c75-102">WCF의 &lt;faultPropagationQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="20c75-102">&lt;faultPropagationQuery&gt; of WCF</span></span>

<span data-ttu-id="20c75-103">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="20c75-104">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="20c75-105">활동 내에서 발생하는 오류 처리를 추적하려면 이러한 쿼리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="20c75-106">추적 참가자가 오류 전파 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="20c75-107">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="20c75-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="20c75-108">\<system.serviceModel></span></span>  
<span data-ttu-id="20c75-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="20c75-109">\<tracking></span></span>  
<span data-ttu-id="20c75-110">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="20c75-110">\<profiles></span></span>  
<span data-ttu-id="20c75-111">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="20c75-111">\<trackingProfile></span></span>  
<span data-ttu-id="20c75-112">\<workflow></span><span class="sxs-lookup"><span data-stu-id="20c75-112">\<workflow></span></span>  
<span data-ttu-id="20c75-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="20c75-113">\<faultPropagationQueries></span></span>  
<span data-ttu-id="20c75-114">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="20c75-114">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20c75-115">구문</span><span class="sxs-lookup"><span data-stu-id="20c75-115">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String" />
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="20c75-116">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="20c75-116">Attributes and elements</span></span>

<span data-ttu-id="20c75-117">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-117">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="20c75-118">특성</span><span class="sxs-lookup"><span data-stu-id="20c75-118">Attributes</span></span>  
  
|<span data-ttu-id="20c75-119">특성</span><span class="sxs-lookup"><span data-stu-id="20c75-119">Attribute</span></span>|<span data-ttu-id="20c75-120">설명</span><span class="sxs-lookup"><span data-stu-id="20c75-120">Description</span></span>|  
|---------------|-----------------|  
|`faultSourceActivityName`|<span data-ttu-id="20c75-121">오류를 전파하는 오류 처리 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="20c75-122">기본값은 \*에 모든 활동에 대해 오류 전파 레코드가 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|`faultHandlerActivityName`|<span data-ttu-id="20c75-123">오류의 출처인 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="20c75-124">자식 요소</span><span class="sxs-lookup"><span data-stu-id="20c75-124">Child elements</span></span>

<span data-ttu-id="20c75-125">없음</span><span class="sxs-lookup"><span data-stu-id="20c75-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20c75-126">부모 요소</span><span class="sxs-lookup"><span data-stu-id="20c75-126">Parent elements</span></span>  
  
|<span data-ttu-id="20c75-127">요소</span><span class="sxs-lookup"><span data-stu-id="20c75-127">Element</span></span>|<span data-ttu-id="20c75-128">설명</span><span class="sxs-lookup"><span data-stu-id="20c75-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20c75-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="20c75-129">\<faultPropagationQueries></span></span>](faultpropagationqueries-of-wcf.md)|<span data-ttu-id="20c75-130">활동 내에서 발생하는 오류의 처리를 추적하는 데 사용되는 구성 요소 목록을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="20c75-131">이 이벤트는 FaultHandler가 오류를 처리할 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="20c75-131">This event occurs each time a FaultHandler processes a fault.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="20c75-132">참고자료</span><span class="sxs-lookup"><span data-stu-id="20c75-132">See also</span></span>  
 
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="20c75-133">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="20c75-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="20c75-134">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="20c75-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
