---
title: ++ 연산자(C# 참조)
ms.date: 11/26/2018
f1_keywords:
- ++_CSharpKeyword
helpviewer_keywords:
- increment operator (++) [C#]
- ++ operator [C#]
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
ms.openlocfilehash: b29f4f1ab00c0f8026f118cb72b090e3b728bfc5
ms.sourcegitcommit: 6ae7cdd0437a32884556dd4826ca90e957b7a4e3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/06/2018
ms.locfileid: "48030472"
---
# <a name="-operator-c-reference"></a>++ 연산자(C# 참조)

단항 증가 연산자(`++`)는 피연산자를 1씩 증가합니다. 후위 증가 연산자 `x++` 및 전위 증가 연산자 `++x`의 두 가지 형태로 지원됩니다.

## <a name="postfix-increment-operator"></a>후위 증가 연산자

`x++`의 결과는 다음 예제와 같이 연산 ‘전’ `x`의 값입니다.

[!code-csharp-interactive[postfix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PostfixIncrement)]

## <a name="prefix-increment-operator"></a>후위 증가 연산자

`++x`의 결과는 다음 예제와 같이 연산 ‘후’ `x`의 값입니다.

[!code-csharp-interactive[prefix increment](~/samples/snippets/csharp/language-reference/operators/DecrementAndIncrementExamples.cs#PrefixIncrement)]

## <a name="remarks"></a>설명

증가 연산자는 모든 [정수 형식](../keywords/integral-types-table.md)([char](../keywords/char.md) 형식 포함), [부동 소수점 형식](../keywords/floating-point-types-table.md) 및 모든 [열거형](../keywords/enum.md) 형식에 대해 미리 정의됩니다.

증가 연산자의 피연산자는 변수, [속성](../../programming-guide/classes-and-structs/properties.md) 액세스 또는 [인덱서](../../../csharp/programming-guide/indexers/index.md) 액세스여야 합니다.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

사용자 정의 형식은 `++` 연산자를 [오버로드](../keywords/operator.md)할 수 있습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [후위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#postfix-increment-and-decrement-operators) 및 [전위 증가 및 감소 연산자](~/_csharplang/spec/expressions.md#prefix-increment-and-decrement-operators) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [-- 연산자](decrement-operator.md)
- [방법: 포인터 증가 및 감소](../../programming-guide/unsafe-code-pointers/how-to-increment-and-decrement-pointers.md)
