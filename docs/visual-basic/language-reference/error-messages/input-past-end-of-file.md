---
title: 입력(값)이 파일의 끝을 넘습니다.
ms.date: 07/20/2015
f1_keywords:
- vbrID62
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
ms.openlocfilehash: 29a9b5ce3c3f8e6a02b52beda1338fd699143570
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491339"
---
# <a name="input-past-end-of-file"></a>입력(값)이 파일의 끝을 넘습니다.
중 하나는 `Input` 문에서 비어 있는 파일 또는 모든 데이터 사용 또는 사용에서 읽고는 `EOF` 함수 파일을 사용 하 여 이진 액세스를 위해 열렸습니다.  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  사용 된 `EOF` 직전 함수를 `Input` 문을 파일의 끝을 검색 합니다.  
  
2.  파일을 이진 액세스에 대 한 열을 사용 하 여 `Seek` 고 `Loc`입니다.  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.FileSystem.Input%2A>
- <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>
