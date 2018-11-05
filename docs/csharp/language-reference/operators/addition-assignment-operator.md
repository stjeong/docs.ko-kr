---
title: += 연산자(C# 참조)
ms.date: 10/22/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ee335e3e2e7d352d4e26b802bad2b08a05c666ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192033"
---
# <a name="-operator-c-reference"></a>+= 연산자(C# 참조)

더하기 대입 연산자.

다음과 같은 `+=` 연산자를 사용하는 식의 경우  

```csharp
x += y
```  

위의 식은 아래의 식과 동일합니다.  

```csharp
x = x + y
```  

단, `x`가 한 번만 계산됩니다.
  
숫자 형식의 경우 [더하기 연산자](addition-operator.md) `+`는 해당 피연산자의 합계를 계산합니다. 피연산자 중 하나 또는 둘 다가 [문자열](../keywords/string.md) 형식이면 +는 피연산자의 문자열 표현을 연결합니다. 대리자 형식의 경우 `+` 연산자는 해당 피연산자의 조합인 새 대리자 인스턴스를 반환합니다.

사용자 정의 형식이 [더하기 연산자](addition-operator.md) `+`를 [오버로드](../keywords/operator.md)하면 더하기 대입 연산자 `+=`는 암시적으로 오버로드됩니다.

또한 [이벤트](../keywords/event.md)를 구독할 때 `+=` 연산자를 사용하여 이벤트 처리기 메서드를 지정합니다. 자세한 내용은 [방법: 이벤트 구독 및 구독 취소](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)를 참조하세요.

다음 예제에서는 `+=` 연산자의 사용법을 보여 줍니다.

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]
  
## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [이벤트](../../programming-guide/events/index.md)
- [대리자](../../programming-guide/delegates/index.md)
