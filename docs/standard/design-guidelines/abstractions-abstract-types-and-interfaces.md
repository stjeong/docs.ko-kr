---
title: 추상화(추상 형식 및 인터페이스)
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- interfaces [.NET Framework], abstract
- abstract interfaces [.NET Framework]
- abstract types [.NET Framework]
- types [.NET Framework], abstract
ms.assetid: 0a632bc7-9b03-44ee-8842-c82f88672a45
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0ad8b2dd3dbf2a7a75c98a3115d4351dfea4e1a0
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46480684"
---
# <a name="abstractions-abstract-types-and-interfaces"></a>추상화(추상 형식 및 인터페이스)
추상 형식인 계약에 설명 하지만 계약의 전체 구현을 제공 하지 않습니다. 추상화는 일반적으로 추상 클래스 또는 인터페이스를 구현 하 고 여기에 잘 정의 된 계약을 구현 하는 형식의 필요한 의미 체계를 설명 하는 참조 설명서 집합입니다. .NET Framework의 가장 중요 한 추상화 같습니다 <xref:System.IO.Stream>, <xref:System.Collections.Generic.IEnumerable%601>, 및 <xref:System.Object>합니다.  
  
 추상화의 계약을 지 원하는 구체적 형식 구현 및 프레임 워크 Api 사용 (작동 중에)이 구체적인 형식을 사용 하 여 프레임 워크를 확장할 수 있습니다를 추상화 합니다.  
  
 시간 테스트를 견딜 수 있는 의미 있고 유용한 추상화를 디자인 하기 매우 어렵습니다. 주요 문제는 멤버를 더 이상 더 적은 수의 올바른 집합을 가져오는 중입니다. 추상화에 멤버가 너무 많은 경우 어렵거나 구현 됩니다. 약속된 기능에 너무 적은 멤버가 있으면 많은 흥미로운 시나리오에서 쓸모 없게 됩니다.  
  
 프레임 워크에서 너무 많은 추상화에는 프레임 워크의 유용성도 부정적인 영향을 합니다. 구체적인 구현과 추상화에서 작동 하는 Api의 큰 그림에 맞추는 방법을 알 수 없는 추상화를 이해 하기 어려운 경우가 있습니다. 또한 추상화 및 해당 멤버의 이름은 반드시 추상 종종을 사용 하면 복잡 하 고 차갑고 첫 번째 용도의 광범위 한 컨텍스트를 알 수 없는 합니다.  
  
 그러나 추상화 기타 확장성 메커니즘과 없습니다 자주 일치 하는 매우 강력한 확장성을 제공 합니다. 이들은 플러그 인과 같은 많은 아키텍처 패턴의 핵심 반전 (IoC) 제어, 파이프라인 및 등입니다. 프레임 워크의 테스트 용이성에 매우 중요 수도 있습니다. 적절 한 추상화를 사용 하면 단위 테스트 목적으로 많은 종속성을 스텁 할 수 있습니다. 요약 하자면, 추상화 많았던 다양 한 최신 개체 지향 프레임 워크를 담당합니다.  
  
 **X DO NOT** 여러 구체적인 구현 및 Api를 사용 하는 추상화를 개발 하 여 테스트 하지 않는 한 추상화를 제공 합니다.  
  
 **✓ DO** 추상화를 디자인할 때, 추상 클래스와 인터페이스를 신중 하 게 선택 합니다.  
  
 **✓ CONSIDER** 추상화의 구체적인 구현에 대 한 참조 테스트를 제공 합니다. 이러한 테스트는 구현 계약을 올바르게 구현 하는지 여부를 테스트 하도록 사용자를 허용 해야 합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [확장성을 위한 디자인](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
