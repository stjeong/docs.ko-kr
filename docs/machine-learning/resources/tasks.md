---
title: 기계 학습 작업 - ML.NET
description: ML.NET에서 지원되는 다양한 기계 학습 작업 및 관련 작업을 살펴봅니다.
ms.custom: seodec18
ms.date: 01/15/2019
author: jralexander
ms.openlocfilehash: 02b454d18eca36c94c27ae15665af5df2ec87905
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415704"
---
# <a name="machine-learning-tasks-in-mlnet"></a><span data-ttu-id="0e1db-103">ML.NET의 기계 학습 작업</span><span class="sxs-lookup"><span data-stu-id="0e1db-103">Machine learning tasks in ML.NET</span></span>

<span data-ttu-id="0e1db-104">기계 학습 모델을 빌드할 때 먼저 데이터로 무엇을 달성하려고 하는지 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-104">When building a machine learning model, you first need to define what you are hoping to achieve with your data.</span></span> <span data-ttu-id="0e1db-105">그런 다음, 상황에 맞는 올바른 기계 학습 작업을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-105">Afterwards, you can pick the right machine learning task for your situation.</span></span> <span data-ttu-id="0e1db-106">다음 목록은 사용자가 선택할 수 있는 다양한 기계 학습 작업과 몇 가지 일반적인 사용 사례에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-106">The following list describes the different machine learning tasks that you can choose from and some common use cases.</span></span>

