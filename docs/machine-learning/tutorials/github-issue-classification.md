---
title: GitHub 문제 다중 클래스 분류 시나리오에서 ML.NET 사용
description: 다중 클래스 분류 시나리오에서 ML.NET을 사용하여 GitHub 문제를 분류하여 지정된 영역에 할당하는 방법을 알아봅니다.
ms.date: 01/24/2019
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: a951e884a7494b0dcc808fc3dafbfadebc5577dc
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254992"
---
# <a name="tutorial-use-mlnet-in-a-multiclass-classification-scenario-to-classify-github-issues"></a><span data-ttu-id="272fa-103">자습서: 다중 클래스 분류 시나리오에서 ML.NET을 사용하여 GitHub 문제를 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-103">Tutorial: Use ML.NET in a multiclass classification scenario to classify GitHub issues.</span></span>

<span data-ttu-id="272fa-104">이 샘플 자습서에서는 ML.NET을 사용하여 Visual Studio 2017에서 C#을 사용하는 .NET Core 콘솔 애플리케이션을 통해 GitHub 문제 분류자를 만드는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-104">This sample tutorial illustrates using ML.NET to create a GitHub issue classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="272fa-105">이 자습서에서는 다음과 같은 작업을 수행하는 방법을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-105">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="272fa-106">문제 이해</span><span class="sxs-lookup"><span data-stu-id="272fa-106">Understand the problem</span></span>
> * <span data-ttu-id="272fa-107">적절한 기계 학습 작업 선택</span><span class="sxs-lookup"><span data-stu-id="272fa-107">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="272fa-108">데이터 준비</span><span class="sxs-lookup"><span data-stu-id="272fa-108">Prepare your data</span></span>
> * <span data-ttu-id="272fa-109">학습 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="272fa-109">Create the learning pipeline</span></span>
> * <span data-ttu-id="272fa-110">분류자 로드</span><span class="sxs-lookup"><span data-stu-id="272fa-110">Load a classifier</span></span>
> * <span data-ttu-id="272fa-111">모델 학습</span><span class="sxs-lookup"><span data-stu-id="272fa-111">Train the model</span></span>
> * <span data-ttu-id="272fa-112">다른 데이터 세트를 사용하여 모델 평가</span><span class="sxs-lookup"><span data-stu-id="272fa-112">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="272fa-113">모델을 사용하여 테스트 데이터 결과의 단일 인스턴스 예측</span><span class="sxs-lookup"><span data-stu-id="272fa-113">Predict a single instance of test data outcome with the model</span></span>
> * <span data-ttu-id="272fa-114">로드된 모델을 사용하여 테스트 데이터 결과 예측</span><span class="sxs-lookup"><span data-stu-id="272fa-114">Predict the test data outcomes with a loaded model</span></span>

> [!NOTE]
> <span data-ttu-id="272fa-115">이 항목은 현재 미리 보기로 제공되는 ML.NET을 참조하며, 자료는 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-115">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="272fa-116">자세한 내용은 [ML.NET 소개](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="272fa-116">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

## <a name="github-issue-sample-overview"></a><span data-ttu-id="272fa-117">GitHub 문제 샘플 개요</span><span class="sxs-lookup"><span data-stu-id="272fa-117">GitHub issue sample overview</span></span>

<span data-ttu-id="272fa-118">샘플은 ML.NET을 사용하여 GitHub 문제에 대한 영역 레이블을 분류하고 예측하는 모델을 학습시키는 콘솔 앱입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-118">The sample is a console app that uses ML.NET to train a model that classifies and predicts the Area label for a GitHub issue.</span></span> <span data-ttu-id="272fa-119">또한 품질 분석을 위해 두 번째 데이터 세트를 사용하여 모델을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-119">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="272fa-120">문제 데이터 세트는 dotnet/corefx GitHub 리포지토리에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-120">The issue datasets are from the dotnet/corefx GitHub repo.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="272fa-121">전제 조건</span><span class="sxs-lookup"><span data-stu-id="272fa-121">Prerequisites</span></span>

