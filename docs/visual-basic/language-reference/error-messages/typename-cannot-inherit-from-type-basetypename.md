---
title: '&#39;&lt;typename&gt; &#39; 에서 상속할 수 없습니다 &lt;형식&gt; &#39; &lt;basetypename&gt; &#39; 자료의 액세스를 확장 하므로 &lt;형식&gt; 어셈블리 외부에서'
ms.date: 07/20/2015
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords:
- BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
ms.openlocfilehash: 108025132bdd0fa86df5ed142aaa39c7b7e18062
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54556485"
---
# <a name="39lttypenamegt39-cannot-inherit-from-lttypegt-39ltbasetypenamegt39-because-it-expands-the-access-of-the-base-lttypegt-outside-the-assembly"></a>&#39;&lt;typename&gt; &#39; 에서 상속할 수 없습니다 &lt;형식&gt; &#39; &lt;basetypename&gt; &#39; 자료의 액세스를 확장 하므로 &lt;형식&gt; 어셈블리 외부에서
기본 클래스에서 상속 하는 클래스 또는 인터페이스 또는 인터페이스의 하지만 덜 제한적인 액세스 수준이 있습니다.  
  
 예를 들어,를 `Public` 인터페이스에서 상속 되는 `Friend` 인터페이스 또는 `Protected` 클래스에서 상속을 `Private` 클래스. 이 기본 클래스 또는 인터페이스 의도 한 수준 이상의 액세스를 제공 합니다.  
  
 **오류 ID:** BC30910  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   파생된 클래스 또는 적어도 제한적으로 기본 클래스 또는 인터페이스의 인터페이스의 액세스 수준을 변경 합니다.  
  
     또는  
  
-   덜 제한적인 액세스 수준에 필요한 경우 제거 된 `Inherits` 문입니다. 좀 더 제한 된 기본 클래스 또는 인터페이스에서 상속할 수 없습니다.  
  
## <a name="see-also"></a>참고자료
- [Class 문](../../../visual-basic/language-reference/statements/class-statement.md)
- [Interface 문](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Inherits 문](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [Visual Basic의 액세스 수준](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
