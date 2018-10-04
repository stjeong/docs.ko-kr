---
title: Throttled Parallel ForEach
ms.date: 03/30/2017
ms.assetid: f2855b5f-e9a7-433d-96a4-40fc31025215
ms.openlocfilehash: 8691edb8a5a61204b187be8def553f2f06be0f0d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48581864"
---
# <a name="throttled-parallel-foreach"></a><span data-ttu-id="1e7a0-102">Throttled Parallel ForEach</span><span class="sxs-lookup"><span data-stu-id="1e7a0-102">Throttled Parallel ForEach</span></span>
<span data-ttu-id="1e7a0-103">합니다 `ThrottleParallelForEach` 작업이 비슷합니다는 <!--zz <xref:System.Activities.Statements.ParallelForEach>--> `System.Activities.Statements.ParallelForEach` 한 가지 예외를 사용 하 여 작업을 설정할 수 있습니다는 동시 비율을 실행할 동시 분기 수를 제한할 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-103">The `ThrottleParallelForEach` activity is similar to the <!--zz <xref:System.Activities.Statements.ParallelForEach>--> `System.Activities.Statements.ParallelForEach` activity with the one exception that it allows setting a concurrency factor to restrict the number of simultaneous branches to execute.</span></span> <span data-ttu-id="1e7a0-104">`ThrottleParallelForEach` 활동은 다른 활동(자식 활동)을 예약해야 하고 <xref:System.Activities.NativeActivity> 클래스를 통해서만 액세스 가능하기 때문에 <xref:System.Activities.NativeActivityContext>에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-104">The `ThrottleParallelForEach` activity derives from <xref:System.Activities.NativeActivity>, because it needs to schedule other activities (the child activities) and this is only accessible through the <xref:System.Activities.NativeActivityContext> class.</span></span>

## <a name="projects"></a><span data-ttu-id="1e7a0-105">프로젝트</span><span class="sxs-lookup"><span data-stu-id="1e7a0-105">Projects</span></span>

|<span data-ttu-id="1e7a0-106">**ProjectName**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-106">**ProjectName**</span></span>|<span data-ttu-id="1e7a0-107">**설명**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-107">**Description**</span></span>|<span data-ttu-id="1e7a0-108">**기본 파일**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-108">**Main Files**</span></span>|
|-|-|-|
|<span data-ttu-id="1e7a0-109">ThrottledParallelForEach</span><span class="sxs-lookup"><span data-stu-id="1e7a0-109">ThrottledParallelForEach</span></span>|<span data-ttu-id="1e7a0-110">`ThrottledParallelForEach` 활동과 이 활동의 디자이너가 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-110">Contains `ThrottledParallelForEach` activity and its designer.</span></span>|<span data-ttu-id="1e7a0-111">ThrottledParallelForEach.cs</span><span class="sxs-lookup"><span data-stu-id="1e7a0-111">ThrottledParallelForEach.cs</span></span><br /><br /> <span data-ttu-id="1e7a0-112">`ThrottledParallelForEach` 활동 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-112">The `ThrottledParallelForEach` activity definition.</span></span>|
|<span data-ttu-id="1e7a0-113">CodeTestClient</span><span class="sxs-lookup"><span data-stu-id="1e7a0-113">CodeTestClient</span></span>|<span data-ttu-id="1e7a0-114">명령적 코드를 사용하여 `ThrottledParallelForEach`가 있는 워크플로를 구성 및 실행하는 샘플 클라이언트 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-114">Sample client application that configures and runs a workflow with a `ThrottledParallelForEach` using imperative code.</span></span>|<span data-ttu-id="1e7a0-115">Program.cs</span><span class="sxs-lookup"><span data-stu-id="1e7a0-115">Program.cs</span></span><br /><br /> <span data-ttu-id="1e7a0-116">샘플 워크플로의 인스턴스를 정의하고 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-116">Defines and runs an instance of the sample workflow.</span></span>|

#### <a name="to-use-this-sample"></a><span data-ttu-id="1e7a0-117">이 샘플을 사용하려면</span><span class="sxs-lookup"><span data-stu-id="1e7a0-117">To use this sample</span></span>

1.  <span data-ttu-id="1e7a0-118">Visual Studio 2010을 사용 하 여 ThrottledParallelForEach.sln 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-118">Using Visual Studio 2010, open the ThrottledParallelForEach.sln file.</span></span>

2.  <span data-ttu-id="1e7a0-119">Ctrl+Shift+B를 눌러 솔루션을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-119">To build the solution, press CTRL+SHIFT+B.</span></span>

3.  <span data-ttu-id="1e7a0-120">F5 키를 눌러 솔루션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-120">To run the solution, press F5.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="1e7a0-121">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-121">The samples may already be installed on your machine.</span></span> <span data-ttu-id="1e7a0-122">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-122">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="1e7a0-123">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-123">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="1e7a0-124">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-124">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\ThrottledParallelForEach`