* <span data-ttu-id="272fa-122">“.NET Core 플랫폼 간 개발” 워크로드가 설치된 [Visual Studio 2017 15.6 이상](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).</span><span class="sxs-lookup"><span data-stu-id="272fa-122">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="272fa-123">[Github에서 탭 분리 파일(issues_train.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv)을 발행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-123">The [Github issues tab separated file (issues_train.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).</span></span>
* <span data-ttu-id="272fa-124">[Github에서 테스트 탭 분리 파일(issues_test.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv)을 발행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-124">The [Github issues test tab separated file (issues_test.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="272fa-125">기계 학습 워크플로</span><span class="sxs-lookup"><span data-stu-id="272fa-125">Machine learning workflow</span></span>

<span data-ttu-id="272fa-126">이 자습서는 프로세스가 체계적으로 이동할 수 있도록 하는 기계 학습 워크플로를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-126">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="272fa-127">워크플로 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-127">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="272fa-128">**문제 이해**</span><span class="sxs-lookup"><span data-stu-id="272fa-128">**Understand the problem**</span></span>
2. <span data-ttu-id="272fa-129">**데이터 준비**</span><span class="sxs-lookup"><span data-stu-id="272fa-129">**Prepare your data**</span></span>
   * <span data-ttu-id="272fa-130">**데이터 로드**</span><span class="sxs-lookup"><span data-stu-id="272fa-130">**Load the data**</span></span>
   * <span data-ttu-id="272fa-131">**기능 추출(데이터 변환)**</span><span class="sxs-lookup"><span data-stu-id="272fa-131">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="272fa-132">**빌드 및 학습**</span><span class="sxs-lookup"><span data-stu-id="272fa-132">**Build and train**</span></span> 
   * <span data-ttu-id="272fa-133">**모델 학습**</span><span class="sxs-lookup"><span data-stu-id="272fa-133">**Train the model**</span></span>
   * <span data-ttu-id="272fa-134">**모델 평가**</span><span class="sxs-lookup"><span data-stu-id="272fa-134">**Evaluate the model**</span></span>
4. <span data-ttu-id="272fa-135">**실행**</span><span class="sxs-lookup"><span data-stu-id="272fa-135">**Run**</span></span>
   * <span data-ttu-id="272fa-136">**모델 사용**</span><span class="sxs-lookup"><span data-stu-id="272fa-136">**Model consumption**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="272fa-137">문제 이해</span><span class="sxs-lookup"><span data-stu-id="272fa-137">Understand the problem</span></span>

<span data-ttu-id="272fa-138">먼저 문제를 이해해야 하므로 모델 빌드 및 학습을 지원할 수 있는 부분으로 문제를 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-138">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="272fa-139">문제를 구분하면 결과를 예측하고 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-139">Breaking  down the problem allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="272fa-140">이 자습서의 문제점은 들어오는 GitHub 문제가 속해 있는 영역을 이해하여 우선순위 지정 및 스케줄링을 위해 올바르게 레이블을 지정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-140">The problem for this tutorial is to understand what area incoming GitHub issues belong to in order to label them correctly for prioritization and scheduling.</span></span>

<span data-ttu-id="272fa-141">다음과 같이 문제를 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-141">You can break down the problem to the following:</span></span>

* <span data-ttu-id="272fa-142">문제 제목 텍스트</span><span class="sxs-lookup"><span data-stu-id="272fa-142">the issue title text</span></span>
* <span data-ttu-id="272fa-143">문제 설명 텍스트</span><span class="sxs-lookup"><span data-stu-id="272fa-143">the issue description text</span></span>
* <span data-ttu-id="272fa-144">모델 학습 데이터에 대한 영역 값</span><span class="sxs-lookup"><span data-stu-id="272fa-144">an area value for the model training data</span></span>
* <span data-ttu-id="272fa-145">평가한 다음, 작동 가능하게 사용할 수 있는 예측된 영역 값</span><span class="sxs-lookup"><span data-stu-id="272fa-145">a predicted area value that you can evaluate and then use operationally</span></span>

<span data-ttu-id="272fa-146">그런 다음, 기계 학습 작업 선택에 도움이 되는 영역을 **확인**해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-146">You then need to **determine** the area, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="272fa-147">적절한 기계 학습 작업 선택</span><span class="sxs-lookup"><span data-stu-id="272fa-147">Select the appropriate machine learning task</span></span>

<span data-ttu-id="272fa-148">이 문제에서 다음 사실을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-148">With this problem, you know the following facts:</span></span>

<span data-ttu-id="272fa-149">학습 데이터:</span><span class="sxs-lookup"><span data-stu-id="272fa-149">Training data:</span></span>

<span data-ttu-id="272fa-150">다음 예제와 같이 GitHub 문제는 여러 영역(**Area**)에 레이블을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-150">GitHub issues can be labeled in several areas (**Area**) as in the following examples:</span></span>

* <span data-ttu-id="272fa-151">area-System.Numerics</span><span class="sxs-lookup"><span data-stu-id="272fa-151">area-System.Numerics</span></span>
* <span data-ttu-id="272fa-152">area-System.Xml</span><span class="sxs-lookup"><span data-stu-id="272fa-152">area-System.Xml</span></span>
* <span data-ttu-id="272fa-153">area-Infrastructure</span><span class="sxs-lookup"><span data-stu-id="272fa-153">area-Infrastructure</span></span>
* <span data-ttu-id="272fa-154">area-System.Linq</span><span class="sxs-lookup"><span data-stu-id="272fa-154">area-System.Linq</span></span>
* <span data-ttu-id="272fa-155">area-System.IO</span><span class="sxs-lookup"><span data-stu-id="272fa-155">area-System.IO</span></span>

<span data-ttu-id="272fa-156">다음 예제와 같이 새 GitHub 문제의 **영역**을 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-156">Predict the **Area** of a new GitHub Issue such as in the following examples:</span></span>

* <span data-ttu-id="272fa-157">Contract.Assert 대 Debug.Assert</span><span class="sxs-lookup"><span data-stu-id="272fa-157">Contract.Assert vs Debug.Assert</span></span>
* <span data-ttu-id="272fa-158">System.Xml에서 읽기 전용으로 필드 만들기</span><span class="sxs-lookup"><span data-stu-id="272fa-158">Make fields readonly in System.Xml</span></span>

<span data-ttu-id="272fa-159">분류 기계 학습 작업이 이 시나리오에 가장 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-159">The classification machine learning task is best suited for this scenario.</span></span>

### <a name="about-the-classification-task"></a><span data-ttu-id="272fa-160">분류 작업 정보</span><span class="sxs-lookup"><span data-stu-id="272fa-160">About the classification task</span></span>

<span data-ttu-id="272fa-161">분류는 데이터를 사용하여 데이터 항목 또는 행의 범주, 형식 또는 클래스를 **확인**하는 기계 학습 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-161">Classification is a machine learning task that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="272fa-162">예를 들어 분류를 사용하여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-162">For example, you can use classification to:</span></span>

* <span data-ttu-id="272fa-163">감정을 긍정적 또는 부정적으로 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-163">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="272fa-164">전자 메일을 스팸, 정크 또는 정상으로 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-164">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="272fa-165">환자의 실험실 샘플이 종양성인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-165">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="272fa-166">영업 캠페인에 응답하는 고객의 성향을 기준으로 고객을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-166">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="272fa-167">일반적으로 분류 작업은 다음 형식 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-167">Classification tasks are frequently one of the following types:</span></span>

* <span data-ttu-id="272fa-168">이진: A 또는 B.</span><span class="sxs-lookup"><span data-stu-id="272fa-168">Binary: either A or B.</span></span>
* <span data-ttu-id="272fa-169">다중 클래스: 단일 모델을 사용하여 예측할 수 있는 여러 범주.</span><span class="sxs-lookup"><span data-stu-id="272fa-169">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

<span data-ttu-id="272fa-170">이러한 유형의 문제에는 다중 클래스 분류 작업을 사용합니다. 문제 범주 예측이 단지 2개(이진)가 아닌 여러 범주(다중 클래스) 중 하나일 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-170">For this type of problem, use a Multiclass classification task, since your issue category prediction can be one of multiple categories (multiclass) rather than just two (binary).</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="272fa-171">콘솔 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="272fa-171">Create a console application</span></span>

### <a name="create-a-project"></a><span data-ttu-id="272fa-172">프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="272fa-172">Create a project</span></span>

1. <span data-ttu-id="272fa-173">Visual Studio 2017을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-173">Open Visual Studio 2017.</span></span> <span data-ttu-id="272fa-174">메뉴 모음에서 **파일** > **새로 만들기** > **프로젝트**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-174">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="272fa-175">**새 프로젝트** 대화 상자에서 **Visual C#** 노드와 **.NET Core** 노드를 차례로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-175">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="272fa-176">그런 다음 **콘솔 앱(.NET Core)** 프로젝트 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-176">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="272fa-177">**이름** 텍스트 상자에 “SentimentAnalysis”를 입력한 다음, **확인** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-177">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="272fa-178">프로젝트에서 *Data* 디렉터리를 만들어 데이터 집합 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-178">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="272fa-179">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 폴더**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-179">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="272fa-180">“Data”를 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-180">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="272fa-181">**Microsoft.ML NuGet 패키지**를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-181">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="272fa-182">솔루션 탐색기에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **NuGet 패키지 관리**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-182">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="272fa-183">“nuget.org”를 패키지 소스로 선택하고, [찾아보기] 탭을 선택하고, **Microsoft.ML**을 검색하고, 목록에서 해당 패키지를 선택하고, **설치** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-183">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="272fa-184">**변경 내용 미리 보기** 대화 상자에서 **확인** 단추를 선택한 다음, 나열된 패키지의 사용 조건에 동의하는 경우 **라이선스 승인** 대화 상자에서 **동의함** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-184">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="272fa-185">데이터 준비</span><span class="sxs-lookup"><span data-stu-id="272fa-185">Prepare your data</span></span>

1. <span data-ttu-id="272fa-186">[issues-train.csv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) 및 [issues-test.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv) 데이터 세트를 다운로드하여 이전에 만든 *Data* 폴더에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-186">Download the [issues_train.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) and the [issues_test.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="272fa-187">첫 번째 데이터 세트는 기계 학습 모델을 교육하고 두 번째 데이터 세트는 모델이 얼마나 정확한지 평가하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-187">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="272fa-188">솔루션 탐색기에서 각 \*.tsv 파일을 마우스 오른쪽 단추로 클릭하고 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-188">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="272fa-189">**고급** 아래에서 **출력 디렉터리에 복사** 값을 **변경된 내용만 복사**로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-189">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="272fa-190">클래스 만들기 및 경로 정의</span><span class="sxs-lookup"><span data-stu-id="272fa-190">Create classes and define paths</span></span>

<span data-ttu-id="272fa-191">*Program.cs* 파일 맨 위에 다음 추가 `using` 문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-191">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddUsings)]

<span data-ttu-id="272fa-192">최근에 다운로드한 파일의 경로와 `TextLoader`의 전역 변수가 포함될 세 개의 전역 필드를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-192">You need to create three global fields to hold the paths to the recently downloaded files, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="272fa-193">`_trainDataPath`에는 모델을 학습시키는 데 사용되는 데이터 세트의 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-193">`_trainDataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="272fa-194">`_testDataPath`에는 모델을 평가하는 데 사용되는 데이터 세트의 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-194">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="272fa-195">`_modelPath`에는 학습된 모델이 저장되는 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-195">`_modelPath` has the path where the trained model is saved.</span></span>
* <span data-ttu-id="272fa-196">`_mlContext`는 처리 컨텍스트를 제공하는 <xref:Microsoft.ML.MLContext>입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-196">`_mlContext` is the <xref:Microsoft.ML.MLContext> that provides processing context.</span></span>
* <span data-ttu-id="272fa-197">`_trainingDataView`는 학습 데이터 세트를 처리하는 데 사용되는 <xref:Microsoft.ML.Data.IDataView>입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-197">`_trainingDataView` is the <xref:Microsoft.ML.Data.IDataView> used to process the training dataset.</span></span>
* <span data-ttu-id="272fa-198">`_predEngine`은 단일 예측에 사용되는 <xref:Microsoft.ML.PredictionEngine%602>입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-198">`_predEngine` is the <xref:Microsoft.ML.PredictionEngine%602> used for single predictions.</span></span>
* <span data-ttu-id="272fa-199">`_reader`는 데이터 세트를 로드하고 변환하는 데 사용되는 <xref:Microsoft.ML.Data.TextLoader>입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-199">`_reader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="272fa-200">`Main` 메서드 바로 위의 줄에 다음 코드를 추가하여 해당 경로와 다른 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-200">Add the following code to the line right above the `Main` method to specify those paths and the other variables:</span></span>

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DeclareGlobalVariables)]

