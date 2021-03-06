---
title: <<= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: d2105fbee4ddfe1b2cb3325d82b0f2f8c5559297
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219453"
---
# <a name="-operator-c-reference"></a>\<\<= 연산자(C# 참조)

왼쪽 시프트 대입 연산자입니다.

다음과 같은 `<<=` 연산자를 사용하는 식의 경우

```csharp
x <<= y
```

위의 식은 아래의 식과 동일합니다.

```csharp
x = x << y
```

단, `x`가 한 번만 계산됩니다.

[`<<` 연산자](left-shift-operator.md)는 첫 번째 피연산자를 두 번째 피연산자로 정의된 비트 수만큼 왼쪽으로 이동합니다.

다음 예제에서는 `<<=` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[left shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#LeftShiftAssignment)]

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식으로 [`<<` 연산자](left-shift-operator.md)를 [오버로드](../keywords/operator.md)하면 왼쪽 시프트 대입 연산자`<<=`는 암시적으로 오버로드됩니다. 사용자 정의 형식에는 왼쪽 시프트 대입 연산자를 명시적으로 오버로드할 수 없습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [복합 할당](~/_csharplang/spec/expressions.md#compound-assignment) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
