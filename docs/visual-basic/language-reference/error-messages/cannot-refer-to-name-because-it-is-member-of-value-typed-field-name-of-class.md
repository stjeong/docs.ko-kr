---
title: 참조할 수 없습니다 &#39; &lt;이름을&gt; &#39; 값 형식 필드의 멤버 이기 때문에 &#39; &lt;이름&gt; &#39; 클래스 &#39; &lt;classname&gt; &#39;있는 &#39;System.MarshalByRefObject&#39; 기본 클래스
ms.date: 07/20/2015
f1_keywords:
- vbc30310
- bc30310
helpviewer_keywords:
- BC30310
ms.assetid: 2aeb8872-7c87-4f01-98ef-9714ba3eebbe
ms.openlocfilehash: a6298c3e0f5102397d5cc3f237a186598c6b5ecc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739299"
---
# <a name="cannot-refer-to-39ltnamegt39-because-it-is-a-member-of-the-value-typed-field-39ltnamegt39-of-class-39ltclassnamegt39-which-has-39systemmarshalbyrefobject39-as-a-base-class"></a>참조할 수 없습니다 &#39; &lt;이름을&gt; &#39; 값 형식 필드의 멤버 이기 때문에 &#39; &lt;이름&gt; &#39; 클래스 &#39; &lt;classname&gt; &#39;있는 &#39;System.MarshalByRefObject&#39; 기본 클래스
`System.MarshalByRefObject` 클래스를 사용 하면 응용 프로그램 도메인 경계를 넘어 개체에 대 한 원격 액세스를 지 원하는 응용 프로그램입니다. 형식에서 상속 해야 합니다는 `MarshalByRejectObject` 클래스 유형이 응용 프로그램 도메인 경계에 걸쳐 사용 됩니다. 개체의 멤버는 만든 응용 프로그램 도메인 외부에서 사용할 수 없기 때문에 개체의 상태는 복사 해야 합니다.  
  
 **오류 ID:** BC30310  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  에 참조 되는 멤버가 올바른지 확인에 대 한 참조를 확인 합니다.  
  
2.  멤버를 명시적으로 한정 된 `Me` 키워드입니다.  
  
## <a name="see-also"></a>참고자료
- <xref:System.MarshalByRefObject>
- [Dim 문](../../../visual-basic/language-reference/statements/dim-statement.md)
