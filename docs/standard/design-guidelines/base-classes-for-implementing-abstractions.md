---
title: 추상화 구현을 위한 기본 클래스
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- abstractions [.NET Framework]
- base classes, abstractions
ms.assetid: 37a2d9a4-9721-482a-a40f-eee2c1d97875
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f326ee895251678c7a23ea84a11e83951edf2cc
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45677073"
---
# <a name="base-classes-for-implementing-abstractions"></a>추상화 구현을 위한 기본 클래스
엄격히 말해, 클래스는 다른 클래스에서 파생 됩니다 하는 경우 기본 클래스를 수 있습니다. 그러나이 섹션 기본 클래스는 클래스 주로 일반적인 추상화를 제공 하거나 일부를 재사용 하는 다른 클래스에 대 한 기본 구현 하지만 상속 하도록 설계 되었습니다. 기본 클래스는 일반적으로 중간 계층의 루트에 추상화 사이의 맨 아래에 몇 가지 사용자 지정 구현이 상속 계층 구조 배치 합니다.  
  
 추상화 구현을 위한 도우미 구현으로 사용 합니다. 예를 들어, 순서가 지정 된 컬렉션 항목에 대 한 프레임 워크의 추상화 중 하나는 <xref:System.Collections.Generic.IList%601> 인터페이스입니다. 구현 <xref:System.Collections.Generic.IList%601> 하며, 따라서 프레임 워크를 제공 몇 가지 기본 클래스와 같은 <xref:System.Collections.ObjectModel.Collection%601> 및 <xref:System.Collections.ObjectModel.KeyedCollection%602>, 사용자 지정 컬렉션을 구현 하기 위한 도우미 역할도 하는 합니다.  
  
 너무 많은 구현을 포함 하는 경향이 있으므로 기본 클래스 추상화로 단독으로 제공 하는 데 적합 하지 일반적으로 합니다. 예를 들어 합니다 `Collection<T>` 기본 클래스 구현 제네릭이 아닌 구현 하는 팩트에 관련 된 많은 포함 `IList` 인터페이스 (제네릭이 아닌 컬렉션을 사용 하 여 더 효율적으로 통합) 및 된다는 것에 저장 된 항목의 컬렉션 해당 필드 중 하나에 메모리입니다.  
  
 앞에서 설명한 대로 기본 클래스 추상화를 구현 해야 하는 사용자에 대 한 매우 유용한 도움말을 제공할 수 있지만 동시에 상당한 부담으로 작용할 수 있습니다. 노출 영역을 추가 및 상속 계층의 깊이 증가 하며 나타내므로 개념적 프레임 워크를 복잡 하 게 합니다. 따라서 프레임 워크의 사용자에 게 중요 한 가치를 제공 하는 경우에 기본 클래스를 사용 해야 합니다. 프레임 워크에는 기본 클래스에서 상속 하는 대신 내부 구현 사례 위임 강력 하 게 고려해 야의 구현자에만 값을 제공 하는 경우 피해 야 합니다.  
  
 **✓ CONSIDER** 함으로써 기본 추상 멤버가 포함 하지 않는 경우에 추상 클래스입니다. 이 사용자에 게 명확 하 게 통신 클래스에서 상속 하는 용도로 설계 됩니다.  
  
 **✓ CONSIDER** 주요 시나리오 형식에서 별도 네임 스페이스에 기본 클래스를 배치 합니다. 정의상, 기본 클래스는 고급 확장성 시나리오를 위한 것 및 따라서는 대부분의 사용자와 관련이 없습니다.  
  
 **X AVOID** 클래스가 공용 Api에서 사용 하기 위한 경우 "기본" 접미사를 사용 하 여 기본 클래스 이름을 지정 합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [확장성을 위한 디자인](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
