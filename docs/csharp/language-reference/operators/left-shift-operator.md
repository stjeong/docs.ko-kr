---
title: << 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: 0271c97bc624a8946b90508e9ce39d217a128c05
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261752"
---
# <a name="-operator-c-reference"></a>\<\< 연산자(C# 참조)

왼쪽 시프트 연산자(`<<`)는 첫 번째 피연산자를 두 번째 피연산자로 지정된 비트 수만큼 왼쪽으로 이동합니다. 두 번째 피연산자의 형식은 [int](../keywords/int.md) 또는 `int`로의 미리 정의된 암시적 숫자 변환이 있는 형식이어야 합니다.

## <a name="remarks"></a>주의

첫 번째 피연산자가 [int](../keywords/int.md) 또는 [uint](../keywords/uint.md)(32비트 수량)이면 두 번째 피연산자의 하위 5비트로 시프트 수가 지정됩니다. 즉, 실제 시프트 수는 0~31비트입니다.

첫 번째 피연산자가 [long](../keywords/long.md) 또는 [ulong](../keywords/ulong.md)(64비트 수량)이면 두 번째 피연산자의 하위 6비트로 시프트 수가 지정됩니다. 즉, 실제 시프트 수는 0~63비트입니다.

시프트 후 첫 번째 피연산자의 형식 범위 내에 없는 상위 비트는 삭제되고, 비어 있는 하위 비트는 0으로 채워집니다. 시프트 작업은 오버플로를 일으키지 않습니다.

사용자 정의 형식은 `<<` 연산자를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조). 첫 번째 피연산자의 형식은 사용자 정의 형식이어야 하고 두 번째 피연산자의 형식은 `int`여야 합니다. 이항 연산자가 오버로드되면 해당 대입 연산자도 암시적으로 오버로드됩니다.

## <a name="example"></a>예

[!code-csharp[csRefOperators#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#14)]

## <a name="comments"></a>설명

`i<<1` 및 `i<<33`은 1과 33의 하위 5비트가 같기 때문에 동일한 결과를 제공합니다.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
