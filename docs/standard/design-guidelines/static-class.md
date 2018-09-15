---
title: 정적 클래스 디자인
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c3a0a51fc6055190f9a0189de2e17d98f88036ea
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45658316"
---
# <a name="static-class-design"></a>정적 클래스 디자인
정적 멤버만 포함 하는 클래스로 정의 된 정적 클래스 (에서 상속 된 인스턴스 멤버 외에도 물론 <xref:System.Object?displayProperty=nameWithType> 및 private 생성자를 사용 가능한 경우). 일부 언어는 정적 클래스에 대 한 기본 제공 지원을 제공 합니다. C# 2.0 이상에서는 클래스를 static으로 선언 봉인 된 추상 하 고, 없는 인스턴스 멤버를 재정의 하거나 선언 합니다.  
  
 정적 클래스는 순수 개체 지향 디자인 및 단순성 절충 합니다. 다른 작업에 대 한 바로 가기를 제공 되는 일반적으로 (같은 <xref:System.IO.File?displayProperty=nameWithType>), 확장 메서드 또는 전체 개체 지향 래퍼를 보장 하지 않습니다 기능 소유자 (같은 <xref:System.Environment?displayProperty=nameWithType>).  
  
 **✓ DO** 가급적 정적 클래스를 사용 합니다.  
  
 클래스는 프레임 워크의 개체 지향 core에 대 한 지원 으로만 정적 클래스를 사용 해야 합니다.  
  
 **X DO NOT** 정적 클래스를 기타 버킷으로 처리 합니다.  
  
 **X DO NOT** 선언 또는 정적 클래스에 인스턴스 멤버를 재정의 합니다.  
  
 **✓ DO** 봉인, 추상으로 정적 클래스를 선언 하 고 선택한 프로그래밍 언어에 정적 클래스에 대 한 기본 제공 지원 없는 경우 전용 인스턴스 생성자를 추가 합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [형식 디자인 지침](../../../docs/standard/design-guidelines/type.md)  
- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)
