---
title: ML.NET의 모델 학습에 대한 기본 개념
description: 이 문서에서는 ML.NET의 *모델 학습* 시나리오에 대한 기본 개념을 설명합니다. 일부 개념은 보다 간단한 *기존 모델을 사용한 예측* 시나리오와 관련이 없습니다.
ms.date: 11/06/2018
ms.topic: overview
ms.custom: mvc
ms.openlocfilehash: cff833b45583bc752bb42616820a95ca6c5c6b12
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "55252442"
---
# <a name="basic-concepts-for-model-training-in-mlnet"></a><span data-ttu-id="148b8-104">ML.NET의 모델 학습에 대한 기본 개념</span><span class="sxs-lookup"><span data-stu-id="148b8-104">Basic concepts for model training in ML.NET</span></span>

<span data-ttu-id="148b8-105">이 문서에서는 ML.NET의 *모델 학습* 시나리오에 대한 기본 개념을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-105">This article explains the basic concepts covering *model training* scenarios in ML.NET.</span></span> <span data-ttu-id="148b8-106">일부 개념은 보다 간단한 *기존 모델을 사용한 예측* 시나리오와 관련이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-106">Not all concepts are relevant to the more simple scenario of *prediction with existing model*.</span></span>

## <a name="model-training-concepts"></a><span data-ttu-id="148b8-107">모델 학습 개념</span><span class="sxs-lookup"><span data-stu-id="148b8-107">Model training concepts</span></span>

<span data-ttu-id="148b8-108">이 문서에서는 ML.NET의 모델 학습과 관련된 다음 개념을 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-108">This document covers the following concepts related to model training in ML.NET:</span></span>

