---
title: 기계 학습 작업 - ML.NET
description: ML.NET에서 지원되는 다양한 기계 학습 작업 및 관련 작업을 살펴봅니다.
ms.custom: seodec18
ms.date: 01/15/2019
author: jralexander
ms.openlocfilehash: 02b454d18eca36c94c27ae15665af5df2ec87905
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415704"
---
# <a name="machine-learning-tasks-in-mlnet"></a>ML.NET의 기계 학습 작업

기계 학습 모델을 빌드할 때 먼저 데이터로 무엇을 달성하려고 하는지 정의해야 합니다. 그런 다음, 상황에 맞는 올바른 기계 학습 작업을 선택할 수 있습니다. 다음 목록은 사용자가 선택할 수 있는 다양한 기계 학습 작업과 몇 가지 일반적인 사용 사례에 대해 설명합니다.

> [!NOTE]
> ML.NET은 현재 미리 보기로 제공됩니다. 일부 기계 학습 작업은 현재 지원되지 않습니다. 특정 작업에 대한 요청을 제출하려면 [dotnet/machinelearning 리포지토리](https://github.com/dotnet/machinelearning/issues)에서 문제를 엽니다.

## <a name="binary-classification"></a>이진 분류

두 클래스(범주) 중에 데이터의 인스턴스가 속한 클래스를 예측하는 데 사용되는 [감독된 기계 학습](glossary.md#supervised-machine-learning) 작업입니다. 분류 알고리즘의 입력은 레이블이 지정된 예제 집합입니다. 여기서 각 레이블은 0 또는 1의 정수입니다. 이진 분류 알고리즘의 출력은 분류자로, 레이블이 없는 새 인스턴스의 클래스를 예측하는 데 사용할 수 있습니다. 이진 분류 시나리오의 예는 다음과 같습니다.

* “긍정적” 또는 “부정적”으로 [Twitter 댓글의 감정 이해](../tutorials/sentiment-analysis.md).
* 환자에게 특정 질병이 있는지 여부 진단.
* 전자 메일을 “스팸”으로 표시할지 여부 결정.
* 사진에 개 또는 과일이 포함되어 있는지 확인.

자세한 내용은 Wikipedia에서 [Binary classification](https://en.wikipedia.org/wiki/Binary_classification)(이진 분류) 문서를 참조하세요.

이진 분류의 권장 학습자:

* AveragedPerceptronTrainer
* StochasticGradientDescentClassificationTrainer
* LightGbmBinaryTrainer
* FastTreeBinaryClassificationTrainer
* SymSgdClassificationTrainer

### <a name="binary-classification-learners"></a>이진 분류 학습자

이진 분류 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [AveragedPerceptronTrainer](xref:Microsoft.ML.Trainers.Online.AveragedPerceptronTrainer)
* [BinaryClassificationGamTrainer](xref:Microsoft.ML.Trainers.FastTree.BinaryClassificationGamTrainer)
* [FastForestClassification](xref:Microsoft.ML.Trainers.FastTree.FastForestClassification)
* [FastTreeBinaryClassificationTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer)
* [FieldAwareFactorizationMachineTrainer](xref:Microsoft.ML.FactorizationMachine.FieldAwareFactorizationMachineTrainer)
* [LightGbmBinaryTrainer](xref:Microsoft.ML.LightGBM.LightGbmBinaryTrainer)
* [LinearSvmTrainer](xref:Microsoft.ML.Trainers.Online.LinearSvmTrainer)
* [LogisticRegression](xref:Microsoft.ML.Learners.LogisticRegression)
* [PriorTrainer](xref:Microsoft.ML.Trainers.PriorTrainer)
* [RandomTrainer](xref:Microsoft.ML.Trainers.RandomTrainer)
* [StochasticGradientDescentClassificationTrainer](xref:Microsoft.ML.Trainers.StochasticGradientDescentClassificationTrainer)
* [SymSgdClassificationTrainer](xref:Microsoft.ML.Trainers.SymSgd.SymSgdClassificationTrainer)

## <a name="multiclass-classification"></a>다중 클래스 분류

데이터 인스턴스의 클래스(범주)를 예측하는 데 사용되는 [감독된 기계 학습](glossary.md#supervised-machine-learning) 작업입니다. 분류 알고리즘의 입력은 레이블이 지정된 예제 집합입니다. 각 레이블은 일반적으로 텍스트로 시작됩니다. 그런 다음, TermTransform을 통해 실행되어 키(숫자) 유형으로 변환됩니다. 분류 알고리즘의 출력은 분류자로, 레이블이 없는 새 인스턴스의 클래스를 예측하는 데 사용할 수 있습니다. 다중 클래스 분류 시나리오의 예는 다음과 같습니다.

* 개의 품종을 “시베리안 허스키”, “골든 리트리버”, “푸들” 등으로 결정.
* 동영상 리뷰를 “긍정적”, “중립” 또는 “부정적”으로 이해.
* 호텔 리뷰를 “위치”, “가격”, “청결도” 등으로 범주화.

자세한 내용은 Wikipedia에서 [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification)(다중 클래스 분류) 문서를 참조하세요.

다중 클래스의 권장 학습자:

* OVA-AveragedPerceptronTrainer
* SdcaMultiClassTrainer
* LightGbmMulticlassTrainer
* OVA-FastTreeBinaryClassificationTrainer

>[!NOTE]
>OVA 및 PKPD는 모든 [이진 분류 학습자](#binary-classification)를 다중 클래스 데이터 세트에서 작동하도록 업그레이드합니다. 자세한 내용은 [Wikipedia](https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest))를 참조하세요.

### <a name="multiclass-classification-learners"></a>다중 클래스 분류 학습자

다중 클래스 분류 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [LightGbmMulticlassTrainer](xref:Microsoft.ML.LightGBM.LightGbmMulticlassTrainer)
* [MetaMulticlassTrainer<TTransformer,TModel>](xref:Microsoft.ML.Learners.MetaMulticlassTrainer%602)
* [MultiClassNaiveBayesTrainer](xref:Microsoft.ML.Trainers.MultiClassNaiveBayesTrainer)
* [Ova](xref:Microsoft.ML.Trainers.Ova)
* [Pkpd](xref:Microsoft.ML.Trainers.Pkpd)
* [SdcaMultiClassTrainer](xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer)

## <a name="regression"></a>재발

관련 기능 집합에서 레이블 값을 예측하는 데 사용되는 [감독된 기계 학습](glossary.md#supervised-machine-learning) 작업입니다. 레이블은 실제 값일 수 있고, 분류 작업과 같이 한정된 값 집합에 속하지 않습니다. 회귀 알고리즘 모델은 기능 값이 달라질 때 레이블이 변경되는 방식을 결정하기 위한 관련 기능에 대한 레이블의 종속성입니다. 회귀 알고리즘의 입력은 알려진 값의 레이블이 포함된 예제 집합입니다. 회귀 알고리즘의 출력은 새 입력 기능 집합의 레이블 값을 예측하는 데 사용할 수 있는 함수입니다. 회귀 시나리오의 예는 다음과 같습니다.

* 침실 수, 위치 또는 규모와 같은 주택 특성을 기반으로 주택 가격 예측.
* 과거 데이터 및 현재 시장 추세를 기반으로 미래 재고 가격 예측.
* 광고 예산을 기반으로 제품 판매 예측.

회귀의 권장 학습자:

* FastTreeTweedieTrainer 
* LightGbmRegressorTrainer 
* SdcaRegressionTrainer 
* FastTreeRegressionTrainer

### <a name="regression-learners"></a>회귀 학습자

회귀 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [FastTreeRegressionTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer)
* [FastTreeTweedieTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer)
* [LightGbmRegressorTrainer](xref:Microsoft.ML.LightGBM.LightGbmRegressorTrainer)
* [OlsLinearRegressionTrainer](xref:Microsoft.ML.Trainers.HalLearners.OlsLinearRegressionTrainer)
* [OnlineGradientDescentTrainer](xref:Microsoft.ML.Trainers.Online.OnlineGradientDescentTrainer)
* [PoissonRegression](xref:Microsoft.ML.Trainers.PoissonRegression)
* [RegressionGamTrainer](xref:Microsoft.ML.Trainers.FastTree.RegressionGamTrainer)
* [SdcaRegressionTrainer](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer)
* [FastTree.SingleTrainer](xref:Microsoft.ML.Trainers.FastTree.SingleTrainer)
* [LightGBM.SingleTrainer](xref:Microsoft.ML.LightGBM.SingleTrainer)

## <a name="clustering"></a>클러스터링

데이터 인스턴스를 비슷한 특성을 포함하는 클러스터로 그룹화하는 데 사용되는 [감독되지 않는 기계 학습](glossary.md#unsupervised-machine-learning) 작업입니다. 클러스터링을 사용하여 검색 또는 단순 관찰을 통해 논리적으로 파생될 수 없는 데이터 세트의 관계를 식별할 수도 있습니다. 클러스터링 알고리즘의 입력 및 출력은 선택한 방법에 따라 다릅니다. 분산, 중심, 연결 또는 밀도 기반 방법을 사용할 수 있습니다. 현재 ML.NET은 K-평균 클러스터링을 사용하는 중심 기반 방법을 지원합니다. 클러스터링 시나리오의 예는 다음과 같습니다.

* 호텔 선택의 습관과 특성을 기반으로 호텔 투숙객 세그먼트 이해.
* 대상 광고 캠페인을 구축하는 데 도움이 되는 고객 세그먼트 및 인구 통계 식별.
* 제조 메트릭을 기반으로 인벤토리 범주화.

### <a name="clustering-learners"></a>클러스터링 학습자

클러스터링 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [KMeansPlusPlusTrainer](xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer)

## <a name="anomaly-detection"></a>변칙 검색

이 작업은 PCA(보안 주체 구성 요소 분석)를 사용하여 변칙 검색 모델을 만듭니다. PCA 기반 변칙 검색은 유효한 트랜잭션과 같은, 한 클래스의 학습 데이터를 얻기는 쉽지만 대상 변칙의 충분한 샘플을 얻기는 어려운 시나리오에서 모델을 빌드하는 데 도움이 됩니다.

기계 학습의 검증된 기술인 PCA는 데이터의 내부 구조를 나타내고 데이터 차이를 설명하기 때문에 탐색적 데이터 분석에서 자주 사용됩니다. PCA는 여러 변수를 포함하는 데이터를 분석하여 작동합니다. 변수 간의 상관 관계를 찾고 결과에서 차이점을 가장 잘 캡처하는 값의 조합을 확인합니다. 이러한 조합된 기능 값이 보안 주체 구성 요소라는 보다 간결한 기능 공간을 만드는 데 사용됩니다.

변칙 검색은 다음과 같은 기계 학습의 여러 중요한 작업을 포함합니다.

* 잠재적으로 사기성이 있는 트랜잭션 식별.
* 네트워크 침입이 발생했음을 나타내는 학습 패턴.
* 비정상적인 환자 클러스터 찾기.
* 시스템에 입력된 값 확인.

변칙은 정의상 거의 발생하지 않으므로 모델링에 사용할 데이터의 대표 샘플을 수집하기 어려울 수 있습니다. 이 범주에 포함된 알고리즘은 특히 불균형 데이터 세트를 사용하여 모델을 빌드하고 학습시키는 핵심 과제를 해결하도록 설계되었습니다.

### <a name="anomaly-detection-learners"></a>변칙 검색 학습자

변칙 검색 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [RandomizedPcaTrainer](xref:Microsoft.ML.Trainers.PCA.RandomizedPcaTrainer)

## <a name="ranking"></a>순위 지정

순위 지정 작업은 레이블이 지정된 예제 세트에서 순위매기기를 구성합니다. 이 예제 세트는 지정된 기준에 따라 점수가 매겨질 수 있는 인스턴스 그룹으로 이루어져 있습니다. 순위 레이블은 각 인스턴스마다 {0, 1, 2, 3, 4}입니다.  순위매기기는 각 인스턴스마다 점수를 알 수 없는 새 인스턴스 그룹의 순위를 지정하도록 학습됩니다. ML.NET 순위 지정 학습자는 [기계 학습 순위 지정](https://en.wikipedia.org/wiki/Learning_to_rank)을 기반으로 합니다.

### <a name="ranking-learners"></a>순위 지정 학습자

순위 지정 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [FastTreeRankingTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer)
* [LightGbmRankingTrainer](xref:Microsoft.ML.LightGBM.LightGbmRankingTrainer)

## <a name="recommendation"></a>권장 사항

권장 사항 작업을 통해 권장 제품 또는 서비스 목록을 생성할 수 있습니다. ML.NET은 카탈로그에 기록 제품 등급 데이터가 있는 경우 [공동 작업 필터링](https://en.wikipedia.org/wiki/Collaborative_filtering) 알고리즘인 [MF(행렬 인수)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29)를 권장 사항에 사용합니다. 예를 들어 사용자에 대한 기록 영화 등급 데이터가 있고, 사용자가 다음에 시청할 가능성이 큰 다른 영화를 추천하려고 합니다.

### <a name="recommendation-learners"></a>권장 사항 학습자

권장 사항 작업에 사용할 수 있는 학습자는 다음과 같습니다.

* [MatrixFactorizationTrainer](xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer)
* [MatrixFactorizationPredictionTransformer](xref:Microsoft.ML.Trainers.Recommender.MatrixFactorizationPredictionTransformer)
