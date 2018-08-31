---
title: 데이터 변환
description: ML.NET에서 지원되는 다양한 데이터 변환을 살펴봅니다.
ms.date: 08/08/2018
author: jralexander
ms.author: johalex
ms.openlocfilehash: 3c483f4a263052eb15435775a47f514893eee049
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43000855"
---
# <a name="data-transforms"></a><span data-ttu-id="023c8-103">데이터 변환</span><span class="sxs-lookup"><span data-stu-id="023c8-103">Data transforms</span></span>

<span data-ttu-id="023c8-104">다음 표는 ML.NET에서 지원되는 모든 데이터 변환에 대한 정보를 포함합니다(데이터 변환 형식을 선택하여 해당 테이블로 이동).</span><span class="sxs-lookup"><span data-stu-id="023c8-104">The following tables contain information about all of the data transforms supported in ML.NET (select the data transform type to navigate to the corresponding table):</span></span>

* [<span data-ttu-id="023c8-105">범주</span><span class="sxs-lookup"><span data-stu-id="023c8-105">Categorical</span></span>](#categorical)
* [<span data-ttu-id="023c8-106">결합자 및 분리기</span><span class="sxs-lookup"><span data-stu-id="023c8-106">Combiners and segregators</span></span>](#combiners-and-segregators)
* [<span data-ttu-id="023c8-107">기능 선택</span><span class="sxs-lookup"><span data-stu-id="023c8-107">Feature selection</span></span>](#feature-selection)
* [<span data-ttu-id="023c8-108">Featurizer</span><span class="sxs-lookup"><span data-stu-id="023c8-108">Featurizers</span></span>](#featurizers)
* [<span data-ttu-id="023c8-109">레이블 구문 분석</span><span class="sxs-lookup"><span data-stu-id="023c8-109">Label parsing</span></span>](#label-parsing)
* [<span data-ttu-id="023c8-110">누락 값</span><span class="sxs-lookup"><span data-stu-id="023c8-110">Missing Values</span></span>](#missing-values)
* [<span data-ttu-id="023c8-111">정규화</span><span class="sxs-lookup"><span data-stu-id="023c8-111">Normalization</span></span>](#normalization)
* [<span data-ttu-id="023c8-112">행 필터</span><span class="sxs-lookup"><span data-stu-id="023c8-112">Row filters</span></span>](#row-filters)
* [<span data-ttu-id="023c8-113">스키마</span><span class="sxs-lookup"><span data-stu-id="023c8-113">Schema</span></span>](#schema)
* [<span data-ttu-id="023c8-114">텍스트 처리 및 기능화</span><span class="sxs-lookup"><span data-stu-id="023c8-114">Text processing and featurization</span></span>](#text-processing-and-featurization)
* [<span data-ttu-id="023c8-115">기타</span><span class="sxs-lookup"><span data-stu-id="023c8-115">Miscellaneous</span></span>](#miscellaneous)

> [!NOTE]
> <span data-ttu-id="023c8-116">ML.NET은 현재 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-116">ML.NET is currently in Preview.</span></span> <span data-ttu-id="023c8-117">일부 데이터 변환은 현재 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-117">Not all data transforms are currently supported.</span></span> <span data-ttu-id="023c8-118">특정 변환에 대한 요청을 제출하려면 [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub 리포지토리에서 문제를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-118">To submit a request for a certain transform, open an issue in the [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub repository.</span></span>

## <a name="categorical"></a><span data-ttu-id="023c8-119">범주</span><span class="sxs-lookup"><span data-stu-id="023c8-119">Categorical</span></span>

| <span data-ttu-id="023c8-120">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-120">Transform</span></span> | <span data-ttu-id="023c8-121">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-121">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CategoricalHashOneHotVectorizer> | <span data-ttu-id="023c8-122">해시 기반 인코딩을 사용하여 범주 변수를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-122">Encodes the categorical variable with hash-based encoding.</span></span> |
| <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer> | <span data-ttu-id="023c8-123">용어 사전 기반의 원-핫 인코딩을 사용하여 범주 변수를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-123">Encodes the categorical variable with one-hot encoding based on a term dictionary.</span></span> |

## <a name="combiners-and-segregators"></a><span data-ttu-id="023c8-124">결합자 및 분리기</span><span class="sxs-lookup"><span data-stu-id="023c8-124">Combiners and segregators</span></span>

| <span data-ttu-id="023c8-125">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-125">Transform</span></span> | <span data-ttu-id="023c8-126">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-126">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CombinerByContiguousGroupId> | <span data-ttu-id="023c8-127">스칼라 열의 값을 인접 그룹 ID 기반의 벡터로 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-127">Groups values of a scalar column into a vector based on a contiguous group ID.</span></span> |
| <xref:Microsoft.ML.Transforms.FeatureCombiner> | <span data-ttu-id="023c8-128">모든 기능을 하나의 기능 열로 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-128">Combines all the features into one feature column.</span></span> |
| <xref:Microsoft.ML.Transforms.ManyHeterogeneousModelCombiner> | <span data-ttu-id="023c8-129">TransformModels의 시퀀스 및 PredictorModel을 단일 PredictorModel로 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-129">Combines a sequence of TransformModels and a PredictorModel into a single PredictorModel.</span></span> |
| <xref:Microsoft.ML.Transforms.ModelCombiner> | <span data-ttu-id="023c8-130">TransformModels의 시퀀스를 단일 모델로 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-130">Combines a sequence of TransformModels into a single model.</span></span> |
| <xref:Microsoft.ML.Transforms.Segregator> | <span data-ttu-id="023c8-131">벡터 열을 행의 시퀀스로 그룹을 해제합니다(그룹 변환의 반대).</span><span class="sxs-lookup"><span data-stu-id="023c8-131">Ungroups vector columns into sequences of rows; the inverse of Group transform.</span></span> |
| <xref:Microsoft.ML.Transforms.TwoHeterogeneousModelCombiner> | <span data-ttu-id="023c8-132">TransformModel 및 PredictorModel을 단일 PredictorModel로 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-132">Combines a TransformModel and a PredictorModel into a single PredictorModel.</span></span> |

## <a name="feature-selection"></a><span data-ttu-id="023c8-133">기능 선택</span><span class="sxs-lookup"><span data-stu-id="023c8-133">Feature selection</span></span>

| <span data-ttu-id="023c8-134">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-134">Transform</span></span> | <span data-ttu-id="023c8-135">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-135">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByCount> | <span data-ttu-id="023c8-136">기본이 아닌 값의 개수가 임계값보다 크거나 같은 슬롯을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-136">Selects the slots for which the count of non-default values is greater than or equal to a threshold.</span></span> |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByMutualInformation> | <span data-ttu-id="023c8-137">레이블 열을 사용하여 해당 상호 정보로 정렬된 지정된 모든 열에서 상위 k 슬롯을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-137">Selects the top k slots across all specified columns ordered by their mutual information with the label column.</span></span> |

## <a name="featurizers"></a><span data-ttu-id="023c8-138">Featurizer</span><span class="sxs-lookup"><span data-stu-id="023c8-138">Featurizers</span></span>

| <span data-ttu-id="023c8-139">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-139">Transform</span></span> | <span data-ttu-id="023c8-140">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-140">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.HashConverter> | <span data-ttu-id="023c8-141">열 값을 해시로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-141">Converts column values into hashes.</span></span> <span data-ttu-id="023c8-142">이 변환은 숫자 및 텍스트 입력 모두와 단일 및 벡터 값 열 모두를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-142">This transform accepts both numeric and text inputs, both single and vector-valued columns.</span></span> |
| <xref:Microsoft.ML.Transforms.TreeLeafFeaturizer> | <span data-ttu-id="023c8-143">트리 앙상블을 학습하거나 파일에서 로드한 다음, 숫자 기능 벡터를 세 개의 출력으로 매핑합니다. 1</span><span class="sxs-lookup"><span data-stu-id="023c8-143">Trains a tree ensemble, or loads it from a file, then maps a numeric feature vector to three outputs: 1.</span></span> <span data-ttu-id="023c8-144">개별 트리를 포함하는 벡터는 트리 앙상블을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-144">A vector containing the individual tree outputs of the tree ensemble.</span></span> <span data-ttu-id="023c8-145">2.</span><span class="sxs-lookup"><span data-stu-id="023c8-145">2.</span></span> <span data-ttu-id="023c8-146">기능 벡터가 트리 앙상블에서 떨어지는 잎을 나타내는 벡터</span><span class="sxs-lookup"><span data-stu-id="023c8-146">A vector indicating the leaves that the feature vector falls on in the tree ensemble.</span></span> <span data-ttu-id="023c8-147">3.</span><span class="sxs-lookup"><span data-stu-id="023c8-147">3.</span></span> <span data-ttu-id="023c8-148">기능 벡터가 트리 앙상블에서 떨어지는 경로를 나타내는 벡터</span><span class="sxs-lookup"><span data-stu-id="023c8-148">A vector indicating the paths that the feature vector falls on in the tree ensemble.</span></span> <span data-ttu-id="023c8-149">모델 파일 및 교육 담당자가 모두 지정된 경우 벡터는 모델 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-149">If both a model file and a trainer are specified, the vector will use the model file.</span></span> <span data-ttu-id="023c8-150">모두 지정되지 않은 경우 벡터는 기본 FastTree 모델을 학습합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-150">If neither are specified, the vector will train a default FastTree model.</span></span> <span data-ttu-id="023c8-151">필요에 따라 해당 순열 인덱스에 대해 회귀 모델을 학습하여 키 레이블을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-151">This can handle key labels by training a regression model towards their optionally permuted indices.</span></span> |

## <a name="label-parsing"></a><span data-ttu-id="023c8-152">레이블 구문 분석</span><span class="sxs-lookup"><span data-stu-id="023c8-152">Label parsing</span></span>

| <span data-ttu-id="023c8-153">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-153">Transform</span></span> | <span data-ttu-id="023c8-154">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-154">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Dictionarizer> | <span data-ttu-id="023c8-155">입력 값(단어, 숫자 등)을 사전의 인덱스로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-155">Converts input values (words, numbers, etc.) to index in a dictionary.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelColumnKeyBooleanConverter> | <span data-ttu-id="023c8-156">분류에 적합하도록 레이블을 키 또는 bool(필요한 경우)로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-156">Transforms the label to either key or bool (if needed) to make it suitable for classification.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelIndicator> | <span data-ttu-id="023c8-157">OVA에서 사용하는 레이블 리매퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-157">Label remapper used by OVA.</span></span> |
| <xref:Microsoft.ML.Transforms.LabelToFloatConverter> | <span data-ttu-id="023c8-158">회귀에 적합하도록 레이블을 부동으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-158">Transforms the label to float to make it suitable for regression.</span></span> |
| <xref:Microsoft.ML.Transforms.PredictedLabelColumnOriginalValueConverter> | <span data-ttu-id="023c8-159">bool 형식이 아닌 한 예측된 레이블 열을 해당 원래 값으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-159">Transforms a predicted label column to its original values, unless it is of type bool.</span></span> |

## <a name="missing-values"></a><span data-ttu-id="023c8-160">누락 값</span><span class="sxs-lookup"><span data-stu-id="023c8-160">Missing Values</span></span>

| <span data-ttu-id="023c8-161">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-161">Transform</span></span> | <span data-ttu-id="023c8-162">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-162">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.MissingValueHandler> | <span data-ttu-id="023c8-163">기본값 또는 평균값/최솟값/최댓값으로 대체하여 누락 값을 처리합니다(텍스트가 아닌 열에만 해당).</span><span class="sxs-lookup"><span data-stu-id="023c8-163">Handle missing values by replacing them with either the default value or the mean/min/max value (for non-text columns only).</span></span> <span data-ttu-id="023c8-164">입력 열 값이 숫자인 경우 표시기 열을 선택적으로 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-164">An indicator column can optionally be concatenated, if the input column type is numeric.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValueIndicator> | <span data-ttu-id="023c8-165">입력 열과 동일한 수의 슬롯을 사용하여 부울 출력 열을 만듭니다. 여기서 출력 값은 입력 열의 값이 누락된 경우 true입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-165">Create a boolean output column with the same number of slots as the input column, where the output value is true if the value in the input column is missing.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValuesDropper> | <span data-ttu-id="023c8-166">벡터 열에서 NA를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-166">Removes NAs from vector columns.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValuesRowDropper> | <span data-ttu-id="023c8-167">누락 값을 포함하는 행을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-167">Filters out rows that contain missing values.</span></span> |
| <xref:Microsoft.ML.Transforms.MissingValueSubstitutor> | <span data-ttu-id="023c8-168">입력 열과 동일한 형식 및 크기의 출력 열을 만듭니다. 여기서 누락 값은 기본값 또는 평균값/최솟값/최댓값으로 대체됩니다(텍스트가 아닌 열에만 해당).</span><span class="sxs-lookup"><span data-stu-id="023c8-168">Create an output column of the same type and size of the input column, where missing values are replaced with either the default value or the mean/min/max value (for non-text columns only).</span></span> |

## <a name="normalization"></a><span data-ttu-id="023c8-169">표준화</span><span class="sxs-lookup"><span data-stu-id="023c8-169">Normalization</span></span>

| <span data-ttu-id="023c8-170">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-170">Transform</span></span> | <span data-ttu-id="023c8-171">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-171">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.BinNormalizer> | <span data-ttu-id="023c8-172">값은 equidensity bin으로 할당되고 값은 해당 bin_number / number_of_bins로 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-172">The values are assigned into equidensity bins and a value is mapped to its bin_number / number_of_bins.</span></span> |
| <xref:Microsoft.ML.Transforms.ConditionalNormalizer> | <span data-ttu-id="023c8-173">필요한 경우에만 열을 정규화합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-173">Normalize the columns only if needed.</span></span> |
| <xref:Microsoft.ML.Transforms.GlobalContrastNormalizer> | <span data-ttu-id="023c8-174">입력 값에 대해 글로벌 대비 정규화를 수행합니다. Y = (s \* X - M) / D 여기서 s는 scale, M은 mean, D는 L2 norm 또는 표준 편차입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-174">Performs a global contrast normalization on input values: Y = (s \* X - M) / D, where s is a scale, M is mean and D is either L2 norm or standard deviation.</span></span> | 
| <xref:Microsoft.ML.Transforms.LogMeanVarianceNormalizer> | <span data-ttu-id="023c8-175">계산된 평균 및 데이터 로그의 분산을 기준으로 데이터를 정규화합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-175">Normalizes the data based on the computed mean and variance of the logarithm of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.LpNormalizer> | <span data-ttu-id="023c8-176">단위 norm(L2, L1 또는 LInf)으로 크기를 재조정하여 벡터(행)를 개별적으로 정규화합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-176">Normalize vectors (rows) individually by rescaling them to the unit norm (L2, L1 or LInf).</span></span> <span data-ttu-id="023c8-177">벡터에서 다음 작업을 수행합니다.X: Y = (X - M) / D 여기서 M은 mean, D는 L2 norm, L1 norm 또는 LInf norm입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-177">Performs the following operation on a vector X: Y = (X - M) / D, where M is mean and D is either the L2 norm, the L1 norm, or the LInf norm.</span></span> |
| <xref:Microsoft.ML.Transforms.MeanVarianceNormalizer> | <span data-ttu-id="023c8-178">계산된 평균 및 데이터의 분산을 기준으로 데이터를 정규화합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-178">Normalizes the data based on the computed mean and variance of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.MinMaxNormalizer> | <span data-ttu-id="023c8-179">데이터의 관찰된 최솟값 및 최댓값을 기준으로 데이터를 정규화합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-179">Normalizes the data based on the observed minimum and maximum values of the data.</span></span> |
| <xref:Microsoft.ML.Transforms.SupervisedBinNormalizer> | <span data-ttu-id="023c8-180"><xref:Microsoft.ML.Transforms.BinNormalizer>와 유사하지만 equidensity가 아닌 레이블 열을 사용하여 상관 관계에 따라 bins를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-180">Similar to <xref:Microsoft.ML.Transforms.BinNormalizer>, but calculates bins based on correlation with the label column, not equidensity.</span></span> <span data-ttu-id="023c8-181">새 값은 bin_number / number_of_bins입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-181">The new value is bin_number / number_of_bins.</span></span> |

## <a name="row-filters"></a><span data-ttu-id="023c8-182">행 필터</span><span class="sxs-lookup"><span data-stu-id="023c8-182">Row Filters</span></span>

| <span data-ttu-id="023c8-183">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-183">Transform</span></span> | <span data-ttu-id="023c8-184">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-184">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.RowRangeFilter> | <span data-ttu-id="023c8-185">Single, Double 또는 Key(연속) 형식의 열에서 데이터 보기를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-185">Filters a dataview on a column of type Single, Double or Key (contiguous).</span></span> <span data-ttu-id="023c8-186">지정된 최소/최대 범위 내에 있는 값을 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-186">Keeps the values that are in the specified min/max range.</span></span> <span data-ttu-id="023c8-187">NaNs는 항상 필터링됩니다. 입력이 Key 형식인 경우 최소/최대는 값 수의 백분율로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-187">NaNs are always filtered out. If the input is a Key type, the min/max are considered percentages of the number of values.</span></span> |
| <xref:Microsoft.ML.Transforms.RowSkipAndTakeFilter> | <span data-ttu-id="023c8-188">선택적 오프셋에서 행의 하위 집합으로 입력 제한을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-188">Allows limiting input to a subset of rows at an optional offset.</span></span> <span data-ttu-id="023c8-189">데이터 페이징을 구현하는 데 사용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-189">Can be used to implement data paging.</span></span> |
| <xref:Microsoft.ML.Transforms.RowSkipFilter> | <span data-ttu-id="023c8-190">행 수를 건너뛰어 행의 하위 집합으로 입력 제한을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-190">Allows limiting input to a subset of rows by skipping a number of rows.</span></span> |
| <xref:Microsoft.ML.Transforms.RowTakeFilter> | <span data-ttu-id="023c8-191">N을 첫 번째 행으로 사용하여 행의 하위 집합으로 입력 제한을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-191">Allows limiting input to a subset of rows by taking N first rows.</span></span> |

## <a name="schema"></a><span data-ttu-id="023c8-192">스키마</span><span class="sxs-lookup"><span data-stu-id="023c8-192">Schema</span></span>

| <span data-ttu-id="023c8-193">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-193">Transform</span></span> | <span data-ttu-id="023c8-194">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-194">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ColumnConcatenator> | <span data-ttu-id="023c8-195">동일한 항목 종류의 두 열을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-195">Concatenates two columns of the same item type.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnCopier> | <span data-ttu-id="023c8-196">데이터 집합에서 열을 복제합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-196">Duplicates columns from the dataset.</span></span>|
| <xref:Microsoft.ML.Transforms.ColumnDropper> | <span data-ttu-id="023c8-197">데이터 집합에서 열을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-197">Drops columns from the dataset.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnSelector> | <span data-ttu-id="023c8-198">다른 모든 열을 삭제하여 열 집합을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-198">Selects a set of columns, dropping all others.</span></span> |
| <xref:Microsoft.ML.Transforms.ColumnTypeConverter> | <span data-ttu-id="023c8-199">표준 변환을 사용하여 다른 형식으로 열을 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-199">Converts a column to a different type, using standard conversions.</span></span> |
| <xref:Microsoft.ML.Transforms.KeyToTextConverter> | <span data-ttu-id="023c8-200">KeyToValueTransform은 KeyValues 메타데이터를 활용하여 키 인덱스를 KeyValues 메타데이터의 해당 값으로 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-200">KeyToValueTransform utilizes KeyValues metadata to map key indices to the corresponding values in the KeyValues metadata.</span></span> |
| <xref:Microsoft.ML.Transforms.NGramTranslator> | <span data-ttu-id="023c8-201">키의 지정된 벡터에서 ngrams 개수 모음(1-n 길이의 연속 값의 시퀀스)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-201">Produces a bag of counts of ngrams (sequences of consecutive values of length 1-n) in a given vector of keys.</span></span> <span data-ttu-id="023c8-202">ngrams의 사전을 빌드하고 모음의 인덱스로 사전의 ID를 사용하여 이를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-202">It does so by building a dictionary of ngrams and using the id in the dictionary as the index in the bag.</span></span> | 
| <xref:Microsoft.ML.Transforms.OptionalColumnCreator> | <span data-ttu-id="023c8-203">역직렬화 후에 원본 열이 존재하지 않는 경우 올바른 형식 및 기본값을 사용하여 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-203">If the source column does not exist after deserialization, create a column with the right type and default values.</span></span> |

## <a name="text-processing-and-featurization"></a><span data-ttu-id="023c8-204">텍스트 처리 및 기능화</span><span class="sxs-lookup"><span data-stu-id="023c8-204">Text processing and featurization</span></span>

| <span data-ttu-id="023c8-205">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-205">Transform</span></span> | <span data-ttu-id="023c8-206">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-206">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CharacterTokenizer> | <span data-ttu-id="023c8-207">텍스트가 문자의 시퀀스로 간주되는 문자 기반 토크나이저입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-207">Character-oriented tokenizer where text is considered a sequence of characters.</span></span> |
| <xref:Microsoft.ML.Transforms.TextFeaturizer> | <span data-ttu-id="023c8-208">텍스트 문서의 컬렉션을 숫자 기능 벡터로 반환하는 변환입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-208">A transform that turns a collection of text documents into numerical feature vectors.</span></span> <span data-ttu-id="023c8-209">기능 벡터는 지정된 토큰화된 텍스트에서 ngrams의 정규화된 개수입니다(단어 및/또는 문자).</span><span class="sxs-lookup"><span data-stu-id="023c8-209">The feature vectors are normalized counts of (word and/or character) ngrams in a given tokenized text.</span></span> |
| <xref:Microsoft.ML.Transforms.TextToKeyConverter> | <span data-ttu-id="023c8-210">입력 값(단어, 숫자 등)을 사전의 인덱스로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-210">Converts input values (words, numbers, etc.) to index in a dictionary.</span></span> |
| <xref:Microsoft.ML.Transforms.WordEmbeddings> | <span data-ttu-id="023c8-211">미리 학습된 모델을 사용하여 텍스트 토큰의 벡터를 숫자 벡터로 변환하는 변환입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-211">A transform that converts vectors of text tokens into numeric vectors using a pre-trained model.</span></span> <span data-ttu-id="023c8-212">기술에 대한 자세한 내용은 [단어 포함](https://en.wikipedia.org/wiki/Word_embedding) Wikipedia 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="023c8-212">For more information about the technique, see the [Word embedding](https://en.wikipedia.org/wiki/Word_embedding) Wikipedia page.</span></span> |
| <xref:Microsoft.ML.Transforms.WordTokenizer> | <span data-ttu-id="023c8-213">이 변환에 대한 입력은 텍스트이며, 출력은 원본 텍스트의 단어(토큰)를 포함하는 텍스트의 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-213">The input to this transform is text, and the output is a vector of text containing the words (tokens) in the original text.</span></span> <span data-ttu-id="023c8-214">구분 기호는 공백이지만 다른 모든 문자(또는 여러 문자)를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-214">The separator is space, but any other character (or multiple characters) can be specified.</span></span> |

## <a name="miscellaneous"></a><span data-ttu-id="023c8-215">기타</span><span class="sxs-lookup"><span data-stu-id="023c8-215">Miscellaneous</span></span>

| <span data-ttu-id="023c8-216">변형</span><span class="sxs-lookup"><span data-stu-id="023c8-216">Transform</span></span> | <span data-ttu-id="023c8-217">정의</span><span class="sxs-lookup"><span data-stu-id="023c8-217">Definition</span></span> |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ApproximateBootstrapSampler> | <span data-ttu-id="023c8-218">근사치 부트스트랩 샘플링</span><span class="sxs-lookup"><span data-stu-id="023c8-218">Approximate bootstrap sampling.</span></span> |
| <xref:Microsoft.ML.Transforms.BinaryPredictionScoreColumnsRenamer> | <span data-ttu-id="023c8-219">이진 예측의 경우 긍정 클래스의 이름을 포함하도록 PredictedLabel 및 Score 열의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-219">For binary prediction, renames the PredictedLabel and Score columns to include the name of the positive class.</span></span>|
| <xref:Microsoft.ML.Transforms.DataCache> | <span data-ttu-id="023c8-220">지정된 캐시 옵션을 사용하여 캐시합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-220">Caches using the specified cache option.</span></span> |
| <xref:Microsoft.ML.Transforms.DatasetScorer> | <span data-ttu-id="023c8-221">예측 모델을 사용하여 데이터 집합의 점수를 매깁니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-221">Scores a dataset with a predictor model.</span></span> |
| <xref:Microsoft.ML.Transforms.DatasetTransformScorer> | <span data-ttu-id="023c8-222">변환 모델을 사용하여 데이터 집합의 점수를 매깁니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-222">Scores a dataset with a transform model.</span></span> |
| <xref:Microsoft.ML.Transforms.NoOperation> | <span data-ttu-id="023c8-223">아무 작업도 수행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-223">Does nothing.</span></span> |
| <xref:Microsoft.ML.Transforms.RandomNumberGenerator> | <span data-ttu-id="023c8-224">생성된 번호 시퀀스를 사용하여 열을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-224">Adds a column with a generated number sequence.</span></span> |
| <xref:Microsoft.ML.Transforms.ScoreColumnSelector> | <span data-ttu-id="023c8-225">마지막 점수 열 및 인수에 지정된 추가 열만을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-225">Selects only the last score columns and the extra columns specified in the arguments.</span></span> |
| <xref:Microsoft.ML.Transforms.Scorer> | <span data-ttu-id="023c8-226">예측 모델을 변환 모델로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-226">Turns the predictor model into a transform model.</span></span> |
| <xref:Microsoft.ML.Transforms.SentimentAnalyzer> | <span data-ttu-id="023c8-227">미리 학습된 감정 모델을 사용하여 입력 문자열의 점수를 매깁니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-227">Uses a pretrained sentiment model to score input strings.</span></span> |
| <xref:Microsoft.ML.Transforms.TrainTestDatasetSplitter> | <span data-ttu-id="023c8-228">데이터 집합을 학습 및 테스트 집합으로 분할합니다.</span><span class="sxs-lookup"><span data-stu-id="023c8-228">Splits the dataset into train and test sets.</span></span> |
