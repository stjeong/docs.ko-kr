---
title: '&#39;#ElseIf&#39; 일치 하는 뒤에 야 &#39;#If&#39; 또는 &#39;#ElseIf&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 1e63595ee573e9356f6870a02b2131897c725baf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505785"
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a>&#39;#ElseIf&#39; 일치 하는 뒤에 야 &#39;#If&#39; 또는 &#39;#ElseIf&#39;
`#ElseIf` 는 조건부 컴파일 지시문입니다. `#ElseIf` 일치 하는 절을 야 `#If` 또는 `#ElseIf` 절.  
  
 **오류 ID:** BC30014  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  확인 앞 `#If` 또는 `#ElseIf` 이에서 분리 없습니다 `#ElseIf` 간섭 조건부 컴파일 블록 또는 잘못 배치 된 `#End If`합니다.  
  
2.  경우는 `#ElseIf` 앞에 `#Else` 지시문을 제거 하거나를 `#Else` 로 변경 하거나는 `#ElseIf`합니다.  
  
3.  다른 모든 항목의 순서가 올바른 경우 `#If` 지시문을 조건부 컴파일 블록의 시작 부분에 추가합니다.  
  
## <a name="see-also"></a>참고자료
- [#If...Then...#Else 지시문](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