<span data-ttu-id="272fa-201">입력 데이터 및 예측에 대한 일부 클래스를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-201">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="272fa-202">새 클래스를 프로젝트에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-202">Add a new class to your project:</span></span>

1. <span data-ttu-id="272fa-203">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-203">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="272fa-204">**새 항목 추가** 대화 상자에서 **클래스**를 선택하고 **이름** 필드를 *GitHubIssueData.cs*로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-204">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *GitHubIssueData.cs*.</span></span> <span data-ttu-id="272fa-205">그런 다음, **추가** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-205">Then, select the **Add** button.</span></span>

    <span data-ttu-id="272fa-206">*GitHubIssueData.cs* 파일이 코드 편집기에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-206">The *GitHubIssueData.cs* file opens in the code editor.</span></span> <span data-ttu-id="272fa-207">다음 `using` 문을 *GitHubIssueData.cs*의 맨 위에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-207">Add the following `using` statement to the top of *GitHubIssueData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#AddUsings)]

<span data-ttu-id="272fa-208">기존 클래스 정의를 제거하고 두 개의 클래스 `GitHubIssue` 및 `IssuePrediction`이 있는 다음 코드를 *GitHubIssueData.cs* 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-208">Remove the existing class definition and add the following code, which has two classes `GitHubIssue` and `IssuePrediction`, to the *GitHubIssueData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#DeclareTypes)]

<span data-ttu-id="272fa-209">`GitHubIssue`는 다음 입력 데이터 세트 클래스이며 다음 <xref:System.String> 필드를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-209">`GitHubIssue` is the input dataset class and has the following <xref:System.String> fields:</span></span>

* <span data-ttu-id="272fa-210">`ID`에 GitHub 문제 ID에 대한 값 포함</span><span class="sxs-lookup"><span data-stu-id="272fa-210">`ID` contains a value for the GitHub issue ID</span></span>
* <span data-ttu-id="272fa-211">`Area`에 `Area` 레이블에 대한 값 포함</span><span class="sxs-lookup"><span data-stu-id="272fa-211">`Area` contains a value for the `Area` label</span></span>
* <span data-ttu-id="272fa-212">`Title`에 GitHub 문제 제목 포함</span><span class="sxs-lookup"><span data-stu-id="272fa-212">`Title` contains the GitHub issue title</span></span>
* <span data-ttu-id="272fa-213">`Description`에 GitHub 문제 설명 포함</span><span class="sxs-lookup"><span data-stu-id="272fa-213">`Description` contains the GitHub issue description</span></span>

