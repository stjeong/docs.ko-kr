---
title: '&#39;Dir&#39; 함수를 사용 하 여 먼저 호출 해야는 &#39;PathName&#39; 인수'
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: f7e9ef9cc6309f24ae9f8963e910b41180c029b7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518490"
---
# <a name="39dir39-function-must-first-be-called-with-a-39pathname39-argument"></a>&#39;Dir&#39; 함수를 사용 하 여 먼저 호출 해야는 &#39;PathName&#39; 인수
에 대 한 초기 호출을 `Dir` 함수는 포함 되지 않습니다는 `PathName` 인수입니다. 첫 번째 호출은 `Dir` 포함 해야 합니다는 `PathName`, 하지만 후속 호출 `Dir` 다음 항목을 검색 하는 매개 변수를 포함할 필요가 없습니다.  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  제공 된 `PathName` 함수 호출의 인수입니다.  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
