---
title: Erase 문(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Erase
helpviewer_keywords:
- Erase keyword [Visual Basic]
- Erase statement [Visual Basic]
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
ms.openlocfilehash: 5828e28b84ec62c7ed674757090806d73c61caea
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966738"
---
# <a name="erase-statement-visual-basic"></a>Erase 문(Visual Basic)
배열 변수를 해제 하 고 해당 요소에 사용 되는 메모리 할당을 취소 하는 데 사용 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
Erase arraylist  
```  
  
## <a name="parts"></a>요소  
 `arraylist`  
 필수 요소. 지울 배열 변수 목록입니다. 여러 변수는 쉼표로 구분됩니다.  
  
## <a name="remarks"></a>설명  
 `Erase` 문을 프로시저 수준 에서만 사용할 수 있습니다. 즉, 클래스 또는 모듈 수준에 없습니다. 하지만 프로시저 내에서 배열을 릴리스할 수 있습니다.  
  
 합니다 `Erase` 할당과 문과 동일 `Nothing` 각 배열 변수에 합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 `Erase` 두 배열을 지우고 해당 메모리를 확보 하는 문 (1000 및 100 저장소 요소 각각). `ReDim` 문은 다음 3 차원 배열에 새 배열 인스턴스를 할당 합니다.  
  
 [!code-vb[VbVbalrStatements#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#19)]  
  
## <a name="see-also"></a>참고자료
- [Nothing](../../../visual-basic/language-reference/nothing.md)
- [ReDim 문](../../../visual-basic/language-reference/statements/redim-statement.md)