> [!NOTE]
> <span data-ttu-id="0e1db-107">ML.NET은 현재 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-107">ML.NET is currently in Preview.</span></span> <span data-ttu-id="0e1db-108">일부 기계 학습 작업은 현재 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-108">Not all machine learning tasks are currently supported.</span></span> <span data-ttu-id="0e1db-109">특정 작업에 대한 요청을 제출하려면 [dotnet/machinelearning 리포지토리](https://github.com/dotnet/machinelearning/issues)에서 문제를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-109">To submit a request for a certain task, open an issue in the [dotnet/machinelearning repository](https://github.com/dotnet/machinelearning/issues).</span></span>

## <a name="binary-classification"></a><span data-ttu-id="0e1db-110">이진 분류</span><span class="sxs-lookup"><span data-stu-id="0e1db-110">Binary classification</span></span>

<span data-ttu-id="0e1db-111">두 클래스(범주) 중에 데이터의 인스턴스가 속한 클래스를 예측하는 데 사용되는 [감독된 기계 학습](glossary.md#supervised-machine-learning) 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-111">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict which of two classes (categories) an instance of data belongs to.</span></span> <span data-ttu-id="0e1db-112">분류 알고리즘의 입력은 레이블이 지정된 예제 집합입니다. 여기서 각 레이블은 0 또는 1의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-112">The input of a classification algorithm is a set of labeled examples, where each label is an integer of either 0 or 1.</span></span> <span data-ttu-id="0e1db-113">이진 분류 알고리즘의 출력은 분류자로, 레이블이 없는 새 인스턴스의 클래스를 예측하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-113">The output of a binary classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="0e1db-114">이진 분류 시나리오의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-114">Examples of binary classification scenarios include:</span></span>

* <span data-ttu-id="0e1db-115">“긍정적” 또는 “부정적”으로 [Twitter 댓글의 감정 이해](../tutorials/sentiment-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0e1db-115">[Understanding sentiment of Twitter comments](../tutorials/sentiment-analysis.md) as either "positive" or "negative".</span></span>
* <span data-ttu-id="0e1db-116">환자에게 특정 질병이 있는지 여부 진단.</span><span class="sxs-lookup"><span data-stu-id="0e1db-116">Diagnosing whether a patient has a certain disease or not.</span></span>
* <span data-ttu-id="0e1db-117">전자 메일을 “스팸”으로 표시할지 여부 결정.</span><span class="sxs-lookup"><span data-stu-id="0e1db-117">Making a decision to mark an email as "spam" or not.</span></span>
* <span data-ttu-id="0e1db-118">사진에 개 또는 과일이 포함되어 있는지 확인.</span><span class="sxs-lookup"><span data-stu-id="0e1db-118">Determining if a photo contains a dog or fruit.</span></span>

<span data-ttu-id="0e1db-119">자세한 내용은 Wikipedia에서 [Binary classification](https://en.wikipedia.org/wiki/Binary_classification)(이진 분류) 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e1db-119">For more information, see the [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) article on Wikipedia.</span></span>

<span data-ttu-id="0e1db-120">이진 분류의 권장 학습자:</span><span class="sxs-lookup"><span data-stu-id="0e1db-120">Recommended learners for binary classification:</span></span>

* <span data-ttu-id="0e1db-121">AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-121">AveragedPerceptronTrainer</span></span>
* <span data-ttu-id="0e1db-122">StochasticGradientDescentClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-122">StochasticGradientDescentClassificationTrainer</span></span>
* <span data-ttu-id="0e1db-123">LightGbmBinaryTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-123">LightGbmBinaryTrainer</span></span>
* <span data-ttu-id="0e1db-124">FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-124">FastTreeBinaryClassificationTrainer</span></span>
* <span data-ttu-id="0e1db-125">SymSgdClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-125">SymSgdClassificationTrainer</span></span>

### <a name="binary-classification-learners"></a><span data-ttu-id="0e1db-126">이진 분류 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-126">Binary Classification Learners</span></span>

<span data-ttu-id="0e1db-127">이진 분류 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-127">The following learners are available for binary classification tasks:</span></span>

* [<span data-ttu-id="0e1db-128">AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-128">AveragedPerceptronTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.AveragedPerceptronTrainer)
* [<span data-ttu-id="0e1db-129">BinaryClassificationGamTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-129">BinaryClassificationGamTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.BinaryClassificationGamTrainer)
* [<span data-ttu-id="0e1db-130">FastForestClassification</span><span class="sxs-lookup"><span data-stu-id="0e1db-130">FastForestClassification</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastForestClassification)
* [<span data-ttu-id="0e1db-131">FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-131">FastTreeBinaryClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer)
* [<span data-ttu-id="0e1db-132">FieldAwareFactorizationMachineTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-132">FieldAwareFactorizationMachineTrainer</span></span>](xref:Microsoft.ML.FactorizationMachine.FieldAwareFactorizationMachineTrainer)
* [<span data-ttu-id="0e1db-133">LightGbmBinaryTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-133">LightGbmBinaryTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmBinaryTrainer)
* [<span data-ttu-id="0e1db-134">LinearSvmTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-134">LinearSvmTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.LinearSvmTrainer)
* [<span data-ttu-id="0e1db-135">LogisticRegression</span><span class="sxs-lookup"><span data-stu-id="0e1db-135">LogisticRegression</span></span>](xref:Microsoft.ML.Learners.LogisticRegression)
* [<span data-ttu-id="0e1db-136">PriorTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-136">PriorTrainer</span></span>](xref:Microsoft.ML.Trainers.PriorTrainer)
* [<span data-ttu-id="0e1db-137">RandomTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-137">RandomTrainer</span></span>](xref:Microsoft.ML.Trainers.RandomTrainer)
* [<span data-ttu-id="0e1db-138">StochasticGradientDescentClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-138">StochasticGradientDescentClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.StochasticGradientDescentClassificationTrainer)
* [<span data-ttu-id="0e1db-139">SymSgdClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-139">SymSgdClassificationTrainer</span></span>](xref:Microsoft.ML.Trainers.SymSgd.SymSgdClassificationTrainer)

## <a name="multiclass-classification"></a><span data-ttu-id="0e1db-140">다중 클래스 분류</span><span class="sxs-lookup"><span data-stu-id="0e1db-140">Multiclass classification</span></span>

<span data-ttu-id="0e1db-141">데이터 인스턴스의 클래스(범주)를 예측하는 데 사용되는 [감독된 기계 학습](glossary.md#supervised-machine-learning) 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-141">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the class (category) of an instance of data.</span></span> <span data-ttu-id="0e1db-142">분류 알고리즘의 입력은 레이블이 지정된 예제 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-142">The input of a classification algorithm is a set of labeled examples.</span></span> <span data-ttu-id="0e1db-143">각 레이블은 일반적으로 텍스트로 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-143">Each label normally starts as text.</span></span> <span data-ttu-id="0e1db-144">그런 다음, TermTransform을 통해 실행되어 키(숫자) 유형으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-144">It is then run through the TermTransform, which converts it to the Key (numeric) type.</span></span> <span data-ttu-id="0e1db-145">분류 알고리즘의 출력은 분류자로, 레이블이 없는 새 인스턴스의 클래스를 예측하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-145">The output of a classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="0e1db-146">다중 클래스 분류 시나리오의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-146">Examples of multi-class classification scenarios include:</span></span>

* <span data-ttu-id="0e1db-147">개의 품종을 “시베리안 허스키”, “골든 리트리버”, “푸들” 등으로 결정.</span><span class="sxs-lookup"><span data-stu-id="0e1db-147">Determining the breed of a dog as a "Siberian Husky", "Golden Retriever", "Poodle", etc.</span></span>
* <span data-ttu-id="0e1db-148">동영상 리뷰를 “긍정적”, “중립” 또는 “부정적”으로 이해.</span><span class="sxs-lookup"><span data-stu-id="0e1db-148">Understanding movie reviews as "positive", "neutral", or "negative".</span></span>
* <span data-ttu-id="0e1db-149">호텔 리뷰를 “위치”, “가격”, “청결도” 등으로 범주화.</span><span class="sxs-lookup"><span data-stu-id="0e1db-149">Categorizing hotel reviews as "location", "price", "cleanliness", etc.</span></span>

<span data-ttu-id="0e1db-150">자세한 내용은 Wikipedia에서 [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification)(다중 클래스 분류) 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e1db-150">For more information, see the [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) article on Wikipedia.</span></span>

<span data-ttu-id="0e1db-151">다중 클래스의 권장 학습자:</span><span class="sxs-lookup"><span data-stu-id="0e1db-151">Recommended learners for Multi-class:</span></span>

* <span data-ttu-id="0e1db-152">OVA-AveragedPerceptronTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-152">OVA-AveragedPerceptronTrainer</span></span>
* <span data-ttu-id="0e1db-153">SdcaMultiClassTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-153">SdcaMultiClassTrainer</span></span>
* <span data-ttu-id="0e1db-154">LightGbmMulticlassTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-154">LightGbmMulticlassTrainer</span></span>
* <span data-ttu-id="0e1db-155">OVA-FastTreeBinaryClassificationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-155">OVA-FastTreeBinaryClassificationTrainer</span></span>

>[!NOTE]
><span data-ttu-id="0e1db-156">OVA 및 PKPD는 모든 [이진 분류 학습자](#binary-classification)를 다중 클래스 데이터 세트에서 작동하도록 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-156">OVA and PKPD upgrades any [binary classification learner](#binary-classification) to act on multiclass datasets.</span></span> <span data-ttu-id="0e1db-157">자세한 내용은 [Wikipedia](https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest))를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e1db-157">More information on [Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest).</span></span>

### <a name="multiclass-classification-learners"></a><span data-ttu-id="0e1db-158">다중 클래스 분류 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-158">Multiclass Classification Learners</span></span>

<span data-ttu-id="0e1db-159">다중 클래스 분류 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-159">The following learners are available for multiclass classification tasks:</span></span>

* [<span data-ttu-id="0e1db-160">LightGbmMulticlassTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-160">LightGbmMulticlassTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmMulticlassTrainer)
* [<span data-ttu-id="0e1db-161">MetaMulticlassTrainer<TTransformer,TModel></span><span class="sxs-lookup"><span data-stu-id="0e1db-161">MetaMulticlassTrainer<TTransformer,TModel></span></span>](xref:Microsoft.ML.Learners.MetaMulticlassTrainer%602)
* [<span data-ttu-id="0e1db-162">MultiClassNaiveBayesTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-162">MultiClassNaiveBayesTrainer</span></span>](xref:Microsoft.ML.Trainers.MultiClassNaiveBayesTrainer)
* [<span data-ttu-id="0e1db-163">Ova</span><span class="sxs-lookup"><span data-stu-id="0e1db-163">Ova</span></span>](xref:Microsoft.ML.Trainers.Ova)
* [<span data-ttu-id="0e1db-164">Pkpd</span><span class="sxs-lookup"><span data-stu-id="0e1db-164">Pkpd</span></span>](xref:Microsoft.ML.Trainers.Pkpd)
* [<span data-ttu-id="0e1db-165">SdcaMultiClassTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-165">SdcaMultiClassTrainer</span></span>](xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer)

## <a name="regression"></a><span data-ttu-id="0e1db-166">재발</span><span class="sxs-lookup"><span data-stu-id="0e1db-166">Regression</span></span>

<span data-ttu-id="0e1db-167">관련 기능 집합에서 레이블 값을 예측하는 데 사용되는 [감독된 기계 학습](glossary.md#supervised-machine-learning) 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-167">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the value of the label from a set of related features.</span></span> <span data-ttu-id="0e1db-168">레이블은 실제 값일 수 있고, 분류 작업과 같이 한정된 값 집합에 속하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-168">The label can be of any real value and is not from a finite set of values as in classification tasks.</span></span> <span data-ttu-id="0e1db-169">회귀 알고리즘 모델은 기능 값이 달라질 때 레이블이 변경되는 방식을 결정하기 위한 관련 기능에 대한 레이블의 종속성입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-169">Regression algorithms model the dependency of the label on its related features to determine how the label will change as the values of the features are varied.</span></span> <span data-ttu-id="0e1db-170">회귀 알고리즘의 입력은 알려진 값의 레이블이 포함된 예제 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-170">The input of a regression algorithm is a set of examples with labels of known values.</span></span> <span data-ttu-id="0e1db-171">회귀 알고리즘의 출력은 새 입력 기능 집합의 레이블 값을 예측하는 데 사용할 수 있는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-171">The output of a regression algorithm is a function, which you can use to predict the label value for any new set of input features.</span></span> <span data-ttu-id="0e1db-172">회귀 시나리오의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-172">Examples of regression scenarios include:</span></span>

* <span data-ttu-id="0e1db-173">침실 수, 위치 또는 규모와 같은 주택 특성을 기반으로 주택 가격 예측.</span><span class="sxs-lookup"><span data-stu-id="0e1db-173">Predicting house prices based on house attributes such as number of bedrooms, location, or size.</span></span>
* <span data-ttu-id="0e1db-174">과거 데이터 및 현재 시장 추세를 기반으로 미래 재고 가격 예측.</span><span class="sxs-lookup"><span data-stu-id="0e1db-174">Predicting future stock prices based on historical data and current market trends.</span></span>
* <span data-ttu-id="0e1db-175">광고 예산을 기반으로 제품 판매 예측.</span><span class="sxs-lookup"><span data-stu-id="0e1db-175">Predicting sales of a product based on advertising budgets.</span></span>

<span data-ttu-id="0e1db-176">회귀의 권장 학습자:</span><span class="sxs-lookup"><span data-stu-id="0e1db-176">Recommended learners for regression:</span></span>

* <span data-ttu-id="0e1db-177">FastTreeTweedieTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-177">FastTreeTweedieTrainer</span></span> 
* <span data-ttu-id="0e1db-178">LightGbmRegressorTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-178">LightGbmRegressorTrainer</span></span> 
* <span data-ttu-id="0e1db-179">SdcaRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-179">SdcaRegressionTrainer</span></span> 
* <span data-ttu-id="0e1db-180">FastTreeRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-180">FastTreeRegressionTrainer</span></span>

### <a name="regression-learners"></a><span data-ttu-id="0e1db-181">회귀 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-181">Regression Learners</span></span>

<span data-ttu-id="0e1db-182">회귀 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-182">The following learners are available for regression tasks:</span></span>

* [<span data-ttu-id="0e1db-183">FastTreeRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-183">FastTreeRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer)
* [<span data-ttu-id="0e1db-184">FastTreeTweedieTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-184">FastTreeTweedieTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer)
* [<span data-ttu-id="0e1db-185">LightGbmRegressorTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-185">LightGbmRegressorTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmRegressorTrainer)
* [<span data-ttu-id="0e1db-186">OlsLinearRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-186">OlsLinearRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.HalLearners.OlsLinearRegressionTrainer)
* [<span data-ttu-id="0e1db-187">OnlineGradientDescentTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-187">OnlineGradientDescentTrainer</span></span>](xref:Microsoft.ML.Trainers.Online.OnlineGradientDescentTrainer)
* [<span data-ttu-id="0e1db-188">PoissonRegression</span><span class="sxs-lookup"><span data-stu-id="0e1db-188">PoissonRegression</span></span>](xref:Microsoft.ML.Trainers.PoissonRegression)
* [<span data-ttu-id="0e1db-189">RegressionGamTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-189">RegressionGamTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.RegressionGamTrainer)
* [<span data-ttu-id="0e1db-190">SdcaRegressionTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-190">SdcaRegressionTrainer</span></span>](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer)
* [<span data-ttu-id="0e1db-191">FastTree.SingleTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-191">FastTree.SingleTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.SingleTrainer)
* [<span data-ttu-id="0e1db-192">LightGBM.SingleTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-192">LightGBM.SingleTrainer</span></span>](xref:Microsoft.ML.LightGBM.SingleTrainer)

## <a name="clustering"></a><span data-ttu-id="0e1db-193">클러스터링</span><span class="sxs-lookup"><span data-stu-id="0e1db-193">Clustering</span></span>

<span data-ttu-id="0e1db-194">데이터 인스턴스를 비슷한 특성을 포함하는 클러스터로 그룹화하는 데 사용되는 [감독되지 않는 기계 학습](glossary.md#unsupervised-machine-learning) 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-194">An [unsupervised machine learning](glossary.md#unsupervised-machine-learning) task that is used to group instances of data into clusters that contain similar characteristics.</span></span> <span data-ttu-id="0e1db-195">클러스터링을 사용하여 검색 또는 단순 관찰을 통해 논리적으로 파생될 수 없는 데이터 세트의 관계를 식별할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-195">Clustering can also be used to identify relationships in a dataset that you might not logically derive by browsing or simple observation.</span></span> <span data-ttu-id="0e1db-196">클러스터링 알고리즘의 입력 및 출력은 선택한 방법에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-196">The inputs and outputs of a clustering algorithm depends on the methodology chosen.</span></span> <span data-ttu-id="0e1db-197">분산, 중심, 연결 또는 밀도 기반 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-197">You can take a distribution, centroid, connectivity, or density-based approach.</span></span> <span data-ttu-id="0e1db-198">현재 ML.NET은 K-평균 클러스터링을 사용하는 중심 기반 방법을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-198">ML.NET currently supports a centroid-based approach using K-Means clustering.</span></span> <span data-ttu-id="0e1db-199">클러스터링 시나리오의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-199">Examples of clustering scenarios include:</span></span>

* <span data-ttu-id="0e1db-200">호텔 선택의 습관과 특성을 기반으로 호텔 투숙객 세그먼트 이해.</span><span class="sxs-lookup"><span data-stu-id="0e1db-200">Understanding segments of hotel guests based on habits and characteristics of hotel choices.</span></span>
* <span data-ttu-id="0e1db-201">대상 광고 캠페인을 구축하는 데 도움이 되는 고객 세그먼트 및 인구 통계 식별.</span><span class="sxs-lookup"><span data-stu-id="0e1db-201">Identifying customer segments and demographics to help build targeted advertising campaigns.</span></span>
* <span data-ttu-id="0e1db-202">제조 메트릭을 기반으로 인벤토리 범주화.</span><span class="sxs-lookup"><span data-stu-id="0e1db-202">Categorizing inventory based on manufacturing metrics.</span></span>

### <a name="clustering-learners"></a><span data-ttu-id="0e1db-203">클러스터링 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-203">Clustering Learners</span></span>

<span data-ttu-id="0e1db-204">클러스터링 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-204">The following learners are available for clustering tasks:</span></span>

* [<span data-ttu-id="0e1db-205">KMeansPlusPlusTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-205">KMeansPlusPlusTrainer</span></span>](xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer)

## <a name="anomaly-detection"></a><span data-ttu-id="0e1db-206">변칙 검색</span><span class="sxs-lookup"><span data-stu-id="0e1db-206">Anomaly detection</span></span>

<span data-ttu-id="0e1db-207">이 작업은 PCA(보안 주체 구성 요소 분석)를 사용하여 변칙 검색 모델을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-207">This task creates an anomaly detection model by using Principal Component Analysis (PCA).</span></span> <span data-ttu-id="0e1db-208">PCA 기반 변칙 검색은 유효한 트랜잭션과 같은, 한 클래스의 학습 데이터를 얻기는 쉽지만 대상 변칙의 충분한 샘플을 얻기는 어려운 시나리오에서 모델을 빌드하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-208">PCA-Based Anomaly Detection helps you build a model in scenarios where it is easy to obtain training data from one class, such as valid transactions, but difficult to obtain sufficient samples of the targeted anomalies.</span></span>

<span data-ttu-id="0e1db-209">기계 학습의 검증된 기술인 PCA는 데이터의 내부 구조를 나타내고 데이터 차이를 설명하기 때문에 탐색적 데이터 분석에서 자주 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-209">An established technique in machine learning, PCA is frequently used in exploratory data analysis because it reveals the inner structure of the data and explains the variance in the data.</span></span> <span data-ttu-id="0e1db-210">PCA는 여러 변수를 포함하는 데이터를 분석하여 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-210">PCA works by analyzing data that contains multiple variables.</span></span> <span data-ttu-id="0e1db-211">변수 간의 상관 관계를 찾고 결과에서 차이점을 가장 잘 캡처하는 값의 조합을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-211">It looks for correlations among the variables and determines the combination of values that best captures differences in outcomes.</span></span> <span data-ttu-id="0e1db-212">이러한 조합된 기능 값이 보안 주체 구성 요소라는 보다 간결한 기능 공간을 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-212">These combined feature values are used to create a more compact feature space called the principal components.</span></span>

<span data-ttu-id="0e1db-213">변칙 검색은 다음과 같은 기계 학습의 여러 중요한 작업을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-213">Anomaly detection encompasses many important tasks in machine learning:</span></span>

* <span data-ttu-id="0e1db-214">잠재적으로 사기성이 있는 트랜잭션 식별.</span><span class="sxs-lookup"><span data-stu-id="0e1db-214">Identifying transactions that are potentially fraudulent.</span></span>
* <span data-ttu-id="0e1db-215">네트워크 침입이 발생했음을 나타내는 학습 패턴.</span><span class="sxs-lookup"><span data-stu-id="0e1db-215">Learning patterns that indicate that a network intrusion has occurred.</span></span>
* <span data-ttu-id="0e1db-216">비정상적인 환자 클러스터 찾기.</span><span class="sxs-lookup"><span data-stu-id="0e1db-216">Finding abnormal clusters of patients.</span></span>
* <span data-ttu-id="0e1db-217">시스템에 입력된 값 확인.</span><span class="sxs-lookup"><span data-stu-id="0e1db-217">Checking values entered into a system.</span></span>

<span data-ttu-id="0e1db-218">변칙은 정의상 거의 발생하지 않으므로 모델링에 사용할 데이터의 대표 샘플을 수집하기 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-218">Because anomalies are rare events by definition, it can be difficult to collect a representative sample of data to use for modeling.</span></span> <span data-ttu-id="0e1db-219">이 범주에 포함된 알고리즘은 특히 불균형 데이터 세트를 사용하여 모델을 빌드하고 학습시키는 핵심 과제를 해결하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-219">The algorithms included in this category have been especially designed to address the core challenges of building and training models by using imbalanced data sets.</span></span>

### <a name="anomaly-detection-learners"></a><span data-ttu-id="0e1db-220">변칙 검색 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-220">Anomaly detection learners</span></span>

<span data-ttu-id="0e1db-221">변칙 검색 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-221">The following learners are available for anomaly detection tasks:</span></span>

* [<span data-ttu-id="0e1db-222">RandomizedPcaTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-222">RandomizedPcaTrainer</span></span>](xref:Microsoft.ML.Trainers.PCA.RandomizedPcaTrainer)

## <a name="ranking"></a><span data-ttu-id="0e1db-223">순위 지정</span><span class="sxs-lookup"><span data-stu-id="0e1db-223">Ranking</span></span>

<span data-ttu-id="0e1db-224">순위 지정 작업은 레이블이 지정된 예제 세트에서 순위매기기를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-224">A ranking task constructs a ranker from a set of labeled examples.</span></span> <span data-ttu-id="0e1db-225">이 예제 세트는 지정된 기준에 따라 점수가 매겨질 수 있는 인스턴스 그룹으로 이루어져 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-225">This example set consists of instance groups that can be scored with a given criteria.</span></span> <span data-ttu-id="0e1db-226">순위 레이블은 각 인스턴스마다 {0, 1, 2, 3, 4}입니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-226">The ranking labels are { 0, 1, 2, 3, 4 } for each instance.</span></span>  <span data-ttu-id="0e1db-227">순위매기기는 각 인스턴스마다 점수를 알 수 없는 새 인스턴스 그룹의 순위를 지정하도록 학습됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-227">The ranker is trained to rank new instance groups with unknown scores for each instance.</span></span> <span data-ttu-id="0e1db-228">ML.NET 순위 지정 학습자는 [기계 학습 순위 지정](https://en.wikipedia.org/wiki/Learning_to_rank)을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-228">ML.NET ranking learners are [machine learned ranking](https://en.wikipedia.org/wiki/Learning_to_rank) based.</span></span>

### <a name="ranking-learners"></a><span data-ttu-id="0e1db-229">순위 지정 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-229">Ranking learners</span></span>

<span data-ttu-id="0e1db-230">순위 지정 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-230">The following learners are available for ranking tasks:</span></span>

* [<span data-ttu-id="0e1db-231">FastTreeRankingTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-231">FastTreeRankingTrainer</span></span>](xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer)
* [<span data-ttu-id="0e1db-232">LightGbmRankingTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-232">LightGbmRankingTrainer</span></span>](xref:Microsoft.ML.LightGBM.LightGbmRankingTrainer)

## <a name="recommendation"></a><span data-ttu-id="0e1db-233">권장 사항</span><span class="sxs-lookup"><span data-stu-id="0e1db-233">Recommendation</span></span>

<span data-ttu-id="0e1db-234">권장 사항 작업을 통해 권장 제품 또는 서비스 목록을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-234">A recommendation task enables producing a list of recommended products or services.</span></span> <span data-ttu-id="0e1db-235">ML.NET은 카탈로그에 기록 제품 등급 데이터가 있는 경우 [공동 작업 필터링](https://en.wikipedia.org/wiki/Collaborative_filtering) 알고리즘인 [MF(행렬 인수)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29)를 권장 사항에 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-235">ML.NET uses [Matrix factorization (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29), a [collaborative filtering](https://en.wikipedia.org/wiki/Collaborative_filtering) algorithm for recommendations when you have historical product rating data in your catalog.</span></span> <span data-ttu-id="0e1db-236">예를 들어 사용자에 대한 기록 영화 등급 데이터가 있고, 사용자가 다음에 시청할 가능성이 큰 다른 영화를 추천하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-236">For example, you have historical movie rating data for your users and want to recommend  other movies they are likely to watch next.</span></span>

### <a name="recommendation-learners"></a><span data-ttu-id="0e1db-237">권장 사항 학습자</span><span class="sxs-lookup"><span data-stu-id="0e1db-237">Recommendation learners</span></span>

<span data-ttu-id="0e1db-238">권장 사항 작업에 사용할 수 있는 학습자는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e1db-238">The following learners are available for recommendation tasks:</span></span>

* [<span data-ttu-id="0e1db-239">MatrixFactorizationTrainer</span><span class="sxs-lookup"><span data-stu-id="0e1db-239">MatrixFactorizationTrainer</span></span>](xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer)
* [<span data-ttu-id="0e1db-240">MatrixFactorizationPredictionTransformer</span><span class="sxs-lookup"><span data-stu-id="0e1db-240">MatrixFactorizationPredictionTransformer</span></span>](xref:Microsoft.ML.Trainers.Recommender.MatrixFactorizationPredictionTransformer)
