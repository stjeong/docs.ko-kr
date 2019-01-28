---
title: ^ 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: 16419342fec9d6c9845e19e434787c5e4f5a5b12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632254"
---
# <a name="-operator-c-reference"></a>^ 연산자(C# 참조)

이항 `^` 연산자는 정수 형식 및 `bool`에 대해 미리 정의되어 있습니다. 정수 형식의 경우 `^` 연산자는 해당 피연산자의 배타적 비트 OR 연산자를 계산합니다. `bool` 피연산자의 경우 `^` 연산자는 피연산자의 배타적 논리 OR 연산을 계산합니다. 즉 피연산자 중 정확히 하나가 `true`일 경우에만 결과가 `true`입니다.

## <a name="remarks"></a>주의

사용자 정의 형식은 `^` 연산자를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조). 정수 계열 형식에 대한 연산은 일반적으로 열거형에서 허용됩니다.

## <a name="example"></a>예제

[!code-csharp[csRefOperators#30](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#30)]

이전 예제에서의 `0xf8 ^ 0x3f` 계산은 16진수 값 F8 및 3F에 해당하는 다음 두 이진 값에 대하여 배타적 비트 OR 연산을 처리합니다.

`1111 1000`

`0011 1111`

배타적 OR 연산 결과는 `1100 0111`이며 16진수로 나타내면 C7입니다.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
