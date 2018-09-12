---
title: 확장성을 위한 디자인
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c1690d0cdf1f57eaf0a794d6e71babfa4fa6425
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44710903"
---
# <a name="designing-for-extensibility"></a>확장성을 위한 디자인
프레임 워크 디자인의 중요 한 측면 있는지 확인 하는 프레임 워크의 확장성을 신중 하 게 고려 했습니다. 그러려면, 비용 및 다양 한 확장성 메커니즘을 사용 하 여 연결 된 혜택을 파악 해야 합니다. 이 장에서 확장성 메커니즘을 결정 하 고-서브클래싱, 이벤트, 가상 멤버, 콜백 및 등-프레임 워크의 요구 사항을 충족할 수 있습니다.  
  
 프레임 워크의 확장성을 허용 하는 방법은 여러 가지입니다. 이러한 범위에서 덜 강력 하지만 비용이 덜 드는 매우 강력 하지만 비용이 많이 드는입니다. 모든 지정 된 확장성 요구 사항에 대 한 요구 사항을 충족 하는 가장 비용이 많이 드는 확장성 메커니즘을 선택 해야 합니다. 일반적으로 더 큰 확장성을 나중에 추가할 수 있기 벗어날 수 있지만 수 고 떨어진 새로운 변경 사항 없이 염두에서에 둡니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [봉인되지 않은 클래스](../../../docs/standard/design-guidelines/unsealed-classes.md)  
 [보호된 멤버](../../../docs/standard/design-guidelines/protected-members.md)  
 [이벤트 및 콜백](../../../docs/standard/design-guidelines/events-and-callbacks.md)  
 [가상 멤버](../../../docs/standard/design-guidelines/virtual-members.md)  
 [추상화(추상 형식 및 인터페이스)](../../../docs/standard/design-guidelines/abstractions-abstract-types-and-interfaces.md)  
 [추상화 구현을 위한 기본 클래스](../../../docs/standard/design-guidelines/base-classes-for-implementing-abstractions.md)  
 [봉인](../../../docs/standard/design-guidelines/sealing.md)  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)
