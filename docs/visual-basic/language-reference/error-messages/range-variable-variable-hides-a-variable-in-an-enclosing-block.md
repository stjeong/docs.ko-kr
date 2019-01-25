---
title: 범위 변수 &lt;변수&gt; 의 변수는 바깥쪽 블록, 이전에 정의한 범위 변수 또는 쿼리 식에서 암시적으로 선언한 변수를 숨깁니다.
ms.date: 07/20/2015
f1_keywords:
- bc36633
- vbc36633
helpviewer_keywords:
- BC36633
ms.assetid: 5d5470e4-3de5-49c2-8831-1087625f4a77
ms.openlocfilehash: aef52ea912a4180a6505949c8077296628592c72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54748118"
---
# <a name="range-variable-ltvariablegt-hides-a-variable-in-an-enclosing-block-a-previously-defined-range-variable-or-an-implicitly-declared-variable-in-a-query-expression"></a>범위 변수 &lt;변수&gt; 의 변수는 바깥쪽 블록, 이전에 정의한 범위 변수 또는 쿼리 식에서 암시적으로 선언한 변수를 숨깁니다.
에 지정 된 범위 변수 이름이 `Select`, `From`를 `Aggregate`, 또는 `Let` 절 쿼리 또는 쿼리에 의해 암시적으로 선언 된 변수 이름에 이미 이전에 지정한 범위 변수 이름과 중복 필드 이름 등을 집계 함수의 이름입니다.  
  
 **오류 ID:** BC36633  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   특정 쿼리 범위 안에 있는 모든 범위 변수 이름이 고유한 지 확인 합니다. 쿼리를 중첩된 쿼리 고유한 범위를 갖도록 괄호로 묶을 수 있습니다.  
  
## <a name="see-also"></a>참고자료
- [Visual Basic의 LINQ 소개](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [From 절](../../../visual-basic/language-reference/queries/from-clause.md)
- [Let 절](../../../visual-basic/language-reference/queries/let-clause.md)
- [Aggregate 절](../../../visual-basic/language-reference/queries/aggregate-clause.md)
- [Select 절](../../../visual-basic/language-reference/queries/select-clause.md)
