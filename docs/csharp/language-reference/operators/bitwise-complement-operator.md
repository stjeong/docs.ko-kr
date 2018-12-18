---
title: ~ 연산자 - C# 참조
ms.custom: seodec18
ms.date: 11/05/2018
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 57e5baee423c0b5d9292d0ad4cbf909646eb3a38
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235727"
---
# <a name="-operator-c-reference"></a>~ 연산자(C# 참조)

비트 보수 연산자 `~`는 각 비트를 반대로 하여 피연산자의 비트 단위 보수를 생성하는 단항 연산자입니다. 모든 정수 형식은 `~` 연산자를 지원합니다.

> [!NOTE]
> 또한 `~` 기호는 종료자를 선언하는 데 사용됩니다. 자세한 내용은 [종료자](../../programming-guide/classes-and-structs/destructors.md)를 참조하세요.

다음 예제에서는 `~` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[bitwise NOT](~/samples/snippets/csharp/language-reference/operators/BitwiseComplementExamples.cs#Example)]

> [!NOTE]
> 앞의 예제에서는 [C# 7.0에서 도입](../../whats-new/csharp-7.md#numeric-literal-syntax-improvements)되고 [C# 7.2에서 향상](../../whats-new/csharp-7-2.md#leading-underscores-in-numeric-literals)된 이진 리터럴을 사용합니다.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식은 `~` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [비트 보수 연산자](~/_csharplang/spec/expressions.md#bitwise-complement-operator) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [종료자](../../programming-guide/classes-and-structs/destructors.md)
- [& 연산자](and-operator.md)
- [| 연산자](or-operator.md)
- [^ 연산자](xor-operator.md)
