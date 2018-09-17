---
title: ML.NET을 사용하여 뉴욕 택시 요금 예측(회귀)
description: 회귀 시나리오에서 ML.NET을 사용하는 방법을 알아봅니다.
author: aditidugar
ms.author: johalex
ms.date: 07/02/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 133b7ad17a98e4eea510f1704555b690b98e9091
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44252846"
---
# <a name="tutorial-use-mlnet-to-predict-new-york-taxi-fares-regression"></a><span data-ttu-id="ade4f-103">자습서: ML.NET을 사용하여 뉴욕 택시 요금 예측(회귀)</span><span class="sxs-lookup"><span data-stu-id="ade4f-103">Tutorial: Use ML.NET to predict New York taxi fares (regression)</span></span>

> [!NOTE]
> <span data-ttu-id="ade4f-104">이 항목은 현재 미리 보기로 제공되는 ML.NET을 참조하며, 자료는 변경될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="ade4f-105">자세한 내용은 [ML.NET 소개](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ade4f-105">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="ade4f-106">이 자습서에서는 ML.NET을 사용하여 뉴욕시 택시 요금을 예측하기 위한 [회귀 모델](../resources/glossary.md#regression)을 빌드하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-106">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting New York City taxi fares.</span></span>

<span data-ttu-id="ade4f-107">이 자습서에서는 다음 방법을 학습합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="ade4f-108">문제 이해</span><span class="sxs-lookup"><span data-stu-id="ade4f-108">Understand the problem</span></span>
> * <span data-ttu-id="ade4f-109">적절한 기계 학습 작업 선택</span><span class="sxs-lookup"><span data-stu-id="ade4f-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="ade4f-110">데이터 준비 및 이해</span><span class="sxs-lookup"><span data-stu-id="ade4f-110">Prepare and understand the data</span></span>
> * <span data-ttu-id="ade4f-111">학습 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="ade4f-111">Create a learning pipeline</span></span>
> * <span data-ttu-id="ade4f-112">데이터 로드 및 변환</span><span class="sxs-lookup"><span data-stu-id="ade4f-112">Load and transform the data</span></span>
> * <span data-ttu-id="ade4f-113">학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="ade4f-113">Choose a learning algorithm</span></span>
> * <span data-ttu-id="ade4f-114">모델 학습</span><span class="sxs-lookup"><span data-stu-id="ade4f-114">Train the model</span></span>
> * <span data-ttu-id="ade4f-115">모델 평가</span><span class="sxs-lookup"><span data-stu-id="ade4f-115">Evaluate the model</span></span>
> * <span data-ttu-id="ade4f-116">예측에 모델 사용</span><span class="sxs-lookup"><span data-stu-id="ade4f-116">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ade4f-117">전제 조건</span><span class="sxs-lookup"><span data-stu-id="ade4f-117">Prerequisites</span></span>

* <span data-ttu-id="ade4f-118">“.NET Core 플랫폼 간 개발” 워크로드가 설치된 [Visual Studio 2017 15.6 이상](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).</span><span class="sxs-lookup"><span data-stu-id="ade4f-118">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="ade4f-119">문제 이해</span><span class="sxs-lookup"><span data-stu-id="ade4f-119">Understand the problem</span></span>

<span data-ttu-id="ade4f-120">이 문제는 뉴욕시의 택시 요금 예측에 관한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-120">This problem is about predicting the fare of a taxi trip in New York City.</span></span> <span data-ttu-id="ade4f-121">처음에는 요금이 단순히 주행 거리에 따라 결정되는 것처럼 보일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-121">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="ade4f-122">그러나 뉴욕 택시 업체는 추가 승객 또는 현금 대신 신용 카드 결제 등의 다른 요소를 고려하여 다양한 금액을 청구합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-122">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="ade4f-123">적절한 기계 학습 작업 선택</span><span class="sxs-lookup"><span data-stu-id="ade4f-123">Select the appropriate machine learning task</span></span>

<span data-ttu-id="ade4f-124">데이터 집합의 기타 요인에 따라 실제 값인 가격 값을 예측하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-124">You want to predict the price value, which is a real value, based on the other factors in the data set.</span></span> <span data-ttu-id="ade4f-125">이렇게 하려면 [회귀](../resources/glossary.md#regression) 기계 학습 작업을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-125">To do that you choose a [regression](../resources/glossary.md#regression) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="ade4f-126">콘솔 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="ade4f-126">Create a console application</span></span>

1. <span data-ttu-id="ade4f-127">Visual Studio 2017을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-127">Open Visual Studio 2017.</span></span> <span data-ttu-id="ade4f-128">메뉴 모음에서 **파일** > **새로 만들기** > **프로젝트**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-128">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="ade4f-129">**새 프로젝트** 대화 상자에서 **Visual C#** 노드와 **.NET Core** 노드를 차례로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-129">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="ade4f-130">그런 다음 **콘솔 앱(.NET Core)** 프로젝트 템플릿을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-130">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="ade4f-131">**이름** 텍스트 상자에 “TaxiFarePrediction”을 입력하고 **확인** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-131">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

1. <span data-ttu-id="ade4f-132">프로젝트에서 *Data* 디렉터리를 만들어 데이터 집합과 모델 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-132">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="ade4f-133">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 폴더**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-133">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="ade4f-134">“Data”를 입력하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-134">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="ade4f-135">**Microsoft.ML** NuGet 패키지를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-135">Install the **Microsoft.ML** NuGet Package:</span></span>

    <span data-ttu-id="ade4f-136">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **NuGet 패키지 관리**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-136">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="ade4f-137">“nuget.org”를 패키지 소스로 선택하고, **찾아보기** 탭을 선택하고, **Microsoft.ML**을 검색하고, 목록에서 해당 패키지를 선택하고, **설치** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-137">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="ade4f-138">**변경 내용 미리 보기** 대화 상자에서 **확인** 단추를 선택한 다음, 나열된 패키지의 사용 조건에 동의하는 경우 **라이선스 승인** 대화 상자에서 **동의함** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-138">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-and-understand-the-data"></a><span data-ttu-id="ade4f-139">데이터 준비 및 이해</span><span class="sxs-lookup"><span data-stu-id="ade4f-139">Prepare and understand the data</span></span>

1. <span data-ttu-id="ade4f-140">[taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) 및 [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) 데이터 집합을 다운로드하여 이전 단계에서 만든 *Data* 폴더에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-140">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="ade4f-141">이러한 데이터 집합을 사용하여 기계 학습 모델을 학습한 다음, 모델의 정확성을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-141">We use these data sets to train the machine learning model and then evaluate how accurate the model is.</span></span> <span data-ttu-id="ade4f-142">이러한 데이터 집합은 원래 [NYC TLC Taxi Trip 데이터 집합](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml)에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-142">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

1. <span data-ttu-id="ade4f-143">**솔루션 탐색기**에서 각 \*.csv 파일을 마우스 오른쪽 단추로 클릭하고 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-143">In **Solution Explorer**, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="ade4f-144">**고급** 아래에서 **출력 디렉터리에 복사** 값을 **변경된 내용만 복사**로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-144">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

1. <span data-ttu-id="ade4f-145">**taxi-fare-train.csv** 데이터 집합을 열고 첫 번째 행에서 열 머리글을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-145">Open the **taxi-fare-train.csv** data set and look at column headers in the first row.</span></span> <span data-ttu-id="ade4f-146">각 열을 살펴보세요.</span><span class="sxs-lookup"><span data-stu-id="ade4f-146">Take a look at each of the columns.</span></span> <span data-ttu-id="ade4f-147">데이터를 이해하고 **기능** 및 **레이블**로 사용할 열을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-147">Understand the data and decide which columns are **features** and which one is the **label**.</span></span>

<span data-ttu-id="ade4f-148">**레이블**은 예측하려는 열의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-148">The **label** is the identifier of the column you want to predict.</span></span> <span data-ttu-id="ade4f-149">식별된 **기능**은 레이블을 예측하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-149">The identified **features** are used to predict the label.</span></span>

<span data-ttu-id="ade4f-150">제공된 데이터 집합에는 다음과 같은 열이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-150">The provided data set contains the following columns:</span></span>

* <span data-ttu-id="ade4f-151">**vendor_id:** 택시 공급업체의 ID가 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-151">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="ade4f-152">**rate_code:** 택시 이동의 요금 유형이 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-152">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="ade4f-153">**passenger_count:** 이동하는 승객 수가 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-153">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="ade4f-154">**trip_time_in_secs**: 이동에 걸린 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-154">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="ade4f-155">이동을 완료하기 전에 이동 요금을 예측하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-155">You want to predict the fare of the trip before the trip is completed.</span></span> <span data-ttu-id="ade4f-156">해당 시간에는 이동이 얼마나 길지 알지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-156">At that moment you don't know how long the trip would take.</span></span> <span data-ttu-id="ade4f-157">따라서 이동 시간은 기능이 아니며 모델에서 이 열을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-157">Thus, the trip time is not a feature and you'll exclude this column from the model.</span></span>
* <span data-ttu-id="ade4f-158">**trip_distance:** 이동 거리가 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-158">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="ade4f-159">**payment_type:** 결제 방법(현금 또는 신용 카드)이 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-159">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="ade4f-160">**fare_amount:** 지급한 총 택시 요금이 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-160">**fare_amount:** The total taxi fare paid is the label.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="ade4f-161">데이터 클래스 만들기</span><span class="sxs-lookup"><span data-stu-id="ade4f-161">Create data classes</span></span>

<span data-ttu-id="ade4f-162">입력 데이터 및 예측에 대한 클래스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-162">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="ade4f-163">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-163">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="ade4f-164">**새 항목 추가** 대화 상자에서 **클래스**를 선택하고 **이름** 필드를 *TaxiTrip.cs*로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-164">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="ade4f-165">그런 다음, **추가** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-165">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="ade4f-166">새 파일에 다음 `using` 지시문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-166">Add the following `using` directives to the new file:</span></span>

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="ade4f-167">기존 클래스 정의를 제거하고 두 개의 클래스 `TaxiTrip` 및 `TaxiTripFarePrediction`가 있는 다음 코드를 *TaxiTrip.cs* 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-167">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="ade4f-168">`TaxiTrip`은 입력 데이터 클래스이며 각 데이터 집합 열의 정의를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-168">`TaxiTrip` is the input data class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="ade4f-169">[Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) 특성을 사용하여 데이터 집합에서 소스 열의 인덱스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-169">Use the [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) attribute to specify the indices of the source columns in the data set.</span></span>

<span data-ttu-id="ade4f-170">`TaxiTripFarePrediction` 클래스는 예측된 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-170">The `TaxiTripFarePrediction` class represents predicted results.</span></span> <span data-ttu-id="ade4f-171">여기에는 `FareAmount`의 단일 부동 필드가 있으며 `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) 특성이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-171">It has a single float field, `FareAmount`, with a `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) attribute applied.</span></span> <span data-ttu-id="ade4f-172">회귀 작업의 경우 **점수** 열에 예측된 레이블 값이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-172">In case of the regression task the **Score** column contains predicted label values.</span></span>

> [!NOTE]
> <span data-ttu-id="ade4f-173">`float` 유형을 사용하여 입력 및 예측 데이터 클래스에서 부동 소수점 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-173">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="ade4f-174">데이터 및 모델 경로 정의</span><span class="sxs-lookup"><span data-stu-id="ade4f-174">Define data and model paths</span></span>

<span data-ttu-id="ade4f-175">*Program.cs* 파일로 돌아가서 데이터 집합이 있는 파일 및 모델을 저장할 파일에 대한 경로를 저장하는 세 개의 필드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-175">Go back to the *Program.cs* file and add three fields to hold the paths to the files with data sets and the file to save the model:</span></span>

* <span data-ttu-id="ade4f-176">`_datapath`에는 모델을 학습하는 데 사용되는 데이터 집합이 있는 파일에 대한 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-176">`_datapath` contains the path to the file with the data set used to train the model.</span></span>
* <span data-ttu-id="ade4f-177">`_testdatapath`에는 모델을 평가하는 데 사용되는 데이터 집합이 있는 파일에 대한 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-177">`_testdatapath` contains the path to the file with the data set used to evaluate the model.</span></span>
* <span data-ttu-id="ade4f-178">`_modelpath`에는 학습된 모델이 저장되는 파일에 대한 경로가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-178">`_modelpath` contains the path to the file where the trained model is stored.</span></span>

<span data-ttu-id="ade4f-179">`Main` 메서드 바로 위에 다음 코드를 추가하여 해당 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-179">Add the following code right above the `Main` method to specify those paths:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

<span data-ttu-id="ade4f-180">위의 코드를 컴파일하려면 *Program.cs* 파일의 맨 위에 있는 다음 `using` 지시문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-180">To make the preceding code compile, add the following `using` directives at the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsingsForPaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Using statements for path definitions")]

## <a name="create-a-learning-pipeline"></a><span data-ttu-id="ade4f-181">학습 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="ade4f-181">Create a learning pipeline</span></span>

<span data-ttu-id="ade4f-182">*Program.cs* 파일 맨 위에 다음 추가 `using` 지시문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-182">Add the following additional `using` directives to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="ade4f-183">`Main` 메서드에서 `Console.WriteLine("Hello World!")`을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-183">In the `Main` method, replace the `Console.WriteLine("Hello World!")` with the following code:</span></span>

```csharp
PredictionModel<TaxiTrip, TaxiTripFarePrediction> model = Train();
```

<span data-ttu-id="ade4f-184">`Train` 메서드는 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-184">The `Train` method trains the model.</span></span> <span data-ttu-id="ade4f-185">다음 코드를 사용하여 `Main` 바로 아래 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-185">Create that method just below `Main`, using the following code:</span></span>

```csharp
public static PredictionModel<TaxiTrip, TaxiTripFarePrediction> Train()
{

}
```

<span data-ttu-id="ade4f-186">학습 파이프라인은 모델을 학습시키는 데 필요한 모든 데이터 및 알고리즘을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-186">The learning pipeline loads all of the data and algorithms necessary to train the model.</span></span> <span data-ttu-id="ade4f-187">`Train` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-187">Add the following code into the `Train` method:</span></span>

```csharp
var pipeline = new LearningPipeline();
```

## <a name="load-and-transform-data"></a><span data-ttu-id="ade4f-188">데이터 로드 및 변환</span><span class="sxs-lookup"><span data-stu-id="ade4f-188">Load and transform data</span></span>

<span data-ttu-id="ade4f-189">수행할 첫 번째 단계는 학습 데이터 집합에서 데이터를 로드하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-189">The first step to perform is to load data from the training data set.</span></span> <span data-ttu-id="ade4f-190">이 경우에 학습 데이터 집합은 `_datapath` 필드로 정의된 경로로 텍스트 파일에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-190">In our case, training data set is stored in the text file with a path defined by the `_datapath` field.</span></span> <span data-ttu-id="ade4f-191">이 파일에는 열 이름으로 된 헤더가 있으므로 데이터를 로드하는 동안 첫 번째 행을 무시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-191">That file has the header with the column names, so the first row should be ignored while loading data.</span></span> <span data-ttu-id="ade4f-192">파일의 열은 쉼표(“,”)로 구분됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-192">Columns in the file are separated by the comma (",").</span></span> <span data-ttu-id="ade4f-193">`Train` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-193">Add the following code into the `Train` method:</span></span>

```csharp
pipeline.Add(new TextLoader(_datapath).CreateFrom<TaxiTrip>(useHeader: true, separator: ','));
```

<span data-ttu-id="ade4f-194">다음 단계에서는 `TaxiTrip` 클래스에 정의된 이름으로 해당 열을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-194">In the next steps we refer to the columns by the names defined in the `TaxiTrip` class.</span></span>

<span data-ttu-id="ade4f-195">모델을 학습하고 평가할 때 기본적으로 **Label** 열의 값이 예측할 올바른 값으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-195">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="ade4f-196">택시 요금을 예측하려면 `FareAmount` 열을 **Label** 열로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-196">As we want to predict the taxi trip fare, copy the `FareAmount` column into the **Label** column.</span></span> <span data-ttu-id="ade4f-197">이를 위해 <xref:Microsoft.ML.Transforms.ColumnCopier>를 사용하고 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-197">To do that, use <xref:Microsoft.ML.Transforms.ColumnCopier> and add the following code:</span></span>

```csharp
pipeline.Add(new ColumnCopier(("FareAmount", "Label")));
```

<span data-ttu-id="ade4f-198">모델을 학습시키는 알고리즘에는 **숫자** 기능이 필요하므로 범주 데이터(`VendorId`, `RateCode` 및 `PaymentType`) 값을 숫자로 변환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-198">The algorithm that trains the model requires **numeric** features, so you have to transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) values into numbers.</span></span> <span data-ttu-id="ade4f-199">이를 위해 각 열의 다른 값에 서로 다른 숫자 키 값을 할당하고 다음 코드를 추가하는 <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer>를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-199">To do that, use <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer>, which assigns different numeric key values to the different values in each of the columns, and add the following code:</span></span>

```csharp
pipeline.Add(new CategoricalOneHotVectorizer("VendorId",
                                             "RateCode",
                                             "PaymentType"));
```

<span data-ttu-id="ade4f-200">데이터 준비의 마지막 단계에서는 <xref:Microsoft.ML.Transforms.ColumnConcatenator> 변환 클래스를 사용하여 모든 기능 열을 **Features** 열에 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-200">The last step in data preparation combines all of the feature columns into the **Features** column using the <xref:Microsoft.ML.Transforms.ColumnConcatenator> transformation class.</span></span> <span data-ttu-id="ade4f-201">기본적으로, 학습 알고리즘은 **Features** 열의 기능만 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-201">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="ade4f-202">다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-202">Add the following code:</span></span>

```csharp
pipeline.Add(new ColumnConcatenator("Features",
                                    "VendorId",
                                    "RateCode",
                                    "PassengerCount",
                                    "TripDistance",
                                    "PaymentType"));
```

<span data-ttu-id="ade4f-203">데이터 집합 파일의 `trip_time_in_secs` 열에 해당하는 `TripTime` 열은 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-203">Notice that the `TripTime` column, which corresponds to the `trip_time_in_secs` column in the data set file, isn't included.</span></span> <span data-ttu-id="ade4f-204">이미 유용한 예측 기능이 아니라고 판단했습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-204">You already determined that it isn't a useful prediction feature.</span></span>

> [!NOTE]
> <span data-ttu-id="ade4f-205">이러한 단계는 성공적인 실행을 위해 위에 지정된 순서대로 파이프라인에 추가되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-205">These steps must be added to the pipeline in the order specified above for successful execution.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="ade4f-206">학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="ade4f-206">Choose a learning algorithm</span></span>

<span data-ttu-id="ade4f-207">파이프라인에 데이터를 추가하고 데이터를 올바른 입력 형식으로 변환한 후 학습 알고리즘(**학습자**)을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-207">After adding the data to the pipeline and transforming it into the correct input format, you select a learning algorithm (**learner**).</span></span> <span data-ttu-id="ade4f-208">학습자는 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-208">The learner trains the model.</span></span> <span data-ttu-id="ade4f-209">이 문제에 대한 **회귀 작업**을 선택했으므로 ML.NET에서 제공한 회귀 학습자 중 하나인 <xref:Microsoft.ML.Trainers.FastTreeRegressor> 학습자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-209">You chose a **regression** task for this problem, so you use a <xref:Microsoft.ML.Trainers.FastTreeRegressor> learner, which is one of the regression learners provided by ML.NET.</span></span>

<span data-ttu-id="ade4f-210"><xref:Microsoft.ML.Trainers.FastTreeRegressor> 학습자는 그라데이션 승격을 활용합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-210"><xref:Microsoft.ML.Trainers.FastTreeRegressor> learner utilizes gradient boosting.</span></span> <span data-ttu-id="ade4f-211">그라데이션 승격은 회귀 문제에 대한 기계 학습 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-211">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="ade4f-212">이 파이프라인은 각 회귀 트리를 단계적으로 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-212">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="ade4f-213">미리 정의된 손실 함수를 사용하여 각 단계에서 오류를 측정한 다음, 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-213">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="ade4f-214">결과는 실제로 더 약한 예측 모델의 앙상블인 예측 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-214">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="ade4f-215">그라데이션 승격에 대한 자세한 내용은 [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression)(승격된 의사 결정 트리 회귀)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ade4f-215">For more information about gradient boosting, see [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="ade4f-216">이전 단계에서 추가된 데이터 처리 코드 다음에 오는 `Train` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-216">Add the following code into the `Train` method following the data processing code added in the previous step:</span></span>

```csharp
pipeline.Add(new FastTreeRegressor());
```

<span data-ttu-id="ade4f-217">모든 이전 단계를 개별 문으로 파이프라인에 추가했지만, C#에는 파이프라인을 더 간단하게 만들고 초기화할 수 있는 편리한 컬렉션 초기화 구문이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-217">You added all the preceding steps to the pipeline as individual statements, but C# has a handy collection initialization syntax that makes it simpler to create and initialize the pipeline.</span></span> <span data-ttu-id="ade4f-218">지금까지 `Train` 메서드에 추가한 코드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-218">Replace the code you added so far to the `Train` method with the following code:</span></span>

[!code-csharp[CreatePipeline](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create and initialize the learning pipeline")]

## <a name="train-the-model"></a><span data-ttu-id="ade4f-219">모델 학습</span><span class="sxs-lookup"><span data-stu-id="ade4f-219">Train the model</span></span>

<span data-ttu-id="ade4f-220">마지막 단계에서는 모델을 학습시킵니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-220">The final step is to train the model.</span></span> <span data-ttu-id="ade4f-221">이 시점까지는 파이프라인에서 아무것도 실행되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-221">Until this point, nothing in the pipeline has been executed.</span></span> <span data-ttu-id="ade4f-222">`pipeline.Train<TInput, TOutput>` 메서드는 `TInput` 형식의 인스턴스를 가져와 `TOutput` 형식의 인스턴스를 출력하는 모델을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-222">The `pipeline.Train<TInput, TOutput>` method produces the model that takes in an instance of the `TInput` type and outputs an instance of the `TOutput` type.</span></span> <span data-ttu-id="ade4f-223">`Train` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-223">Add the following code into the `Train` method:</span></span>

[!code-csharp[TrainMOdel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Train your model")]

<span data-ttu-id="ade4f-224">됐습니다!</span><span class="sxs-lookup"><span data-stu-id="ade4f-224">And that's it!</span></span> <span data-ttu-id="ade4f-225">NYC에서 택시 요금을 예측할 수 있는 기계 학습 모델을 성공적으로 학습시켰습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-225">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="ade4f-226">이제 모델이 얼마나 정확한지 살펴보고 이를 사용하여 택시 요금을 예측하는 방법에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-226">Now let's take a look to understand how accurate the model is and learn how to use it to predict taxi fare values.</span></span>

### <a name="save-the-model"></a><span data-ttu-id="ade4f-227">모델 저장</span><span class="sxs-lookup"><span data-stu-id="ade4f-227">Save the model</span></span>

<span data-ttu-id="ade4f-228">이 시점에 기존 또는 새 .NET 응용 프로그램에 통합할 수 있는 모델이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-228">At this point, you have a model that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="ade4f-229">모델을 .zip 파일로 저장하려면 `Train` 메서드 끝에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-229">To save the model to a .zip file, add the following code at the end of the `Train` method:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Save the model asynchronously and return the model")]

<span data-ttu-id="ade4f-230">`model.WriteAsync` 호출에 `await` 문을 추가하면 `Train` 메서드를 작업을 반환하는 비동기 메서드로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-230">Adding the `await` statement to the `model.WriteAsync` call means that the `Train` method must be changed to an async method that returns a task.</span></span> <span data-ttu-id="ade4f-231">다음 코드에 표시된 대로 `Train`의 시그니처를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-231">Modify the signature of `Train` as shown in the following code:</span></span>

[!code-csharp[AsyncTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "Make the Train method async and return a task.")]

<span data-ttu-id="ade4f-232">`Train` 메서드의 반환 형식을 변경하면 다음 코드에 표시된 대로 `Main` 메서드에서 `Train`을 호출하는 코드에 `await`를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-232">Changing the return type of the `Train` method means you have to add an `await` to the code that calls `Train` in the `Main` method as shown in the following code:</span></span>

[!code-csharp[AwaitTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Await the Train method")]

<span data-ttu-id="ade4f-233">`Main` 메서드에 `await`를 사용하면 `Main` 메서드는 `async` 한정자를 포함하고 `Task`를 반환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-233">Using `await` in the `Main` method means the `Main` method must have the `async` modifier and return a `Task`:</span></span>

[!code-csharp[AsyncMain](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Make the Main method async and return a task.")]

<span data-ttu-id="ade4f-234">또한 파일의 맨 위에 있는 다음 `using` 지시문도 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-234">You also need to add the following `using` directive at the top of the file:</span></span>

[!code-csharp[UsingTasks](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Add System.Threading.Tasks. to your usings.")]

<span data-ttu-id="ade4f-235">`async Main` 메서드는 C# 7.1의 기능이고 프로젝트의 기본 언어 버전은 C# 7.0이므로 언어 버전을 C# 7.1 이상으로 변경해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-235">Because the `async Main` method is the feature added in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span> <span data-ttu-id="ade4f-236">이 작업을 하려면 **솔루션 탐색기**에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭하고 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-236">To do that, right-click the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="ade4f-237">**빌드** 탭을 선택하고 **고급** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-237">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="ade4f-238">드롭다운에서 **C# 7.1**(또는 이상 버전)을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-238">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="ade4f-239">**확인** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-239">Select the **OK** button.</span></span>

## <a name="evaluate-the-model"></a><span data-ttu-id="ade4f-240">모델 평가</span><span class="sxs-lookup"><span data-stu-id="ade4f-240">Evaluate the model</span></span>

<span data-ttu-id="ade4f-241">평가는 모델이 레이블 값을 얼마나 잘 예측하는지 확인하는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-241">Evaluation is the process of checking how well the model predicts label values.</span></span> <span data-ttu-id="ade4f-242">모델을 학습될 때 사용하지 않은 데이터를 기반으로 모델이 적절한 예측을 하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-242">It's important that the model makes good predictions on data that was not used to train the model.</span></span> <span data-ttu-id="ade4f-243">이를 수행하는 한 가지 방법은 이 자습서에서 한 것처럼 데이터를 학습 및 테스트 데이터 집합으로 분할하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-243">One way to do this is to split the data into training and test data sets, as it's done in this tutorial.</span></span> <span data-ttu-id="ade4f-244">학습 데이터를 기반으로 모델을 학습시켰으므로 테스트 데이터에서 모델이 얼마나 잘 작동하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-244">Now that you've trained the model on the training data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="ade4f-245">`Main` 메서드로 돌아가서 `Train` 메서드 호출 아래에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-245">Go back to the `Main` method and add the following code beneath the call to the `Train`method:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Evaluate the model.")]

<span data-ttu-id="ade4f-246">`Evaluate` 메서드는 모델을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-246">The `Evaluate` method evaluates the model.</span></span> <span data-ttu-id="ade4f-247">해당 메서드를 만들려면 `Train` 메서드 아래에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-247">To create that method, add the following code below the `Train` method:</span></span>

```csharp
private static void Evaluate(PredictionModel<TaxiTrip, TaxiTripFarePrediction> model)
{

}
```

<span data-ttu-id="ade4f-248">`Evaluate` 메서드에 다음 코드를 추가하여 테스트 데이터의 로드를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-248">Add the following code into the `Evaluate` method to setup loading of the test data:</span></span>

[!code-csharp[LoadTestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Load the test data.")]

<span data-ttu-id="ade4f-249">다음 코드를 추가하여 모델을 평가하고 평가 메트릭을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-249">Add the following code to evaluate the model and produce the evaluation metrics:</span></span>

[!code-csharp[EvaluateAndMeasure](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Evaluate the model and its predictions.")]

<span data-ttu-id="ade4f-250">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse)는 회귀 모델의 평가 메트릭 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-250">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) is one of the evaluation metrics of the regression model.</span></span> <span data-ttu-id="ade4f-251">RMS가 낮을수록 더 나은 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-251">The lower it is, the better the model is.</span></span> <span data-ttu-id="ade4f-252">RMS 값을 표시하려면 `Evaluate` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-252">Add the following code into the `Evaluate` method to display the RMS value:</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Display the RMS metric.")]

<span data-ttu-id="ade4f-253">[RSquared](../resources/glossary.md#coefficient-of-determination)는 회귀 모델의 다른 평가 메트릭입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-253">[RSquared](../resources/glossary.md#coefficient-of-determination) is another evaluation metric of the regression models.</span></span> <span data-ttu-id="ade4f-254">RSquared에서는 0과 1 사이의 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-254">RSquared takes values between 0 and 1.</span></span> <span data-ttu-id="ade4f-255">해당 값이 1에 가까울수록 더 나은 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-255">The closer its value is to 1, the better the model is.</span></span> <span data-ttu-id="ade4f-256">RSquared 값을 표시하려면 `Evaluate` 메서드에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-256">Add the following code into the `Evaluate` method to display the RSquared value:</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Display the RSquared metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="ade4f-257">예측에 모델 사용</span><span class="sxs-lookup"><span data-stu-id="ade4f-257">Use the model for predictions</span></span>

<span data-ttu-id="ade4f-258">테스트 데이터 인스턴스를 수용할 클래스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-258">Create a class to house test data instances:</span></span>

1. <span data-ttu-id="ade4f-259">**솔루션 탐색기**에서 프로젝트를 마우스 오른쪽 단추로 클릭하고 **추가** > **새 항목**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-259">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="ade4f-260">**새 항목 추가** 대화 상자에서 **클래스**를 선택하고 **이름** 필드를 *TestTrips.cs*로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-260">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TestTrips.cs*.</span></span> <span data-ttu-id="ade4f-261">그런 다음, **추가** 단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-261">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="ade4f-262">다음 예제처럼 클래스를 static으로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-262">Modify the class to be static like in the following example:</span></span>

   [!code-csharp[StaticClass](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#1 "Change class to be a static class.")]

<span data-ttu-id="ade4f-263">이 자습서에서는 이 클래스 내에서 하나의 테스트 이동을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-263">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="ade4f-264">나중에 이 모델로 실험할 다른 시나리오를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-264">Later you can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="ade4f-265">다음 코드를 `TestTrips` 클래스에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-265">Add the following code into the `TestTrips` class:</span></span>

[!code-csharp[TestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#2 "Create aq trip to predict its cost.")]

<span data-ttu-id="ade4f-266">이 이동의 실제 요금은 29.5입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-266">This trip's actual fare is 29.5.</span></span> <span data-ttu-id="ade4f-267">모델에서 요금을 예측하므로 자리 표시자로 0을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-267">Use 0 as a placeholder, as the model will predict the fare.</span></span>

<span data-ttu-id="ade4f-268">지정된 이동 요금을 예측하려면 *Program.cs* 파일로 돌아가 다음 코드를 `Main`메서드에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-268">To predict the fare of the specified trip, go back to the *Program.cs* file and add the following code into the `Main` method:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Try a prediction.")]

<span data-ttu-id="ade4f-269">프로그램을 실행하여 테스트 사례에 대해 예측된 택시 요금을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-269">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="ade4f-270">지금까지</span><span class="sxs-lookup"><span data-stu-id="ade4f-270">Congratulations!</span></span> <span data-ttu-id="ade4f-271">택시 요금 예측을 위한 기계 학습 모델을 성공적으로 빌드하고, 정확도를 평가하고, 예측하는 데 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-271">You've now successfully built a machine learning model for predicting taxi trip fares, evaluated its accuracy, and used it to make predictions.</span></span> <span data-ttu-id="ade4f-272">[dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub 리포지토리에서 이 자습서의 소스 코드를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-272">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ade4f-273">다음 단계</span><span class="sxs-lookup"><span data-stu-id="ade4f-273">Next steps</span></span>

<span data-ttu-id="ade4f-274">이 자습서에서는 다음 방법을 학습했습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4f-274">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="ade4f-275">문제 이해</span><span class="sxs-lookup"><span data-stu-id="ade4f-275">Understand the problem</span></span>
> * <span data-ttu-id="ade4f-276">적절한 기계 학습 작업 선택</span><span class="sxs-lookup"><span data-stu-id="ade4f-276">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="ade4f-277">데이터 준비 및 이해</span><span class="sxs-lookup"><span data-stu-id="ade4f-277">Prepare and understand the data</span></span>
> * <span data-ttu-id="ade4f-278">학습 파이프라인 만들기</span><span class="sxs-lookup"><span data-stu-id="ade4f-278">Create a learning pipeline</span></span>
> * <span data-ttu-id="ade4f-279">데이터 로드 및 변환</span><span class="sxs-lookup"><span data-stu-id="ade4f-279">Load and transform the data</span></span>
> * <span data-ttu-id="ade4f-280">학습 알고리즘 선택</span><span class="sxs-lookup"><span data-stu-id="ade4f-280">Choose a learning algorithm</span></span>
> * <span data-ttu-id="ade4f-281">모델 학습</span><span class="sxs-lookup"><span data-stu-id="ade4f-281">Train the model</span></span>
> * <span data-ttu-id="ade4f-282">모델 평가</span><span class="sxs-lookup"><span data-stu-id="ade4f-282">Evaluate the model</span></span>
> * <span data-ttu-id="ade4f-283">예측에 모델 사용</span><span class="sxs-lookup"><span data-stu-id="ade4f-283">Use the model for predictions</span></span>

<span data-ttu-id="ade4f-284">다음 자습서로 이동하여 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="ade4f-284">Advance to the next tutorial to learn more.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="ade4f-285">아이리스 클러스터링</span><span class="sxs-lookup"><span data-stu-id="ade4f-285">Iris clustering</span></span>](iris-clustering.md)
