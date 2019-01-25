---
title: ^= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: 12189d6469a9716d3b7ebcffef23423a75692d1a
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333553"
---
# <a name="-operator-c-reference"></a>^= 연산자(C# 참조)

배타적 OR 대입 연산자입니다.

## <a name="remarks"></a>주의

다음 형태의 식이 있다고 가정합니다.

```csharp
x ^= y
```

이 식은 다음과 같이 계산됩니다.

```csharp
x = x ^ y
```

단, `x`가 한 번만 계산됩니다. [^ 연산자](xor-operator.md)는 정수 피연산자에 대한 배타적 비트 OR 연산과 [bool](../keywords/bool.md) 피연산자에 대한 배타적 논리 OR 연산을 수행합니다.

^= 연산자는 직접 오버로드할 수 없지만 사용자 정의 형식은 [^ 연산자](xor-operator.md)를 오버로드할 수 있습니다([연산자](../keywords/operator.md) 참조).

## <a name="example"></a>예제

[!code-csharp[csRefOperators#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#23)]

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)