---
title: '&#39;&lt;eventname&gt; &#39; 은 (는) 이벤트 및 직접 호출할 수 없습니다.'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 3efd8c18497ce288e16659db4ca4693d5a3e6acc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54581998"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a>&#39;&lt;eventname&gt; &#39; 은 (는) 이벤트 및 직접 호출할 수 없습니다.
' <`eventname`>'은 (는) 이벤트 및 이므로 직접 호출할 수 없습니다. 사용 된 `RaiseEvent` 이벤트를 발생 시키는 문입니다.  
  
 프로시저 호출이 프로시저 이름에 대 한 이벤트를 지정합니다. 이벤트 처리기 프로시저 되었지만 이벤트 자체는 일종의 신호 발생 하 고 처리 해야 합니다.  
  
 **오류 ID:** BC32022  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  사용 하 여를 `RaiseEvent` 문을 이벤트 신호를 보내고 처리 하는 프로시저를 호출 합니다.  
  
## <a name="see-also"></a>참고자료
- [RaiseEvent 문](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
