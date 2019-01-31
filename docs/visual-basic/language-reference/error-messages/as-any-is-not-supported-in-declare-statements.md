---
title: "'Declare' 문에서는 'As Any'가 지원되지 않습니다."
ms.date: 07/20/2015
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
ms.openlocfilehash: bdf339e0d91106a6d6527e085608a06b0439951c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274090"
---
# <a name="as-any-is-not-supported-in-declare-statements"></a>'Declare' 문에서는 'As Any'가 지원되지 않습니다.
합니다 `Any` 데이터 형식을 사용한 `Declare` Visual Basic 6.0 및 이전 버전의 모든 종류의 데이터를 포함할 수 있는 인수 사용을 허용 하는 문입니다. 하지만 오버 로드를 허용, Visual Basic 지원 하 고 따라서로 전환 합니다 `Any` 데이터 형식은 사용 되지 않습니다.  
  
 **오류 ID:** BC30828  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  사용 하려는 특정 형식의 매개 변수를 선언 합니다. 예를 들어.  
  
     [!code-vb[VbVbalrStatements#95](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_1.vb)]  
  
2.  사용 된 <xref:System.Runtime.InteropServices.MarshalAsAttribute> 지정 하는 특성 `As Any` 때 `Void*` 호출 되는 프로시저에서 예상 하는 합니다.  
  
     [!code-vb[VbVbalrStatements#96](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_2.vb)]  
  
## <a name="see-also"></a>참고자료
- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [연습: Windows API 호출](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [Declare 문](../../../visual-basic/language-reference/statements/declare-statement.md)
- [관리 코드에서 프로토타입 만들기](../../../framework/interop/creating-prototypes-in-managed-code.md)
