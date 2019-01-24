---
title: '&#39;줄&#39; 문은 더 이상 지원 (Visual Basic 컴파일러 오류)'
ms.date: 07/20/2015
f1_keywords:
- bc30830
- vbc30830
helpviewer_keywords:
- BC30830
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
ms.openlocfilehash: 36226cc371ffb8a51cb8d0f918952f1c717aea10
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702977"
---
# <a name="39line39-statements-are-no-longer-supported-visual-basic-compiler-error"></a>&#39;줄&#39; 문은 더 이상 지원 (Visual Basic 컴파일러 오류)
줄 문은 지원 하지 않습니다. 파일 I/O 기능은 사용할 수 있습니다 `Microsoft.VisualBasic.FileSystem.LineInput` 그래픽 기능으로 제공 되며 `System.Drawing.Graphics.DrawLine`합니다.  
  
 **오류 ID:** BC30830  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  파일 액세스를 수행 하는 경우 사용 하 여 `Microsoft.VisualBasic.FileSystem.LineInput`입니다.  
  
2.  그래픽을 수행하는 경우 `System.Drawing.Graphics.Drawline`을 사용합니다.  
  
## <a name="see-also"></a>참고자료
- <xref:System.IO>
- <xref:System.Drawing>
- [Visual Basic을 사용한 파일 액세스](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)
