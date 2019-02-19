---
title: 감정 분석 이진 분류 시나리오에서 ML.NET 사용
description: 감정 예측을 통해 적절한 작업을 수행하는 방법을 이해하기 위해 이진 분류 시나리오에서 ML.NET을 사용하는 방법을 살펴봅니다.
ms.date: 02/15/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: d6d5cae107e25000add5c8430a35131a79696bc2
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092763"
---
# <a name="tutorial-use-mlnet-in-a-sentiment-analysis-binary-classification-scenario"></a><span data-ttu-id="91780-103">자습서: 감정 분석 이진 분류 시나리오에서 ML.NET 사용</span><span class="sxs-lookup"><span data-stu-id="91780-103">Tutorial: Use ML.NET in a sentiment analysis binary classification scenario</span></span>

> [!NOTE]
> <span data-ttu-id="91780-104">이 항목은 현재 미리 보기로 제공되는 ML.NET을 참조하며, 자료는 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="91780-105">자세한 내용은 [ML.NET 소개](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="91780-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="91780-106">이 샘플 자습서에서는 ML.NET을 사용하여 Visual Studio 2017에서 C#를 사용하는 .NET Core 콘솔 애플리케이션을 통해 감정 분류자를 만드는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-106">This sample tutorial illustrates using ML.NET to create a sentiment classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="91780-107">이 자습서에서는 다음과 같은 작업을 수행하는 방법을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="91780-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="91780-108">문제 이해</span><span class="sxs-lookup"><span data-stu-id="91780-108">Understand the problem</span></span>
> * <span data-ttu-id="91780-109">적절한 기계 학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="91780-109">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="91780-110">데이터 준비</span><span class="sxs-lookup"><span data-stu-id="91780-110">Prepare your data</span></span>
> * <span data-ttu-id="91780-111">데이터 변환</span><span class="sxs-lookup"><span data-stu-id="91780-111">Transform the data</span></span>
> * <span data-ttu-id="91780-112">모델 학습</span><span class="sxs-lookup"><span data-stu-id="91780-112">Train the model</span></span>
> * <span data-ttu-id="91780-113">모델 평가</span><span class="sxs-lookup"><span data-stu-id="91780-113">Evaluate the model</span></span>
> * <span data-ttu-id="91780-114">학습된 모델을 통해 예측</span><span class="sxs-lookup"><span data-stu-id="91780-114">Predict with the trained model</span></span>
> * <span data-ttu-id="91780-115">로드된 모델을 통해 배포 및 예측</span><span class="sxs-lookup"><span data-stu-id="91780-115">Deploy and Predict with a loaded model</span></span>

## <a name="sentiment-analysis-sample-overview"></a><span data-ttu-id="91780-116">감정 분석 샘플 개요</span><span class="sxs-lookup"><span data-stu-id="91780-116">Sentiment analysis sample overview</span></span>

<span data-ttu-id="91780-117">샘플은 ML.NET을 사용하여 감정을 긍정적 또는 부정적으로 분류하고 예측하는 모델을 학습시키는 콘솔 앱입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-117">The sample is a console app that uses ML.NET to train a model that classifies and predicts sentiment as either positive or negative.</span></span> <span data-ttu-id="91780-118">또한 품질 분석을 위해 두 번째 데이터 세트를 사용하여 모델을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-118">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="91780-119">감정 데이터 세트는 WikiDetox 프로젝트에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91780-119">The sentiment datasets are from the WikiDetox project.</span></span>

<span data-ttu-id="91780-120">[dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) 리포지토리에서 이 자습서의 소스 코드를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-120">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="91780-121">전제 조건</span><span class="sxs-lookup"><span data-stu-id="91780-121">Prerequisites</span></span>

* <span data-ttu-id="91780-122">“.NET Core 플랫폼 간 개발” 워크로드가 설치된 [Visual Studio 2017 15.6 이상](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).</span><span class="sxs-lookup"><span data-stu-id="91780-122">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="91780-123">[Wikipedia detox 줄 데이터 탭 구분 파일(wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).</span><span class="sxs-lookup"><span data-stu-id="91780-123">The [Wikipedia detox line data tab separated file (wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).</span></span>
* <span data-ttu-id="91780-124">[Wikipedia detox 줄 테스트 탭 구분 파일(wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).</span><span class="sxs-lookup"><span data-stu-id="91780-124">The [Wikipedia detox line test tab separated file (wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="91780-125">기계 학습 워크플로</span><span class="sxs-lookup"><span data-stu-id="91780-125">Machine learning workflow</span></span>

<span data-ttu-id="91780-126">이 자습서는 프로세스가 체계적으로 이동할 수 있도록 하는 기계 학습 워크플로를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="91780-126">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="91780-127">워크플로 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-127">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="91780-128">**문제 이해**</span><span class="sxs-lookup"><span data-stu-id="91780-128">**Understand the problem**</span></span>
2. <span data-ttu-id="91780-129">**데이터 준비**</span><span class="sxs-lookup"><span data-stu-id="91780-129">**Prepare your data**</span></span>
   * <span data-ttu-id="91780-130">**데이터 로드**</span><span class="sxs-lookup"><span data-stu-id="91780-130">**Load the data**</span></span>
   * <span data-ttu-id="91780-131">**기능 추출(데이터 변환)**</span><span class="sxs-lookup"><span data-stu-id="91780-131">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="91780-132">**빌드 및 학습**</span><span class="sxs-lookup"><span data-stu-id="91780-132">**Build and train**</span></span> 
   * <span data-ttu-id="91780-133">**모델 학습**</span><span class="sxs-lookup"><span data-stu-id="91780-133">**Train the model**</span></span>
   * <span data-ttu-id="91780-134">**모델 평가**</span><span class="sxs-lookup"><span data-stu-id="91780-134">**Evaluate the model**</span></span>
4. <span data-ttu-id="91780-135">**모델 배포**</span><span class="sxs-lookup"><span data-stu-id="91780-135">**Deploy Model**</span></span>
   * <span data-ttu-id="91780-136">**예측 모델 사용**</span><span class="sxs-lookup"><span data-stu-id="91780-136">**Use the Model to predict**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="91780-137">문제 이해</span><span class="sxs-lookup"><span data-stu-id="91780-137">Understand the problem</span></span>

<span data-ttu-id="91780-138">먼저 문제를 이해해야 하므로 모델 빌드 및 학습을 지원할 수 있는 부분으로 문제를 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-138">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="91780-139">문제를 구분하면 결과를 예측하고 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-139">Breaking the problem down allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="91780-140">이 자습서의 문제는 들어오는 웹 사이트 댓글 감정을 이해하여 적절한 작업을 수행하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-140">The problem for this tutorial is to understand incoming website comment sentiment to take the appropriate action.</span></span>

<span data-ttu-id="91780-141">모델 학습에 사용할 데이터의 감정 텍스트와 감정 값 및 평가 후 조작에 사용할 수 있는 예측 감정 값으로 문제를 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-141">You can break down the problem to the sentiment text and sentiment value for the data you want to train the model with, and a predicted sentiment value that you can evaluate and then use operationally.</span></span>

<span data-ttu-id="91780-142">그런 다음, 기계 학습 작업 선택에 도움이 되는 감정을 **확인**해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-142">You then need to **determine** the sentiment, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-algorithm"></a><span data-ttu-id="91780-143">적절한 기계 학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="91780-143">Select the appropriate machine learning algorithm</span></span>

<span data-ttu-id="91780-144">이 문제에서 다음 사실을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-144">With this problem, you know the following facts:</span></span>

<span data-ttu-id="91780-145">학습 데이터: 웹 사이트 댓글은 악의적(1) 또는 비악의적(0)(**감정**)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-145">Training data: website comments can be toxic (1) or not toxic (0) (**sentiment**).</span></span>
<span data-ttu-id="91780-146">다음 예제와 같이 새로운 웹 사이트 댓글의 **감정**을 악의적 또는 비악의적으로 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-146">Predict the **sentiment** of a new website comment, either toxic or not toxic, such as in the following examples:</span></span>

* <span data-ttu-id="91780-147">Wikipedia에 의미 없는 내용을 추가하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="91780-147">Please refrain from adding nonsense to Wikipedia.</span></span>
* <span data-ttu-id="91780-148">그는 최고이고 기사에 이 내용이 언급되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-148">He is the best, and the article should say that.</span></span>

<span data-ttu-id="91780-149">이 시나리오에서는 분류 기계 학습 알고리즘이 가장 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-149">The classification machine learning algorithm is best suited for this scenario.</span></span>

### <a name="about-the-classification-task"></a><span data-ttu-id="91780-150">분류 작업 정보</span><span class="sxs-lookup"><span data-stu-id="91780-150">About the classification task</span></span>

<span data-ttu-id="91780-151">분류는 데이터를 사용하여 데이터 항목 또는 행의 범주, 형식 또는 클래스를 **확인**하는 기계 학습 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-151">Classification is a machine learning algorithm that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="91780-152">예를 들어 분류를 사용하여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-152">For example, you can use classification to:</span></span>

* <span data-ttu-id="91780-153">감정을 긍정적 또는 부정적으로 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-153">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="91780-154">전자 메일을 스팸, 정크 또는 정상으로 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-154">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="91780-155">환자의 실험실 샘플이 종양성인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-155">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="91780-156">영업 캠페인에 응답하는 고객의 성향을 기준으로 고객을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-156">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="91780-157">일반적으로 분류 알고리즘은 다음 형식 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-157">Classification algorithms are frequently one of the following types:</span></span>

* <span data-ttu-id="91780-158">이진: A 또는 B.</span><span class="sxs-lookup"><span data-stu-id="91780-158">Binary: either A or B.</span></span>
* <span data-ttu-id="91780-159">다중 클래스: 단일 모델을 사용하여 예측할 수 있는 여러 범주.</span><span class="sxs-lookup"><span data-stu-id="91780-159">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="91780-160">콘솔 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="91780-160">Create a console application</span></span>

1. <span data-ttu-id="91780-161">Visual Studio 2017을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="91780-161">Open Visual Studio 2017.</span></span> <span data-ttu-id="91780-162">메뉴 모음에서 **파일** > **새로 만들기** > **프로젝트**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-162">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="91780-163">**새 프로젝트** 대화 상자에서 **Visual C#** 노드와 **.NET Core** 노드를 차례로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-163">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="91780-164">그런 다음 **콘솔 앱(.NET Core)** 프로젝트 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-164">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="91780-165">**이름** 텍스트 상자에 “SentimentAnalysis”를 입력한 다음, **확인** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-165">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="91780-166">프로젝트에서 *Data* 디렉터리를 만들어 데이터 집합 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-166">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="91780-167">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 폴더**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-167">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="91780-168">“Data”를 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="91780-168">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="91780-169">**Microsoft.ML NuGet 패키지**를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-169">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="91780-170">솔루션 탐색기에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **NuGet 패키지 관리**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-170">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="91780-171">“nuget.org”를 패키지 소스로 선택하고, [찾아보기] 탭을 선택하고, **Microsoft.ML**을 검색하고, 목록에서 해당 패키지를 선택하고, **설치** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-171">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="91780-172">**변경 내용 미리 보기** 대화 상자에서 **확인** 단추를 선택한 다음, 나열된 패키지의 사용 조건에 동의하는 경우 **라이선스 승인** 대화 상자에서 **동의함** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-172">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="91780-173">데이터 준비</span><span class="sxs-lookup"><span data-stu-id="91780-173">Prepare your data</span></span>

1. <span data-ttu-id="91780-174">[WikiPedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) 및 [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv) 데이터 세트를 다운로드하여 이전에 만든 *Data* 폴더에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-174">Download the [Wikipedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) and the [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="91780-175">첫 번째 데이터 세트는 기계 학습 모델을 교육하고 두 번째 데이터 세트는 모델이 얼마나 정확한지 평가하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-175">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="91780-176">솔루션 탐색기에서 각 \*.tsv 파일을 마우스 오른쪽 단추로 클릭하고 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-176">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="91780-177">**고급** 아래에서 **출력 디렉터리에 복사** 값을 **변경된 내용만 복사**로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-177">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="91780-178">클래스 만들기 및 경로 정의</span><span class="sxs-lookup"><span data-stu-id="91780-178">Create classes and define paths</span></span>

<span data-ttu-id="91780-179">*Program.cs* 파일 맨 위에 다음 추가 `using` 문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-179">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="91780-180">최근에 다운로드한 파일의 경로와 `TextLoader`의 전역 변수가 포함될 세 개의 전역 필드를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-180">You need to create three global fields to hold the paths to the recently downloaded files, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="91780-181">`_trainDataPath`에는 모델을 학습시키는 데 사용되는 데이터 세트의 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-181">`_trainDataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="91780-182">`_testDataPath`에는 모델을 평가하는 데 사용되는 데이터 세트의 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-182">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="91780-183">`_modelPath`에는 학습된 모델이 저장되는 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-183">`_modelPath` has the path where the trained model is saved.</span></span>
* <span data-ttu-id="91780-184">`_textLoader`는 데이터 세트를 로드하고 변환하는 데 사용되는 <xref:Microsoft.ML.Data.TextLoader>입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-184">`_textLoader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="91780-185">`Main` 메서드 바로 위의 줄에 다음 코드를 추가하여 해당 경로와 `_textLoader` 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-185">Add the following code to the line right above the `Main` method to specify those paths and the `_textLoader` variable:</span></span>

[!code-csharp[Declare global variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#2 "Declare global variables")]

<span data-ttu-id="91780-186">입력 데이터 및 예측에 대한 일부 클래스를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-186">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="91780-187">새 클래스를 프로젝트에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-187">Add a new class to your project:</span></span>

1. <span data-ttu-id="91780-188">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-188">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="91780-189">**새 항목 추가** 대화 상자에서 **클래스**를 선택하고 **이름** 필드를 *SentimentData.cs*로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-189">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="91780-190">그런 다음, **추가** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-190">Then, select the **Add** button.</span></span>

    <span data-ttu-id="91780-191">*SentimentData.cs* 파일이 코드 편집기에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="91780-191">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="91780-192">다음 `using` 문을 *SentimentData.cs*의 맨 위에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-192">Add the following `using` statement to the top of *SentimentData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#1 "Add necessary usings")]

<span data-ttu-id="91780-193">기존 클래스 정의를 제거하고 두 개의 클래스 `SentimentData` 및 `SentimentPrediction`가 있는 다음 코드를 *SentimentData.cs* 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-193">Remove the existing class definition and add the following code, which has two classes `SentimentData` and `SentimentPrediction`, to the *SentimentData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#2 "Declare data record types")]

<span data-ttu-id="91780-194">`SentimentData`는 입력 데이터 세트 클래스이며 긍정적 또는 부정적 감정 값을 가진 `float`(`Sentiment`) 및 댓글 문자열(`SentimentText`)을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-194">`SentimentData` is the input dataset class and has a `float` (`Sentiment`) that has a value for sentiment of either positive or negative, and a string for the comment (`SentimentText`).</span></span> <span data-ttu-id="91780-195">두 필드에 모두 `Column` 특성이 연결되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-195">Both fields have `Column` attributes attached to them.</span></span> <span data-ttu-id="91780-196">이 특성은 데이터 파일의 각 필드 순서와 어떤 것이 `Label` 필드인지 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-196">This attribute describes the order of each field in the data file, and which is the `Label` field.</span></span> <span data-ttu-id="91780-197">`SentimentPrediction`은 모델이 학습된 후 예측에 사용되는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-197">`SentimentPrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="91780-198">여기에는 단일 부울(`Sentiment`)과 `PredictedLabel` `ColumnName` 특성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-198">It has a single boolean (`Sentiment`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="91780-199">`Label`은 세트를 만들고 학습시키는 데 사용되며 두 번째 데이터 세트와 함께 모델을 평가하는 데도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-199">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="91780-200">`PredictedLabel`은 예측 및 평가 중에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-200">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="91780-201">평가를 위해 학습 데이터가 있는 입력, 예측 값 및 모델이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-201">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="91780-202">ML .NET를 사용하여 모델을 작성하는 경우 먼저 `MLContext`를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-202">When building a model with ML.NET you start by creating an `MLContext`.</span></span> <span data-ttu-id="91780-203">이는 Entity Framework에서 `DbContext`를 사용하는 것과 개념이 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-203">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="91780-204">환경은 예외 추적 및 로깅에 사용할 수 있는 ML 작업의 컨텍스트를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-204">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="91780-205">Main에서 변수 초기화</span><span class="sxs-lookup"><span data-stu-id="91780-205">Initialize variables in Main</span></span>

<span data-ttu-id="91780-206">`mlContext`라는 변수를 만들고 `MLContext`의 새 인스턴스로 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-206">Create a variable called `mlContext` and initialize it with a new instance of `MLContext`.</span></span>  <span data-ttu-id="91780-207">`Main` 메서드에서 `Console.WriteLine("Hello World!")` 줄을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="91780-207">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#3 "Create the ML Context")]

<span data-ttu-id="91780-208">다음으로, 데이터 로드를 설정하려면 `_textLoader` 전역 변수를 다시 사용하기 위해 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-208">Next, to setup for data loading initialize the `_textLoader` global variable in order to reuse it.</span></span>  <span data-ttu-id="91780-209">`MLContext.Data.CreateTextLoader`를 사용하여 `TextLoader`를 만드는 경우 필요한 컨텍스트 및 사용자 지정을 가능하게 하는 <xref:Microsoft.ML.Data.TextLoader.Arguments> 클래스를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-209">When you create a `TextLoader` using  `MLContext.Data.CreateTextLoader`, you pass in the context needed and the <xref:Microsoft.ML.Data.TextLoader.Arguments> class which enables customization.</span></span>

 <span data-ttu-id="91780-210">모든 열 이름과 열 형식을 포함하는 <xref:Microsoft.ML.Data.TextLoader.Column> 개체 배열을 로더에 전달하여 데이터 스키마를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-210">Specify the data schema by passing an array of <xref:Microsoft.ML.Data.TextLoader.Column> objects to the loader containing all the column names and their types.</span></span> <span data-ttu-id="91780-211">이전에 `SentimentData` 클래스를 만들 때 데이터 스키마를 정의했습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-211">You defined the data schema previously when you created our `SentimentData` class.</span></span> <span data-ttu-id="91780-212">스키마의 첫 번째 열(Label)은 <xref:System.Boolean>(예측)이고 두 번째 열(SentimentText)은 감정을 예측하는 데 사용되는 텍스트/문자열 형식의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-212">For our schema, the first column (Label) is a <xref:System.Boolean> (the prediction) and the second column (SentimentText) is the feature of type text/string used for predicting the sentiment.</span></span>
<span data-ttu-id="91780-213">`TextLoader` 클래스는 완전히 초기화된 <xref:Microsoft.ML.Data.TextLoader>를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-213">The `TextLoader` class returns a fully initialized <xref:Microsoft.ML.Data.TextLoader></span></span>  

<span data-ttu-id="91780-214">필요한 데이터 세트에 다시 사용하기 위해 `_textLoader` 글로벌 변수를 초기화하려면 `mlContext` 초기화 뒤에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-214">To initialize the `_textLoader` global variable in order to reuse it for the needed datasets, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[initTextLoader](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#4 "Initialize the TextLoader")]

<span data-ttu-id="91780-215">`Main` 메서드에 아래 코드를 다음 코드 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-215">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[Train](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#5 "Train your model")]

<span data-ttu-id="91780-216">`Train` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-216">The `Train` method executes the following tasks:</span></span>

* <span data-ttu-id="91780-217">데이터를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-217">Loads the data.</span></span>
* <span data-ttu-id="91780-218">데이터를 추출하고 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-218">Extracts and transforms the data.</span></span>
* <span data-ttu-id="91780-219">모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="91780-219">Trains the model.</span></span>
* <span data-ttu-id="91780-220">테스트 데이터를 기반으로 감정을 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-220">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="91780-221">모델을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-221">Returns the model.</span></span>

<span data-ttu-id="91780-222">다음 코드를 사용하여 `Main` 메서드 바로 뒤에 `Train` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-222">Create the `Train` method, just after the `Main` method, using the following code:</span></span>

```csharp
 public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

<span data-ttu-id="91780-223">두 개의 매개 변수가 Train 메서드에 전달됩니다. 하나는 컨텍스트(`mlContext`)를 나타내는 `MLContext`이고, 다른 하나는 데이터 세트 경로(`dataPath`)를 나타내는 <xref:System.String>입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-223">Notice that two parameters are passed into the Train method; a `MLContext` for the context (`mlContext`), and a <xref:System.String> for the dataset path (`dataPath`).</span></span> <span data-ttu-id="91780-224">학습 및 테스트를 위해 이 메서드를 두 번 이상 사용하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-224">You're going to use this method more than once for training and testing.</span></span>

## <a name="load-the-data"></a><span data-ttu-id="91780-225">데이터 로드</span><span class="sxs-lookup"><span data-stu-id="91780-225">Load the data</span></span>

<span data-ttu-id="91780-226">`dataPath` 매개 변수에 `_textLoader` 전역 변수를 사용하여 데이터를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-226">You'll load the data using the `_textLoader` global variable with the `dataPath` parameter.</span></span> <span data-ttu-id="91780-227"><xref:Microsoft.Data.DataView.IDataView>가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-227">It returns a <xref:Microsoft.Data.DataView.IDataView>.</span></span> <span data-ttu-id="91780-228">`Transforms`의 입력 및 출력으로 사용되는 `DataView`는 `LINQ`의 `IEnumerable`과 비슷한 기본적인 데이터 파이프라인 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-228">As the input and output of `Transforms`, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="91780-229">ML.NET에서 데이터는 SQL 뷰와 유사합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-229">In ML.NET, data is similar to a SQL view.</span></span> <span data-ttu-id="91780-230">지연 계산되고, 스키마화되며, 형식이 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="91780-230">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="91780-231">개체가 파이프라인의 첫 번째 부분이며 데이터를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-231">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="91780-232">이 자습서에서 개체는 댓글과 해당하는 악의적 또는 비악의적 감정을 포함하는 데이터 세트를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-232">For this tutorial, it loads a dataset with comments and corresponding toxic or non toxic sentiment.</span></span> <span data-ttu-id="91780-233">이 데이터 세트는 모델을 만들고 학습시키는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-233">This is used to create the model, and train it.</span></span>

 <span data-ttu-id="91780-234">다음 코드를 `Train` 메서드의 첫 번째 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-234">Add the following code as the first line of the `Train` method:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#6 "loading training dataset")]

## <a name="extract-and-transform-the-data"></a><span data-ttu-id="91780-235">데이터 추출 및 변환</span><span class="sxs-lookup"><span data-stu-id="91780-235">Extract and transform the data</span></span>

<span data-ttu-id="91780-236">데이터 전처리 및 정리는 데이터 세트가 기계 학습에 효과적으로 사용되기 전에 수행되는 중요한 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-236">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="91780-237">원시 데이터는 종종 정리되지 않고 불안정하며 값이 누락될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-237">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="91780-238">이러한 모델링 작업 없이 데이터를 사용하면 잘못된 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-238">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="91780-239">ML.NET의 변환 파이프라인은 학습 또는 테스트 전에 데이터에 적용되는 사용자 지정 변환 세트로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-239">ML.NET's transform pipelines compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="91780-240">변환의 기본 목적은 데이터 [기능화](../resources/glossary.md#feature-engineering)입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-240">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="91780-241">기계 학습 알고리즘은 [기능화된](../resources/glossary.md#feature) 데이터를 인식하므로 다음 단계는 텍스트 데이터를 ML 알고리즘이 인식하는 형식으로 변환하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-241">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="91780-242">해당 형식은 [숫자 벡터](../resources/glossary.md#numerical-feature-vector)입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-242">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="91780-243">다음으로, 텍스트(`SentimentText`) 열을 기계 학습 알고리즘에서 사용되는 `Features`라는 숫자 벡터로 기능화하는 `mlContext.Transforms.Text.FeaturizeText`를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-243">Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text column (`SentimentText`) column into a numeric vector called `Features` used by the machine learning algorithm.</span></span> <span data-ttu-id="91780-244">이는 실제로 파이프라인이 될 <xref:Microsoft.ML.Data.EstimatorChain%601>을 반환하는 래퍼 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-244">This is a wrapper call that returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="91780-245">이 학습자를 `EstimatorChain`에 추가할 때 `pipeline`으로 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-245">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="91780-246">아래 코드를 다음 코드 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-246">Add this as the next line of code:</span></span>

[!code-csharp[TextFeaturizingEstimator](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#7 "Add a TextFeaturizingEstimator")]

<span data-ttu-id="91780-247">이것이 전처리/기능화 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-247">This is the preprocessing/featurization step.</span></span> <span data-ttu-id="91780-248">ML.NET에서 사용 가능한 추가 구성 요소를 사용하면 모델에서 더 나은 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-248">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="91780-249">학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="91780-249">Choose a learning algorithm</span></span>

<span data-ttu-id="91780-250">학습자를 추가하려면 <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer> 개체를 반환하는 `mlContext.Transforms.Text.FeaturizeText` 래퍼 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-250">To add the trainer, call the `mlContext.Transforms.Text.FeaturizeText` wrapper method which returns a <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer> object.</span></span> <span data-ttu-id="91780-251">이 개체는 이 파이프라인에서 사용할 의사 결정 트리 학습자입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-251">This is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="91780-252">`FastTreeBinaryClassificationTrainer`는 `pipeline`에 추가되며, 기록 데이터에서 학습할 기능화된 `SentimentText`(`Features`) 및 `Label` 입력 매개 변수를 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-252">The `FastTreeBinaryClassificationTrainer` is appended to the `pipeline` and accepts the featurized `SentimentText` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="91780-253">`Train` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-253">Add the following code to the `Train` method:</span></span>

[!code-csharp[FastTreeBinaryClassificationTrainer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#8 "Add a FastTreeBinaryClassificationTrainer")]

## <a name="train-the-model"></a><span data-ttu-id="91780-254">모델 학습</span><span class="sxs-lookup"><span data-stu-id="91780-254">Train the model</span></span>

<span data-ttu-id="91780-255">로드되고 변환된 데이터 세트를 기반으로 <xref:Microsoft.ML.Data.TransformerChain%601> 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="91780-255">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="91780-256">추정기가 정의된 후, 이미 로드된 학습 데이터를 제공하는 동시에 <xref:Microsoft.ML.Data.EstimatorChain%601.Fit*>을 사용하여 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="91780-256">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit*> while providing the already loaded training data.</span></span> <span data-ttu-id="91780-257">그러면 예측에 사용할 모델이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-257">This returns a model to use for predictions.</span></span> <span data-ttu-id="91780-258">`pipeline.Fit()`은 파이프라인을 학습시키고, 전달된 `DataView`에 따라 `Transformer`를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-258">`pipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="91780-259">이 문제가 발생할 때까지 실험이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-259">The experiment is not executed until this happens.</span></span>

<span data-ttu-id="91780-260">`Train` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-260">Add the following code to the `Train` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#9 "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="91780-261">평가에 사용하기 위해 학습된 모델 저장 및 반환</span><span class="sxs-lookup"><span data-stu-id="91780-261">Save and Return the model trained to use for evaluation</span></span>

<span data-ttu-id="91780-262">이 시점에는 기존 또는 새 .NET 애플리케이션에 통합할 수 있는 <xref:Microsoft.ML.Data.TransformerChain%601> 형식의 모델이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-262">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="91780-263">`Train` 메서드의 끝에 모델을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-263">Return the model at the end of the `Train` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#10 "Return the model")]

## <a name="evaluate-the-model"></a><span data-ttu-id="91780-264">모델 평가</span><span class="sxs-lookup"><span data-stu-id="91780-264">Evaluate the model</span></span>

<span data-ttu-id="91780-265">이제 모델을 만들고 학습시켰으므로 품질 보증 및 유효성 검사를 위해 다른 데이터 세트를 사용하여 평가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-265">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="91780-266">`Evaluate` 메서드에서는 `Train`에서 만들어진 모델을 전달하여 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-266">In the `Evaluate` method, the model created in `Train` is passed in to be evaluated.</span></span> <span data-ttu-id="91780-267">다음 코드와 같이 `Train` 바로 뒤에 `Evaluate` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-267">Create the `Evaluate` method, just after `Train`, as in the following code:</span></span>

```csharp
public static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="91780-268">`Evaluate` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-268">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="91780-269">테스트 데이터 세트를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-269">Loads the test dataset.</span></span>
* <span data-ttu-id="91780-270">이진 평가자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-270">Creates the binary evaluator.</span></span>
* <span data-ttu-id="91780-271">모델을 평가하고 메트릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-271">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="91780-272">메트릭을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-272">Displays the metrics.</span></span>

<span data-ttu-id="91780-273">다음 코드를 사용하여 `Train` 메서드 호출 바로 아래에 `Main` 메서드의 새 메서드 호출을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-273">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#11 "Call the Evaluate method")]

<span data-ttu-id="91780-274">이전에 초기화한 `_textLoader` 글로벌 변수를 `_testDataPath` 글로벌 필드에 사용하여 테스트 데이터 세트를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-274">You'll load the test dataset using the previously initialized  `_textLoader` global variable with the `_testDataPath` global field.</span></span> <span data-ttu-id="91780-275">이 데이터 세트를 품질 검사로 사용하여 모델을 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-275">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="91780-276">`Evaluate` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-276">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#12 "Load the test dataset")]

<span data-ttu-id="91780-277">다음으로, 기계 학습 `model` 매개 변수(변환기)를 사용하여 기능을 입력하고 예측을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-277">Next, you'll use the machine learning `model` parameter (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="91780-278">`Evaluate` 메서드에 아래 코드를 다음 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-278">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#13 "Predict using the Transformer")]

<span data-ttu-id="91780-279">`BinaryClassificationContext.Evaluate` 메서드는 지정된 데이터 세트를 사용하여 `PredictionModel`에 대한 품질 메트릭을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-279">The `BinaryClassificationContext.Evaluate` method computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="91780-280">이진 분류 평가자가 계산한 전체 메트릭이 포함된 `BinaryClassificationEvaluator.CalibratedResult` 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-280">It returns a `BinaryClassificationEvaluator.CalibratedResult` object contains the overall metrics computed by binary classification evaluators.</span></span> <span data-ttu-id="91780-281">모델의 품질을 확인하기 위해 이러한 메트릭을 표시하려면 먼저 메트릭을 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-281">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="91780-282">`Evaluate` 메서드에 아래 코드를 다음 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-282">Add the following code as the next line in the `Evaluate` method:</span></span>

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#14 "Compute Metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="91780-283">모델 유효성 검사를 위해 메트릭 표시</span><span class="sxs-lookup"><span data-stu-id="91780-283">Displaying the metrics for model validation</span></span>

<span data-ttu-id="91780-284">다음 코드를 사용하여 메트릭을 표시하고, 결과를 공유한 다음, 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-284">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#15 "Display selected metrics")]

<span data-ttu-id="91780-285">반환하기 전에 모델을 .zip 파일로 저장하려면 `SaveModelAsFile` 메서드를 호출하는 아래 코드를 `Evaluate`에 다음 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-285">To save your model to a .zip file before returning, add the following code to call the `SaveModelAsFile` method as the next line in `Evaluate`:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#23 "Save the model")]

## <a name="save-the-model-as-azip-file"></a><span data-ttu-id="91780-286">모델을 .zip 파일로 저장</span><span class="sxs-lookup"><span data-stu-id="91780-286">Save the model as a.zip file</span></span>

<span data-ttu-id="91780-287">다음 코드를 사용하여 `Evaluate` 메서드 바로 뒤에 `SaveModelAsFile` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-287">Create the `SaveModelAsFile` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="91780-288">`SaveModelAsFile` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-288">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="91780-289">모델을 .zip 파일로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-289">Saves the model as a .zip file.</span></span>

<span data-ttu-id="91780-290">다음으로, 다른 애플리케이션에서 다시 사용하고 이용할 수 있도록 모델을 저장하는 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-290">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="91780-291">`ITransformer`에는 `_modelPath` 전역 필드를 사용하는 <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> 메서드와 <xref:System.IO.Stream>이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-291">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="91780-292">이 파일을 zip 파일로 저장하기 위해 `SaveTo` 메서드를 호출하기 직전에 `FileStream`을 만들겠습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-292">To save this as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="91780-293">`SaveModelAsFile` 메서드에 아래 코드를 다음 줄로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-293">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#24 "Add the SaveTo Method")]
<span data-ttu-id="91780-294">로드된 모델을 통해 배포 및 예측. 다음 코드를 사용하여 `_modelPath`가 포함된 콘솔 메시지를 작성하여 파일이 작성된 위치를 표시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-294">Deploy and Predict with a loaded model You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="91780-295">저장된 모델을 사용하여 테스트 데이터 결과 예측</span><span class="sxs-lookup"><span data-stu-id="91780-295">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="91780-296">다음 코드를 사용하여 `Evaluate` 메서드 바로 뒤에 `Predict` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-296">Create the `Predict` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void Predict(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="91780-297">`Predict` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-297">The `Predict` method executes the following tasks:</span></span>

* <span data-ttu-id="91780-298">테스트 데이터의 단일 댓글을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-298">Creates a single comment of test data.</span></span>
* <span data-ttu-id="91780-299">테스트 데이터를 기반으로 감정을 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-299">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="91780-300">보고를 위해 테스트 데이터 및 예측을 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-300">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="91780-301">예측 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-301">Displays the predicted results.</span></span>

<span data-ttu-id="91780-302">다음 코드를 사용하여 `Evaluate` 메서드 호출 바로 아래에 `Main` 메서드의 새 메서드 호출을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-302">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallPredict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#16 "Call the Predict method")]

<span data-ttu-id="91780-303">`model`은 여러 데이터 행에서 작동하는 `transformer`이지만, 일반적인 프로덕션 시나리오에서는 개별 예제에 대한 예측이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-303">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="91780-304"><xref:Microsoft.ML.PredictionEngine%602>은 `CreatePredictionEngine` 메서드에서 반환되는 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="91780-304">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="91780-305">다음 코드를 추가하여 `PredictionEngine`을 `Predict` 메서드의 첫째 줄로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-305">Let's add the following code to create the `PredictionEngine` as the first line in the `Predict` Method:</span></span>

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#17 "Create the PredictionEngine")]
  
<span data-ttu-id="91780-306">`SentimentData` 인스턴스를 만들어 댓글을 추가하여 `Predict` 메서드에서 학습된 모델의 예측을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-306">Add a comment to test the trained model's prediction in the `Predict` method by creating an instance of `SentimentData`:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#18 "Create test data for single prediction")]

 <span data-ttu-id="91780-307">해당 메서드를 사용하여 댓글 데이터의 단일 인스턴스에서 악의적 또는 비악의적 감정을 예측할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-307">You can use that to predict the Toxic or Non Toxic sentiment of a single instance of the comment data.</span></span> <span data-ttu-id="91780-308">예측을 가져오려면 데이터에 대해 <xref:Microsoft.ML.PredictionEngine%602.Predict%2A>을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-308">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="91780-309">입력 데이터는 문자열이고 모델은 기능화를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-309">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="91780-310">파이프라인은 학습 및 예측 중에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-310">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="91780-311">특별히 예측을 위해 전처리/기능화 코드를 작성할 필요가 없고 동일한 API가 배치 및 일회성 예측을 둘 다 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-311">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#19 "Create a prediction of sentiment")]

### <a name="using-the-model-prediction"></a><span data-ttu-id="91780-312">모델 사용: prediction</span><span class="sxs-lookup"><span data-stu-id="91780-312">Using the model: prediction</span></span>

<span data-ttu-id="91780-313">결과를 공유하고 이에 따라 작업을 수행하기 위해 `SentimentText` 및 해당 감정 예측을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-313">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="91780-314">이것을 반환된 데이터를 운영 정책의 일부로 사용하는 연산화라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-314">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="91780-315">다음 <xref:System.Console.WriteLine?displayProperty=nameWithType> 코드를 사용하여 결과 표시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-315">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#20 "Display prediction output")]

## <a name="deploy-and-predict-with-a-loaded-model"></a><span data-ttu-id="91780-316">로드된 모델을 통해 배포 및 예측</span><span class="sxs-lookup"><span data-stu-id="91780-316">Deploy and Predict with a loaded model</span></span>

<span data-ttu-id="91780-317">다음 코드를 사용하여 `SaveModelAsFile` 메서드 바로 앞에 `PredictWithModelLoadedFromFile` 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-317">Create the `PredictWithModelLoadedFromFile` method, just before the `SaveModelAsFile` method, using the following code:</span></span>

```csharp
public static void PredictWithModelLoadedFromFile(MLContext mlContext)
{

}
```

<span data-ttu-id="91780-318">`PredictWithModelLoadedFromFile` 메서드는 다음 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-318">The `PredictWithModelLoadedFromFile` method executes the following tasks:</span></span>

* <span data-ttu-id="91780-319">일괄 처리 테스트 데이터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-319">Creates batch test data.</span></span>
* <span data-ttu-id="91780-320">테스트 데이터를 기반으로 감정을 예측합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-320">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="91780-321">보고를 위해 테스트 데이터 및 예측을 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-321">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="91780-322">예측 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-322">Displays the predicted results.</span></span>

<span data-ttu-id="91780-323">다음 코드를 사용하여 `Predict` 메서드 호출 바로 아래에 `Main` 메서드의 새 메서드 호출을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-323">Add a call to the new method from the `Main` method, right under the `Predict` method call, using the following code:</span></span>

[!code-csharp[CallPredictModelLoaded](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#25 "Call the PredictWithModelLoadedFromFile method")]

<span data-ttu-id="91780-324">몇몇 댓글을 추가하여 `PredictWithModelLoadedFromFile` 메서드에서 학습된 모델의 예측을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-324">Add some comments to test the trained model's predictions in the `PredictWithModelLoadedFromFile` method:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#26 "Create test data for predictions")]

<span data-ttu-id="91780-325">모델 로드</span><span class="sxs-lookup"><span data-stu-id="91780-325">Load the model</span></span>

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#27 "Load the model")]

<span data-ttu-id="91780-326">이제 모델이 있으므로 해당 모델을 통해 <xref:Microsoft.ML.Core.Data.ITransformer.Transform%2A> 메서드를 사용하여 댓글 데이터의 악의적 또는 비악의적 감정을 예측할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-326">Now that you have a model, you can use that to predict the Toxic or Non Toxic sentiment of the comment data using the <xref:Microsoft.ML.Core.Data.ITransformer.Transform%2A> method.</span></span> <span data-ttu-id="91780-327">예측을 가져오려면 새 데이터에서 `Predict`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-327">To get a prediction, use `Predict` on new data.</span></span> <span data-ttu-id="91780-328">입력 데이터는 문자열이고 모델은 기능화를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-328">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="91780-329">파이프라인은 학습 및 예측 중에 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91780-329">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="91780-330">특별히 예측을 위해 전처리/기능화 코드를 작성할 필요가 없고 동일한 API가 배치 및 일회성 예측을 둘 다 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-330">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="91780-331">예측을 위해 `PredictWithModelLoadedFromFile` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-331">Add the following code to the `PredictWithModelLoadedFromFile` method for the predictions:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#28 "Create predictions of sentiments")]

### <a name="using-the-loaded-model-for-prediction"></a><span data-ttu-id="91780-332">예측에 로드된 모델 사용</span><span class="sxs-lookup"><span data-stu-id="91780-332">Using the loaded model for prediction</span></span>

<span data-ttu-id="91780-333">결과를 공유하고 이에 따라 작업을 수행하기 위해 `SentimentText` 및 해당 감정 예측을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-333">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="91780-334">이것을 반환된 데이터를 운영 정책의 일부로 사용하는 연산화라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-334">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="91780-335">다음 <xref:System.Console.WriteLine?displayProperty=nameWithType> 코드를 사용하여 결과에 대한 헤더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91780-335">Create a header for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#29 "Display prediction outputs")]

<span data-ttu-id="91780-336">예측 결과를 표시하기 전에 감정과 예측을 결합하여 예측된 감정이 있는 원래 주석을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-336">Before displaying the predicted results, combine the sentiment and prediction together to see the original comment with its predicted sentiment.</span></span> <span data-ttu-id="91780-337">다음 코드는 <xref:System.Linq.Enumerable.Zip%2A> 메서드를 사용하여 작업이 수행되도록 하므로, 다음으로 해당 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-337">The following code uses the <xref:System.Linq.Enumerable.Zip%2A> method to make that happen, so add that code next:</span></span>

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#30 "Build the pairs of sentiment data and predictions")]

<span data-ttu-id="91780-338">이제 `SentimentText` 및 `Sentiment`를 클래스로 결합했으므로 <xref:System.Console.WriteLine?displayProperty=nameWithType> 메서드를 사용하여 결과를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-338">Now that you've combined the `SentimentText` and `Sentiment` into a class, you can display the results using the <xref:System.Console.WriteLine?displayProperty=nameWithType> method:</span></span>

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#31 "Display the predictions")]

<span data-ttu-id="91780-339">유추된 튜플 요소 이름은 C# 7.1의 새로운 기능이고 프로젝트의 기본 언어 버전은 C# 7.0이므로 언어 버전을 C# 7.1 이상으로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-339">Because inferred tuple element names are a new feature in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span>
<span data-ttu-id="91780-340">이 작업을 하려면 **솔루션 탐색기**에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-340">To do that, right-click on the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="91780-341">**빌드** 탭을 선택하고 **고급** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-341">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="91780-342">드롭다운에서 **C# 7.1**(또는 이상 버전)을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-342">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="91780-343">**확인** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-343">Select the **OK** button.</span></span>

## <a name="results"></a><span data-ttu-id="91780-344">결과</span><span class="sxs-lookup"><span data-stu-id="91780-344">Results</span></span>

<span data-ttu-id="91780-345">다음과 같은 결과가 나타나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-345">Your results should be similar to the following.</span></span> <span data-ttu-id="91780-346">파이프라인이 처리할 때 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="91780-346">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="91780-347">경고 또는 메시지 처리를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-347">You may see warnings, or processing messages.</span></span> <span data-ttu-id="91780-348">이해하기 쉽도록 이러한 결과는 다음 결과에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-348">These have been removed from the following results for clarity.</span></span>

```console
Model quality metrics evaluation
--------------------------------
Accuracy: 94.44%
Auc: 98.77%
F1Score: 94.74%
=============== End of model evaluation ===============

=============== Prediction Test of model with a single sample and test dataset ===============

Sentiment: This is a very rude movie | Prediction: Toxic | Probability: 0.5297049
=============== End of Predictions ===============

=============== New iteration of Model ===============
=============== Create and Train the Model ===============
=============== End of training ===============


The model is saved to: C:\Tutorial\SentimentAnalysis\bin\Debug\netcoreapp2.1\Data\Model.zip

=============== Prediction Test of loaded model with a multiple sample ===============

Sentiment: This is a very rude movie | Prediction: Toxic | Probability: 0.4585565
Sentiment: I love this article. | Prediction: Not Toxic | Probability: 0.09454837

```

<span data-ttu-id="91780-349">지금까지</span><span class="sxs-lookup"><span data-stu-id="91780-349">Congratulations!</span></span> <span data-ttu-id="91780-350">이제 메시지 감정을 분류하고 예측하기 위한 기계 학습 모델을 성공적으로 빌드했습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-350">You've now successfully built a machine learning model for classifying and predicting messages sentiment.</span></span> <span data-ttu-id="91780-351">[dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) 리포지토리에서 이 자습서의 소스 코드를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-351">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="91780-352">다음 단계</span><span class="sxs-lookup"><span data-stu-id="91780-352">Next steps</span></span>

<span data-ttu-id="91780-353">본 자습서에서는 다음 작업에 관한 방법을 학습했습니다.</span><span class="sxs-lookup"><span data-stu-id="91780-353">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="91780-354">문제 이해</span><span class="sxs-lookup"><span data-stu-id="91780-354">Understand the problem</span></span>
> * <span data-ttu-id="91780-355">적절한 기계 학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="91780-355">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="91780-356">데이터 준비</span><span class="sxs-lookup"><span data-stu-id="91780-356">Prepare your data</span></span>
> * <span data-ttu-id="91780-357">데이터 변환</span><span class="sxs-lookup"><span data-stu-id="91780-357">Transform the data</span></span>
> * <span data-ttu-id="91780-358">모델 학습</span><span class="sxs-lookup"><span data-stu-id="91780-358">Train the model</span></span>
> * <span data-ttu-id="91780-359">모델 평가</span><span class="sxs-lookup"><span data-stu-id="91780-359">Evaluate the model</span></span>
> * <span data-ttu-id="91780-360">학습된 모델을 통해 예측</span><span class="sxs-lookup"><span data-stu-id="91780-360">Predict with the trained model</span></span>
> * <span data-ttu-id="91780-361">로드된 모델을 통해 배포 및 예측</span><span class="sxs-lookup"><span data-stu-id="91780-361">Deploy and Predict with a loaded model</span></span>

<span data-ttu-id="91780-362">다음 자습서로 이동하여 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="91780-362">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="91780-363">문제 분류</span><span class="sxs-lookup"><span data-stu-id="91780-363">Issue Classification</span></span>](github-issue-classification.md)
