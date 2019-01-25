---
title: '|= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '|=_CSharpKeyword'
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
ms.openlocfilehash: f4f7806c8679af400a371decd0c367929b3fb81d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333267"
---
# <a name="-operator-c-reference"></a>|= 연산자(C# 참조)

OR 대입 연산자입니다.

## <a name="remarks"></a>주의

다음과 같은 `|=` 대입 연산자를 사용하는 식의 경우

```csharp
x |= y
```

위의 식은 아래의 식과 동일합니다.

```csharp
x = x | y
```

단, `x`가 한 번만 계산됩니다. [&#124; 연산자](or-operator.md)는 정수 피연산자에 대한 비트 논리적 OR 연산과 부울 피연산자에 대한 논리적 OR 연산을 수행합니다.

`|=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [&#124; 연산자](or-operator.md)를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).

## <a name="example"></a>예제

[!code-csharp[csRefOperators#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#10)]

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)