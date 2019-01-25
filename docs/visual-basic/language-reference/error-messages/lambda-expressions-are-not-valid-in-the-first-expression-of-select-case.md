---
title: 람다 식의 첫 번째 식에서는 사용할 수 없습니다는 &#39;Select Case&#39; 문
ms.date: 07/20/2015
f1_keywords:
- bc36635
- vbc36635
helpviewer_keywords:
- BC36635
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
ms.openlocfilehash: afefa821f9695dbbfe2a96aee5afd3171ae5b1db
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700223"
---
# <a name="lambda-expressions-are-not-valid-in-the-first-expression-of-a-39select-case39-statement"></a>람다 식의 첫 번째 식에서는 사용할 수 없습니다는 &#39;Select Case&#39; 문
테스트 식에 람다 식을 사용할 수 없습니다는 `Select Case` 문입니다. 람다 식 정의는 함수를 테스트 식의 반환을 `Select Case` 문은 기본 데이터 형식 이어야 합니다.  
  
 다음 코드는이 오류가 발생합니다.  
  
```vb  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 **오류 ID:** BC36635  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   코드를 검사하여 `If...Then...Else` 문과 같은 다른 조건부 생성이 적합한지 결정합니다.  
  
-   계획 했던 함수를 호출 하려면 다음 코드 에서처럼:  
  
```vb  
Dim num? As Integer  
Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
    ' List of the cases  
End Select  
```  
  
## <a name="see-also"></a>참고자료
- [람다 식](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [If...Then...Else 문](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [Select...Case 문](../../../visual-basic/language-reference/statements/select-case-statement.md)
