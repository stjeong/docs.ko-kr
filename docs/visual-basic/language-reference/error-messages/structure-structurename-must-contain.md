---
title: 구조 &#39; &lt;structurename&gt; &#39; 하나 이상의 인스턴스 멤버 변수 또는 표시 되지 않은 하나 이상의 이벤트 선언이 있어야 &#39;사용자 지정&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: d8c654c212a459d40c6cf20cd62c3e0fcda8511b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54603783"
---
# <a name="structure-39ltstructurenamegt39-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-39custom39"></a>구조 &#39; &lt;structurename&gt; &#39; 하나 이상의 인스턴스 멤버 변수 또는 표시 되지 않은 하나 이상의 이벤트 선언이 있어야 &#39;사용자 지정&#39;
구조체 정의 비공유 변수 또는 비공유 비 사용자 정의 이벤트 포함 되지 않습니다.  
  
 모든 구조체는 변수 또는 모든 인스턴스에 (비공유) 대신 특정 인스턴스의 전체적으로 적용 되는 이벤트 해야 합니다. ([공유](../../../visual-basic/language-reference/modifiers/shared.md)). 비공유 상수, 속성 및 절차가 요구이 사항을 충족 하지 않습니다. 또한 비공유 변수가 없고 하나의 비공유 이벤트가 없으면 이벤트 일 수 없습니다는 `Custom` 이벤트입니다.  
  
 **오류 ID:** BC30941  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   하나 이상의 변수 또는 없는 이벤트를 정의 `Shared`합니다. 하나의 이벤트를 정의 하는 경우 사용자와 공유 되지 않는 이어야 합니다.  
  
## <a name="see-also"></a>참고자료
- [구조체](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [방법: 구조 선언](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [Structure 문](../../../visual-basic/language-reference/statements/structure-statement.md)
