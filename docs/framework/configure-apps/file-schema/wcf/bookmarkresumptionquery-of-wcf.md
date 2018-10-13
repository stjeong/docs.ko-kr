---
title: WCF의 &lt;bookmarkResumptionQuery&gt;
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: f0721e7e14d543b1ff212fe59ed6a2de0a8a9968
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2018
ms.locfileid: "49308436"
---
# <a name="ltbookmarkresumptionquerygt-of-wcf"></a><span data-ttu-id="a10c1-102">WCF의 &lt;bookmarkResumptionQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="a10c1-102">&lt;bookmarkResumptionQuery&gt; of WCF</span></span>

<span data-ttu-id="a10c1-103">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a10c1-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="a10c1-104">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a10c1-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="a10c1-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="a10c1-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>
  
<span data-ttu-id="a10c1-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a10c1-106">\<system.serviceModel></span></span>  
<span data-ttu-id="a10c1-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="a10c1-107">\<tracking></span></span>  
<span data-ttu-id="a10c1-108">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="a10c1-108">\<profiles></span></span>  
<span data-ttu-id="a10c1-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="a10c1-109">\<trackingProfile></span></span>  
<span data-ttu-id="a10c1-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="a10c1-110">\<workflow></span></span>  
<span data-ttu-id="a10c1-111">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="a10c1-111">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="a10c1-112">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="a10c1-112">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a10c1-113">구문</span><span class="sxs-lookup"><span data-stu-id="a10c1-113">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="a10c1-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a10c1-114">Attributes and elements</span></span>

<span data-ttu-id="a10c1-115">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a10c1-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a10c1-116">특성</span><span class="sxs-lookup"><span data-stu-id="a10c1-116">Attributes</span></span>  
  
|<span data-ttu-id="a10c1-117">특성</span><span class="sxs-lookup"><span data-stu-id="a10c1-117">Attribute</span></span>|<span data-ttu-id="a10c1-118">설명</span><span class="sxs-lookup"><span data-stu-id="a10c1-118">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="a10c1-119">구독할 책갈피 레코드의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a10c1-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a10c1-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a10c1-120">Child elements</span></span>

<span data-ttu-id="a10c1-121">없음</span><span class="sxs-lookup"><span data-stu-id="a10c1-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a10c1-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a10c1-122">Parent elements</span></span>  
  
|<span data-ttu-id="a10c1-123">요소</span><span class="sxs-lookup"><span data-stu-id="a10c1-123">Element</span></span>|<span data-ttu-id="a10c1-124">설명</span><span class="sxs-lookup"><span data-stu-id="a10c1-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a10c1-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="a10c1-125">\<bookmarkResumptionQueries></span></span>](bookmarkresumptionqueries-of-wcf.md)|<span data-ttu-id="a10c1-126">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a10c1-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a10c1-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="a10c1-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="a10c1-128">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="a10c1-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a10c1-129">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="a10c1-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
