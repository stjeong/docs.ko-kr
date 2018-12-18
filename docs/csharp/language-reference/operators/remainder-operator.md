---
title: '% 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%_CSharpKeyword'
helpviewer_keywords:
- remainder operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
ms.openlocfilehash: a5c12b6683e35cc1ec2d40446dd0ed068c3d2552
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236481"
---
# <a name="-operator-c-reference"></a>% 연산자(C# 참조)

나머지 연산자 `%`는 첫 번째 피연산자를 두 번째 피연산자로 나눈 후 나머지를 계산합니다.

사용자 정의 형식은 `%` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다. `%`가 오버로드되면 [나머지 할당 연산자](remainder-assignment-operator.md) `%=`도 암시적으로 오버로드됩니다.

모든 숫자 형식은 나머지 연산자를 지원합니다.

## <a name="integer-remainder"></a>정수 나머지
  
정수 피연산자의 경우 `a % b`의 결과가 `a - (a / b) * b`에서 생성된 값입니다. 다음 예와 같이 0이 아닌 나머지의 부호는 첫 번째 피연산자와 동일합니다.

[!code-csharp-interactive[integer remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#1)]

## <a name="floating-point-remainder"></a>부동 소수점 나머지

[float](../keywords/float.md) 및 [double](../keywords/double.md) 피연산자의 경우, 유한 `x` 및 `y`에 대한 `x % y`의 결과는 다음과 같은 `z` 값입니다.

- 0이 아닌 경우 `z`의 부호는 `x`의 부호와 동일합니다.
- `z`의 절대 값은 `|x| - n * |y|`에서 생성된 값입니다. 여기서 `n`은 `|x| / |y|`보다 작거나 같은 최대 가능한 정수이고 `|x|` 및 `|y|`는 각각 `x` 및 `y`의 절대 값입니다.

무한 피연산자가 있는 `%` 연산자의 동작에 대한 자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [나머지 연산자](~/_csharplang/spec/expressions.md#remainder-operator) 섹션을 참조하세요.

> [!NOTE]
> 나머지 계산 방법은 정수 피연산자에 사용되는 것과 유사하지만 IEEE 754와는 다릅니다. IEEE 754를 준수하는 나머지 작업이 필요한 경우 <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType> 메서드를 사용합니다.

다음 예제에서는 `float` 및 `double` 피연산자에 대한 나머지 연산자의 동작을 보여 줍니다.

[!code-csharp-interactive[float and double remainder](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#2)]

부동 소수점 형식과 연결될 수 있는 반올림 오류를 기록합니다.

[10진수](../keywords/decimal.md) 피연산자의 경우 나머지 연산자 `%`는 <xref:System.Decimal?displayProperty=nameWithType> 형식의 [나머지 연산자](<xref:System.Decimal.op_Modulus(System.Decimal,System.Decimal)>)와 동일합니다.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- <xref:System.Math.IEEERemainder%2A?displayProperty=nameWithType>
- <xref:System.Math.DivRem%2A?displayProperty=nameWithType>
