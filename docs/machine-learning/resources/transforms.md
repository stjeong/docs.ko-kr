---
title: ML.NET의 데이터 변환
description: ML.NET에서 지원되는 다양한 데이터 변환을 살펴봅니다.
author: JRAlexander
ms.date: 10/16/2018
ms.openlocfilehash: c169319937dac13747935e451952bd75d4cc174d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143950"
---
# <a name="data-transforms-in-mlnet"></a>ML.NET의 데이터 변환

다음 표는 ML.NET에서 지원되는 모든 데이터 변환에 대한 정보를 포함합니다(데이터 변환 형식을 선택하여 해당 테이블로 이동).

* [범주](#categorical)
* [결합자 및 분리기](#combiners-and-segregators)
* [기능 선택](#feature-selection)
* [Featurizer](#featurizers)
* [레이블 구문 분석](#label-parsing)
* [누락 값](#missing-values)
* [정규화](#normalization)
* [행 필터](#row-filters)
* [스키마](#schema)
* [텍스트 처리 및 기능화](#text-processing-and-featurization)
* [기타](#miscellaneous)

> [!NOTE]
> ML.NET은 현재 미리 보기로 제공됩니다. 일부 데이터 변환은 현재 지원되지 않습니다. 특정 변환에 대한 요청을 제출하려면 [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) GitHub 리포지토리에서 문제를 엽니다.

## <a name="categorical"></a>범주

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CategoricalHashOneHotVectorizer> | 해시 기반 인코딩을 사용하여 범주 변수를 인코딩합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.CategoricalOneHotVectorizer> | 용어 사전 기반의 원-핫 인코딩을 사용하여 범주 변수를 인코딩합니다. |

## <a name="combiners-and-segregators"></a>결합자 및 분리기

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CombinerByContiguousGroupId> | 스칼라 열의 값을 인접 그룹 ID 기반의 벡터로 그룹화합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureCombiner> | 모든 기능을 하나의 기능 열로 결합합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ManyHeterogeneousModelCombiner> | TransformModels의 시퀀스 및 PredictorModel을 단일 PredictorModel로 결합합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ModelCombiner> | TransformModels의 시퀀스를 단일 모델로 결합합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.Segregator> | 벡터 열을 행의 시퀀스로 그룹을 해제합니다(그룹 변환의 반대). |
| <xref:Microsoft.ML.Legacy.Transforms.TwoHeterogeneousModelCombiner> | TransformModel 및 PredictorModel을 단일 PredictorModel로 결합합니다. |

## <a name="feature-selection"></a>기능 선택

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureSelectorByCount> | 기본이 아닌 값의 개수가 임계값보다 크거나 같은 슬롯을 선택합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureSelectorByMutualInformation> | 레이블 열을 사용하여 해당 상호 정보로 정렬된 지정된 모든 열에서 상위 k 슬롯을 선택합니다. |

## <a name="featurizers"></a>Featurizer

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.HashConverter> | 열 값을 해시로 변환합니다. 이 변환은 숫자 및 텍스트 입력 모두와 단일 및 벡터 값 열 모두를 허용합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.TreeLeafFeaturizer> | 트리 앙상블을 학습하거나 파일에서 로드한 다음, 숫자 기능 벡터를 세 개의 출력으로 매핑합니다. 1 개별 트리를 포함하는 벡터는 트리 앙상블을 출력합니다. 2. 기능 벡터가 트리 앙상블에서 떨어지는 잎을 나타내는 벡터 3. 기능 벡터가 트리 앙상블에서 떨어지는 경로를 나타내는 벡터 모델 파일 및 교육 담당자가 모두 지정된 경우 벡터는 모델 파일을 사용합니다. 모두 지정되지 않은 경우 벡터는 기본 FastTree 모델을 학습합니다. 필요에 따라 해당 순열 인덱스에 대해 회귀 모델을 학습하여 키 레이블을 처리할 수 있습니다. |

## <a name="label-parsing"></a>레이블 구문 분석

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.Dictionarizer> | 입력 값(단어, 숫자 등)을 사전의 인덱스로 변환합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.LabelColumnKeyBooleanConverter> | 분류에 적합하도록 레이블을 키 또는 bool(필요한 경우)로 변환합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.LabelIndicator> | OVA에서 사용하는 레이블 리매퍼입니다. |
| <xref:Microsoft.ML.Legacy.Transforms.LabelToFloatConverter> | 회귀에 적합하도록 레이블을 부동으로 변환합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.PredictedLabelColumnOriginalValueConverter> | bool 형식이 아닌 한 예측된 레이블 열을 해당 원래 값으로 변환합니다. |

## <a name="missing-values"></a>누락 값

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueHandler> | 기본값 또는 평균값/최솟값/최댓값으로 대체하여 누락 값을 처리합니다(텍스트가 아닌 열에만 해당). 입력 열 값이 숫자인 경우 표시기 열을 선택적으로 연결할 수 있습니다. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueIndicator> | 입력 열과 동일한 수의 슬롯을 사용하여 부울 출력 열을 만듭니다. 여기서 출력 값은 입력 열의 값이 누락된 경우 true입니다. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValuesDropper> | 벡터 열에서 NA를 제거합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValuesRowDropper> | 누락 값을 포함하는 행을 필터링합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueSubstitutor> | 입력 열과 동일한 형식 및 크기의 출력 열을 만듭니다. 여기서 누락 값은 기본값 또는 평균값/최솟값/최댓값으로 대체됩니다(텍스트가 아닌 열에만 해당). |

## <a name="normalization"></a>표준화

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.BinNormalizer> | 값은 equidensity bin으로 할당되고 값은 해당 bin_number / number_of_bins로 매핑됩니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ConditionalNormalizer> | 필요한 경우에만 열을 정규화합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.GlobalContrastNormalizer> | 입력 값에 대해 글로벌 대비 정규화를 수행합니다. Y = (s * X - M) / D 여기서 s는 scale, M은 mean, D는 L2 norm 또는 표준 편차입니다. | 
| <xref:Microsoft.ML.Legacy.Transforms.LogMeanVarianceNormalizer> | 계산된 평균 및 데이터 로그의 분산을 기준으로 데이터를 정규화합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.LpNormalizer> | 단위 norm(L2, L1 또는 LInf)으로 크기를 재조정하여 벡터(행)를 개별적으로 정규화합니다. 벡터에서 다음 작업을 수행합니다.X: Y = (X - M) / D 여기서 M은 mean, D는 L2 norm, L1 norm 또는 LInf norm입니다. |
| <xref:Microsoft.ML.Legacy.Transforms.MeanVarianceNormalizer> | 계산된 평균 및 데이터의 분산을 기준으로 데이터를 정규화합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.MinMaxNormalizer> | 데이터의 관찰된 최솟값 및 최댓값을 기준으로 데이터를 정규화합니다. |

## <a name="row-filters"></a>행 필터

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.RowRangeFilter> | Single, Double 또는 Key(연속) 형식의 열에서 데이터 보기를 필터링합니다. 지정된 최소/최대 범위 내에 있는 값을 유지합니다. NaNs는 항상 필터링됩니다. 입력이 Key 형식인 경우 최소/최대는 값 수의 백분율로 간주됩니다. |
| <xref:Microsoft.ML.Legacy.Transforms.RowSkipAndTakeFilter> | 선택적 오프셋에서 행의 하위 집합으로 입력 제한을 허용합니다. 데이터 페이징을 구현하는 데 사용될 수 있습니다. |
| <xref:Microsoft.ML.Legacy.Transforms.RowSkipFilter> | 행 수를 건너뛰어 행의 하위 집합으로 입력 제한을 허용합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.RowTakeFilter> | N을 첫 번째 행으로 사용하여 행의 하위 집합으로 입력 제한을 허용합니다. |

## <a name="schema"></a>스키마

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator> | 동일한 항목 종류의 두 열을 연결합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnCopier> | 데이터 집합에서 열을 복제합니다.|
| <xref:Microsoft.ML.Legacy.Transforms.ColumnDropper> | 데이터 집합에서 열을 삭제합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnSelector> | 다른 모든 열을 삭제하여 열 집합을 선택합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnTypeConverter> | 표준 변환을 사용하여 다른 형식으로 열을 변환합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.KeyToTextConverter> | KeyToValueTransform은 KeyValues 메타데이터를 활용하여 키 인덱스를 KeyValues 메타데이터의 해당 값으로 매핑합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.NGramTranslator> | 키의 지정된 벡터에서 ngrams 개수 모음(1-n 길이의 연속 값의 시퀀스)을 생성합니다. ngrams의 사전을 빌드하고 모음의 인덱스로 사전의 ID를 사용하여 이를 수행합니다. | 
| <xref:Microsoft.ML.Legacy.Transforms.OptionalColumnCreator> | 역직렬화 후에 원본 열이 존재하지 않는 경우 올바른 형식 및 기본값을 사용하여 열을 만듭니다. |

## <a name="text-processing-and-featurization"></a>텍스트 처리 및 기능화

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CharacterTokenizer> | 텍스트가 문자의 시퀀스로 간주되는 문자 기반 토크나이저입니다. |
| <xref:Microsoft.ML.Legacy.Transforms.TextFeaturizer> | 텍스트 문서의 컬렉션을 숫자 기능 벡터로 반환하는 변환입니다. 기능 벡터는 지정된 토큰화된 텍스트에서 ngrams의 정규화된 개수입니다(단어 및/또는 문자). |
| <xref:Microsoft.ML.Legacy.Transforms.TextToKeyConverter> | 입력 값(단어, 숫자 등)을 사전의 인덱스로 변환합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.WordEmbeddings> | 미리 학습된 모델을 사용하여 텍스트 토큰의 벡터를 숫자 벡터로 변환하는 변환입니다. 기술에 대한 자세한 내용은 [단어 포함](https://en.wikipedia.org/wiki/Word_embedding) Wikipedia 페이지를 참조하세요. |
| <xref:Microsoft.ML.Legacy.Transforms.WordTokenizer> | 이 변환에 대한 입력은 텍스트이며, 출력은 원본 텍스트의 단어(토큰)를 포함하는 텍스트의 벡터입니다. 구분 기호는 공백이지만 다른 모든 문자(또는 여러 문자)를 지정할 수 있습니다. |

## <a name="miscellaneous"></a>기타

| 변형 | 정의 |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.ApproximateBootstrapSampler> | 근사치 부트스트랩 샘플링 |
| <xref:Microsoft.ML.Legacy.Transforms.BinaryPredictionScoreColumnsRenamer> | 이진 예측의 경우 긍정 클래스의 이름을 포함하도록 PredictedLabel 및 Score 열의 이름을 바꿉니다.|
| <xref:Microsoft.ML.Legacy.Transforms.DataCache> | 지정된 캐시 옵션을 사용하여 캐시합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.DatasetScorer> | 예측 모델을 사용하여 데이터 집합의 점수를 매깁니다. |
| <xref:Microsoft.ML.Legacy.Transforms.DatasetTransformScorer> | 변환 모델을 사용하여 데이터 집합의 점수를 매깁니다. |
| <xref:Microsoft.ML.Legacy.Transforms.NoOperation> | 아무 작업도 수행하지 않습니다. |
| <xref:Microsoft.ML.Legacy.Transforms.RandomNumberGenerator> | 생성된 번호 시퀀스를 사용하여 열을 추가합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.ScoreColumnSelector> | 마지막 점수 열 및 인수에 지정된 추가 열만을 선택합니다. |
| <xref:Microsoft.ML.Legacy.Transforms.Scorer> | 예측 모델을 변환 모델로 바꿉니다. |
| <xref:Microsoft.ML.Legacy.Transforms.SentimentAnalyzer> | 미리 학습된 감정 모델을 사용하여 입력 문자열의 점수를 매깁니다. |
| <xref:Microsoft.ML.Legacy.Transforms.TrainTestDatasetSplitter> | 데이터 집합을 학습 및 테스트 집합으로 분할합니다. |
