---
title: '&amp;= 연산자(C# 참조)'
ms.date: 10/29/2018
f1_keywords:
- '&=_CSharpKeyword'
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
ms.openlocfilehash: 8ce27c999cf21a9059ba23ee3c86b8fa024c7341
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "50980611"
---
# <a name="amp-operator-c-reference"></a>&amp;= 연산자(C# 참조)

AND 대입 연산자.

다음과 같은 `&=` 연산자를 사용하는 식의 경우

```csharp
x &= y
```

위의 식은 아래의 식과 동일합니다.

```csharp
x = x & y
```

단, `x`가 한 번만 계산됩니다.

정수 피연산자의 경우 [`&` 연산자](and-operator.md)는 피연산자의 비트 논리 AND를 계산합니다. [bool](../keywords/bool.md) 피연산자의 경우 피연산자의 논리 AND를 계산합니다.

다음 예제에서는 `&=` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[AND assignment example](~/samples/snippets/csharp/language-reference/operators/AndOperatorExamples.cs#AndAssignmentExample)]

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식으로 [`&` 연산자 ](and-operator.md)를 [오버로드](../keywords/operator.md)하면 AND 대입 연산자 `&=`는 암시적으로 오버로드됩니다. 사용자 정의 형식에는 AND 대입 연산자를 명시적으로 오버로드할 수 없습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [복합 할당](~/_csharplang/spec/expressions.md#compound-assignment) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
