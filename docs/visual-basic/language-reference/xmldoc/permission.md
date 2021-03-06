---
title: <permission> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: 6c684a674e8d6e3bf218e0131e5fac2821855456
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966374"
---
# <a name="permission-visual-basic"></a>\<사용 권한 > (Visual Basic)
멤버에 대 한 필요한 사용 권한을 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a>매개 변수  
 `member`  
 현재 컴파일 환경에서 호출할 수 있는 멤버 또는 필드에 대한 참조입니다. 컴파일러는 지정된 코드 요소가 있으며 `member`를 출력 XML의 정식 요소 이름으로 변환하는지 확인합니다. 묶습니다 `member` 큰따옴표에서 ("").  
  
 `description`  
 멤버 액세스 권한에 대한 설명입니다.  
  
## <a name="remarks"></a>설명  
 사용 된 `<permission>` 멤버에 대 한 액세스를 문서화 하는 태그입니다. 사용 된 <xref:System.Security.PermissionSet> 멤버에 대 한 액세스를 지정 하는 클래스입니다.  
  
 [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.  
  
## <a name="example"></a>예제  
 이 예에서는 `<permission>` 태그를 설명 하는 <xref:System.Security.Permissions.FileIOPermission> 에 필요한는 `ReadFile` 메서드.  
  
 [!code-vb[VbVbcnXmlDocComments#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#7)]  
  
## <a name="see-also"></a>참고자료
- [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md)
