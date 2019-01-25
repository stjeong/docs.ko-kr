---
title: '&#39;&lt;membername&gt; &#39; 형식을 노출할 수 없습니다 &#39; &lt;typename&gt; &#39; 를 통해 프로젝트 외부 &lt;containertype&gt; &#39; &lt;containertypename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30909
- vbc30909
helpviewer_keywords:
- BC30909
ms.assetid: ffa7395d-e182-4087-8ce8-079810fdae54
ms.openlocfilehash: 39d316aca5ec306de4b1e43e2eb2d1495f5525d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672346"
---
# <a name="39ltmembernamegt39-cannot-expose-type-39lttypenamegt39-outside-the-project-through-ltcontainertypegt-39ltcontainertypenamegt39"></a>&#39;&lt;membername&gt; &#39; 형식을 노출할 수 없습니다 &#39; &lt;typename&gt; &#39; 를 통해 프로젝트 외부 &lt;containertype&gt; &#39; &lt;containertypename&gt;&#39;
변수, 프로시저 매개 변수 또는 함수 반환 해당 컨테이너 외부에 노출 됩니다 있지만 컨테이너 외부 하지 노출 해야 하는 형식으로 선언 되어 있습니다.  
  
 다음 기본 코드를이 오류를 생성 하는 경우를 보여 줍니다.  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 선언 된 형식을 `Protected`, `Friend`를 `Protected Friend`, 또는 `Private` 해당 선언 컨텍스트 외부 액세스가 제한 됩니다. 사용 하 여 데이터와 덜 제한적인된 액세스를 사용 하 여 변수 형식을 벗어나는이 목적입니다. 앞의 기본 코드에서 `exposedVar` 은 `Public` 노출 및 `privateClass` 액세스할 수 없어야 하는 코드를 합니다.  
  
 **오류 ID:** BC30909  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   변수, 프로시저 매개 변수 또는 함수에 대 한 액세스 수준을 변경 하는 최소 제한적으로 해당 데이터 형식의 액세스 수준을 돌아갑니다.  
  
## <a name="see-also"></a>참고자료
- [Visual Basic의 액세스 수준](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
