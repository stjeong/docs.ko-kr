---
title: "'<keyword>'은(는) 인스턴스 메서드 안에서만 사용할 수 있습니다."
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: af3bc95e2db88577c7c53e4b58fb60aed8a83453
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267649"
---
# <a name="keyword-is-valid-only-within-an-instance-method"></a>'\<키워드 >'는 인스턴스 메서드 내 에서만 유효
합니다 `Me`, `MyClass`, 및 `MyBase` 키워드 특정 클래스 인스턴스를 참조 하세요. 공유 내에서 사용할 수 없습니다 `Function` 또는 `Sub` 프로시저입니다.  
  
 **오류 ID:** BC30043  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   프로시저에서 키워드를 제거 하거나 제거 합니다 `Shared` 프로시저 선언에서 키워드입니다.  
  
## <a name="see-also"></a>참고자료
- [개체 변수 할당](../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Me, My, MyBase 및 MyClass](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [상속 기본 사항](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
