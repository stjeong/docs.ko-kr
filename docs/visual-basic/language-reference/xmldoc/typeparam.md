---
title: <typeparam> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- typeparam XML tag
- <typeparam> XML tag
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
ms.openlocfilehash: d7fb980545a532e39310ea3e9d663a2b5a81a006
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56968454"
---
# <a name="typeparam-visual-basic"></a>\<typeparam > (Visual Basic)
형식 매개 변수 이름 및 설명을 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
#### <a name="parameters"></a>매개 변수  
 `name`  
 형식 매개 변수의 이름입니다. 이름을 큰따옴표(“ ”)로 묶습니다.  
  
 `description`  
 형식 매개 변수의 설명입니다.  
  
## <a name="remarks"></a>설명  
 사용 하 여를 `<typeparam>` 태그의 주석에 제네릭 형식 또는 제네릭 멤버 선언은 형식 매개 변수 중 하나를 설명 합니다.  
  
 [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 합니다 `<typeparam>` 설명 하는 태그를 `id` 매개 변수입니다.  
  
 [!code-vb[VbVbcnXmlDocComments#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#8)]  
  
## <a name="see-also"></a>참고자료
- [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md)