<span data-ttu-id="272fa-214">`IssuePrediction`은 모델이 학습된 후 예측에 사용되는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-214">`IssuePrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="272fa-215">여기에는 단일 `string`(`Area`) 및 `PredictedLabel` `ColumnName` 특성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-215">It has a single `string` (`Area`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="272fa-216">`Label`은 세트를 만들고 학습시키는 데 사용되며 두 번째 데이터 세트와 함께 모델을 평가하는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-216">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="272fa-217">`PredictedLabel`은 예측 및 평가 중에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-217">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="272fa-218">평가를 위해 학습 데이터가 있는 입력, 예측 값 및 모델이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-218">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="272fa-219">ML.NET를 사용하여 모델을 빌드하는 경우 먼저 <xref:Microsoft.ML.MLContext>를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-219">When building a model with ML.NET, you start by creating an <xref:Microsoft.ML.MLContext>.</span></span> <span data-ttu-id="272fa-220">이는 Entity Framework에서 `DbContext`를 사용하는 것과 개념이 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-220">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="272fa-221">환경은 예외 추적 및 로깅에 사용할 수 있는 ML 작업의 컨텍스트를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-221">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="272fa-222">Main에서 변수 초기화</span><span class="sxs-lookup"><span data-stu-id="272fa-222">Initialize variables in Main</span></span>

<span data-ttu-id="272fa-223">여러 학습에서 반복 가능한/결정적 결과를 얻기 위해 임의의 시드(`seed: 0`)가 있는 `MLContext`의 새 인스턴스로 `_mlContext` 글로벌 변수를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-223">Initialize the `_mlContext` global variable  with a new instance of `MLContext` with a random seed (`seed: 0`) for repeatable/deterministic results across multiple trainings.</span></span>  <span data-ttu-id="272fa-224">`Main` 메서드에서 `Console.WriteLine("Hello World!")` 줄을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-224">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateMLContext)]

## <a name="load-the-data"></a><span data-ttu-id="272fa-225">데이터 로드</span><span class="sxs-lookup"><span data-stu-id="272fa-225">Load the data</span></span>

<span data-ttu-id="272fa-226">그런 다음, `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> 글로벌 변수 초기화하고 `_trainDataPath` 매개 변수를 사용하여 데이터를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-226">Next, initialize the `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> global variable and load the data with the `_trainDataPath` parameter.</span></span>

 <span data-ttu-id="272fa-227">`Transforms`의 입력 및 출력으로 사용되는 `DataView`는 `LINQ`의 `IEnumerable`과 비슷한 기본적인 데이터 파이프라인 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-227">As the input and output of `Transforms`, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="272fa-228">ML.NET에서 데이터는 `SQL view`와 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-228">In ML.NET, data is similar to a `SQL view`.</span></span> <span data-ttu-id="272fa-229">지연 계산되고, 스키마화되며, 형식이 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-229">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="272fa-230">개체가 파이프라인의 첫 번째 부분이며 데이터를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-230">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="272fa-231">이 자습서에서는 문제 제목, 설명 및 해당 영역 GitHub 레이블이 있는 데이터 세트를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-231">For this tutorial, it loads a dataset with issue titles, descriptions, and corresponding area GitHub label.</span></span> <span data-ttu-id="272fa-232">`DataView`는 모델을 만들고 학습시키는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-232">The `DataView` is used to create and train the model.</span></span>

<span data-ttu-id="272fa-233">이전에 만든 `GitHubIssue` 데이터 모델 유형이 데이터 세트 스키마와 일치하므로 초기화, 매핑 및 데이터 세트 로드를 한 줄의 코드로 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-233">Since your previously created `GitHubIssue` data model type matches the dataset schema, you can combine the initialization, mapping, and dataset loading into one line of code.</span></span>

<span data-ttu-id="272fa-234">줄의 첫 번재 부분(`CreateTextReader<GitHubIssue>(hasHeader: true)`)에서는 `GitHubIssue` 데이터 모델 유형의 데이터 세트 스키마를 추론하고 데이터 세트 헤더를 사용하여 <xref:Microsoft.ML.Data.TextLoader>를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-234">The first part of the line (`CreateTextReader<GitHubIssue>(hasHeader: true)`) creates a <xref:Microsoft.ML.Data.TextLoader> by inferencing the dataset schema from the `GitHubIssue` data model type and using the dataset header.</span></span>

<span data-ttu-id="272fa-235">이전에 `GitHubIssue` 클래스를 만들 때 데이터 스키마를 정의했습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-235">You defined the data schema previously when you created the `GitHubIssue` class.</span></span> <span data-ttu-id="272fa-236">스키마의 경우:</span><span class="sxs-lookup"><span data-stu-id="272fa-236">For your schema:</span></span>

