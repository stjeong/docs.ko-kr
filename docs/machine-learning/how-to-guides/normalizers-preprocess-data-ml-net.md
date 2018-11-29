---
title: 데이터 처리에서 사용할 normalizer를 사용하여 학습 데이터 전처리 - ML.NET
description: normalizer를 사용하여 ML.NET에서 기계 학습 모델 빌드, 교육 및 점수 매기기에 사용하기 위해 학습 데이터를 전처리하는 방법 알아보기
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: c8b959904705e996c97bdcd8b3444e754d14d046
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297620"
---
# <a name="preprocess-training-data-with-normalizers-to-use-in-data-processing---mlnet"></a><span data-ttu-id="b421f-103">데이터 처리에서 사용할 normalizer를 사용하여 학습 데이터 전처리 - ML.NET</span><span class="sxs-lookup"><span data-stu-id="b421f-103">Preprocess training data with normalizers to use in data processing - ML.NET</span></span>

<span data-ttu-id="b421f-104">ML.NET는 많은 [파라메트릭 및 비파라메트릭 알고리즘](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/)을 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="b421f-104">ML.NET exposes a number of [parametric and non-parametric algorithms](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/).</span></span>

<span data-ttu-id="b421f-105">선형 또는 기타 파라메트릭 모델을 학습할 때 normalizer를 **사용**하는 것만큼 normalizer를 선택하는 것이 중요하지 **않습니다**.</span><span class="sxs-lookup"><span data-stu-id="b421f-105">It's **not** as important which normalizer you choose as it is to **use** a normalizer when training linear or other parametric models.</span></span>

<span data-ttu-id="b421f-106">항상 ML.NET 학습 파이프라인에 직접 normalizer를 포함합니다. 따라서:</span><span class="sxs-lookup"><span data-stu-id="b421f-106">Always include the normalizer directly in the ML.NET learning pipeline, so it:</span></span>

- <span data-ttu-id="b421f-107">테스트 데이터가 아닌 학습 데이터에 대해서만 학습합니다.</span><span class="sxs-lookup"><span data-stu-id="b421f-107">is only trained on the training data, and not on your test data,</span></span>
- <span data-ttu-id="b421f-108">예측 시 추가 사전 처리를 수행할 필요 없이 새로 들어오는 모든 데이터에 올바르게 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b421f-108">is correctly applied to all the new incoming data, without the need for extra pre-processing at prediction time.</span></span>

<span data-ttu-id="b421f-109">학습 파이프라인의 정규화를 보여주는 코드 조각은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b421f-109">Here's a snippet of code that demonstrates normalization in learning pipelines.</span></span> <span data-ttu-id="b421f-110">아이리스 데이터 세트를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="b421f-110">It assumes the Iris dataset:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.TextReader(new TextLoader.Arguments
{
    Column = new[] {
        // The four features of the Iris dataset will be grouped together as one Features column.
        new TextLoader.Column("Features", DataKind.R4, 0, 3),
        // Label: kind of iris.
        new TextLoader.Column("Label", DataKind.TX, 4),
    },
    // Default separator is tab, but the dataset has comma.
    Separator = ","
});

// Read the training data.
var trainData = reader.Read(dataPath);

// Apply all kinds of standard ML.NET normalization to the raw features.
var pipeline =
    mlContext.Transforms.Normalize(
        new NormalizingEstimator.MinMaxColumn("Features", "MinMaxNormalized", fixZero: true),
        new NormalizingEstimator.MeanVarColumn("Features", "MeanVarNormalized", fixZero: true),
        new NormalizingEstimator.BinningColumn("Features", "BinNormalized", numBins: 256));

// Let's train our pipeline of normalizers, and then apply it to the same data.
var normalizedData = pipeline.Fit(trainData).Transform(trainData);

// Inspect one column of the resulting dataset.
var meanVarValues = normalizedData.GetColumn<float[]>(mlContext, "MeanVarNormalized").ToArray();
```
