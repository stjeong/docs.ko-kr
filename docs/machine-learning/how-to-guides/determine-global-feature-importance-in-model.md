---
title: ML.NET에서 순열 기능 중요도를 사용하여 모델의 기능 중요도 판별
description: ML.NET에서 순열 기능 중요도를 사용하여 모델의 기능 중요도 파악
ms.date: 12/04/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 4b93e085dbb99e7f6f5a0a839b863aad1c69c7ba
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156571"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a><span data-ttu-id="5ff79-103">ML.NET에서 순열 기능 중요도를 사용하여 모델의 기능 중요도 판별</span><span class="sxs-lookup"><span data-stu-id="5ff79-103">Determine the feature importance of models with Permutation Feature Importance in ML.NET</span></span>

<span data-ttu-id="5ff79-104">기계 학습 모델을 만들 때는 예측을 수행하기에 부족한 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-104">When creating machine learning models, it is often not enough to simply make predictions.</span></span> <span data-ttu-id="5ff79-105">기계 학습 개발자, 의사 결정자 및 모델의 영향을 받는 사람이 기계 학습 모델의 의사 결정 방법 및 성과에 도움이 되는 기능을 이해해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-105">Often, machine learning developers, decision makers, and those affected by the models need to understand how machine learning models make decisions and which features contribute to their performance.</span></span> <span data-ttu-id="5ff79-106">PFI(`Permutation Feature Importance`)는 모델의 기능 중요성에 대한 기계 학습 개발자의 이해를 돕기 위해 Microsoft 내부에서 사용되는 모델 설명 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-106">`Permutation Feature Importance` (PFI) is a model explainability tool that is used internally at Microsoft to help machine learning developers better understand the feature importance of models.</span></span>

<span data-ttu-id="5ff79-107">PFI는 [“랜덤 포레스트” 논문, 섹션 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf)에서 Breimanin이 제기한 기계 학습 모델의 **전역 기능 중요도**를 파악하는 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-107">PFI is a technique to determine **global feature importance** in a trained machine learning model, motivated by Breiman in the ["Random Forests" paper, section 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf).</span></span> <span data-ttu-id="5ff79-108">PFI는 “기능의 값이 임의\* 값으로 설정된 경우 모델에 어떤 영향을 미치나요?”라는 질문을 통해 기능 중요도를 측정합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-108">PFI measures feature importance by asking the question, "What would the effect on the model be if the values for a feature were set to a random\* value?".</span></span> <span data-ttu-id="5ff79-109">PFI 방법의 장점은 모델에 종속되지 않는다는 것입니다. 평가할 수 있는 모든 모델에서 작동하며, 학습 세트만이 아닌 모든 데이터 세트를 사용하여 기능 중요도를 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-109">The advantage of the PFI method is that it is model agnostic — it works with any model that can be evaluated — and it can use any dataset, not just the training set, to compute feature importance.</span></span> <span data-ttu-id="5ff79-110">따라서 PFI를 사용하여 다음 그래프와 같은 기능 중요도를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-110">You can use PFI like so to produce feature importances like this graph:</span></span>

![순열 기능 중요도 그래프](./media/determine-global-feature-importance-in-model/pfi-graph.png)

```csharp
// Compute the feature importance using PFI
var permutationMetrics = mlContext.Regression.PermutationFeatureImportance(model, data);
 
// Get the feature names from the training set
var featureNames = data.Schema.GetColumns()
                .Select(tuple => tuple.column.Name) // Get the column names
                .Where(name => name != labelName) // Drop the Label
                .ToArray();
 
// Write out the feature names and their importance to the model's R-squared value
for (int i = 0; i < featureNames.Length; i++)
  Console.WriteLine($"{featureNames[i]}\t{permutationMetrics[i].rSquared:G4}");
```

<span data-ttu-id="5ff79-112">PFI를 사용하여 모델의 기능 중요도를 분석하는 샘플은 [dotnet/machinelearning GitHub 리포지토리](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance.cs)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5ff79-112">For a sample using PFI to analyze the feature importance of a model, see [the dotnet/machinelearning GitHub repository](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance.cs).</span></span>

<span data-ttu-id="5ff79-113">/\* 정확히 임의는 아니지만 예제 세트에서 순열로 치환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ff79-113">/\* Well, not random exactly, but permuted across the set of examples.</span></span>
