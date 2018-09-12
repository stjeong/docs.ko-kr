---
title: 구조체 디자인
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- deallocating structures
- allocating structures
- value types, structures
- structure design
- type design guidelines, structures
- structures [.NET Framework], design guidelines
ms.assetid: 1f48b2d8-608c-4be6-9ba4-d8f203ed9f9f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3879dc3f0270a56132b44882a74c50d05914ff89
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44709573"
---
# <a name="struct-design"></a>구조체 디자인
범용 값 형식 대부분의 구조체를 해당 C# 키워드 라고 합니다. 이 섹션에서는 일반 구조체 디자인에 대 한 지침을 제공 합니다.  
  
 **X DO NOT** 구조체에 대 한 기본 생성자를 제공 합니다.  
  
 이 지침은 다음 배열을 구조체를 배열의 각 항목에 대해 생성자를 실행할 필요 없이 만들 수 있습니다. C#을 허용 하지 않도록 구조체에는 기본 생성자를 확인할 수 있습니다.  
  
 **X DO NOT** 변경할 수 있는 값 형식을 정의 합니다.  
  
 변경할 수 있는 값 형식에는 몇 가지 문제가 있습니다. 예를 들어, 속성 getter에서 값 형식을 반환 하는 경우 호출자에 게 복사본을 받습니다. 복사본을 암시적으로 만들어지기 때문에 개발자가 알지 못할 복사 하 고 원래 값이 아니라 변경 됩니다. 또한 일부 언어 (특히에서 동적 언어) 문제가 있으므로 변경할 수 있는 값 형식을 사용 하 여 역참조 시 로컬 변수에도, 하면 복사 되도록 합니다.  
  
 **✓ DO** 0으로 설정 되어 있는 모든 인스턴스 데이터는 상태, false 또는 적절 하 게 null 올바른지 확인 합니다.  
  
 이 구조체 배열을 만들어질 때 잘못 된 인스턴스도 실수로 생성을 방지 합니다.  
  
 **✓ DO** 구현 <xref:System.IEquatable%601> 값 형식에 있습니다.  
  
 <xref:System.Object.Equals%2A?displayProperty=nameWithType> 하면 boxing, 값 형식에 메서드 및 리플렉션을 사용 하 여 해당 기본 구현은 매우 효율적 이므로 합니다. <xref:System.IEquatable%601.Equals%2A> 훨씬 더 나은 성능이 있습니다 및 boxing 되지 것입니다 있도록 구현할 수 있습니다.  
  
 **X DO NOT** 명시적으로 확장 <xref:System.ValueType>합니다. 사실 대부분의 언어가를 방지 합니다.  
  
 일반적으로 구조체 매우 유용할 수 있지만 자주 boxed 하지는 small, single, 변경할 수 없는 값만 사용 해야 합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [형식 디자인 지침](../../../docs/standard/design-guidelines/type.md)  
- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [클래스와 구조체 간의 선택](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)