* <span data-ttu-id="272fa-237">첫 번째 열 `ID`(GitHub 문제 ID)</span><span class="sxs-lookup"><span data-stu-id="272fa-237">the first column `ID` (GitHub Issue ID)</span></span>
* <span data-ttu-id="272fa-238">두 번째 열 `Area`(학습 예측)</span><span class="sxs-lookup"><span data-stu-id="272fa-238">the second column `Area` (the prediction for training)</span></span>
* <span data-ttu-id="272fa-239">세 번째 열 `Title`(GitHub 문제 제목)은 `Area`를 예측하는 데 사용되는 첫 번째 [기능](../resources/glossary.md##feature)입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-239">the third column `Title` (GitHub issue title) is the first [feature](../resources/glossary.md##feature)  used for predicting the `Area`</span></span>
* <span data-ttu-id="272fa-240">네 번째 열 `Description`은 `Area`를 예측하는 데 사용되는 두 번째 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-240">the fourth column  `Description` is the second feature used for predicting the `Area`</span></span>

<span data-ttu-id="272fa-241">줄의 두 번째 부분(`.Read(_trainDataPath)`)에서는 `_trainDataPath`를 통해 `IDataView`(`_trainingDataView`) 글로벌 변수에 학습 텍스트 파일을 로드하는 데 <xref:Microsoft.ML.Data.TextLoader.Read%2A> 메서드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-241">The second part of the line  (`.Read(_trainDataPath)`) uses <xref:Microsoft.ML.Data.TextLoader.Read%2A> method to load the training text file using `_trainDataPath` into the `IDataView` (`_trainingDataView`) global variable.</span></span>  

<span data-ttu-id="272fa-242">`_trainingDataView` 글로벌 변수를 파이프라인에 사용하기 위해 초기화 및 로드하려면 `mlContext` 초기화 후에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-242">To initialize and load the `_trainingDataView` global variable in order to use it for the pipeline, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTrainData)]


<span data-ttu-id="272fa-243">`Main` 메서드에 아래 코드를 다음 코드 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-243">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallProcessData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallProcessData)]

<span data-ttu-id="272fa-244">`ProcessData` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-244">The `ProcessData` method executes the following tasks:</span></span>

* <span data-ttu-id="272fa-245">데이터를 추출하고 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-245">Extracts and transforms the data.</span></span>
* <span data-ttu-id="272fa-246">처리 파이프라인을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-246">Returns the processing pipeline.</span></span>

<span data-ttu-id="272fa-247">다음 코드를 사용하여 `Main` 메서드 바로 뒤에 `ProcessData` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-247">Create the `ProcessData` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static EstimatorChain<ITransformer> ProcessData()
{

}
```

## <a name="extract-and-transform-the-data"></a><span data-ttu-id="272fa-248">데이터 추출 및 변환</span><span class="sxs-lookup"><span data-stu-id="272fa-248">Extract and transform the data</span></span>

<span data-ttu-id="272fa-249">데이터 전처리 및 정리는 데이터 세트가 기계 학습에 효과적으로 사용되기 전에 수행되는 중요한 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-249">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="272fa-250">원시 데이터는 종종 정리되지 않고 불안정하며 값이 누락될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-250">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="272fa-251">이러한 모델링 작업 없이 데이터를 사용하면 잘못된 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-251">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="272fa-252">ML.NET의 변환 파이프라인은 학습 또는 테스트 전에 데이터에 적용되는 사용자 지정 변환 세트로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-252">ML.NET's transform pipelines compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="272fa-253">변환의 기본 목적은 데이터 [기능화](../resources/glossary.md#feature-engineering)입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-253">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="272fa-254">기계 학습 알고리즘은 [기능화된](../resources/glossary.md#feature) 데이터를 인식하므로 다음 단계는 텍스트 데이터를 ML 알고리즘이 인식하는 형식으로 변환하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-254">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="272fa-255">해당 형식은 [숫자 벡터](../resources/glossary.md#numerical-feature-vector)입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-255">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="272fa-256">다음 단계에서는 `GitHubIssue` 클래스에 정의된 이름으로 해당 열을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-256">In the next steps, we refer to the columns by the names defined in the `GitHubIssue` class.</span></span>

<span data-ttu-id="272fa-257">모델을 학습하고 평가할 때 기본적으로 **Label** 열의 값이 예측할 올바른 값으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-257">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="272fa-258">`GitHubIssue`에 대한 Area GitHub 레이블을 예측하려면 `Area` 열을 **Label** 열로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-258">As we want to predict the Area GitHub label for a `GitHubIssue`, copy the `Area` column into the **Label** column.</span></span> <span data-ttu-id="272fa-259">이렇게 하려면 <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A> 변환 클래스의 래퍼인 `MLContext.Transforms.Conversion.MapValueToKey`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-259">To do that, use the `MLContext.Transforms.Conversion.MapValueToKey`, which is a wrapper for the <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A> transformation class.</span></span>  <span data-ttu-id="272fa-260">`MapValueToKey`는 실제로 파이프라인이 될 <xref:Microsoft.ML.Data.EstimatorChain%601>을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-260">The `MapValueToKey` returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="272fa-261">이 학습자를 `EstimatorChain`에 추가할 때 `pipeline`으로 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-261">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="272fa-262">아래 코드를 다음 코드 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-262">Add this as the next line of code:</span></span>

[!code-csharp[MapValueToKey](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#MapValueToKey)]

<span data-ttu-id="272fa-263">모델을 학습하는 알고리즘은 **숫자** 기능이 필요하므로, 다음으로 `mlContext.Transforms.Text.FeaturizeText`를 호출하여 텍스트(`Title` 및 `Description`) 열을 각각 `TitleFeaturized` 및 `DescriptionFeaturized`라는 숫자 벡터로 기능화합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-263">The algorithm that trains the model requires **numeric** features, so you have Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text (`Title` and `Description`) columns into a numeric vector for each called `TitleFeaturized` and `DescriptionFeaturized`.</span></span> <span data-ttu-id="272fa-264">기능화는 각 열의 다른 값에 서로 다른 숫자 키 값을 할당하고 기계 학습 알고리즘에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-264">Featurizing assigns different numeric key values to the different values in each of the columns and is used by the machine learning algorithm.</span></span>
<span data-ttu-id="272fa-265">다음 코드를 사용하여 두 열에 대한 기능화(featurization)를 파이프라인에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-265">Append the featurization for both columns to the pipeline with the following code:</span></span>

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#FeaturizeText)]

<span data-ttu-id="272fa-266">데이터 준비의 마지막 단계에서는 `Concatenate` 변환 클래스를 사용하여 모든 기능 열을 **Features** 열에 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-266">The last step in data preparation combines all of the feature columns into the **Features** column using the `Concatenate` transformation class.</span></span> <span data-ttu-id="272fa-267">기본적으로, 학습 알고리즘은 **Features** 열의 기능만 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-267">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="272fa-268">다음 코드를 사용하여 이 변환을 파이프라인에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-268">Append this transformation to the pipeline with the following code:</span></span>

[!code-csharp[Concatenate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Concatenate)]

 <span data-ttu-id="272fa-269">그런 다음, <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A>를 추가하여 DataView를 여러 번 캐시합니다. 따라서 캐시를 사용하여 데이터를 여러 번 반복할 때 다음 코드와 같이 성능이 향상될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-269">Next, append a <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> to cache the DataView so when you iterate over the data multiple times using the cache might get better performance, as with the following code</span></span>

[!code-csharp[AppendCache](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AppendCache)]

<span data-ttu-id="272fa-270">`ProcessData` 메서드의 끝에 파이프라인을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-270">Return the pipeline at the end of the `ProcessData` method.</span></span>

[!code-csharp[ReturnPipeline](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnPipeline)]

<span data-ttu-id="272fa-271">이 단계는 전처리/기능화를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-271">This step handles preprocessing/featurization.</span></span> <span data-ttu-id="272fa-272">ML.NET에서 사용 가능한 추가 구성 요소를 사용하면 모델에서 더 나은 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-272">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="build-and-train-the-model"></a><span data-ttu-id="272fa-273">모델 빌드 및 학습</span><span class="sxs-lookup"><span data-stu-id="272fa-273">Build and train the model</span></span>

<span data-ttu-id="272fa-274">`BuildAndTrainModel` 메서드에 다음 호출을 `Main` 메서드의 다음 코드 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-274">Add the following call to the `BuildAndTrainModel`method as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallBuildAndTrainModel)]

<span data-ttu-id="272fa-275">`BuildAndTrainModel` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-275">The `BuildAndTrainModel` method executes the following tasks:</span></span>

* <span data-ttu-id="272fa-276">학습 알고리즘 클래스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-276">Creates the training algorithm class.</span></span>
* <span data-ttu-id="272fa-277">모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-277">Trains the model.</span></span>
* <span data-ttu-id="272fa-278">학습 데이터를 기반으로 영역을 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-278">Predicts area based on training data.</span></span>
* <span data-ttu-id="272fa-279">모델을 `.zip` 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-279">Saves the model to a `.zip` file.</span></span>
* <span data-ttu-id="272fa-280">모델을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-280">Returns the model.</span></span>

<span data-ttu-id="272fa-281">다음 코드를 사용하여 `Main` 메서드 바로 뒤에 `BuildAndTrainModel` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-281">Create the `BuildAndTrainModel` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static void BuildAndTrainModel()
{

}
```

<span data-ttu-id="272fa-282">BuildAndTrainModel 메서드에는 학습 데이터 세트(`trainingDataView`)에 대한 `IDataView` 및 ProcessData(`pipeline`)에서 만든 처리 파이프라인에 대한 <xref:Microsoft.ML.Data.EstimatorChain%601>이라는 두 개의 매개 변수가 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-282">Notice that two parameters are passed into the BuildAndTrainModel method; an `IDataView` for the training dataset (`trainingDataView`), and a <xref:Microsoft.ML.Data.EstimatorChain%601> for the processing pipeline created in ProcessData (`pipeline`).</span></span>

 <span data-ttu-id="272fa-283">다음 코드를 `BuildAndTrainModel` 메서드의 첫 번째 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-283">Add the following code as the first line of the `BuildAndTrainModel` method:</span></span>

### <a name="choose-a-trainer-algorithm"></a><span data-ttu-id="272fa-284">강사 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="272fa-284">Choose a trainer algorithm</span></span>

<span data-ttu-id="272fa-285">강사 알고리즘을 추가하려면 <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer> 개체를 반환하는 `mlContext.Transforms.Text.FeaturizeText` 래퍼 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-285">To add the trainer algorithm, call the `mlContext.Transforms.Text.FeaturizeText` wrapper method which returns a <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer> object.</span></span> <span data-ttu-id="272fa-286">이 개체는 이 파이프라인에서 사용할 의사 결정 트리 학습자입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-286">This is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="272fa-287">`SdcaMultiClassTrainer`는 `pipeline`에 추가되고 기록 데이터에서 학습할 기능화된 `Title`, `Description`(`Features`) 및 `Label` 입력 매개 변수를 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-287">The `SdcaMultiClassTrainer` is appended to the `pipeline` and accepts the featurized `Title` and `Description` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="272fa-288">`BuildAndTrainModel` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-288">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[SdcaMultiClassTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SdcaMultiClassTrainer)]

