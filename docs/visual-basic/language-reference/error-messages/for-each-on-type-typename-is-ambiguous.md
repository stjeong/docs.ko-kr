---
title: '&#39;각&#39; 형식의 &#39; &lt;typename&gt; &#39; 종류의 여러 인스턴스화를 구현 하기 때문에 모호 &#39;System.Collections.Generic.IEnumerable (Of T)&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc32096
- bc32096
helpviewer_keywords:
- BC32096
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
ms.openlocfilehash: 7fd779ba34afa2a59fa6c42971597df8ce01495a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597348"
---
# <a name="39for-each39-on-type-39lttypenamegt39-is-ambiguous-because-the-type-implements-multiple-instantiations-of-39systemcollectionsgenericienumerableof-t39"></a>&#39;각&#39; 형식의 &#39; &lt;typename&gt; &#39; 종류의 여러 인스턴스화를 구현 하기 때문에 모호 &#39;System.Collections.Generic.IEnumerable (Of T)&#39;
A `For Each` 둘 이상 있는 반복기 변수를 지정 하는 문을 <xref:System.Collections.IEnumerable.GetEnumerator%2A> 메서드.  
  
 반복기 변수를 구현 하는 형식 이어야 합니다는 <xref:System.Collections.IEnumerable?displayProperty=nameWithType> 또는 <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> 인터페이스 중 하나에 `Collections` 의 네임 스페이스는 [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]합니다. 둘 이상의 생성 된 제네릭 인터페이스를 각 생성에 대 한 다양 한 형식 인수를 사용 하 여 구현 하는 클래스에 대 한 것 같습니다. 이 작업을 수행 하는 클래스에서 반복기 변수를 사용 하는 경우 해당 변수가 둘 이상의 <xref:System.Collections.IEnumerable.GetEnumerator%2A> 메서드. 이러한 경우 Visual Basic 호출할 메서드를 선택할 수 없습니다.  
  
 **오류 ID:** BC32096  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   사용 하 여 [DirectCast 연산자](../../../visual-basic/language-reference/operators/directcast-operator.md) 또는 [TryCast 연산자](../../../visual-basic/language-reference/operators/trycast-operator.md) 정의 하는 인터페이스를 반복기 변수 형식으로 캐스팅할는 <xref:System.Collections.IEnumerable.GetEnumerator%2A> 메서드를 사용 합니다.  
  
## <a name="see-also"></a>참고자료
- [For Each...Next 문](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [인터페이스](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
