---
title: 기계 학습 처리를 위해 여러 파일의 데이터 로드 - ML.NET
description: ML.NET를 사용하여 기계 학습 모델을 빌드하고, 학습하고, 점수를 매기는 데 사용할 여러 파일의 데이터를 로드하는 방법 알아보기
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: c9b34bd6bcbac62e9f9c33226f5d0feb41168392
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53150734"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a><span data-ttu-id="a5252-103">기계 학습 처리를 위해 여러 파일의 데이터 로드 - ML.NET</span><span class="sxs-lookup"><span data-stu-id="a5252-103">Load data from multiple files for machine learning processing - ML.NET</span></span>

<span data-ttu-id="a5252-104">`TextLoader`를 사용하고, `Read` 메서드에 대한 파일의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5252-104">Use the `TextLoader`, and specify an array of files to the `Read` method.</span></span> <span data-ttu-id="a5252-105">파일에는 동일한 스키마(동일한 번호 및 열 형식)가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5252-105">The files must have the same schema (same number and type of columns):</span></span>

* [<span data-ttu-id="a5252-106">예제 파일1</span><span class="sxs-lookup"><span data-stu-id="a5252-106">Example file1</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [<span data-ttu-id="a5252-107">예제 파일2</span><span class="sxs-lookup"><span data-stu-id="a5252-107">Example file2</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.TextReader(new TextLoader.Arguments
{
    Column = new[] {
        // A boolean column depicting the 'label'.
        new TextLoader.Column("IsOver50k", DataKind.BL, 0),
        // Three text columns.
        new TextLoader.Column("Workclass", DataKind.TX, 1),
        new TextLoader.Column("Education", DataKind.TX, 2),
        new TextLoader.Column("MaritalStatus", DataKind.TX, 3)
    },
    // First line of the file is a header, not a data row.
    HasHeader = true
});

var data = reader.Read(exampleFile1, exampleFile2);
```