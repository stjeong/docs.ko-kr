---
title: '방법: 속성 (Visual Basic) 값 입력'
ms.date: 07/20/2015
helpviewer_keywords:
- property values [Visual Basic]
- Visual Basic code, procedures
- values [Visual Basic], properties
- Visual Basic code, properties
- properties [Visual Basic], values
ms.assetid: c39401e5-b5fc-4439-8f31-ed640f7ce6ed
ms.openlocfilehash: 34348d57db0875d9c2c6192ac754b4f83f515ac4
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56965472"
---
# <a name="how-to-put-a-value-in-a-property-visual-basic"></a>방법: 속성 (Visual Basic) 값 입력
대입문의 왼쪽에 속성 이름을 입력 하 여 속성에 값을 저장 합니다.  
  
 속성의 `Set` 프로시저에서 값을 저장 하지만 명시적으로 호출 하지 해당 이름으로 합니다. 변수를 사용할 때 처럼 속성을 사용 합니다. Visual Basic에서는 속성의 프로시저를 호출 합니다.  
  
### <a name="to-store-a-value-in-a-property"></a>속성에 값을 저장 하려면  
  
1.  대입문의 왼쪽에 속성 이름을 사용 합니다.  
  
     다음 예제에서는 Visual Basic의 값을 설정 `TimeOfDay` 암시적으로 호출 정오에 속성 해당 `Set` 프로시저입니다.  
  
     [!code-vb[VbVbcnProcedures#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#11)]  
  
2.  속성 인수를 사용 하는 경우에 속성 이름을 괄호로 묶어 인수 목록에 따릅니다. 인수가 없는 경우에 필요에 따라 괄호를 생략할 수 있습니다.  
  
3.  쉼표로 구분 하 여 괄호 안에 인수 목록의 인수를 배치 합니다. 속성은 해당 매개 변수 정의 동일한 순서로 인수를 지정 해야 합니다.  
  
4.  대입문의 오른쪽에 생성 된 값을 속성에 저장 됩니다.  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.DateAndTime.TimeOfDay%2A>
- [속성 프로시저](./property-procedures.md)
- [프로시저 매개 변수 및 인수](./procedure-parameters-and-arguments.md)
- [Property 문](../../../../visual-basic/language-reference/statements/property-statement.md)
- [Visual Basic에서 속성과 변수의 차이점](./differences-between-properties-and-variables.md)
- [방법: 속성 만들기](./how-to-create-a-property.md)
- [방법: 액세스 수준이 혼합된 된 속성 선언](./how-to-declare-a-property-with-mixed-access-levels.md)
- [방법: 속성 프로시저 호출](./how-to-call-a-property-procedure.md)
- [방법: 선언 및 Visual Basic의 기본 속성을 호출](./how-to-declare-and-call-a-default-property.md)
- [방법: 속성에서 값 가져오기](./how-to-get-a-value-from-a-property.md)
