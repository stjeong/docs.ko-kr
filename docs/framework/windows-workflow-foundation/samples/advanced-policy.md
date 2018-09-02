---
title: Advanced Policy
ms.date: 03/30/2017
ms.assetid: 75a22c88-5e54-4ae8-84cb-fbb22a612f0a
ms.openlocfilehash: becdc28affd877239474d6f0f007a480297bccb8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43387891"
---
# <a name="advanced-policy"></a><span data-ttu-id="acc43-102">Advanced Policy</span><span class="sxs-lookup"><span data-stu-id="acc43-102">Advanced Policy</span></span>
<span data-ttu-id="acc43-103">이 샘플은 Simple Policy 샘플의 확장입니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-103">This sample extends the Simple Policy sample.</span></span> <span data-ttu-id="acc43-104">Simple Policy 예제의 가계 할인 규칙과 기업 할인 규칙 이외에 새로운 규칙이 몇 가지 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-104">In addition to the residential discount and business discount rules from the Simple Policy example, several new rules have been added.</span></span>  
  
 <span data-ttu-id="acc43-105">첫째, 고가치 규칙이 추가되어 값이 큰 주문에 대해 더 큰 할인을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-105">A high-value rule is added, which provides a bigger discount for high-value orders.</span></span> <span data-ttu-id="acc43-106">이 규칙은 할인 필드를 덮어쓰고 가계 할인 규칙과 기업 할인 규칙보다 우선적으로 적용되도록 이전 두 규칙보다 작은 우선 순위 값이 부여되었습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-106">It is given a priority value less than the previous two rules so that it will overwrite the discount field and take precedence over both the residential and business discount rules.</span></span>  
  
 <span data-ttu-id="acc43-107">둘째, 합계 계산 규칙이 추가되어 할인 수준을 기반으로 합계를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-107">A calculate total rule is also added, which computes the total based on the discount level.</span></span> <span data-ttu-id="acc43-108">워크플로 활동에 정의된 메서드를 참조하는 방법과 Else 작업 사용 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-108">It shows how to reference a method defined on the workflow activity, as well as how to use else actions.</span></span> <span data-ttu-id="acc43-109">이 규칙은 할인 필드가 변경될 때마다 확인되는 연결 동작을 보여 주기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-109">This rule also demonstrates chaining behavior since it will be evaluated anytime the discount field changes.</span></span> <span data-ttu-id="acc43-110">뿐만 아니라 CalculateTotal 메서드의 RuleWriteAttribute를 사용하여 메서드 특성 지정도 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-110">Furthermore, method attributing is shown with the RuleWriteAttribute on the CalculateTotal method.</span></span> <span data-ttu-id="acc43-111">이로 인해 이 규칙의 영향을 받는 규칙(ErrorTotalRule)은 메서드가 실행될 때마다 재확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-111">This causes impacted rules (ErrorTotalRule) to be re-evaluated whenever the method gets executed.</span></span>  
  
 <span data-ttu-id="acc43-112">셋째, 오류를 감지하는 규칙이 추가되었습니다(이 경우에는 합계가 0보다 작을 때).</span><span class="sxs-lookup"><span data-stu-id="acc43-112">The last rule added is one that detects errors (in this case, Total less than 0).</span></span> <span data-ttu-id="acc43-113">오류가 감지되면 정책 실행이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-113">If this occurs, the policy execution is halted.</span></span>  
  
 <span data-ttu-id="acc43-114">이러한 규칙 추가 외에도, 각 규칙에 `Console.Writeline` 호출이 작업으로 추가되어 규칙 실행 상황을 보기 쉬울 뿐만 아니라 참조된 형식의 정적 메서드에 액세스할 수 있음을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-114">Finally, `Console.Writeline` calls are added as actions to each rule to provide more visibility into rule execution, while also showing that it is possible to access static methods on referenced types.</span></span> <span data-ttu-id="acc43-115">사용자는 추적을 사용하여 실행된 규칙을 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-115">You could also use tracking to get visibility into the rules that are executed.</span></span>  
  
 <span data-ttu-id="acc43-116">이 샘플에 사용된 규칙은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-116">The rules used in this sample are:</span></span>  
  
 <span data-ttu-id="acc43-117">**ResidentialDiscountRule:**</span><span class="sxs-lookup"><span data-stu-id="acc43-117">**ResidentialDiscountRule:**</span></span>  
  
 <span data-ttu-id="acc43-118">IF OrderValue > 500 AND CustomerType = Residential</span><span class="sxs-lookup"><span data-stu-id="acc43-118">IF OrderValue > 500 AND CustomerType = Residential</span></span>  
  
 <span data-ttu-id="acc43-119">THEN Discount = 5%</span><span class="sxs-lookup"><span data-stu-id="acc43-119">THEN Discount = 5%</span></span>  
  
 <span data-ttu-id="acc43-120">**BusinessDiscountRule:**</span><span class="sxs-lookup"><span data-stu-id="acc43-120">**BusinessDiscountRule:**</span></span>  
  
 <span data-ttu-id="acc43-121">IF OrderValue > 10000 AND CustomerType = Business</span><span class="sxs-lookup"><span data-stu-id="acc43-121">IF OrderValue > 10000 AND CustomerType = Business</span></span>  
  
 <span data-ttu-id="acc43-122">THEN Discount = 10%</span><span class="sxs-lookup"><span data-stu-id="acc43-122">THEN Discount = 10%</span></span>  
  
 <span data-ttu-id="acc43-123">**HighValueDiscountRule:**</span><span class="sxs-lookup"><span data-stu-id="acc43-123">**HighValueDiscountRule:**</span></span>  
  
 <span data-ttu-id="acc43-124">IF OrderValue > 20000</span><span class="sxs-lookup"><span data-stu-id="acc43-124">IF OrderValue > 20000</span></span>  
  
 <span data-ttu-id="acc43-125">THEN Discount = 15%</span><span class="sxs-lookup"><span data-stu-id="acc43-125">THEN Discount = 15%</span></span>  
  
 <span data-ttu-id="acc43-126">**TotalRule:**</span><span class="sxs-lookup"><span data-stu-id="acc43-126">**TotalRule:**</span></span>  
  
 <span data-ttu-id="acc43-127">IF Discount > 0</span><span class="sxs-lookup"><span data-stu-id="acc43-127">IF Discount > 0</span></span>  
  
 <span data-ttu-id="acc43-128">THEN CalculateTotal(OrderValue, Discount)</span><span class="sxs-lookup"><span data-stu-id="acc43-128">THEN CalculateTotal(OrderValue, Discount)</span></span>  
  
 <span data-ttu-id="acc43-129">ELSE Total = OrderValue</span><span class="sxs-lookup"><span data-stu-id="acc43-129">ELSE Total = OrderValue</span></span>  
  
 <span data-ttu-id="acc43-130">**Errortotalrule은:**</span><span class="sxs-lookup"><span data-stu-id="acc43-130">**ErrorTotalRule:**</span></span>  
  
 <span data-ttu-id="acc43-131">경우에 총 \< 0</span><span class="sxs-lookup"><span data-stu-id="acc43-131">IF Total \< 0</span></span>  
  
 <span data-ttu-id="acc43-132">THEN Error = "Fired ErrorTotalRule"; Halt</span><span class="sxs-lookup"><span data-stu-id="acc43-132">THEN Error = "Fired ErrorTotalRule"; Halt</span></span>  
  
 <span data-ttu-id="acc43-133">규칙 확인 및 실행은 추적을 통해서도 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-133">Rule evaluation and execution can also be seen through tracing and tracking.</span></span>  
  
