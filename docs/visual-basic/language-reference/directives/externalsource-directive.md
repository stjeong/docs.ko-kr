---
title: '#ExternalSource 지시문 (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '#Externalsource'
- '#ExternalSource'
- vb.ExternalSource
- Externalsource
- vb.#ExternalSource
- ExternalSource
helpviewer_keywords:
- ExternalSource directive (#ExternalSource)
- '#ExternalSource directive'
ms.assetid: 243bc6a2-34c3-4eeb-a776-9fd2bf988149
ms.openlocfilehash: dcde8507eb033d0a47d5c5d3fa36176cd63b0856
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861791"
---
# <a name="externalsource-directive"></a>#ExternalSource 지시문
소스 코드의 특정 줄과 소스 외부에 있는 텍스트 간의 매핑을 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
#ExternalSource( StringLiteral , IntLiteral )  
    [ LogicalLine+ ]  
#End ExternalSource  
```  
  
## <a name="parts"></a>요소  
 `StringLiteral`  
 외부 원본에 대 한 경로입니다.  
  
 `IntLiteral`  
 외부 원본의 첫 번째 줄의 줄 번호입니다.  
  
 `LogicalLine`  
 외부 원본에서 오류가 발생 하는 줄.  
  
 `#End ExternalSource`  
 `#ExternalSource` 블록을 종료합니다.  
  
## <a name="remarks"></a>설명  
 이 지시문은 컴파일러 및 디버거가 의해서만 사용 됩니다.  
  
 소스 파일을 소스 파일에서 코드의 특정 줄과 외부.aspx 파일 같이 원본에 있는 텍스트 간의 매핑을 나타내는 외부 소스 지시문을 포함할 수 있습니다. 지정 된 소스 코드에서를 컴파일하는 동안 오류가 발생 하면 외부 원본에서 오는 것으로 식별 됩니다.  
  
 외부 소스 지시문 컴파일에 영향을 주지 않으며 중첩할 수 없습니다. 이러한는 내부 용도로 응용 프로그램에서 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [조건부 컴파일](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