<span data-ttu-id="272fa-289">이제 강사 알고리즘을 만들었으므로 `pipeline`에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-289">Now that you've created a trainer algorithm, append it to the `pipeline`.</span></span> <span data-ttu-id="272fa-290">또한 레이블을 원래 읽기 가능한 상태로 반환하려면 값에 매핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-290">You also need to map the label to the value to return to its original readable state.</span></span> <span data-ttu-id="272fa-291">다음 코드를 사용하여 해당 작업 모두를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-291">Do both of those actions with the following code:</span></span>

[!code-csharp[AddTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTrainer)]

### <a name="train-the-model"></a><span data-ttu-id="272fa-292">모델 학습</span><span class="sxs-lookup"><span data-stu-id="272fa-292">Train the model</span></span>

<span data-ttu-id="272fa-293">로드되고 변환된 데이터 세트를 기반으로 <xref:Microsoft.ML.Data.TransformerChain%601> 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-293">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="272fa-294">추정기가 정의된 후, 이미 로드된 학습 데이터를 제공하는 동시에 <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A>을 사용하여 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-294">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="272fa-295">그러면 예측에 사용할 모델이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-295">This returns a model to use for predictions.</span></span> <span data-ttu-id="272fa-296">`trainingPipeline.Fit()`은 파이프라인을 학습시키고, 전달된 `DataView`에 따라 `Transformer`를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-296">`trainingPipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="272fa-297">이 문제가 발생할 때까지 실험이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-297">The experiment is not executed until this happens.</span></span>

<span data-ttu-id="272fa-298">`BuildAndTrainModel` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-298">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#TrainModel)]

<span data-ttu-id="272fa-299">`model`은 여러 데이터 행에서 작동하는 `transformer`이지만, 일반적인 프로덕션 시나리오에서는 개별 예제에 대한 예측이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-299">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="272fa-300"><xref:Microsoft.ML.PredictionEngine%602>은 `CreatePredictionEngine` 메서드에서 반환되는 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-300">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="272fa-301">다음 코드를 추가하여 `PredictionEngine`을 `BuildAndTrainModel` 메서드의 다음 줄로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-301">Let's add the following code to create the `PredictionEngine` as the next line in the `BuildAndTrainModel` Method:</span></span>

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]

<span data-ttu-id="272fa-302">`GitHubIssue`의 인스턴스를 만들어 GitHub 문제를 추가하여 `Predict` 메서드에서 학습된 모델의 예측을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-302">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[CreateTestIssue1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateTestIssue1)]

<span data-ttu-id="272fa-303">문제 데이터의 단일 인스턴스에 대한 `Area` 레이블을 예측하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-303">You can use that to predict the `Area` label of a single instance of the issue data.</span></span> <span data-ttu-id="272fa-304">예측을 가져오려면 데이터에 대해 <xref:Microsoft.ML.PredictionEngine%602.Predict%2A>을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-304">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="272fa-305">입력 데이터는 문자열이고 모델은 기능화를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-305">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="272fa-306">파이프라인은 학습 및 예측 중에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-306">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="272fa-307">특별히 예측을 위해 전처리/기능화 코드를 작성할 필요가 없고 동일한 API가 배치 및 일회성 예측을 둘 다 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-307">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Predict)]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="272fa-308">모델 연산화: 예측</span><span class="sxs-lookup"><span data-stu-id="272fa-308">Model operationalization: prediction</span></span>

<span data-ttu-id="272fa-309">결과를 공유하고 이에 따라 작업을 수행하기 위해 `GitHubIssue` 및 해당 `Area` 레이블 예측을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-309">Display `GitHubIssue` and corresponding `Area` label prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="272fa-310">이것을 반환된 데이터를 운영 정책의 일부로 사용하는 연산화라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-310">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="272fa-311">다음 <xref:System.Console.WriteLine?displayProperty=nameWithType> 코드를 사용하여 결과 표시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-311">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#OutputPrediction)]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="272fa-312">평가에 사용하기 위해 학습된 모델 저장 및 반환</span><span class="sxs-lookup"><span data-stu-id="272fa-312">Save and return the model trained to use for evaluation</span></span>

<span data-ttu-id="272fa-313">이 시점에는 기존 또는 새 .NET 애플리케이션에 통합할 수 있는 <xref:Microsoft.ML.Data.TransformerChain%601> 형식의 모델이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-313">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="272fa-314">학습된 모델을 .zip 파일로 저장하려면 다음 코드를 추가하여 `SaveModelAsFile` 메서드를 `BuildAndTrainModel`에 다음 줄로 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-314">To save your trained model to a .zip file, add the following code to call the `SaveModelAsFile` method as the next line in `BuildAndTrainModel`:</span></span>

[!code-csharp[CallSaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallSaveModel)]

<span data-ttu-id="272fa-315">`BuildAndTrainModel` 메서드의 끝에 모델을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-315">Return the model at the end of the `BuildAndTrainModel` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnModel)]

## <a name="save-the-model-as-azip-file"></a><span data-ttu-id="272fa-316">모델을 .zip 파일로 저장</span><span class="sxs-lookup"><span data-stu-id="272fa-316">Save the model as a.zip file</span></span>

<span data-ttu-id="272fa-317">다음 코드를 사용하여 `BuildAndTrainModel` 메서드 바로 뒤에 `SaveModelAsFile` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-317">Create the `SaveModelAsFile` method, just after the `BuildAndTrainModel` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="272fa-318">`SaveModelAsFile` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-318">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="272fa-319">모델을 .zip 파일로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-319">Saves the model as a .zip file.</span></span>

<span data-ttu-id="272fa-320">다음으로, 다른 애플리케이션에서 다시 사용하고 이용할 수 있도록 모델을 저장하는 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-320">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="272fa-321">`ITransformer`에는 `_modelPath` 전역 필드를 사용하는 <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> 메서드와 <xref:System.IO.Stream>이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-321">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="272fa-322">이 파일을 zip 파일로 저장하기 위해 `SaveTo` 메서드를 호출하기 직전에 `FileStream`을 만들겠습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-322">To save this as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="272fa-323">`SaveModelAsFile` 메서드에 아래 코드를 다음 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-323">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SaveModel)]

<span data-ttu-id="272fa-324">다음 코드를 사용해서 `_modelPath`가 포함된 콘솔 메시지를 작성하여 파일이 작성된 위치를 표시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-324">You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a><span data-ttu-id="272fa-325">모델 평가</span><span class="sxs-lookup"><span data-stu-id="272fa-325">Evaluate the model</span></span>

<span data-ttu-id="272fa-326">이제 모델을 만들고 학습시켰으므로 품질 보증 및 유효성 검사를 위해 다른 데이터 세트를 사용하여 평가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-326">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="272fa-327">`Evaluate` 메서드에서는 `BuildAndTrainModel`에서 만들어진 모델을 전달하여 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-327">In the `Evaluate` method, the model created in `BuildAndTrainModel` is passed in to be evaluated.</span></span> <span data-ttu-id="272fa-328">다음 코드와 같이 `BuildAndTrainModel` 바로 뒤에 `Evaluate` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-328">Create the `Evaluate` method, just after `BuildAndTrainModel`, as in the following code:</span></span>

```csharp
public static void Evaluate()
{

}
```

<span data-ttu-id="272fa-329">`Evaluate` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-329">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="272fa-330">테스트 데이터 세트를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-330">Loads the test dataset.</span></span>
* <span data-ttu-id="272fa-331">다중 클래스 평가자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-331">Creates the multiclass evaluator.</span></span>
* <span data-ttu-id="272fa-332">모델을 평가하고 메트릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-332">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="272fa-333">메트릭을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-333">Displays the metrics.</span></span>

<span data-ttu-id="272fa-334">다음 코드를 사용하여 `BuildAndTrainModel` 메서드 호출 바로 아래에 `Main` 메서드의 새 메서드 호출을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-334">Add a call to the new method from the `Main` method, right under the `BuildAndTrainModel` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallEvaluate)]

<span data-ttu-id="272fa-335">이전에 학습 데이터 세트를 사용했을 때처럼 초기화, 매핑 및 테스트 데이터 세트 로드를 하나의 코드 행에 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-335">As you did previously with the training dataset, you can combine the initialization, mapping, and test dataset loading into one line of code.</span></span> <span data-ttu-id="272fa-336">이 데이터 세트를 품질 검사로 사용하여 모델을 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-336">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="272fa-337">`Evaluate` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-337">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTestDataset)]

<span data-ttu-id="272fa-338">`MulticlassClassificationContext.Evaluate`는 지정된 데이터 세트를 사용하여 모델의 품질 메트릭을 계산하는 <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> 메서드의 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-338">The `MulticlassClassificationContext.Evaluate` is a wrapper for the <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> method that computes the quality metrics for the model using the specified dataset.</span></span> <span data-ttu-id="272fa-339">다중 클래스 분류 평가자가 계산한 전체 메트릭을 포함하는 <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-339">It returns a <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> object that contains the overall metrics computed by multiclass classification evaluators.</span></span>
<span data-ttu-id="272fa-340">모델의 품질을 확인하기 위해 이러한 메트릭을 표시하려면 먼저 메트릭을 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-340">To display these to determine the quality of the model, you need to get the metrics first.</span></span>
<span data-ttu-id="272fa-341">기계 학습 `_trainedModel` 글로벌 변수(변환기)의 `Transform` 메서드를 사용하여 기능을 입력하고 예측을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-341">Notice the use of the `Transform` method of the machine learning `_trainedModel` global variable (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="272fa-342">`Evaluate` 메서드에 아래 코드를 다음 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-342">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Evaluate)]

<span data-ttu-id="272fa-343">다중 클래스 분류에 대한 다음 메트릭이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-343">The following metrics are evaluated for multiclass classification:</span></span>

* <span data-ttu-id="272fa-344">마이크로 정확도 - 모든 샘플 클래스 쌍은 정확도 메트릭에 동일하게 기여합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-344">Micro Accuracy - Every sample-class pair contributes equally to the accuracy metric.</span></span>  <span data-ttu-id="272fa-345">마이크로 정확도를 가능한 한 1에 가깝게 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-345">You want Micro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="272fa-346">매크로 정확도 - 모든 클래스 정확도 메트릭에 동일하게 기여합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-346">Macro Accuracy - Every class contributes equally to the accuracy metric.</span></span> <span data-ttu-id="272fa-347">소수 클래스는 큰 클래스와 같은 가중치를 부여받습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-347">Minority classes are given equal weight as the larger classes.</span></span> <span data-ttu-id="272fa-348">매크로 정확도를 가능한 한 1에 가깝게 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-348">You want Macro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="272fa-349">로그 손실 - [로그 손실](../resources/glossary.md#log-loss)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="272fa-349">Log-loss - see [Log Loss](../resources/glossary.md#log-loss).</span></span> <span data-ttu-id="272fa-350">로그 손실을 가능한 한 0에 가깝게 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-350">You want Log-loss to be as close to zero as possible.</span></span>

* <span data-ttu-id="272fa-351">로그 손실 감소 - [-inf, 100]의 범위입니다. 여기서 100은 완벽한 예측이고 0은 평균 예측을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-351">Log-loss reduction - Ranges from [-inf, 100], where 100 is perfect predictions and 0 indicates mean predictions.</span></span> <span data-ttu-id="272fa-352">로그 손실 감소를 가능한 한 0에 가깝게 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-352">You want Log-loss reduction to be as close to zero as possible.</span></span>

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="272fa-353">모델 유효성 검사를 위해 메트릭 표시</span><span class="sxs-lookup"><span data-stu-id="272fa-353">Displaying the metrics for model validation</span></span>

<span data-ttu-id="272fa-354">다음 코드를 사용하여 메트릭을 표시하고, 결과를 공유한 다음, 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-354">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayMetrics)]

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="272fa-355">저장된 모델을 사용하여 테스트 데이터 결과 예측</span><span class="sxs-lookup"><span data-stu-id="272fa-355">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="272fa-356">다음 코드를 사용하여 `Evaluate` 메서드 호출 바로 아래에 `Main` 메서드의 새 메서드 호출을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-356">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallPredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallPredictIssue)]

<span data-ttu-id="272fa-357">다음 코드를 사용하여 `Evaluate` 메서드 바로 뒤에 `PredictIssue` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-357">Create the `PredictIssue` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void PredictIssue()
{

}
```

