---
title: 기계 학습 처리를 위해 텍스트 파일에서 데이터 로드 - ML.NET
description: ML.NET를 통해 기계 학습 모델을 빌드하고, 학습시키고, 점수 매기는 데 사용할 데이터를 텍스트 파일에서 로드하는 방법 알아보기
ms.date: 01/29/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 6a8f74cc5324050ca94e60592f083c35afc68377
ms.sourcegitcommit: dcc8feeff4718664087747529638ec9b47e65234
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55479674"
---
# <a name="load-data-from-a-text-file-for-machine-learning-processing---mlnet"></a><span data-ttu-id="7a1ae-103">기계 학습 처리를 위해 텍스트 파일에서 데이터 로드 - ML.NET</span><span class="sxs-lookup"><span data-stu-id="7a1ae-103">Load data from a text file for machine learning processing - ML.NET</span></span>

<span data-ttu-id="7a1ae-104">`TextLoader`는 텍스트 파일에서 데이터를 로드하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1ae-104">`TextLoader` is used to load data from text files.</span></span> <span data-ttu-id="7a1ae-105">데이터 열, 열 형식 및 텍스트 파일에서 해당 위치를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a1ae-105">You need to specify the data columns, their types, and their location in the text file.</span></span>

<span data-ttu-id="7a1ae-106">파일의 일부 열을 읽거나 동일한 열을 여러 번 읽어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a1ae-106">Note that it's perfectly acceptable to read some columns of a file, or read the same column multiple times.</span></span>

<span data-ttu-id="7a1ae-107">[예제 파일](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt):</span><span class="sxs-lookup"><span data-stu-id="7a1ae-107">[Example file](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt):</span></span>

```console
Label   Workclass   education   marital-status
0   Private 11th    Never-married
0   Private HS-grad Married-civ-spouse
1   Local-gov   Assoc-acdm  Married-civ-spouse
1   Private Some-college    Married-civ-spouse
```

<span data-ttu-id="7a1ae-108">텍스트 파일에서 데이터를 로드하려면</span><span class="sxs-lookup"><span data-stu-id="7a1ae-108">To load the data from a text file:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(
    columns: new TextLoader.Column[]
    {
        // A boolean column depicting the 'target label'.
        new TextLoader.Column("IsOver50k",DataKind.BL,0),
        // Three text columns.
        new TextLoader.Column("WorkClass",DataKind.TX,1),
        new TextLoader.Column("Education",DataKind.TX,2),
        new TextLoader.Column("MaritalStatus",DataKind.TX,3)
    },
    hasHeader: true
);

// Now read the file (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(dataPath);
```