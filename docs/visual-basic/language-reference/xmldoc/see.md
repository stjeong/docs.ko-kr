---
title: '&lt;참조&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- see XML tag
- <see> XML tag
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
ms.openlocfilehash: 78311651593d3d4a47c723f64a9a74d4660f7c90
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43403679"
---
# <a name="ltseegt-visual-basic"></a>&lt;참조&gt; (Visual Basic)
다른 멤버에 대 한 링크를 지정합니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<see cref="member"/>  
```  
  
#### <a name="parameters"></a>매개 변수  
 `member`  
 현재 컴파일 환경에서 호출할 수 있는 멤버 또는 필드에 대한 참조입니다. 컴파일러는 지정 된 코드 요소가 있고 전달 확인 `member` 를 출력 XML에에서 요소 이름입니다. `member`는 큰따옴표(" ")로 묶어야 합니다.  
  
## <a name="remarks"></a>설명  
 사용 된 `<see>` 텍스트 내에서 링크를 지정 하는 태그입니다. 사용 하 여 [ \<seealso >](../../../visual-basic/language-reference/xmldoc/seealso.md) "참고 항목" 섹션에 표시 하려는 텍스트를 나타냅니다.  
  
 [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 합니다 `<see>` 태그를 `UpdateRecord` 주의 섹션을 참조는 `DoesRecordExist` 메서드.  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/see_1.vb)]  
  
## <a name="see-also"></a>참고 항목  
 [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md)
