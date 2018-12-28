---
title: "'Object' 형식의 인수를 사용하는 경우 'FilePut' 대신 'FilePutObject'를 사용하세요."
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: df7d7c54992984bcb1684e41f60ae8361a3aed03
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/22/2018
ms.locfileid: "53774227"
---
# <a name="use-fileputobject-instead-of-fileput-when-using-argument-of-type-object"></a>'Object' 형식의 인수를 사용하는 경우 'FilePut' 대신 'FilePutObject'를 사용하세요.
`FilePut` 메서드는 `Object`형식의 인수를 포함합니다. 모호성을 피하기 위해`FilePutObject` 대신 `FilePut` 를 사용해야 합니다.  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   `FilePut` 을 `FilePutObject`로 바꿉니다.  
  
-   `Object` 인수를 더 구체적인 형식으로 캐스트합니다.  
  
-   `My.Computer.FileSystem` 개체에서 사용할 수 있는 기능을 사용합니다.  
  
## <a name="see-also"></a>참고 항목  
   
 [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)  
 [My.Computer.FileSystem.WriteAllBytes](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
