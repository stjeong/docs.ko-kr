---
title: XML 주석 예외 있어야는 &#39;cref&#39; 특성
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: 0f276781165e80b2d869da2518dbe34b33085d5c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649949"
---
# <a name="xml-comment-exception-must-have-a-39cref39-attribute"></a>XML 주석 예외 있어야는 &#39;cref&#39; 특성
\<예외 > 태그는 메서드에서 throw 될 수 있는 예외를 문서화 하는 방법을 제공 합니다. 필수 `cref` 특성 설명서 생성기에서 확인 하는 멤버의 이름을 지정 합니다. 멤버가 있는 경우 문서 파일의 정식 요소 이름으로 변환 됩니다.  
  
 **오류 ID:** BC42319  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   추가 된 `cref` 예외에 특성을 다음과 같이 합니다.  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## <a name="see-also"></a>참고자료
- [\<exception>](../../../visual-basic/language-reference/xmldoc/exception.md)
- [방법: XML 문서 만들기](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
- [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md)
