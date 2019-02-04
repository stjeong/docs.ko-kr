---
title: ML.NET 파이프라인을 처리하는 동안 중간 데이터 값 검사
description: ML.NET 기계 학습 파이프라인을 처리하는 동안 실제 중간 데이터 값을 검사하는 방법 알아보기
ms.date: 01/30/2019
ms.custom: mvc,how-to
ms.openlocfilehash: b3a554bf7cd88219a66f91a18b9d983bb91c0f0e
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/03/2019
ms.locfileid: "55675012"
---
# <a name="inspect-intermediate-data-values-during-mlnet-pipeline-processing"></a><span data-ttu-id="77c65-103">ML.NET 파이프라인을 처리하는 동안 중간 데이터 값 검사</span><span class="sxs-lookup"><span data-stu-id="77c65-103">Inspect intermediate data values during ML.NET pipeline processing</span></span>

<span data-ttu-id="77c65-104">실험 중에 지정된 지점에서 데이터 처리 결과를 관찰하고 확인하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c65-104">During the experiment, you may want to observe and validate the data processing results at a given point.</span></span> <span data-ttu-id="77c65-105">ML.NET 작업이 지연되어 데이터의 '프라미스'인 개체를 생성하는 것이 쉽지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77c65-105">This isn't easy since ML.NET operations are lazy, constructing objects that are 'promises' of data.</span></span>

<span data-ttu-id="77c65-106">`GetColumn<T>` 확장 메서드를 사용하면 중간 데이터를 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c65-106">The `GetColumn<T>` extension method lets you inspect the intermediate data.</span></span> <span data-ttu-id="77c65-107">그러면 한 데이터 열의 콘텐츠를 `IEnumerable`로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="77c65-107">It returns the contents of one data column as an `IEnumerable`.</span></span>

<span data-ttu-id="77c65-108">다음 예제에서는 `GetColumn<T>` 확장 메서드를 사용하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="77c65-108">The following example shows how to use the `GetColumn<T>` extension method:</span></span>

<span data-ttu-id="77c65-109">[예제 파일](https://github.com/dotnet/machinelearning/tree/master/test/data/adult.tiny.with-schema.txt):</span><span class="sxs-lookup"><span data-stu-id="77c65-109">[Example file](https://github.com/dotnet/machinelearning/tree/master/test/data/adult.tiny.with-schema.txt):</span></span>
```
Label   Workclass   education   marital-status
0   Private 11th    Never-married
0   Private HS-grad Married-civ-spouse
1   Local-gov   Assoc-acdm  Married-civ-spouse
1   Private Some-college    Married-civ-spouse

```

<span data-ttu-id="77c65-110">클래스는 다음과 같이 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c65-110">Our class is defined as follows:</span></span>

```csharp
public class InspectedRow
{
    [LoadColumn(0)]
    public bool IsOver50K { get; set; }
    [LoadColumn(1)]
    public string WorkClass { get; set; }
    [LoadColumn(2)]
    public string Education { get; set; }
    [LoadColumn(3)]
    public string MaritalStatus { get; set; }
}
```

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Read the data into a data view.
var data = mlContext.Data.ReadFromTextFile<InspectedRow>(dataPath, hasHeader: true);

// Start creating our processing pipeline. For now, let's just concatenate all the text columns
// together into one.
var pipeline = mlContext.Transforms.Concatenate("AllFeatures", "WorkClass", "Education", "MaritalStatus");

// Fit our data pipeline and transform data with it.
var transformedData = pipeline.Fit(data).Transform(data);

// Extract the 'AllFeatures' column.
// This will give the entire dataset: make sure to only take several row
// in case the dataset is huge. The is similar to the static API, except
// you have to specify the column name and type.
var featureColumns =
    transformedData
        .GetColumn<string[]>(mlContext, "AllFeatures")
        .Take(20)
        .ToArray();
```
