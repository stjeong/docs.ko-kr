---
title: '>> 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 809cd2cab29d3378892ea224cf846e9d0909b073
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219726"
---
# <a name="-operator-c-reference"></a>>> 연산자(C# 참조)

오른쪽 시프트 연산자 `>>`는 첫 번째 피연산자를 두 번째 피연산자로 정의된 비트 수만큼 오른쪽으로 이동합니다. 모든 정수 형식은 `>>` 연산자를 지원합니다. 그러나 두 번째 피연산자의 형식은 [int](../keywords/int.md) 또는 `int`로의 [미리 정의된 암시적 숫자 변환](../keywords/implicit-numeric-conversions-table.md)이 있는 형식이어야 합니다.

오른쪽 시프트 연산은 하위 비트를 삭제합니다. 빈 상위 공백 비트 위치는 다음과 같이 첫 번째 피연산자 형식에 따라 설정됩니다.

- 첫 번째 피연산자가 [int](../keywords/int.md) 또는 [long](../keywords/long.md) 형식인 경우 오른쪽 시프트 연산자는 **산술** 시프트를 수행합니다. 첫 번째 피연산자의 최상위 비트(부호 비트) 값이 빈 상위 비트 위치로 전파됩니다. 즉, 빈 상위 비트 위치는 첫 번째 피연산자가 음수가 아닌 경우 0으로 설정되고, 음수인 경우 1로 설정됩니다.

- 첫 번째 피연산자가 [uint](../keywords/uint.md) 또는 [ulong](../keywords/ulong.md) 형식이면 오른쪽 시프트 피연산자는 **논리적** 시프트를 수행합니다. 빈 상위 비트 위치가 항상 0으로 설정됩니다.

다음 예제에서는 해당 동작을 보여줍니다.

[!code-csharp-interactive[right shift example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShift)]

## <a name="shift-count"></a>시프트 수

`x >> count` 식의 경우 실제 시프트 수는 다음과 같이 `x` 형식에 따라 달라집니다.

- `x` 형식이 [int](../keywords/int.md) 또는 [uint](../keywords/uint.md)이면 두 번째 피연산자의 하위 *5*비트로 시프트 수가 지정됩니다. 즉, 시프트 수는 `count & 0x1F`(또는 `count & 0b_1_1111`)에서 계산됩니다.

- `x` 형식이 [long](../keywords/long.md) 또는 [ulong](../keywords/ulong.md)이면 두 번째 피연산자의 하위 *6*비트로 시프트 수가 지정됩니다. 즉, 시프트 수는 `count & 0x3F`(또는 `count & 0b_11_1111`)에서 계산됩니다.

다음 예제에서는 해당 동작을 보여줍니다.

[!code-csharp-interactive[shift count example](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftByLargeCount)]

## <a name="remarks"></a>주의

시프트 작업으로 인해 오버플로가 발생하지 않고 [Checked 및 Unchecked](../keywords/checked-and-unchecked.md) 컨텍스트에서 동일한 결과가 생성되지 않습니다.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식은 `>>` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다. 사용자 정의 형식 `T`가 `>>` 연산자를 오버로드하는 경우 첫 번째 피연산자의 형식은 `T`여야 하고, 두 번째 피연산자의 형식은 `int`여야 합니다. `>>` 연산자가 오버로드되면 [오른쪽 시프트 대입 연산자](right-shift-assignment-operator.md) `>>=`도 암시적으로 오버로드됩니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [시프트 연산자](~/_csharplang/spec/expressions.md#shift-operators) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [<< 연산자](left-shift-operator.md)