<span data-ttu-id="272fa-358">`PredictIssue` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-358">The `PredictIssue` method executes the following tasks:</span></span>

* <span data-ttu-id="272fa-359">테스트 데이터의 단일 문제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-359">Creates a single issue of test data.</span></span>
* <span data-ttu-id="272fa-360">테스트 데이터를 기반으로 영역을 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-360">Predicts Area based on test data.</span></span>
* <span data-ttu-id="272fa-361">보고를 위해 테스트 데이터 및 예측을 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-361">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="272fa-362">예측 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-362">Displays the predicted results.</span></span>

<span data-ttu-id="272fa-363">먼저 다음 코드를 사용하여 이전에 저장한 모델을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-363">First, load the model that you saved previously with the following code:</span></span>

[!code-csharp[LoadModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadModel)]

<span data-ttu-id="272fa-364">`GitHubIssue`의 인스턴스를 만들어 GitHub 문제를 추가하여 `Predict` 메서드에서 학습된 모델의 예측을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-364">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[AddTestIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTestIssue)]

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]
  
<span data-ttu-id="272fa-365">이제 모델을 설정했으므로 GitHub 문제 데이터의 단일 인스턴스에 대한 Area GitHub 레이블을 예측하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-365">Now that you have a model, you can use that to predict the Area GitHub label of a single instance of the GitHub issue data.</span></span> <span data-ttu-id="272fa-366">예측을 가져오려면 데이터에 대해 <xref:Microsoft.ML.PredictionEngine%602.Predict%2A>을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-366">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="272fa-367">입력 데이터는 문자열이고 모델은 기능화를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-367">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="272fa-368">파이프라인은 학습 및 예측 중에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-368">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="272fa-369">특별히 예측을 위해 전처리/기능화 코드를 작성할 필요가 없고 동일한 API가 배치 및 일회성 예측을 둘 다 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-369">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="272fa-370">예측을 위해 `PredictIssue` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-370">Add the following code to the `PredictIssue` method for the predictions:</span></span>

