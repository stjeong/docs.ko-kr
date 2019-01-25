---
title: '&lt;para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: 5932ddb55a4dab48267cdd9b9f321cec8660d77a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662324"
---
# <a name="ltparagt-visual-basic"></a>&lt;para&gt; (Visual Basic)
콘텐츠를 단락으로 형식이 지정 되었는지 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a>매개 변수  
 `content`  
 단락의 텍스트입니다.  
  
## <a name="remarks"></a>설명  
 합니다 `<para>` 태그와 같은 태그 내에서 사용 하기 위한 것 [ \<요약 >](../../../visual-basic/language-reference/xmldoc/summary.md)를 [ \<설명 >](../../../visual-basic/language-reference/xmldoc/remarks.md), 또는 [ \<반환 >](../../../visual-basic/language-reference/xmldoc/returns.md), 텍스트에 구조를 추가할 수 있습니다.  
  
 [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 합니다 `<para>` 태그에 대 한 설명 부분을 분할 하는 `UpdateRecord` 두 단락 메서드.  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a>참고자료
- [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md)
