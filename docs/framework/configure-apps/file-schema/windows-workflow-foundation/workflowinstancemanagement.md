---
title: '&lt;workflowInstanceManagement&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 63ac89ba-c844-4ae2-96ae-cd752a90a109
ms.openlocfilehash: ba3d9415efc21012b470fd2e9a7f426ca8f3aad1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662064"
---
# <a name="ltworkflowinstancemanagementgt"></a><span data-ttu-id="43dc7-102">&lt;workflowInstanceManagement&gt;</span><span class="sxs-lookup"><span data-stu-id="43dc7-102">&lt;workflowInstanceManagement&gt;</span></span>
<span data-ttu-id="43dc7-103">지속성 예외, 처리되지 않은 예외 동작 및 유휴 동작을 비롯하여 워크플로 인스턴스 실행 방법을 제어하는 설정을 지정할 수 있는 서비스 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="43dc7-103">A service behavior that enables you to specify settings that control how workflow instances are run, including persistence, unhandled Exception behavior and idle behavior.</span></span>  
  
<span data-ttu-id="43dc7-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="43dc7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="43dc7-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="43dc7-105">\<behaviors></span></span>  
<span data-ttu-id="43dc7-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="43dc7-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="43dc7-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="43dc7-107">\<behavior></span></span>  
<span data-ttu-id="43dc7-108">\<workflowInstanceManagement></span><span class="sxs-lookup"><span data-stu-id="43dc7-108">\<workflowInstanceManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43dc7-109">구문</span><span class="sxs-lookup"><span data-stu-id="43dc7-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowInstanceManagement authorizedWindowsGroup="" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43dc7-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="43dc7-110">Attributes and Elements</span></span>  
 <span data-ttu-id="43dc7-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="43dc7-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43dc7-112">특성</span><span class="sxs-lookup"><span data-stu-id="43dc7-112">Attributes</span></span>  
  
|<span data-ttu-id="43dc7-113">특성</span><span class="sxs-lookup"><span data-stu-id="43dc7-113">Attribute</span></span>|<span data-ttu-id="43dc7-114">설명</span><span class="sxs-lookup"><span data-stu-id="43dc7-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="43dc7-115">authorizedWindowsGroup</span><span class="sxs-lookup"><span data-stu-id="43dc7-115">authorizedWindowsGroup</span></span>||  
  
### <a name="child-elements"></a><span data-ttu-id="43dc7-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="43dc7-116">Child Elements</span></span>  
 <span data-ttu-id="43dc7-117">없음</span><span class="sxs-lookup"><span data-stu-id="43dc7-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="43dc7-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="43dc7-118">Parent Elements</span></span>  
  
|<span data-ttu-id="43dc7-119">요소</span><span class="sxs-lookup"><span data-stu-id="43dc7-119">Element</span></span>|<span data-ttu-id="43dc7-120">설명</span><span class="sxs-lookup"><span data-stu-id="43dc7-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="43dc7-121">\<동작 >의 \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="43dc7-121">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="43dc7-122">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43dc7-122">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="43dc7-123">참고자료</span><span class="sxs-lookup"><span data-stu-id="43dc7-123">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.WorkflowInstanceManagementBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowInstanceManagementElement>
