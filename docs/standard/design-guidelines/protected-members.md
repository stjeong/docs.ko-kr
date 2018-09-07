---
title: 보호된 멤버
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4574dffc3f9dd1b60d655bfde33a4ddc1a81d350
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44068978"
---
# <a name="protected-members"></a>보호된 멤버
단독으로 보호 된 멤버 모든 확장성을 제공 하지 않지만 내릴 수 서브클래싱 통해 확장성을 더 강력 합니다. 기본 공용 인터페이스를 불필요 하 게 복잡 하 게 만들지 않고 고급 사용자 지정 옵션을 표시 하려면 사용할 수 있습니다.  
  
 프레임 워크 디자이너 "보호" 이름을 보안에 대해 잘못 된를 지정할 수 없기 때문에 보호 된 멤버를 사용 하 여 신중 하 게 되도록 해야 합니다. 모든 사용자가 하위 클래스는 봉인 되지 않은 클래스 및 멤버에 보호 된 액세스를 수 있고 public 멤버에 사용 되는 코딩 관례 protected 멤버에 적용 되는 동일한 하므로.  
  
 **✓ CONSIDER** 를 사용 하 여 고급 사용자 지정에 대 한 멤버를 보호 합니다.  
  
 **✓ DO** 보안, 설명서 및 호환성 분석용으로 public으로 봉인 되지 않은 클래스의 보호 된 멤버를 처리 합니다.  
  
 누구 든 지 클래스에서 상속 하 고 보호 된 멤버에 액세스할 수 있습니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [확장성을 위한 디자인](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
