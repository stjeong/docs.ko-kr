---
title: '&lt;variable&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 46cc8cbc-10ec-4625-8813-3f5cd6c6afde
ms.openlocfilehash: 185e7e7196f6679ec3d1fae8a2a256b934022ca9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647883"
---
# <a name="ltvariablegt"></a><span data-ttu-id="1588e-102">&lt;variable&gt;</span><span class="sxs-lookup"><span data-stu-id="1588e-102">&lt;variable&gt;</span></span>
<span data-ttu-id="1588e-103">이 활동 쿼리와 연결된 변수의 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-103">Represents a collection of variables associated with this activity query.</span></span>  
  
 <span data-ttu-id="1588e-104">추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="1588e-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="1588e-105">\<system.serviceModel></span></span>  
<span data-ttu-id="1588e-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="1588e-106">\<tracking></span></span>  
<span data-ttu-id="1588e-107">\<profiles></span><span class="sxs-lookup"><span data-stu-id="1588e-107">\<profiles></span></span>  
<span data-ttu-id="1588e-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="1588e-108">\<trackingProfile></span></span>  
<span data-ttu-id="1588e-109">\<workflow></span><span class="sxs-lookup"><span data-stu-id="1588e-109">\<workflow></span></span>  
<span data-ttu-id="1588e-110">\<activityStateQueries></span><span class="sxs-lookup"><span data-stu-id="1588e-110">\<activityStateQueries></span></span>  
<span data-ttu-id="1588e-111">\<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="1588e-111">\<activityStateQuery></span></span>  
<span data-ttu-id="1588e-112">\<variables></span><span class="sxs-lookup"><span data-stu-id="1588e-112">\<variables></span></span>  
<span data-ttu-id="1588e-113">\<variable></span><span class="sxs-lookup"><span data-stu-id="1588e-113">\<variable></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1588e-114">구문</span><span class="sxs-lookup"><span data-stu-id="1588e-114">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <variables>
          <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1588e-115">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="1588e-115">Attributes and Elements</span></span>  
 <span data-ttu-id="1588e-116">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-116">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1588e-117">특성</span><span class="sxs-lookup"><span data-stu-id="1588e-117">Attributes</span></span>  
  
|<span data-ttu-id="1588e-118">특성</span><span class="sxs-lookup"><span data-stu-id="1588e-118">Attribute</span></span>|<span data-ttu-id="1588e-119">설명</span><span class="sxs-lookup"><span data-stu-id="1588e-119">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1588e-120">name</span><span class="sxs-lookup"><span data-stu-id="1588e-120">name</span></span>|<span data-ttu-id="1588e-121">변수의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-121">A string that specifies the name of the variable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1588e-122">자식 요소</span><span class="sxs-lookup"><span data-stu-id="1588e-122">Child Elements</span></span>  
 <span data-ttu-id="1588e-123">없음</span><span class="sxs-lookup"><span data-stu-id="1588e-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1588e-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="1588e-124">Parent Elements</span></span>  
  
|<span data-ttu-id="1588e-125">요소</span><span class="sxs-lookup"><span data-stu-id="1588e-125">Element</span></span>|<span data-ttu-id="1588e-126">설명</span><span class="sxs-lookup"><span data-stu-id="1588e-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1588e-127">\<variable></span><span class="sxs-lookup"><span data-stu-id="1588e-127">\<variable></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/variable.md)|<span data-ttu-id="1588e-128">활동 상태 쿼리와 연결되는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-128">A variable associated with an activity state query.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1588e-129">설명</span><span class="sxs-lookup"><span data-stu-id="1588e-129">Remarks</span></span>  
 <span data-ttu-id="1588e-130">ActivityStateQuery의 한 가지 고유한 특징은 워크플로 실행을 추적할 때 데이터를 추출하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-130">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="1588e-131">이 기능은 추적 레코드 사후 실행에 액세스할 때 추가 컨텍스트를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-131">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="1588e-132">사용할 수는 [ \<인수 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)를 [ \<상태 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) 고 [ \<상태 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) 변수 또는 인수를 추출 하는 요소 워크플로의 모든 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-132">You can use the [\<arguments>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md), [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) and [\<states>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="1588e-133">다음 예제에서는 활동의 `Closed` 추적 레코드를 내보낼 때 변수와 인수를 추출하는 활동 상태 쿼리를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-133">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="1588e-134">ActivityStateRecord 사용해 서만 추출할 수 있으므로 구독 하는 추적 내에서 변수 및 인수를 사용 하 여 프로 파일링 [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="1588e-134">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md).</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1588e-135">참고자료</span><span class="sxs-lookup"><span data-stu-id="1588e-135">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.VariableElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="1588e-136">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="1588e-136">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="1588e-137">추적 프로필</span><span class="sxs-lookup"><span data-stu-id="1588e-137">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
