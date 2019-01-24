---
title: '&lt;bookmarkResumptionQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 226de75d-d25c-48d5-b069-4b7d80a6852b
ms.openlocfilehash: a5eb00d1e094484e3ec01e0db18719ec50e4b953
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515073"
---
# <a name="ltbookmarkresumptionquerygt"></a><span data-ttu-id="a1b22-102">&lt;bookmarkResumptionQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="a1b22-102">&lt;bookmarkResumptionQuery&gt;</span></span>
<span data-ttu-id="a1b22-103">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1b22-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="a1b22-104">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b22-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="a1b22-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="a1b22-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="a1b22-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a1b22-106">\<system.serviceModel></span></span>  
<span data-ttu-id="a1b22-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="a1b22-107">\<tracking></span></span>  
<span data-ttu-id="a1b22-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="a1b22-108">\<trackingProfile></span></span>  
<span data-ttu-id="a1b22-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="a1b22-109">\<workflow></span></span>  
<span data-ttu-id="a1b22-110">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="a1b22-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="a1b22-111">\<bookmarkResumptionQuery></span><span class="sxs-lookup"><span data-stu-id="a1b22-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1b22-112">구문</span><span class="sxs-lookup"><span data-stu-id="a1b22-112">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a1b22-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a1b22-113">Attributes and Elements</span></span>  
 <span data-ttu-id="a1b22-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a1b22-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a1b22-115">특성</span><span class="sxs-lookup"><span data-stu-id="a1b22-115">Attributes</span></span>  
  
|<span data-ttu-id="a1b22-116">특성</span><span class="sxs-lookup"><span data-stu-id="a1b22-116">Attribute</span></span>|<span data-ttu-id="a1b22-117">설명</span><span class="sxs-lookup"><span data-stu-id="a1b22-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a1b22-118">name</span><span class="sxs-lookup"><span data-stu-id="a1b22-118">name</span></span>|<span data-ttu-id="a1b22-119">구독할 책갈피 레코드의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a1b22-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a1b22-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a1b22-120">Child Elements</span></span>  
 <span data-ttu-id="a1b22-121">없음</span><span class="sxs-lookup"><span data-stu-id="a1b22-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a1b22-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a1b22-122">Parent Elements</span></span>  
  
|<span data-ttu-id="a1b22-123">요소</span><span class="sxs-lookup"><span data-stu-id="a1b22-123">Element</span></span>|<span data-ttu-id="a1b22-124">설명</span><span class="sxs-lookup"><span data-stu-id="a1b22-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a1b22-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="a1b22-125">\<bookmarkResumptionQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionqueries.md)|<span data-ttu-id="a1b22-126">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1b22-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a1b22-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="a1b22-127">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="a1b22-128">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="a1b22-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a1b22-129">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="a1b22-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
