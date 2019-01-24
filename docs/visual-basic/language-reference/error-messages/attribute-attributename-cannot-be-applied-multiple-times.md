---
title: 특성 &#39; &lt;attributename&gt; &#39; 여러 번 적용할 수 없습니다
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: 6609ce299799bc3c4b78d48478e99e4d4101dd72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565165"
---
# <a name="attribute-39ltattributenamegt39-cannot-be-applied-multiple-times"></a>특성 &#39; &lt;attributename&gt; &#39; 여러 번 적용할 수 없습니다
특성 한 번만 적용할 수 있습니다. `AttributeUsage` 특성 특성을 두 번 이상 적용할 수 있는지 여부를 결정 합니다.  
  
 **오류 ID:** BC30663  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  특성은 한 번만 적용 해야 합니다.  
  
2.  개발한 사용자 지정 특성을 사용 하는 경우 변경해 보십시오 해당 `AttributeUsage` 다음 예제에서와 마찬가지로 여러 특성 사용을 허용 하는 특성입니다.  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a>참고자료
- <xref:System.AttributeUsageAttribute>
- [사용자 지정 특성 만들기](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)
- [AttributeUsage](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
