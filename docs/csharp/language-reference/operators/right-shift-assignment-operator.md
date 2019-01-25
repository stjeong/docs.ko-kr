---
title: '&gt;&gt;= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 02a9559a5c4086eeed09094c15c3620366ffad8c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333693"
---
# <a name="gtgt-operator-c-reference"></a>&gt;&gt;= 연산자(C# 참조)

오른쪽 시프트 대입 연산자입니다.

## <a name="remarks"></a>주의

다음 형태의 식이 있다고 가정합니다.

```csharp
x >>= y
```

이 식은 다음과 같이 계산됩니다.

```csharp
x = x >> y
```

단, `x`가 한 번만 계산됩니다. [>> 연산자](right-shift-operator.md)는 `y`로 지정된 양만큼 `x`를 오른쪽으로 이동합니다.

>>= 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [>> 연산자](right-shift-operator.md)를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).

## <a name="example"></a>예제

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)