---
title: ML.NET에서 순열 기능 중요도를 사용하여 모델의 기능 중요도 판별
description: ML.NET에서 순열 기능 중요도를 사용하여 모델의 기능 중요도 파악
ms.date: 02/01/2019
ms.custom: mvc,how-to
ms.openlocfilehash: a61e5dbbd544aa7df56291db9207343cb6f03e6e
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738814"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a>ML.NET에서 순열 기능 중요도를 사용하여 모델의 기능 중요도 판별

기계 학습 모델을 만들 때는 예측을 수행하기에 부족한 경우가 많습니다. 기계 학습 개발자, 의사 결정자 및 모델의 영향을 받는 사람이 기계 학습 모델의 의사 결정 방법 및 성과에 도움이 되는 기능을 이해해야 합니다. PFI(`Permutation Feature Importance`)는 모델의 기능 중요성에 대한 기계 학습 개발자의 이해를 돕기 위해 Microsoft 내부에서 사용되는 모델 설명 도구입니다.

PFI는 [“랜덤 포레스트” 논문, 섹션 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf)에서 Breimanin이 제기한 기계 학습 모델의 **전역 기능 중요도**를 파악하는 기술입니다. PFI는 “기능의 값이 임의* 값으로 설정된 경우 모델에 어떤 영향을 미치나요?”라는 질문을 통해 기능 중요도를 측정합니다. PFI 방법의 장점은 모델에 종속되지 않는다는 것입니다. 평가할 수 있는 모든 모델에서 작동하며, 학습 세트만이 아닌 모든 데이터 세트를 사용하여 기능 중요도를 계산할 수 있습니다. 따라서 PFI를 사용하여 다음 그래프와 같은 기능 중요도를 생성할 수 있습니다.

![순열 기능 중요도 그래프](./media/determine-global-feature-importance-in-model/pfi-graph.png)

```csharp
// Compute the feature importance using PFI
var permutationMetrics = mlContext.Regression.PermutationFeatureImportance(model.LastTransformer, model.Transform(data), "MedianHomeValue");

// Get the feature names from the training set
var featureNames =
    data.Schema.AsEnumerable()
    .Select(column => column.Name) // Get the column names
    .Where(name => name != "MedianHomeValue") // Drop the Label
    .ToArray();

// Write out the feature names and their importance to the model's Mean R-squared value
for (int i = 0; i < featureNames.Length;i++)
{
    Console.WriteLine($"{featureNames[i]}\t{permutationMetrics[i].RSquared.Mean:G4}");
}
```

PFI를 사용하여 모델의 기능 중요도를 분석하는 샘플은 [dotnet/machinelearning GitHub 리포지토리](https://github.com/dotnet/machinelearning/tree/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance)를 참조하세요.

/* 정확히 임의는 아니지만 예제 세트에서 순열로 치환됩니다.