- <span data-ttu-id="148b8-109">[데이터(*Data*)](#data)는 `IDataView` 인터페이스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-109">[*Data*](#data) represented as an `IDataView` interface.</span></span>
  - <span data-ttu-id="148b8-110">ML.NET에서 데이터는 SQL 보기와 유사합니다. 지연 평가되고, 변경할 수 없고, 커서가 가능하고, 형식이 다르며, 스키마화된 데이터 세트입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-110">In ML.NET, data is similar to a SQL view: It's a lazily evaluated, immutable, cursorable, heterogenous, schematized dataset.</span></span> 
  - <span data-ttu-id="148b8-111">데이터 인터페이스에 대한 훌륭한 문서는 [IDataView 디자인 원칙](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-111">An excellent document about the data interface is [IDataView Design Principles](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md).</span></span>
- <span data-ttu-id="148b8-112">[변환기(*Transformer*)](#transformer)는 `ITransformer` 인터페이스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-112">[*Transformer*](#transformer) represented as `ITransformer` interface.</span></span>
  - <span data-ttu-id="148b8-113">변환기는 데이터를 가져다가, 데이터에 작업을 수행하고, 변환된 새로운 데이터를 반환하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-113">A transformer is a component that takes data, does some work on it, and returns new transformed data.</span></span>
  - <span data-ttu-id="148b8-114">예를 들어 기계 학습 모델은 기능을 사용하고 예측을 반환하는 변환기로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-114">For example, you can think of a machine learning model as a transformer that takes features and returns predictions.</span></span>
  - <span data-ttu-id="148b8-115">또 다른 예로, 텍스트 토크나이저는 단일 텍스트 열을 가져와서 텍스트에서 개별 단어를 추출하여 벡터 열을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-115">Another example, text tokenizer takes a single text column and output a vector column with individual words extracted out of the texts.</span></span>
- <span data-ttu-id="148b8-116">[데이터 판독기(*Data reader*)](#data-reader)는 `IDataReader<T>` 인터페이스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-116">[*Data reader*](#data-reader) represented as an `IDataReader<T>` interface.</span></span>
  - <span data-ttu-id="148b8-117">데이터 판독기는 데이터를 만드는 ML.NET 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-117">The data reader is ML.NET component to create data.</span></span> <span data-ttu-id="148b8-118">`T` 인스턴스를 가져다가 데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-118">It takes an instance of `T` and returns data out of it.</span></span> 
  - <span data-ttu-id="148b8-119">예를 들어, *TextLoader*는 `IDataReader<FileSource>`입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-119">For example, a *TextLoader* is an `IDataReader<FileSource>`.</span></span> <span data-ttu-id="148b8-120">파일 소스를 가져다가 데이터를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-120">It takes the file source and produces data.</span></span> 
- <span data-ttu-id="148b8-121">[평가자(*Estimator*)](#estimator)는 `IEstimator<T>` 인터페이스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-121">[*Estimator*](#estimator) represented as an `IEstimator<T>` interface.</span></span>
  - <span data-ttu-id="148b8-122">데이터를 통해 학습하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-122">This is an object that learns from data.</span></span> <span data-ttu-id="148b8-123">학습의 결과는 변환기(*transformer*)입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-123">The result of the learning is a *transformer*.</span></span>
  - <span data-ttu-id="148b8-124">기계 학습 알고리즘(*algorithm*)은 데이터를 학습하고 기계 학습 모델(*model*)을 생성하는 평가자라고 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-124">You can think of a machine learning *algorithm* as an estimator that learns on data and produces a machine learning *model*.</span></span>
- <span data-ttu-id="148b8-125">[예측 함수(*Prediction function*)](#prediction-function)는 `PredictionFunction<TSrc, TDst>` 클래스로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-125">[*Prediction function*](#prediction-function) represented as a `PredictionFunction<TSrc, TDst>` class.</span></span>
  - <span data-ttu-id="148b8-126">예측 함수는 예측 시간과 같은 변환기를 한 행에 적용하는 머신으로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-126">The prediction function can be seen as a machine that applies a transformer to one row, such as at prediction time.</span></span>

## <a name="data"></a><span data-ttu-id="148b8-127">데이터</span><span class="sxs-lookup"><span data-stu-id="148b8-127">Data</span></span>

<span data-ttu-id="148b8-128">ML.NET에서 데이터는 SQL 보기와 유사합니다. 지연 평가되고, 커서가 가능하고, 형식이 다르며, 스키마화된 데이터 세트입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-128">In ML.NET, data is similar to a SQL view: It's a lazily evaluated, cursorable, heterogenous, schematized dataset.</span></span>

- <span data-ttu-id="148b8-129">데이터 뷰의 열에 대한 정보가 포함된 스키마(*Schema*)(`ISchema` 인터페이스의 인스턴스)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-129">It has *Schema* (an instance of an `ISchema` interface) that contains the information about the data view's columns.</span></span>
  - <span data-ttu-id="148b8-130">각 열에는 이름(*Name*), 유형(*Type*) 및 이와 관련된 임의의 메타데이터(*metadata*) 세트가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-130">Each column has a *Name*, a *Type*, and an arbitrary set of *metadata* associated with it.</span></span>
  - <span data-ttu-id="148b8-131">열의 메타데이터(*metadata*)에는 벡터 열의 슬롯 이름 등과 같은 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-131">The column's *metadata* contains information like slot names of a vector column and the like.</span></span> <span data-ttu-id="148b8-132">메타데이터 자체는 각 열에 고유한 또 다른 한 행 데이터(*data*)로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-132">The metadata itself is represented as another one-row *data* that is unique to each column.</span></span>
  - <span data-ttu-id="148b8-133">데이터 뷰는 커서(*cursors*)의 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-133">The data view is a source of *cursors*.</span></span> <span data-ttu-id="148b8-134">SQL 커서를 생각해보면: 커서는 한 번에 한 행씩 데이터를 반복하고 사용 가능한 데이터를 표시하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-134">Think SQL cursors: A cursor is an object that iterates through the data, one row at a time, and presents the available data.</span></span>
  - <span data-ttu-id="148b8-135">물론 데이터에는 필요한 만큼 활성 커서가 많이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-135">Naturally, data can have as many active cursors over it as needed.</span></span> <span data-ttu-id="148b8-136">데이터 자체는 변경할 수 없기 때문에 커서는 완전히 독립적입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-136">Since data itself is immutable, cursors are truly independent.</span></span>
  - <span data-ttu-id="148b8-137">커서는 일반적으로 열의 하위 집합에만 액세스합니다. 효율성을 높이기 위해 ML.NET은 커서에 필요한 열의 값만 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-137">Cursors typically access only a subset of columns: For efficiency, ML.NET computes only the values of columns that are needed by the cursor.</span></span>

## <a name="transformer"></a><span data-ttu-id="148b8-138">변환기</span><span class="sxs-lookup"><span data-stu-id="148b8-138">Transformer</span></span>

<span data-ttu-id="148b8-139">변환기는 데이터를 가져다가, 데이터에 작업을 수행하고, 변환된 새로운 데이터를 반환하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-139">A transformer is a component that takes data, does some work on it, and return new transformed data.</span></span>

<span data-ttu-id="148b8-140">ML.NET에서 대부분의 변환기는 한 번에 하나의 입력 열(*input column*)에 작동하고 출력 열(*output column*)을 생성하는 경향이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-140">Most transformers in ML.NET tend to operate on one *input column* at a time, and produce the *output column*.</span></span> <span data-ttu-id="148b8-141">예를 들어 `new HashTransformer("foo", "bar")`는 "foo" 열의 값을 가져다가, 해시를 지정하고, "bar" 열에 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-141">For example, a `new HashTransformer("foo", "bar")` takes the values from column "foo", hash them, and put them into column "bar".</span></span> 

<span data-ttu-id="148b8-142">또한, 입력 및 출력 열 이름이 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-142">It's also common that the input and output column names are the same.</span></span> <span data-ttu-id="148b8-143">이런 경우 기존 열이 새 열로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-143">In this case, the old column is replaced with the new one.</span></span> <span data-ttu-id="148b8-144">예를 들어 `new HashTransformer("foo")`는 "foo" 열의 값을 가져다가, 해시를 지정하고, "bar" 열에 다시 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-144">For example, a `new HashTransformer("foo")` takes the values from column "foo", hash them, and put them back into "foo".</span></span> 

<span data-ttu-id="148b8-145">물론, `Transform`이 호출될 때 모든 변환기는 새로운 데이터 보기를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-145">Any transformer, of course, produces a new data view when `Transform` is called.</span></span> <span data-ttu-id="148b8-146">데이터 보기는 변경할 수 없다는 것을 기억하십시오.</span><span class="sxs-lookup"><span data-stu-id="148b8-146">Remember, data views are immutable.</span></span>

<span data-ttu-id="148b8-147">또 다른 주요 고려 사항은 데이터가 지연 평가되기 때문에 *변환기도 지연*된다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-147">Another important consideration is that, because data is lazily evaluated, *transformers are lazy too*.</span></span> <span data-ttu-id="148b8-148">특히, 호출 후에</span><span class="sxs-lookup"><span data-stu-id="148b8-148">Essentially, after you call</span></span>

```csharp
var newData = transformer.Transform(oldData)
```

<span data-ttu-id="148b8-149">실제 계산 수행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-149">no actual computation happens.</span></span> <span data-ttu-id="148b8-150">`newData`에서 커서를 가져다가 값을 사용하기 시작한 후에야 `newData`는 `transformer` 변환 논리를 호출합니다(요청된 열을 생성하기 위해 `transformer`가 필요한 경우에만 해당).</span><span class="sxs-lookup"><span data-stu-id="148b8-150">Only after you get a cursor from `newData` and start consuming the value does `newData` invoke the `transformer` transformation logic (and even that only if `transformer` in question is needed to produce the requested columns).</span></span>

### <a name="transformer-chains"></a><span data-ttu-id="148b8-151">변환기 체인</span><span class="sxs-lookup"><span data-stu-id="148b8-151">Transformer chains</span></span>

<span data-ttu-id="148b8-152">변환기의 유용한 속성은 변환기의 순차적인 적용을 또 다른 변환기로 사용할 수 있다는 점입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-152">A useful property of a transformer is that *you can phrase a sequential application of transformers as yet another transformer*:</span></span>

```csharp
var fullTransformer = transformer1.Append(transformer2).Append(transformer3);
```

<span data-ttu-id="148b8-153">이 속성은 ML.NET에서 일반적으로 사용됩니다. 일반적으로, 학습된 ML.NET 모델은 모든 의도와 목적을 위한 변환기(*transformer*)의 연결인 변환기 체인입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-153">This property is commonly used in ML.NET: typically, the trained ML.NET model is a chain of transformers, which is, for all intents and purposes, a *transformer*.</span></span> 

## <a name="data-reader"></a><span data-ttu-id="148b8-154">데이터 판독기</span><span class="sxs-lookup"><span data-stu-id="148b8-154">Data reader</span></span>

<span data-ttu-id="148b8-155">데이터 판독기는 데이터를 '생성'하는 ML.NET 구성 요소입니다. `T` 인스턴스를 가져다가 데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-155">The data reader is ML.NET component to 'create' data: it takes an instance of `T` and returns data out of it.</span></span>

<span data-ttu-id="148b8-156">흥미로운 점은, 기존 데이터 판독기에 변환기를 연결하여 데이터 판독기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-156">An interesting property to note is that you can create a data reader by attaching a transformer to an existing data reader.</span></span> <span data-ttu-id="148b8-157">이러한 방식으로 변환 동작이 베이킹된 판독기를 사용 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-157">This way you can have a reader with transformation behavior baked in:</span></span>

```c#
var newReader = reader.Append(transformer1).Append(transformer2)
```

<span data-ttu-id="148b8-158">변환기와 유사한 또 다른 점은 데이터가 지연 평가되기 때문에 판독기가 지연된다는 점입니다. `dataReader.Read()`를 호출하면 실제로 '읽기'가 발생하지 않습니다(또는 최소로 발생함). 커서가 결과 데이터에 요청된 경우에만 판독기 작업이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-158">Another similarity to transformers is that, since data is lazily evaluated, *readers are lazy*: no (or minimal) actual 'reading' happens when you call `dataReader.Read()`: only when a cursor is requested on the resulting data does the reader begin to work.</span></span>

## <a name="estimator"></a><span data-ttu-id="148b8-159">평가자</span><span class="sxs-lookup"><span data-stu-id="148b8-159">Estimator</span></span>

<span data-ttu-id="148b8-160">평가자(*estimator*)는 데이터를 통해 학습하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-160">The *estimator* is an object that learns from data.</span></span> <span data-ttu-id="148b8-161">학습의 결과는 변환기(*transformer*)입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-161">The result of the learning is a *transformer*.</span></span>

<span data-ttu-id="148b8-162">ML.NET에서는 이 속성을 사용하여 다른 평가자를 연결하는 학습 파이프 라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-162">In ML.NET, use this property to create learning pipelines that chain together different estimators:</span></span>

```csharp
MLContext mlContext = new MLContext(seed: 0);

var pipeline = new CopyColumnsEstimator(mlContext, "FareAmount", "Label")
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "VendorId"))
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "RateCode"))
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "PaymentType"))
.Append(new ColumnConcatenatingEstimator(mlContext, "Features", "VendorId", "RateCode", "PassengerCount", "TripTime", "TripDistance", "PaymentType"))
.Append(mlContext.Regression.Trainers.FastTree("Label", "Features"));

var model = pipeline.Fit(dataView);
```

<span data-ttu-id="148b8-163">평가자의 중요한 특성 중 하나는 지연되지 않고 즉시 수행된다는 점입니다.`Fit`을 호출할 때마다 학습이 발생하며 이러한 작업은 잠재적으로 시간이 오래 걸리는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-163">One important property of estimators is that *estimators are eager, not lazy*: every call to `Fit` is causing learning to happen, which is potentially a time-consuming operation.</span></span>

## <a name="prediction-function"></a><span data-ttu-id="148b8-164">예측 함수</span><span class="sxs-lookup"><span data-stu-id="148b8-164">Prediction function</span></span>

<span data-ttu-id="148b8-165">예측 함수는 변환기를 한 행에 적용하는 머신으로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-165">The prediction function can be seen as a machine that applies a transformer to one row.</span></span>

<span data-ttu-id="148b8-166">모델(`Fit()`을 통해 학습된 또는 다른 곳에서 로드한 변환기(*transformer*))을 얻은 후에는 `model.Transform(data)`에 대한 일반적인 호출을 사용하여 예측을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-166">Once you get the model (a *transformer* either trained via `Fit()`, or loaded from somewhere), you can use it to make predictions using the normal calls to `model.Transform(data)`.</span></span> <span data-ttu-id="148b8-167">하지만 실제 시나리오에 이 모델을 사용하면 예측할 사례가 많지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-167">However, when you use this model in a real-life scenario, you often don't have many examples to predict on.</span></span> <span data-ttu-id="148b8-168">대신, 한 번에 하나의 예제가 있으며, 적절한 시기에 즉시 예측을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-168">Instead, you have one example at a time, and you need to make timely predictions on them immediately.</span></span>

<span data-ttu-id="148b8-169">물론 이러한 작업을 일괄 처리 예측으로 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-169">Of course, you can reduce this to the batch prediction:</span></span>

- <span data-ttu-id="148b8-170">정확히 하나의 행으로 데이터 뷰를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-170">Create a data view with exactly one row.</span></span>
- <span data-ttu-id="148b8-171">`model.Transform(data)`을 호출하여 예측된 데이터 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-171">Call `model.Transform(data)` to get the predicted data view.</span></span>
- <span data-ttu-id="148b8-172">결과 데이터에 대해 커서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-172">Get a cursor over the resulting data.</span></span>
- <span data-ttu-id="148b8-173">커서를 한 단계 전진하여 첫 번째(유일한) 행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-173">Advance the cursor one step to get to the first (and only) row.</span></span>
- <span data-ttu-id="148b8-174">여기에서 예측된 값을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-174">Extract the predicted values out of it.</span></span>

<span data-ttu-id="148b8-175">앞의 알고리즘은 다음과 같이 두 개의 사용자 정의 개체(`InputExample` 및 `OutputPrediction`)를 사용하여 [스키마 이해를](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md) 사용하여 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-175">The preceding algorithm can be implemented using the [schema comprehension](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md), with two user-defined objects `InputExample` and `OutputPrediction` as follows:</span></span>

```c#
var inputData = env.CreateDataView(new InputExample[] { example });
var outputData = model.Transform(inputData);
var output = outputData.AsDynamic.AsEnumerable<OutputPrediction>(env, reuseRowObject: false).Single();
```

<span data-ttu-id="148b8-176">하지만 이 작업은 번거롭고 성능 비용이 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-176">But this is cumbersome and incurs performance costs.</span></span> <span data-ttu-id="148b8-177">대신, 예측 함수 개체는 확장 메서드, `MakePredictionFunction`을 통해 동일한 작업을 더 빠르고 편리하게 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-177">Instead, a prediction function object performs the same work, but faster and more convenient, via an extension method `MakePredictionFunction`:</span></span>

```c#
var predictionFunc = model.MakePredictionFunction<InputExample, OutputPrediction>(env);
var output = predictionFunc.Predict(example);
```

<span data-ttu-id="148b8-178">예측 함수는 재진입하지 않고/스레드로부터 안전합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-178">The prediction function is *not re-entrant / thread-safe*.</span></span> <span data-ttu-id="148b8-179">여러 스레드에서 동시에 예측을 수행하려면 스레드당 예측 함수가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="148b8-179">If you want to conduct predictions simultaneously with multiple threads, you need to have a prediction function per thread.</span></span>
