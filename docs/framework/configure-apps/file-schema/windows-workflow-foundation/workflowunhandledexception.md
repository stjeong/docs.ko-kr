---
title: '&lt;workflowUnhandledException&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 57adeab5-f06a-44b2-916b-0e177cf0f4a6
ms.openlocfilehash: 5c5dddc6d126811d7fd1eaae2f85df1e42c1cd41
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700873"
---
# <a name="ltworkflowunhandledexceptiongt"></a><span data-ttu-id="884ce-102">&lt;workflowUnhandledException&gt;</span><span class="sxs-lookup"><span data-stu-id="884ce-102">&lt;workflowUnhandledException&gt;</span></span>
<span data-ttu-id="884ce-103">워크플로 서비스 내에서 처리되지 않은 예외가 발생할 때 수행할 동작을 지정할 수 있는 서비스 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="884ce-103">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>  
  
<span data-ttu-id="884ce-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="884ce-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="884ce-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="884ce-105">\<behaviors></span></span>  
<span data-ttu-id="884ce-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="884ce-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="884ce-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="884ce-107">\<behavior></span></span>  
<span data-ttu-id="884ce-108">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="884ce-108">\<workflowUnhandledException></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="884ce-109">구문</span><span class="sxs-lookup"><span data-stu-id="884ce-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="884ce-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="884ce-110">Attributes and Elements</span></span>  
 <span data-ttu-id="884ce-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="884ce-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="884ce-112">특성</span><span class="sxs-lookup"><span data-stu-id="884ce-112">Attributes</span></span>  
  
|<span data-ttu-id="884ce-113">특성</span><span class="sxs-lookup"><span data-stu-id="884ce-113">Attribute</span></span>|<span data-ttu-id="884ce-114">설명</span><span class="sxs-lookup"><span data-stu-id="884ce-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="884ce-115">action</span><span class="sxs-lookup"><span data-stu-id="884ce-115">action</span></span>|<span data-ttu-id="884ce-116">처리되지 않은 예외가 발생했을 때 수행할 동작을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="884ce-116">A string that specifies the action to take when an unhandled exception occurs.</span></span> <span data-ttu-id="884ce-117">이 특성은 <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="884ce-117">This attribute is of type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="884ce-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="884ce-118">Child Elements</span></span>  
 <span data-ttu-id="884ce-119">없음</span><span class="sxs-lookup"><span data-stu-id="884ce-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="884ce-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="884ce-120">Parent Elements</span></span>  
  
|<span data-ttu-id="884ce-121">요소</span><span class="sxs-lookup"><span data-stu-id="884ce-121">Element</span></span>|<span data-ttu-id="884ce-122">설명</span><span class="sxs-lookup"><span data-stu-id="884ce-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="884ce-123">\<동작 >의 \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="884ce-123">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="884ce-124">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="884ce-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="884ce-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="884ce-125">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowUnhandledExceptionElement>
