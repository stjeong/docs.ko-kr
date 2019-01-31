---
title: <etwTracking>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: cb45c82e-6ea1-4c4d-924c-118a25ae1f35
ms.openlocfilehash: 12589ab7c6cb65618a5f53a3e4be49d85a2ffbb7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277202"
---
# <a name="etwtracking"></a><span data-ttu-id="b6ef7-101">\<etwTracking></span><span class="sxs-lookup"><span data-stu-id="b6ef7-101">\<etwTracking></span></span>
<span data-ttu-id="b6ef7-102">서비스가 <xref:System.Activities.Tracking.EtwTrackingParticipant>를 통해 ETW 추적을 사용할 수 있도록 하는 서비스 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-102">A service behavior that allows a service to utilize ETW tracking using an <xref:System.Activities.Tracking.EtwTrackingParticipant>.</span></span>  
  
<span data-ttu-id="b6ef7-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b6ef7-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="b6ef7-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="b6ef7-104">\<behaviors></span></span>  
<span data-ttu-id="b6ef7-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="b6ef7-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="b6ef7-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="b6ef7-106">\<behavior></span></span>  
<span data-ttu-id="b6ef7-107">\<etwTracking></span><span class="sxs-lookup"><span data-stu-id="b6ef7-107">\<etwTracking></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6ef7-108">구문</span><span class="sxs-lookup"><span data-stu-id="b6ef7-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <etwTracking profileName="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b6ef7-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="b6ef7-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b6ef7-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b6ef7-111">특성</span><span class="sxs-lookup"><span data-stu-id="b6ef7-111">Attributes</span></span>  
  
|<span data-ttu-id="b6ef7-112">특성</span><span class="sxs-lookup"><span data-stu-id="b6ef7-112">Attribute</span></span>|<span data-ttu-id="b6ef7-113">설명</span><span class="sxs-lookup"><span data-stu-id="b6ef7-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b6ef7-114">profileName</span><span class="sxs-lookup"><span data-stu-id="b6ef7-114">profileName</span></span>|<span data-ttu-id="b6ef7-115">이 동작과 연결된 추적 프로필의 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-115">A string that specifies the name of the tracking profile associated with this behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b6ef7-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="b6ef7-116">Child Elements</span></span>  
 <span data-ttu-id="b6ef7-117">없음</span><span class="sxs-lookup"><span data-stu-id="b6ef7-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b6ef7-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="b6ef7-118">Parent Elements</span></span>  
  
|<span data-ttu-id="b6ef7-119">요소</span><span class="sxs-lookup"><span data-stu-id="b6ef7-119">Element</span></span>|<span data-ttu-id="b6ef7-120">설명</span><span class="sxs-lookup"><span data-stu-id="b6ef7-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b6ef7-121">\<동작 >의 \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="b6ef7-121">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="b6ef7-122">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-122">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b6ef7-123">설명</span><span class="sxs-lookup"><span data-stu-id="b6ef7-123">Remarks</span></span>  
 <span data-ttu-id="b6ef7-124">이 구성 요소를 서비스의 동작 구성에 추가하는 경우 워크플로 서비스에서 추적 참가자를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-124">When added to the service’s behavior configuration, this configuration element configures a tracking participant on a workflow service.</span></span>  
  
 <span data-ttu-id="b6ef7-125">추적 참가자는 워크플로에서 내보내지는 추적 데이터를 가져오고 이 데이터를 다른 미디어에 저장하기 위해 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-125">Tracking participants are used to get the tracking data emitted from the workflow and store it into different mediums.</span></span> <span data-ttu-id="b6ef7-126">마찬가지로 추적 레코드에 대한 모든 사후 처리를 추적 참가자 내에서 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-126">Likewise, any post processing on the tracking Records can also be done within the tracking participant.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b6ef7-127">예제</span><span class="sxs-lookup"><span data-stu-id="b6ef7-127">Example</span></span>  
 <span data-ttu-id="b6ef7-128">다음 구성 예제에서는 Web.config 파일에서 구성되는 표준 ETW 추적 참가자를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-128">The following configuration example shows the standard ETW tracking participant being configured in the Web.config file.</span></span>  
  
 <span data-ttu-id="b6ef7-129">에 정의 된 ETW 추적 참가자가 ETW에 추적 레코드를 쓰기 위해 사용 하는 공급자 Id를  **\<진단 >** 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-129">The Provider Id that the ETW Tracking Participant uses for writing the Tracking Records to ETW is defined in the **\<diagnostics>** section.</span></span> <span data-ttu-id="b6ef7-130">추적 참가자에는 구독하는 추적 레코드를 지정하기 위해 연결된 프로필이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-130">The tracking participant has a profile associated with it to specify the tracking records it has subscribed to.</span></span> <span data-ttu-id="b6ef7-131">이 정의한 합니다 **profileName** 특성을  **\<추가 >** 요소.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-131">This is defined by the **profileName** attribute of the **\<add>** element.</span></span> <span data-ttu-id="b6ef7-132">추적 참가자가 정의 되 면 추가할 합니다  **\<etwTracking >** 서비스 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-132">Once these are defined, the Tracking Participant is added to the **\<etwTracking>** service behavior.</span></span> <span data-ttu-id="b6ef7-133">이렇게 하면 선택된 추적 참가자가 워크플로 인스턴스의 확장에 추가되어 추적 레코드를 받기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ef7-133">This will add the selected Tracking Participants to the Workflow instance’s extensions, so that they begin to receive the Tracking Records.</span></span>  
  
```xml  
<configuration>   
  <system.web>   
    <compilation targetFrameworkMoniker=".NETFramework,Version=v4.0"/>   
  </system.web>   
  <system.serviceModel>   
    <diagnostics etwProviderId="52A3165D-4AD9-405C-B1E8-7D9A257EAC9F" />                
    <tracking>   
      <participants>   
        <add name="EtwTrackingParticipant"   
             type="System.Activities.Tracking.EtwTrackingParticipant, System.Activities, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"   
             profileName="HealthMonitoring_Tracking_Profile"/>   
      </participants>   
    </tracking>   
    <behaviors>   
      <serviceBehaviors>   
        <behavior>   
          <etwTracking profileName="Sample Tracking Profile"/>  
        </behavior>   
      </serviceBehaviors>   
    </behaviors>   
  </system.serviceModel>   
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b6ef7-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="b6ef7-134">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior>
- <xref:System.ServiceModel.Activities.Configuration.EtwTrackingBehaviorElement>
- [<span data-ttu-id="b6ef7-135">워크플로 추적</span><span class="sxs-lookup"><span data-stu-id="b6ef7-135">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="b6ef7-136">추적 참가자</span><span class="sxs-lookup"><span data-stu-id="b6ef7-136">Tracking Participants</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md)
