---
title: 앱에서 학습된 기계 학습 모델 운용 - ML.NET
description: ML.NET을 사용하여 애플리케이션에서 학습 및 평가된 기계 학습 모델을 이용하는 방법을 알아봅니다.
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: ff3f0a8856382d020129693bcf722f572fd87606
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131647"
---
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a>앱에서 학습된 기계 학습 모델 운용 - ML.NET

모델 메트릭이 올바른 것으로 보이면 모델을 ‘운용’할 때가 되었습니다. 빌드한 `model` 개체를 사용 및 유지하고 다양한 환경에서 학습 중에 ‘배운’ 것과 동일한 단계를 적용하여 다시 사용할 수 있습니다.

모델을 파일에 저장하고 (잠재적으로 다른 컨텍스트에서) 다시 로드하려면 다음 예제를 사용합니다.

```csharp
using (var stream = File.Create(modelPath))
{
    // Saving and loading happens to 'dynamic' models.
    mlContext.Model.Save(model, stream);
}

// Potentially, the lines below can be in a different process altogether.

// When you load the model, it's a transformer.
ITransformer loadedModel;
using (var stream = File.OpenRead(modelPath))
    loadedModel = mlContext.Model.Load(stream);
```
