---
title: / 연산자 - C# 참조
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: 45bcd64b60e7d13f389064faefeda815ea1f32c9
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286535"
---
# <a name="-operator-c-reference"></a>/ 연산자(C# 참조)

나누기 연산자 `/`는 두 번째 피연산자로 첫 번째 피연산자를 나눕니다. 모든 숫자 형식은 나누기 연산자를 지원합니다.

## <a name="integer-division"></a>정수 나누기

정수 형식의 피연산자의 경우 `/` 연산자의 결과는 정수 형식이고 두 피연산자의 몫과 동일한 값은 0으로 반올림됩니다.

[!code-csharp-interactive[integer division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#Integer)]

두 피연산자의 몫을 부동 소수점 숫자로 가져오려면 `float`, `double` 또는 `decimal` 형식을 사용하세요.

[!code-csharp-interactive[integer as floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#IntegerAsFloatingPoint)]

## <a name="floating-point-division"></a>부동 소수점 나누기

`float`, `double` 및 `decimal` 형식의 경우 `/` 연산자의 결과는 두 피연산자의 몫입니다.

[!code-csharp-interactive[floating-point division](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#FloatingPoint)]

피연산자 중 하나가 `decimal`이면 `float` 또는 `double` 모두 `decimal`로 암시적으로 변환할 수 없기 때문에 나머지 피연산자는 `float` 또는 `double`일 수 없습니다. `float` 또는 `double` 피연산자를 `decimal` 형식으로 암시적으로 변환해야 합니다. 숫자 형식 간의 암시적 변환에 대한 자세한 내용은 [암시적 숫자 변환 표](../keywords/implicit-numeric-conversions-table.md)를 참조하세요.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식은 `/` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다. `/` 연산자가 오버로드되면 [나누기 대입 연산자](division-assignment-operator.md) `/=`도 암시적으로 오버로드됩니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [나누기 연산자](~/_csharplang/spec/expressions.md#division-operator) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [% 연산자](remainder-operator.md)
