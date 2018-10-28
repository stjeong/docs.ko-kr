---
title: Null 조건부 연산자 (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: c29362a1e335e18b66821919e266b1ce57774692
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195998"
---
# <a name="-and--null-conditional-operators-visual-basic"></a>?. 및? null 조건부 연산자 () (Visual Basic)

Null에 대 한 왼쪽 피연산자의 값을 테스트 (`Nothing`)는 멤버 액세스를 수행 하기 전에 (`?.`) 또는 인덱스 (`?()`) 작업; 반환 `Nothing` 왼쪽 피연산자가 `Nothing`입니다. 일반적으로 값 형식을 반환 하는 식, null 조건부 연산자를 반환,는 <xref:System.Nullable%601>합니다.

이러한 연산자는 데이터 구조에서 아래로 내려가는 경우에 특히 null 검사를 처리 하는 작은 코드를 작성할 수 있습니다. 예를 들어:

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

반면 null 조건부 연산자 없이 이러한 식의 첫 번째에 대 한 대체 코드는 다음과 같습니다.

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

Null 조건부 연산자는 단락 연산자입니다.  조건부 멤버 액세스 및 인덱스 작업의 체인에 하나의 작업 Nothing을 반환 하면 체인 실행의 나머지 부분을 중지 합니다.  하는 경우 다음 예제에서는 c (e) 평가 되지 않습니다 `A`, `B`, 또는 `C` Nothing으로 계산 합니다.

```vb
A?.B?.C?(E);
```

Null 조건부 멤버 액세스에 대 한 또 다른 용도 훨씬 더 적은 코드를 사용 하 여 스레드로부터 안전한 방식으로 대리자를 호출 하는 것입니다.  이전 방식에서는 다음과 같은 코드가 필요합니다.  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

새로운 방식은 훨씬 더 간단합니다.  

```vb
PropertyChanged?.Invoke(…)
```

새로운 방식은 컴파일러가 `PropertyChanged`를 한 번만 평가하는 코드를 생성하고 결과를 임시 변수에 유지하기 때문에 스레드로부터 안전합니다. null 조건부 대리자 호출 구문 `PropertyChanged?(e)`가 없기 때문에 `Invoke` 메서드를 명시적으로 호출해야 합니다.  

## <a name="see-also"></a>참고자료

- [연산자 (Visual Basic)](index.md)
- [Visual Basic 프로그래밍 가이드](../../../visual-basic/programming-guide/index.md)
- [Visual Basic 언어 참조](../../../visual-basic/language-reference/index.md)  
