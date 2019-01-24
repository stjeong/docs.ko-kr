---
title: '방법: 프로시저에 Visual Basic에서 다른 프로시저 전달'
ms.date: 07/20/2015
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- delegates [Visual Basic], passing procedures
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
ms.openlocfilehash: cf5a8447cbedcd8071da98ac6763ff06eb608199
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506760"
---
# <a name="how-to-pass-procedures-to-another-procedure-in-visual-basic"></a>방법: 프로시저에 Visual Basic에서 다른 프로시저 전달
이 예제에서는 대리자를 사용 하 여 프로시저에 다른 프로시저 전달 하는 방법을 보여 줍니다.  
  
 대리자 형식이 Visual Basic에서 다른 형식 처럼 사용할 수 있습니다. `AddressOf` 연산자 프로시저 이름에 적용 될 때 대리자 개체를 반환 합니다.  
  
 이 예제에 사용 하 여 얻은 다른 프로시저에 대 한 참조를 사용할 수 있는 대리자 매개 변수를 사용 하 여 프로시저를 `AddressOf` 연산자입니다.  
  
### <a name="create-the-delegate-and-matching-procedures"></a>대리자 및 일치 하는 프로시저 만들기  
  
1.  명명 된 대리자를 만드는 `MathOperator`합니다.  
  
     [!code-vb[VbVbalrDelegates#1](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_1.vb)]  
  
2.  라는 프로시저를 만듭니다 `AddNumbers` 매개 변수 및 반환 값의 일치 하는 `MathOperator`서명이 일치 되도록 합니다.  
  
     [!code-vb[VbVbalrDelegates#2](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_2.vb)]  
  
3.  라는 프로시저를 만듭니다 `SubtractNumbers` 일치 하는 서명을 사용 하 여 `MathOperator`입니다.  
  
     [!code-vb[VbVbalrDelegates#3](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_3.vb)]  
  
4.  라는 프로시저를 만들어 `DelegateTest` 대리자를 매개 변수로 사용 합니다.  
  
     이 절차에 대 한 참조를 사용할 수 있습니다 `AddNumbers` 또는 `SubtractNumbers`이므로 해당 서명이 일치는 `MathOperator` 서명 합니다.  
  
     [!code-vb[VbVbalrDelegates#4](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_4.vb)]  
  
5.  라는 프로시저를 만듭니다 `Test` 를 호출 하는 `DelegateTest` 에 대 한 대리자를 사용 하 여 한 번 `AddNumbers` 매개 변수로 사용 하 여 대리자를 다시 `SubtractNumbers` 매개 변수로 합니다.  
  
     [!code-vb[VbVbalrDelegates#5](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_5.vb)]  
  
     때 `Test` 는 호출 처음 표시 하면 `AddNumbers` 에서 작동 하 `5` 및 `3`, 8 인 합니다. 결과 `SubtractNumbers` 역할을 하 `9` 및 `3` 표시 되 면 6이 있습니다.  
  
## <a name="see-also"></a>참고자료
- [대리자](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [AddressOf 연산자](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Delegate 문](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [방법: 대리자 메서드 호출](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
