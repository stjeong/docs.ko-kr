---
title: 문 줄 외부의 블록에서 끝날 수 없습니다 &#39;경우&#39; 문
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 78fe136acbd09e202b1daeb16dd540cf42ada390
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574718"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-39if39-statement"></a>문 줄 외부의 블록에서 끝날 수 없습니다 &#39;경우&#39; 문
한 줄 `If` 문에서 여러 개의 문이 콜론 (:), 그 중 하나는 `End` 문을 한 줄의 외부 컨트롤 블록용 `If`합니다. 한 줄 `If` 문을 사용 하지 마십시오는 `End If` 문입니다.  
  
 **오류 ID:** BC32005  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   단일 줄으로 이동 `If` 문을 포함 하는 컨트롤 블록 밖의 `End If` 문입니다.  
  
## <a name="see-also"></a>참고자료
- [If...Then...Else 문](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
