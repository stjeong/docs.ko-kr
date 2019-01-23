---
title: Alias 절(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Alias
helpviewer_keywords:
- Alias keyword [Visual Basic]
ms.assetid: 58c06b11-465d-4d87-906a-73200a3d7f19
ms.openlocfilehash: 9cf97402d0b0a6cd16dd75a970c1d29a2fcc30a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498572"
---
# <a name="alias-clause-visual-basic"></a>Alias 절(Visual Basic)
외부 프로시저의 DLL에 다른 이름이 있음을 나타냅니다.  
  
## <a name="remarks"></a>설명  
 `Alias` 키워드는이 컨텍스트에서 사용할 수 있습니다.  
  
 [Declare 문](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 다음 예제에서는 `Alias` 키워드 advapi32.dll에서 함수의 이름을 제공 하는 데 사용 됩니다 `GetUserNameA`는 `getUserName` 이 예에서 대신 사용 됩니다. 함수 `getUserName` sub 라고 `getUser`, 현재 사용자의 이름을 표시 합니다.  
  
 [!code-vb[VbVbalrStatements#15](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/alias-clause_1.vb)]  
  
## <a name="see-also"></a>참고자료
- [C++ 키워드](../../../visual-basic/language-reference/keywords/index.md)
