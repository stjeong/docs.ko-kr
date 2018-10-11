---
title: WCF의 &lt;bookmarkResumptionQuery&gt;
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: 07215347da19a05d5915296668d990853fdae646
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49087793"
---
# <a name="ltbookmarkresumptionquerygt-of-wcf"></a><span data-ttu-id="e68cd-102">WCF의 &lt;bookmarkResumptionQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="e68cd-102">&lt;bookmarkResumptionQuery&gt; of WCF</span></span>
<span data-ttu-id="e68cd-103">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e68cd-103">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="e68cd-104">추적 참가자가 책갈피 다시 시작 레코드를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e68cd-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="e68cd-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="e68cd-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="e68cd-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="e68cd-106">\<system.serviceModel></span></span>  
<span data-ttu-id="e68cd-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="e68cd-107">\<tracking></span></span>  
<span data-ttu-id="e68cd-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="e68cd-108">\<trackingProfile></span></span>  
<span data-ttu-id="e68cd-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="e68cd-109">\<workflow></span></span>  
<span data-ttu-id="e68cd-110">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="e68cd-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="e68cd-111">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="e68cd-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e68cd-112">구문</span><span class="sxs-lookup"><span data-stu-id="e68cd-112">Syntax</span></span>  
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="e68cd-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="e68cd-113">Attributes and Elements</span></span>  
 <span data-ttu-id="e68cd-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e68cd-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e68cd-115">특성</span><span class="sxs-lookup"><span data-stu-id="e68cd-115">Attributes</span></span>  
  
|<span data-ttu-id="e68cd-116">특성</span><span class="sxs-lookup"><span data-stu-id="e68cd-116">Attribute</span></span>|<span data-ttu-id="e68cd-117">설명</span><span class="sxs-lookup"><span data-stu-id="e68cd-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e68cd-118">name</span><span class="sxs-lookup"><span data-stu-id="e68cd-118">name</span></span>|<span data-ttu-id="e68cd-119">구독할 책갈피 레코드의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="e68cd-119">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e68cd-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="e68cd-120">Child Elements</span></span>  
 <span data-ttu-id="e68cd-121">없음</span><span class="sxs-lookup"><span data-stu-id="e68cd-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e68cd-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="e68cd-122">Parent Elements</span></span>  
  
|<span data-ttu-id="e68cd-123">요소</span><span class="sxs-lookup"><span data-stu-id="e68cd-123">Element</span></span>|<span data-ttu-id="e68cd-124">설명</span><span class="sxs-lookup"><span data-stu-id="e68cd-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e68cd-125">\<bookmarkResumptionQueries></span><span class="sxs-lookup"><span data-stu-id="e68cd-125">\<bookmarkResumptionQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionqueries.md)|<span data-ttu-id="e68cd-126">워크플로 인스턴스 내의 책갈피 다시 시작을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e68cd-126">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e68cd-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e68cd-127">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="e68cd-128">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="e68cd-128">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="e68cd-129">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="e68cd-129">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