[!code-csharp[PredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="272fa-371">모델 연산화: 예측</span><span class="sxs-lookup"><span data-stu-id="272fa-371">Model operationalization: prediction</span></span>

<span data-ttu-id="272fa-372">문제를 분류하고 이에 따라 조치를 취하기 위해 `Area`를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-372">Display `Area` in order to categorize the issue and act on it accordingly.</span></span> <span data-ttu-id="272fa-373">이것을 반환된 데이터를 운영 정책의 일부로 사용하는 연산화라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-373">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="272fa-374">다음 <xref:System.Console.WriteLine?displayProperty=nameWithType> 코드를 사용하여 결과 표시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-374">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[DisplayResults](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayResults)]

## <a name="results"></a><span data-ttu-id="272fa-375">결과</span><span class="sxs-lookup"><span data-stu-id="272fa-375">Results</span></span>

<span data-ttu-id="272fa-376">다음과 같은 결과가 나타나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-376">Your results should be similar to the following.</span></span> <span data-ttu-id="272fa-377">파이프라인이 처리할 때 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-377">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="272fa-378">경고 또는 메시지 처리를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-378">You may see warnings, or processing messages.</span></span> <span data-ttu-id="272fa-379">이해하기 쉽도록 이러한 결과는 다음 결과에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-379">These have been removed from the following results for clarity.</span></span>

```console
=============== Single Prediction just-trained-model - Result: area-System.Net ===============
The model is saved to C:\Users\johalex\dotnet-samples\samples\machine-learning\tutorials\GitHubIssueClassification\bin\Debug\netcoreapp2.0\..\..\..\Models\model.zip
*************************************************************************************************************
*       Metrics for Multi-class Classification model - Test Data
*------------------------------------------------------------------------------------------------------------
*       MicroAccuracy:    0.74
*       MacroAccuracy:    0.687
*       LogLoss:          .932
*       LogLossReduction: 63.852
*************************************************************************************************************
=============== Single Prediction - Result: area-System.Data ===============
```

<span data-ttu-id="272fa-380">지금까지</span><span class="sxs-lookup"><span data-stu-id="272fa-380">Congratulations!</span></span> <span data-ttu-id="272fa-381">이제 GitHub 문제의 영역 레이블을 분류하고 예측하기 위한 기계 학습 모델을 성공적으로 빌드했습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-381">You've now successfully built a machine learning model for classifying and predicting an Area label for a GitHub issue.</span></span> <span data-ttu-id="272fa-382">[dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) 리포지토리에서 이 자습서의 소스 코드를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-382">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="272fa-383">다음 단계</span><span class="sxs-lookup"><span data-stu-id="272fa-383">Next steps</span></span>

<span data-ttu-id="272fa-384">본 자습서에서는 다음 작업에 관한 방법을 학습했습니다.</span><span class="sxs-lookup"><span data-stu-id="272fa-384">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="272fa-385">문제 이해</span><span class="sxs-lookup"><span data-stu-id="272fa-385">Understand the problem</span></span>
> * <span data-ttu-id="272fa-386">적절한 기계 학습 작업 선택</span><span class="sxs-lookup"><span data-stu-id="272fa-386">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="272fa-387">데이터 준비</span><span class="sxs-lookup"><span data-stu-id="272fa-387">Prepare your data</span></span>
> * <span data-ttu-id="272fa-388">학습 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="272fa-388">Create the learning pipeline</span></span>
> * <span data-ttu-id="272fa-389">분류자 로드</span><span class="sxs-lookup"><span data-stu-id="272fa-389">Load a classifier</span></span>
> * <span data-ttu-id="272fa-390">모델 학습</span><span class="sxs-lookup"><span data-stu-id="272fa-390">Train the model</span></span>
> * <span data-ttu-id="272fa-391">다른 데이터 세트를 사용하여 모델 평가</span><span class="sxs-lookup"><span data-stu-id="272fa-391">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="272fa-392">모델을 사용하여 테스트 데이터 결과 예측</span><span class="sxs-lookup"><span data-stu-id="272fa-392">Predict the test data outcomes with the model</span></span>

<span data-ttu-id="272fa-393">다음 자습서로 이동하여 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="272fa-393">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="272fa-394">택시 요금 예측기</span><span class="sxs-lookup"><span data-stu-id="272fa-394">Taxi Fare Predictor</span></span>](taxi-fare.md)
