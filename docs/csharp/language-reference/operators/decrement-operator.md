---
title: -- 연산자 - C# 참조
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- --_CSharpKeyword
helpviewer_keywords:
- -- operator [C#]
- decrement operator (--) [C#]
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
ms.openlocfilehash: 4fba014e8dabc13cd874e17f23515dc29d93f24b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236930"
---
# <a name="---operator-c-reference"></a>-- 연산자(C# 참조)

단항 감소 연산자(`--`)는 피연산자를 1씩 감소합니다. 후위 감소 연산자 `x--` 및 전위 감소 연산자 `--x`의 두 가지 형태로 지원됩니다.

## <a name="postfix-decrement-operator"></a>후위 감소 연산자

`x--`의 결과는 다음 예제와 같이 연산 ‘전’ `x`의 값입니다.

[!code-csharp-interactive[postfix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixDecrement)]

## <a name="prefix-decrement-operator"></a>후위 감소 연산자

`--x`의 결과는 다음 예제와 같이 연산 ‘후’ `x`의 값입니다.

[!code-csharp-interactive[prefix decrement](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixDecrement)]

## <a name="remarks"></a>설명

감소 연산자는 모든 [정수 형식](../keywords/integral-types-table.md)([char](../keywords/char.md) 형식 포함), [부동 소수점 형식](../keywords/floating-point-types-table.md) 및 모든 [열거형](../keywords/enum.md) 형식에 대해 미리 정의됩니다.

감소 연산자의 피연산자는 변수, [속성](../../programming-guide/classes-and-structs/properties.md) 액세스 또는 [인덱서](../../../csharp/programming-guide/indexers/index.md) 액세스여야 합니다.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식은 `--` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [후위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) 및 [전위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [++ 연산자](increment-operator.md)
- [방법: 포인터 증가 및 감소](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
