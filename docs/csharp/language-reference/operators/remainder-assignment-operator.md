---
title: '%= 연산자(C# 참조)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: ab3a6a8d5cbfeb4d527ca1f9c233ddfaba3d35ff
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188718"
---
# <a name="-operator-c-reference"></a>%= 연산자(C# 참조)

나머지 대입 연산자입니다.

다음과 같은 `%=` 연산자를 사용하는 식의 경우  

```csharp
x %= y
```  

위의 식은 아래의 식과 동일합니다.  

```csharp
x = x % y
```  

단, `x`가 한 번만 계산됩니다.
  
[나머지 연산자](remainder-operator.md)(`%`)는 피연산자를 나눈 후 나머지를 계산합니다. 모든 숫자 형식에서 지원됩니다.

사용자 정의 형식이 [나머지 연산자](remainder-operator.md) `%`에 [오버로드](../keywords/operator.md)되면, 나머지 할당 연산자 `%=`는 암시적으로 오버로드됩니다.
  
다음 예제에서는 `%=` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
