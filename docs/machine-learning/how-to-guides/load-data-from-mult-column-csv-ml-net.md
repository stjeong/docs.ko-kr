---
title: 기계 학습 처리를 위해 CSV 파일에서 많은 열을 포함하는 데이터 로드 - ML.NET
description: ML.NET를 사용하여 기계 학습 모델을 빌드하고, 학습시키고, 점수 매기는 데 사용하기 위해 CSV 파일에서 많은 열을 포함하는 데이터를 로드하는 방법 알아보기
ms.date: 01/29/2019
ms.custom: mvc,how-to
ms.openlocfilehash: a06d7edfb4746a39377116b15903b68f8723cb02
ms.sourcegitcommit: dcc8feeff4718664087747529638ec9b47e65234
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55479713"
---
# <a name="load-data-with-many-columns-from-a-csv-file-for-machine-learning-processing---mlnet"></a>기계 학습 처리를 위해 CSV 파일에서 많은 열을 포함하는 데이터 로드 - ML.NET

`TextLoader`는 텍스트 파일에서 데이터를 로드하는 데 사용됩니다. 데이터 열, 열 형식 및 텍스트 파일에서 해당 위치를 지정해야 합니다.

입력 파일에 동일한 형식의 많은 열이 있고 항상 함께 사용되는 경우 *벡터 열*로 읽습니다. 이 전략을 사용하면 다음 예제와 같이 데이터 스키마가 정리되고 불필요한 성능 저하를 방지할 수 있습니다.

[예제 파일](https://github.com/dotnet/machinelearning/tree/master/test/data/generated_regression_dataset.csv):

```console
-2.75;0.77;-0.61;0.14;1.39;0.38;-0.53;-0.50;-2.13;-0.39;0.46;140.66
-0.61;-0.37;-0.12;0.55;-1.00;0.84;-0.02;1.30;-0.24;-0.50;-2.12;148.12
-0.85;-0.91;1.81;0.02;-0.78;-1.41;-1.09;-0.65;0.90;-0.37;-0.22;402.20
0.28;1.05;-0.24;0.30;-0.99;0.19;0.32;-0.95;-1.19;-0.63;0.75;443.51
```

`TextLoader`를 사용하여 이 파일 읽기:

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(
    columns: new TextLoader.Column[]
    {
    // We read the first 10 values as a single float vector.
        new TextLoader.Column("FeatureVector",DataKind.R4,0,9),
        // Separately, read the target variable.
        new TextLoader.Column("Target",DataKind.R4,10)
    },
    // Default separator is tab, but we need a semicolon.
    separatorChar: ';',
    hasHeader: true
);

// Now read the file (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(dataPath);
```    