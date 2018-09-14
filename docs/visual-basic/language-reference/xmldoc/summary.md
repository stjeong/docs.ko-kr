---
title: '&lt;요약&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: 5ef9b7a98503ff36174de4418ca7d599c365f5aa
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45593784"
---
# <a name="ltsummarygt-visual-basic"></a>&lt;요약&gt; (Visual Basic)
멤버의 요약을 지정합니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a>매개 변수  
 `description`  
 개체에 대한 요약입니다.  
  
## <a name="remarks"></a>설명  
 사용 된 `<summary>` 형식 또는 형식 멤버를 설명 하는 태그입니다. [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md)를 사용하여 형식 설명에 보충 정보를 추가할 수 있습니다.  
  
 에 대 한 텍스트는 `<summary>` 태그는 IntelliSense의 형식에 대 한 정보의 원본 및 개체 브라우저에도 표시 됩니다. 개체 브라우저에 대 한 정보를 참조 하세요 [코드 구조 보기](/visualstudio/ide/viewing-the-structure-of-code)합니다.  
  
 [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 합니다 `<summary>` 태그를 설명 하는 `ResetCounter` 메서드 및 `Counter` 속성입니다.  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/summary_1.vb)]  
  
## <a name="see-also"></a>참고 항목  
 [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md)
