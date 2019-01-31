---
title: <cancelRequestedQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: eab5af7e-76fa-434d-9d36-873e995cee05
ms.openlocfilehash: 989d6e99457108336c38fb1eece4c9ac2444c974
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271501"
---
# <a name="cancelrequestedqueries"></a><span data-ttu-id="350ed-101">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="350ed-101">\<cancelRequestedQueries></span></span>
<span data-ttu-id="350ed-102">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="350ed-102">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="350ed-103">추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="350ed-103">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="350ed-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="350ed-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="350ed-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="350ed-105">\<system.serviceModel></span></span>  
<span data-ttu-id="350ed-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="350ed-106">\<tracking></span></span>  
<span data-ttu-id="350ed-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="350ed-107">\<trackingProfile></span></span>  
<span data-ttu-id="350ed-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="350ed-108">\<workflow></span></span>  
<span data-ttu-id="350ed-109">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="350ed-109">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="350ed-110">구문</span><span class="sxs-lookup"><span data-stu-id="350ed-110">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String" 
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="350ed-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="350ed-111">Attributes and Elements</span></span>  
 <span data-ttu-id="350ed-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="350ed-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="350ed-113">특성</span><span class="sxs-lookup"><span data-stu-id="350ed-113">Attributes</span></span>  
 <span data-ttu-id="350ed-114">없음</span><span class="sxs-lookup"><span data-stu-id="350ed-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="350ed-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="350ed-115">Child Elements</span></span>  
  
|<span data-ttu-id="350ed-116">요소</span><span class="sxs-lookup"><span data-stu-id="350ed-116">Element</span></span>|<span data-ttu-id="350ed-117">설명</span><span class="sxs-lookup"><span data-stu-id="350ed-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="350ed-118">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="350ed-118">\<cancelRequestedQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|<span data-ttu-id="350ed-119">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="350ed-119">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="350ed-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="350ed-120">Parent Elements</span></span>  
  
|<span data-ttu-id="350ed-121">요소</span><span class="sxs-lookup"><span data-stu-id="350ed-121">Element</span></span>|<span data-ttu-id="350ed-122">설명</span><span class="sxs-lookup"><span data-stu-id="350ed-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="350ed-123">\<workflow></span><span class="sxs-lookup"><span data-stu-id="350ed-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="350ed-124">로 식별 되는 특정 워크플로에 대 한 모든 쿼리를 포함 하는 구성 요소를 **activityDefinitionId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="350ed-124">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="350ed-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="350ed-125">See also</span></span>
- [<span data-ttu-id="350ed-126">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="350ed-126">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="350ed-127">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="350ed-127">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
