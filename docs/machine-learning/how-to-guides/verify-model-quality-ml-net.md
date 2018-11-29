---
title: 메트릭을 계산하여 기계 학습 모델 품질 평가 - ML.NET
description: ML.NET에서 기계 학습 모델 품질을 평가하고 확인하기 위해 메트릭을 계산하는 방법 알아보기
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 6fd4dfab6104b4398918e42ed70584b04169a8c1
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297570"
---
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality---mlnet"></a><span data-ttu-id="f0dd4-103">메트릭을 계산하여 기계 학습 모델 품질 평가 - ML.NET</span><span class="sxs-lookup"><span data-stu-id="f0dd4-103">Calculate metrics to evaluate machine learning model quality - ML.NET</span></span>

<span data-ttu-id="f0dd4-104">모델을 학습한 후에 품질을 평가하려면 어떻게 할까요?</span><span class="sxs-lookup"><span data-stu-id="f0dd4-104">How do you evaluate quality after you train the model?</span></span> <span data-ttu-id="f0dd4-105">각 기계 학습 작업은 품질 평가를 위한 메트릭을 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="f0dd4-105">Each machine learning task exposes metrics for quality evaluation.</span></span>

<span data-ttu-id="f0dd4-106">다음 예제와 같이 모델을 평가하는 작업에 해당하는 '컨텍스트'를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0dd4-106">You can use the corresponding 'context' of the task to evaluate the model, as in the following example:</span></span>

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```