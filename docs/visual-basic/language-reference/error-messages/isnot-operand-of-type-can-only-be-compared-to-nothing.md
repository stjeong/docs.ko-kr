---
title: '&#39;IsNot&#39; 형식의 피연산자는 &#39;typename&#39; 만 비교할 수 있습니다 &#39;Nothing&#39;이므로 &#39;typename&#39; 이 nullable 형식이'
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: 65b04c85bccd169bbb2eea847d7b8af96c1a292f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505720"
---
# <a name="39isnot39-operand-of-type-39typename39-can-only-be-compared-to-39nothing39-because-39typename39-is-a-nullable-type"></a>&#39;IsNot&#39; 형식의 피연산자는 &#39;typename&#39; 만 비교할 수 있습니다 &#39;Nothing&#39;이므로 &#39;typename&#39; 이 nullable 형식이
Nullable로 선언 된 변수를 식으로 비교 된 이외의 `Nothing` 를 사용 하 여 `IsNot` 연산자입니다.  
  
 **오류 ID:** BC32128  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  `Nothing` 연산자를 사용하여 nullable 형식을 `IsNot` 이외의 식과 비교하려면 다음 예제와 같이 nullable 형식에서 `GetType` 메서드를 호출하고 그 결과를 식과 비교합니다.  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a>참고자료
- [Nullable 값 형식](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [IsNot 연산자](../../../visual-basic/language-reference/operators/isnot-operator.md)
