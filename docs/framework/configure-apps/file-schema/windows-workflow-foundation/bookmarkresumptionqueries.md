---
title: <bookmarkResumptionQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8ed61a7f-4254-439c-bdd8-b474971533f7
ms.openlocfilehash: 4277df5b4c36fa2f3571ba8441a7eb8aaf6d106a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261552"
---
# <a name="bookmarkresumptionqueries"></a><span data-ttu-id="80623-101">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="80623-101">\<bookmarkResumptionQueries></span></span>
<span data-ttu-id="80623-102">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80623-102">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="80623-103">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="80623-103">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="80623-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="80623-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="80623-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="80623-105">\<system.serviceModel></span></span>  
<span data-ttu-id="80623-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="80623-106">\<tracking></span></span>  
<span data-ttu-id="80623-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="80623-107">\<trackingProfile></span></span>  
<span data-ttu-id="80623-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="80623-108">\<workflow></span></span>  
<span data-ttu-id="80623-109">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="80623-109">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="80623-110">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="80623-110">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80623-111">구문</span><span class="sxs-lookup"><span data-stu-id="80623-111">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <bookmarkResumptionQueries>
        <bookmarkResumptionQuery name="String" />
      </bookmarkResumptionQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="80623-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="80623-112">Attributes and Elements</span></span>  
 <span data-ttu-id="80623-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="80623-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="80623-114">특성</span><span class="sxs-lookup"><span data-stu-id="80623-114">Attributes</span></span>  
 <span data-ttu-id="80623-115">없음</span><span class="sxs-lookup"><span data-stu-id="80623-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="80623-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="80623-116">Child Elements</span></span>  
  
|<span data-ttu-id="80623-117">요소</span><span class="sxs-lookup"><span data-stu-id="80623-117">Element</span></span>|<span data-ttu-id="80623-118">설명</span><span class="sxs-lookup"><span data-stu-id="80623-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80623-119">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="80623-119">\<bookmarkResumptionQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionquery.md)|<span data-ttu-id="80623-120">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="80623-120">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="80623-121">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="80623-121">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="80623-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="80623-122">Parent Elements</span></span>  
  
|<span data-ttu-id="80623-123">요소</span><span class="sxs-lookup"><span data-stu-id="80623-123">Element</span></span>|<span data-ttu-id="80623-124">설명</span><span class="sxs-lookup"><span data-stu-id="80623-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80623-125">\<workflow></span><span class="sxs-lookup"><span data-stu-id="80623-125">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="80623-126">로 식별 되는 특정 워크플로에 대 한 모든 쿼리를 포함 하는 구성 요소를 **activityDefinitionId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="80623-126">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="80623-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="80623-127">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="80623-128">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="80623-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="80623-129">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="80623-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
