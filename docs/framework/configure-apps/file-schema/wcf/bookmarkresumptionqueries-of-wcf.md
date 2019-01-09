---
title: WCF의 &lt;bookmarkResumptionQueries&gt;
ms.date: 03/30/2017
ms.assetid: ed086712-1dc7-4932-a592-d1116a0155f3
ms.openlocfilehash: ba8c98557a859f4bd37b9aaca80a44c393429da4
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146084"
---
# <a name="ltbookmarkresumptionqueriesgt-of-wcf"></a><span data-ttu-id="9eebb-102">WCF의 &lt;bookmarkResumptionQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="9eebb-102">&lt;bookmarkResumptionQueries&gt; of WCF</span></span>
  
<span data-ttu-id="9eebb-103">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-103">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="9eebb-104">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="9eebb-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="9eebb-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9eebb-106">\<system.serviceModel></span></span>  
<span data-ttu-id="9eebb-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="9eebb-107">\<tracking></span></span>  
<span data-ttu-id="9eebb-108">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="9eebb-108">\<profiles></span></span>  
<span data-ttu-id="9eebb-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="9eebb-109">\<trackingProfile></span></span>  
<span data-ttu-id="9eebb-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="9eebb-110">\<workflow></span></span>  
<span data-ttu-id="9eebb-111">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="9eebb-111">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="9eebb-112">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="9eebb-112">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9eebb-113">구문</span><span class="sxs-lookup"><span data-stu-id="9eebb-113">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <bookmarkResumptionQueries>
          <bookmarkResumptionQuery name="String" />
        </bookmarkResumptionQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9eebb-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="9eebb-114">Attributes and elements</span></span>  
  
<span data-ttu-id="9eebb-115">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9eebb-116">특성</span><span class="sxs-lookup"><span data-stu-id="9eebb-116">Attributes</span></span>  
  
<span data-ttu-id="9eebb-117">없음</span><span class="sxs-lookup"><span data-stu-id="9eebb-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9eebb-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="9eebb-118">Child elements</span></span>  
  
|<span data-ttu-id="9eebb-119">요소</span><span class="sxs-lookup"><span data-stu-id="9eebb-119">Element</span></span>|<span data-ttu-id="9eebb-120">설명</span><span class="sxs-lookup"><span data-stu-id="9eebb-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9eebb-121">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="9eebb-121">\<bookmarkResumptionQuery></span></span>](bookmarkresumptionquery-of-wcf.md)|<span data-ttu-id="9eebb-122">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-122">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="9eebb-123">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-123">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9eebb-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="9eebb-124">Parent elements</span></span>  
  
|<span data-ttu-id="9eebb-125">요소</span><span class="sxs-lookup"><span data-stu-id="9eebb-125">Element</span></span>|<span data-ttu-id="9eebb-126">설명</span><span class="sxs-lookup"><span data-stu-id="9eebb-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9eebb-127">\<workflow></span><span class="sxs-lookup"><span data-stu-id="9eebb-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="9eebb-128">`activityDefinitionId` 속성에 의해 식별되는 특정 워크플로에 대한 모든 쿼리를 포함하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9eebb-128">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9eebb-129">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9eebb-129">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType> 
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>       
- [<span data-ttu-id="9eebb-130">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="9eebb-130">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [<span data-ttu-id="9eebb-131">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="9eebb-131">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