### <a name="to-build-the-sample"></a><span data-ttu-id="acc43-134">이 샘플을 빌드하려면</span><span class="sxs-lookup"><span data-stu-id="acc43-134">To build the sample</span></span>  
  
1.  <span data-ttu-id="acc43-135">[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]에서 솔루션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-135">Open the solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="acc43-136">Ctrl+Shift+B를 눌러 솔루션을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-136">Build the solution by pressing CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="acc43-137">Ctrl+F5를 눌러 디버깅 없이 솔루션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-137">Run the solution without debugging by pressing CTRL+F5.</span></span>  
  
### <a name="to-run-the-sample"></a><span data-ttu-id="acc43-138">이 샘플을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="acc43-138">To run the sample</span></span>  
  
-   <span data-ttu-id="acc43-139">SDK 명령 프롬프트 창에서 샘플의 주 폴더 아래에 있는 AdvancedPolicy\bin\debug 폴더 또는 AdvancedPolicy\bin 폴더(Visual Basic 버전 샘플의 경우)의 .exe 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-139">In the SDK Command Prompt window, run the .exe file in the AdvancedPolicy\bin\debug folder (or the AdvancedPolicy \bin folder for the Visual Basic version of the sample), which is located below the main folder for the sample.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="acc43-140">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-140">The samples may already be installed on your computer.</span></span> <span data-ttu-id="acc43-141">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="acc43-141">Check for the following (default) directory before continuing:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="acc43-142">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="acc43-142">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="acc43-143">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acc43-143">This sample is located in the following directory:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Rules\Policy\AdvancedPolicy`  
  
## <a name="see-also"></a><span data-ttu-id="acc43-144">참고 항목</span><span class="sxs-lookup"><span data-stu-id="acc43-144">See Also</span></span>  
 <xref:System.Workflow.Activities.Rules.RuleSet>  
 <xref:System.Workflow.Activities.PolicyActivity>  
 [<span data-ttu-id="acc43-145">단순 정책</span><span class="sxs-lookup"><span data-stu-id="acc43-145">Simple Policy</span></span>](../../../../docs/framework/windows-workflow-foundation/samples/simple-policy.md)
