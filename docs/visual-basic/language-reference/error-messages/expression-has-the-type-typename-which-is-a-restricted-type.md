---
title: 식의 형식은 &#39; &lt;typename&gt; &#39; 제한 된 형식 및에서 상속 된 멤버에 액세스를 사용할 수 있는 &#39;개체&#39; 또는 &#39;ValueType&#39;
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: d44b9a29f0848508d8cd814e857d9b01819ce7ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535959"
---
# <a name="expression-has-the-type-39lttypenamegt39-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-39object39-or-39valuetype39"></a>식의 형식은 &#39; &lt;typename&gt; &#39; 제한 된 형식 및에서 상속 된 멤버에 액세스를 사용할 수 있는 &#39;개체&#39; 또는 &#39;ValueType&#39;
식 형식에 CLR (공용 언어 런타임)에서 넣을 수 없습니다. 계산 하지만 boxing 해야 하는 멤버에 액세스 합니다.  
  
 *Boxing* 은 형식을 경우에 따라 `Object` 또는 <xref:System.ValueType>으로 변환하는 데 필요한 처리를 참조합니다. 공용 언어 런타임에서 특정 구조 종류를 예를 들어 상자 수 없습니다 <xref:System.ArgIterator>하십시오 <xref:System.RuntimeArgumentHandle>, 및 <xref:System.TypedReference>합니다.  
  
 이 식에서 상속 된 메서드를 호출 하려면 제한 된 형식을 사용 하려고 <xref:System.Object> 나 <xref:System.ValueType>와 같은 <xref:System.Object.GetHashCode%2A> 또는 <xref:System.Object.ToString%2A>합니다. 이 메서드에 액세스 하려면 Visual Basic에서이 오류가 발생 하는 암시적 boxing 변환을 시도 했습니다.  
  
 **오류 ID:** BC31393  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  제시된 형식으로 계산되는 식을 찾습니다.  
  
2.  상속 된 메서드를 호출 하려는 문의 일부를 찾습니다 <xref:System.Object> 또는 <xref:System.ValueType>합니다.  
  
3.  메서드 호출을 방지 하려면 문을 다시 작성 합니다.  
  
## <a name="see-also"></a>참고자료
- [암시적 변환과 명시적 변환](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
