---
title: '방법: (Visual Basic) 다른 응용 프로그램과 어셈블리 공유'
ms.date: 07/20/2015
ms.assetid: 5388aedc-cb42-4622-8b70-8e701eee057a
ms.openlocfilehash: d0e1dafc700b55a63342331b3280337d2c93cbd1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631830"
---
# <a name="how-to-share-an-assembly-with-other-applications-visual-basic"></a>방법: (Visual Basic) 다른 응용 프로그램과 어셈블리 공유
어셈블리는 전용이거나 공유될 수 있습니다. 기본적으로 대부분의 간단한 프로그램은 다른 애플리케이션에서 사용되지 않으므로 전용 어셈블리로 구성됩니다.  
  
 다른 애플리케이션과 어셈블리를 공유하려면 GAC([전역 어셈블리 캐시](../../../../framework/app-domains/gac.md))에 배치해야 합니다.  
  
### <a name="sharing-an-assembly"></a>어셈블리 공유  
  
1.  어셈블리를 만듭니다. 자세한 내용은 [어셈블리 만들기](../../../../framework/app-domains/create-assemblies.md)를 참조하세요.  
  
2.  어셈블리에 강력한 이름을 할당합니다. 자세한 내용은 [방법: 강력한 이름으로 어셈블리 서명](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)을 참조하세요.  
  
3.  어셈블리에 버전 정보를 할당합니다. 자세한 내용은 [어셈블리 버전 관리](../../../../framework/app-domains/assembly-versioning.md)를 참조하세요.  
  
4.  전역 어셈블리 캐시에 어셈블리를 추가합니다. 자세한 내용은 [방법: 전역 어셈블리 캐시에 어셈블리 설치](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md)합니다.  
  
5.  다른 애플리케이션에서 어셈블리에 포함된 형식에 액세스합니다. 자세한 내용은 [방법: 강력한 이름의 어셈블리 참조](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md)합니다.  
  
## <a name="see-also"></a>참고자료

- [프로그래밍 개념](../../../../visual-basic/programming-guide/concepts/index.md)
- [어셈블리와 전역 어셈블리 캐시(Visual Basic)](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [어셈블리를 사용한 프로그래밍](../../../../framework/app-domains/programming-with-assemblies.md)
