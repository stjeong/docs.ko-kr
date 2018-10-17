---
title: WCF의 &lt;cancelRequestedQuery&gt;
ms.date: 03/30/2017
ms.assetid: b690d870-02eb-4c56-8bc3-e5ca99d7097b
ms.openlocfilehash: 3943d604b586eec37a1d153f10ac049fc9bd5747
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347571"
---
# <a name="ltcancelrequestedquerygt-of-wcf"></a><span data-ttu-id="369fc-102">WCF의 &lt;cancelRequestedQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="369fc-102">&lt;cancelRequestedQuery&gt; of WCF</span></span>

<span data-ttu-id="369fc-103">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 쿼리를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-103">Represents a query that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="369fc-104">추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-104">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
<span data-ttu-id="369fc-105">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>
  
<span data-ttu-id="369fc-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="369fc-106">\<system.serviceModel></span></span>  
<span data-ttu-id="369fc-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="369fc-107">\<tracking></span></span>  
<span data-ttu-id="369fc-108">\<프로필 ></span><span class="sxs-lookup"><span data-stu-id="369fc-108">\<profiles></span></span>  
<span data-ttu-id="369fc-109">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="369fc-109">\<trackingProfile></span></span>  
<span data-ttu-id="369fc-110">\<workflow></span><span class="sxs-lookup"><span data-stu-id="369fc-110">\<workflow></span></span>  
<span data-ttu-id="369fc-111">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="369fc-111">\<cancelRequestedQueries></span></span>  
<span data-ttu-id="369fc-112">\<cancelRequestedQuery ></span><span class="sxs-lookup"><span data-stu-id="369fc-112">\<cancelRequestedQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="369fc-113">구문</span><span class="sxs-lookup"><span data-stu-id="369fc-113">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <cancelRequestedQueries>
          <cancelRequestedQuery activityName="String"
                              childActivityName="String"/>
        </cancelRequestedQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="369fc-114">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="369fc-114">Attributes and elements</span></span>

<span data-ttu-id="369fc-115">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="369fc-116">특성</span><span class="sxs-lookup"><span data-stu-id="369fc-116">Attributes</span></span>  
  
|<span data-ttu-id="369fc-117">특성</span><span class="sxs-lookup"><span data-stu-id="369fc-117">Attribute</span></span>|<span data-ttu-id="369fc-118">설명</span><span class="sxs-lookup"><span data-stu-id="369fc-118">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="369fc-119">취소를 요청하는 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-119">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="369fc-120">취소가 요청된 자식 활동의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-120">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="369fc-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="369fc-121">Child elements</span></span>

<span data-ttu-id="369fc-122">없음</span><span class="sxs-lookup"><span data-stu-id="369fc-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="369fc-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="369fc-123">Parent elements</span></span>
  
|<span data-ttu-id="369fc-124">요소</span><span class="sxs-lookup"><span data-stu-id="369fc-124">Element</span></span>|<span data-ttu-id="369fc-125">설명</span><span class="sxs-lookup"><span data-stu-id="369fc-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="369fc-126">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="369fc-126">\<cancelRequestedQueries></span></span>](cancelrequestedqueries-of-wcf.md)|<span data-ttu-id="369fc-127">부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 쿼리의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="369fc-127">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="369fc-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="369fc-128">See also</span></span>  

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CancelRequestedQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CancelRequestedQuery?displayProperty=nameWithType>
- [<span data-ttu-id="369fc-129">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="369fc-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="369fc-130">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="369fc-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
