---
title: '방법: 컬렉션 이니셜라이저 (Visual Basic)에서 사용 하는 컬렉션 만들기'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
ms.openlocfilehash: aaa367e5a1739f26e9b0458d8f2fc44462b73b7b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631726"
---
# <a name="how-to-create-a-collection-used-by-a-collection-initializer-visual-basic"></a>방법: 컬렉션 이니셜라이저 (Visual Basic)에서 사용 하는 컬렉션 만들기
Visual Basic 컴파일러에 대 한 검색 컬렉션 이니셜라이저를 사용 하 여 컬렉션을 만드는 경우는 `Add` 는 컬렉션 형식의 메서드 매개 변수는 `Add` 컬렉션 이니셜라이저의 값의 형식과 일치 하는 메서드. 이 `Add` 메서드 컬렉션을 컬렉션 이니셜라이저의 값으로 채우는 데 사용 됩니다.  
  
## <a name="example"></a>예제  
 에서는 다음 예제는 `OrderCollection` 공용 포함 된 컬렉션 `Add` 형식의 개체를 추가할 컬렉션 이니셜라이저를 사용할 수 있는 메서드 `Order`합니다. `Add` 메서드 약식된 컬렉션 이니셜라이저 구문을 사용할 수 있습니다.  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#4](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_1.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#1](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_2.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#2](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_3.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#3](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_4.vb)]  
  
## <a name="see-also"></a>참고자료
- [컬렉션 이니셜라이저](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)
- [방법: 만들기는 컬렉션 이니셜라이저에서 사용 되는 확장 메서드를 추가 합니다.](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)
