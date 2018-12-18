---
title: /= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: ed4dd6c0c944b77543aae4de8d51534b4df4f4ef
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286522"
---
# <a name="-operator-c-reference"></a>/= 연산자(C# 참조)

나누기 대입 연산자입니다.

다음과 같은 `/=` 연산자를 사용하는 식의 경우

```csharp
x /= y
```

위의 식은 아래의 식과 동일합니다.

```csharp
x = x / y
```

단, `x`가 한 번만 계산됩니다.

[나누기 연산자](division-operator.md) `/`는 두 번째 피연산자로 첫 번째 피연산자를 나눕니다. 모든 숫자 형식에서 지원됩니다.

다음 예제에서는 `/=` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[divide and assign](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#DivisionAssignment)]

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식이 [나누기 연산자](division-operator.md) `/`를 [오버로드](../keywords/operator.md)하면 나누기 대입 연산자 `/=`는 암시적으로 오버로드됩니다. 사용자 정의 형식에는 나누기 대입 연산자를 명시적으로 오버로드할 수 없습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [복합 할당](~/_csharplang/spec/expressions.md#compound-assignment) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
