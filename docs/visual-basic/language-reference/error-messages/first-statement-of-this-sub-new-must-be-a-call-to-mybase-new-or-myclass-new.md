---
title: 이 첫 번째 문은 &#39;Sub&#39; 에 대 한 호출 이어야 합니다 &#39;MyBase.New&#39; 또는 &#39;m y&#39; (No 액세스할 수 있는 매개 변수가 없는 생성자)
ms.date: 07/20/2015
f1_keywords:
- bc30148
- vbc30148
helpviewer_keywords:
- BC30148
ms.assetid: 4426e8fc-cb39-4eb8-ba95-503cd32fcc89
ms.openlocfilehash: 75832ae88908094c1cb74ce04ad84c0d2ae91e68
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728897"
---
# <a name="first-statement-of-this-39sub-new39-must-be-a-call-to-39mybasenew39-or-39myclassnew39-no-accessible-constructor-without-parameters"></a>이 첫 번째 문은 &#39;Sub&#39; 에 대 한 호출 이어야 합니다 &#39;MyBase.New&#39; 또는 &#39;m y&#39; (No 액세스할 수 있는 매개 변수가 없는 생성자)
때문에이 ' Sub n e '의 첫째 문은 'MyBase.New' 또는 'm y'에 대 한 호출 이어야 합니다 기본 클래스\<basename >'의 '\<derivedname >' 인수 없이 호출할 수 있는 액세스 가능한 ' Sub n이 없습니다.  
  
 모든 생성자는 파생된 클래스에서 기본 클래스 생성자를 호출 해야 합니다 (`MyBase.New`). 기본 클래스에 파생된 클래스에 액세스할 수 있는 매개 변수가 없는 생성자가 하는 경우 `MyBase.New` 자동으로 호출할 수 있습니다. 그렇지 않은 경우 매개 변수를 사용 하 여 기본 클래스 생성자를 호출 해야 하 고 자동으로 수행할 수 없습니다. 이 경우 모든 파생된 클래스 생성자의 첫 번째 문 기본 클래스에서 매개 변수화 된 생성자를 호출 하거나 기본 클래스 생성자를 호출 하는 파생된 클래스의 다른 생성자를 호출 해야 합니다.  
  
 **오류 ID:** BC30148  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   호출 `MyBase.New` 필수 매개 변수를 제공 하거나 이러한 호출 피어 생성자를 호출 합니다.  
  
     예를 들어, 기본 클래스에 생성자로 선언 된 경우 `Public Sub New(ByVal index as Integer)`, 파생의 첫째 문은 클래스 생성자 않을 `MyBase.New(100)`합니다.  
  
## <a name="see-also"></a>참고자료
- [상속 기본 사항](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
