---
title: CommentOut 활동
ms.date: 03/30/2017
ms.assetid: 340204c3-f827-45fb-870e-55e2ac457ca5
ms.openlocfilehash: 3e9f6945755bd60c551674ea8a3471a9f612da52
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43404752"
---
# <a name="commentout-activity"></a><span data-ttu-id="0e2f8-102">CommentOut 활동</span><span class="sxs-lookup"><span data-stu-id="0e2f8-102">CommentOut Activity</span></span>
<span data-ttu-id="0e2f8-103">이 샘플에서는 다른 활동을 사실상 주석으로 처리하여 실행 경로에서 제거하는 사용자 지정 활동을 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-103">This sample demonstrates how to write a custom activity that removes other activities from the path of execution, effectively commenting them out.</span></span>  
  
## <a name="the-commentout-activity"></a><span data-ttu-id="0e2f8-104">CommentOut 활동</span><span class="sxs-lookup"><span data-stu-id="0e2f8-104">The CommentOut Activity</span></span>  
 <span data-ttu-id="0e2f8-105">목표를 달성하기 위해 CommentOut 활동은 <xref:System.Activities.CodeActivity> 기본 클래스에서 파생되며 빈 <xref:System.Activities.CodeActivity.Execute%2A> 메서드를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-105">To achieve its goal, the CommentOut activity derives from the <xref:System.Activities.CodeActivity> base class and implements an empty <xref:System.Activities.CodeActivity.Execute%2A> method.</span></span>  
  
```  
protected override void Execute(CodeActivityContext context)  
{  
}  
```  
  
 <span data-ttu-id="0e2f8-106">다음 예제와 같이 클래스를 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-106">The class is declared as shown in the following example.</span></span>  
  
```  
[Designer(typeof(CommentOutDesigner))]  
[ContentProperty("Body")]  
public sealed class CommentOut : CodeActivity  
```  
  
 <span data-ttu-id="0e2f8-107">`Designer` 특성은 디자인 타임에 활동의 시각적 인터페이스를 구현하는 클래스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-107">The `Designer` attribute specifies the class that implements the visual interface of the activity at design time.</span></span> <span data-ttu-id="0e2f8-108">`ContentProperty` 특성은 이 활동의 인스턴스에 대한 XAML 표현에서 `"Body"` 속성을 건너뛸 수 있다고 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-108">The `ContentProperty` attribute declares that the `"Body"` property can be skipped in the XAML representation of an instance of this activity.</span></span>  
  
```  
<Border x:Uid="Border_1" BorderThickness ="1">  
    <sad:WorkflowItemPresenter   
    x:Uid="sad:WorkflowItemPresenter_1" AutomationProperties.AutomationId="Body" Item="{Binding Path=ModelItem.Body, Mode=TwoWay}"  
    AllowedItemType="{x:Type sa:Activity}"  
    HintText="Drop activity here"   
    Margin="5,5,5,5" />  
</Border>  
```  
  
 <span data-ttu-id="0e2f8-109">디자이너 클래스에서 XAML은 활동의 사용자 지정 시각적 표현을 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-109">In the designer class, XAML is used to create a custom visual representation of the activity.</span></span> <span data-ttu-id="0e2f8-110"><xref:System.Activities.Presentation.WorkflowItemPresenter>는 시각적 편집기를 제공하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-110"><xref:System.Activities.Presentation.WorkflowItemPresenter> is a class that provides the visual editor.</span></span>  
  
 <span data-ttu-id="0e2f8-111">단일 활동을 `CommentOut` 활동 화면에 끌어 놓을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-111">A single activity can be dropped onto the `CommentOut` activity surface.</span></span> <span data-ttu-id="0e2f8-112">이 화면에 여러 활동을 추가하려면 먼저 Sequence 활동을 여기에 끌어 옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-112">If you want to add multiple activities to this surface, drag a sequence activity here first.</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="0e2f8-113">이 샘플을 사용하려면</span><span class="sxs-lookup"><span data-stu-id="0e2f8-113">To use this sample</span></span>  
  
1.  <span data-ttu-id="0e2f8-114">[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]에서 CommentOut.sln을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-114">Open CommentOut.sln in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="0e2f8-115">Ctrl+Shift+B를 눌러 솔루션을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-115">Compile the solution by pressing CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="0e2f8-116">Ctrl+F5를 눌러 디버깅 없이 샘플을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-116">Start the sample without debugging by pressing CTRL+F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="0e2f8-117">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-117">The samples may already be installed on your machine.</span></span> <span data-ttu-id="0e2f8-118">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-118">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="0e2f8-119">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-119">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="0e2f8-120">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e2f8-120">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\CommentOut`
