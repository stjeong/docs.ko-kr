---
title: '&lt;services&gt;의 &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 6bdc4590-aa9c-4ec8-9345-879d780cd141
ms.openlocfilehash: 9a86b7549e0efef10cbeb16dcc427d04065e43d3
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145538"
---
# <a name="ltaddgt-of-ltservicesgt"></a><span data-ttu-id="695c3-102">&lt;services&gt;의 &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="695c3-102">&lt;add&gt; of &lt;services&gt;</span></span>
<span data-ttu-id="695c3-103">인스턴스에 대 한 설정을 지정 <xref:System.Workflow.Runtime.WorkflowRuntime> 호스팅 워크플로 기반 Windows Communication Foundation (WCF) 서비스에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-103">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="695c3-104">이 요소는 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-104">This element is of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  
  
 <span data-ttu-id="695c3-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="695c3-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="695c3-106">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="695c3-106">\<behaviors></span></span>  
<span data-ttu-id="695c3-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="695c3-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="695c3-108">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="695c3-108">\<behavior></span></span>  
<span data-ttu-id="695c3-109">\<services></span><span class="sxs-lookup"><span data-stu-id="695c3-109">\<services></span></span>  
<span data-ttu-id="695c3-110">\<add></span><span class="sxs-lookup"><span data-stu-id="695c3-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="695c3-111">구문</span><span class="sxs-lookup"><span data-stu-id="695c3-111">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <services>
    <add type="String" />
  </services>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="695c3-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="695c3-112">Attributes and Elements</span></span>  
 <span data-ttu-id="695c3-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="695c3-114">특성</span><span class="sxs-lookup"><span data-stu-id="695c3-114">Attributes</span></span>  
  
|<span data-ttu-id="695c3-115">특성</span><span class="sxs-lookup"><span data-stu-id="695c3-115">Attribute</span></span>|<span data-ttu-id="695c3-116">설명</span><span class="sxs-lookup"><span data-stu-id="695c3-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="695c3-117">형식</span><span class="sxs-lookup"><span data-stu-id="695c3-117">type</span></span>|<span data-ttu-id="695c3-118">초기화할 서비스의 정규화된 어셈블리 형식 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-118">A string that specifies the assembly-qualified type name of the service to be initialized.</span></span> <span data-ttu-id="695c3-119">지정된 서비스는 생성자의 시그니처에 대한 특정 규칙을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-119">The service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="695c3-120">자세한 내용은 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="695c3-120">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="695c3-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="695c3-121">Child Elements</span></span>  
 <span data-ttu-id="695c3-122">없음</span><span class="sxs-lookup"><span data-stu-id="695c3-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="695c3-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="695c3-123">Parent Elements</span></span>  
  
|<span data-ttu-id="695c3-124">요소</span><span class="sxs-lookup"><span data-stu-id="695c3-124">Element</span></span>|<span data-ttu-id="695c3-125">설명</span><span class="sxs-lookup"><span data-stu-id="695c3-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="695c3-126">\<services></span><span class="sxs-lookup"><span data-stu-id="695c3-126">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services-of-workflowruntime.md)|<span data-ttu-id="695c3-127"><xref:System.Workflow.Runtime.WorkflowRuntime> 엔진에 추가할 서비스 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-127">A collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="695c3-128">요소는 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-128">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="695c3-129">컬렉션에 지정된 서비스는 워크플로 런타임 엔진에 의해 초기화되며 해당 <xref:System.Workflow.Runtime.WorkflowRuntime> 생성자를 호출할 때 서비스에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-129">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="695c3-130">따라서 컬렉션에 지정된 서비스는 생성자의 시그니처에 대한 특정 규칙을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-130">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="695c3-131">자세한 내용은 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="695c3-131">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="695c3-132">설명</span><span class="sxs-lookup"><span data-stu-id="695c3-132">Remarks</span></span>  
 <span data-ttu-id="695c3-133">이 요소에 지정된 서비스는 워크플로 런타임 엔진에 의해 초기화되며 해당 <xref:System.Workflow.Runtime.WorkflowRuntime> 생성자를 호출할 때 서비스에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-133">The service specified in this element will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="695c3-134">따라서 지정된 서비스는 생성자의 시그니처에 대한 특정 규칙을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="695c3-134">Therefore, the service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="695c3-135">자세한 내용은 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="695c3-135">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="695c3-136">예제</span><span class="sxs-lookup"><span data-stu-id="695c3-136">Example</span></span>  
  
```xml  
<serviceBehaviors>
  <behavior name="ServiceBehavior">
    <workflowRuntime name="WorkflowServiceHostRuntime"
                     validateOnCreate="true"
                     enablePerformanceCounters="true">
      <services>
        <add type="NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common.TestPersistenceService.FilePersistenceService, NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common" />
      </services>
    </workflowRuntime>
  </behavior>
</serviceBehaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="695c3-137">참고 항목</span><span class="sxs-lookup"><span data-stu-id="695c3-137">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>  
 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>  
 <xref:System.Workflow.Runtime.WorkflowRuntime>  
 <span data-ttu-id="695c3-138">[워크플로 구성 파일](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="695c3-138">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
