---
title: 멤버 오버로드
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- default arguments
- members [.NET Framework], overloaded
- member design guidelines [.NET Framework], overloading
- overloaded members
- signatures, members
ms.assetid: 964ba19e-8b94-4b5b-b1e3-5a0b531a0bb1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2127497d294cbfd4e1bb24d033f432378627ff13
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44208233"
---
# <a name="member-overloading"></a>멤버 오버로드
멤버 오버 로드 매개 변수의 형식이 나 개수 에서만 차이가 있지만 이름이 같은 동일한 형식에 두 개 이상의 멤버를 만드는 것을 의미 합니다. 예를 들어, 다음 표에 `WriteLine` 메서드가 오버 로드 됩니다.  
  
```  
public static class Console {  
    public void WriteLine();  
    public void WriteLine(string value);  
    public void WriteLine(bool value);  
    ...  
}  
```  
  
 메서드, 생성자 및 인덱싱된 속성 매개 변수를 가질 수 있으므로 해당 멤버를 오버 로드할 수 있습니다.  
  
 오버 로드 사용 편의성, 생산성 및 재사용 가능한 라이브러리의 가독성을 개선 하기 위한 가장 중요 한 기술 중 하나입니다. 매개 변수 개수에 오버 로드 하는 메서드와 생성자의 간단 버전을 제공할 수 있습니다. 매개 변수 형식에 오버 로드 버전이 서로 다른 유형의 선택한 집합에서 동일한 작업을 수행 하는 멤버에 대 한 동일한 멤버 이름을 사용할 수 있습니다.  
  
 **✓ DO** 짧은 오버 로드에서 사용 되는 기본값을 나타내기 위해 설명 매개 변수 이름을 사용 하려고 합니다.  
  
 **X AVOID** 임의의 여러 오버 로드에 매개 변수 이름입니다. 하나의 오버 로드에 매개 변수가 다른 오버 로드에 매개 변수로 동일한 입력을 나타내는 경우 매개 변수는 이름이 있어야 합니다.  
  
 **X AVOID** 오버 로드 된 멤버의 매개 변수 순서에 일관 되지 않은 것입니다. 동일한 이름 가진 매개 변수는 모든 오버 로드에서 같은 위치에 표시 됩니다.  
  
 **✓ DO** (확장 기능이 필요) 하는 경우 가상 가장 긴 오버 로드를 확인 합니다. 짧은 오버 로드는 긴 오버 로드를 통해 호출 해야 합니다.  
  
 **X DO NOT** 사용 `ref` 또는 `out` 한정자를 멤버를 오버 로드 합니다.  
  
 일부 언어는 다음과 같은 오버 로드에 대 한 호출을 확인할 수 없습니다. 또한 이러한 오버 로드 완전히 다른 의미 체계를가지고 있으며 아마도 안 오버 로드 하지만 별도 두 가지 방법 대신 합니다.  
  
 **X DO NOT** 서로 다른 의미 체계 하면서도 동일한 위치와 유사한 형식 매개 변수를 사용 하는 오버 로드를 갖고 있습니다.  
  
 **✓ DO** 허용 `null` 선택적 인수를 전달 하도록 합니다.  
  
 **✓ DO** 멤버 기본 인수가 있는 멤버를 정의 하는 대신 오버 로드를 사용 합니다.  
  
 기본 인수 CLS 규격이있지 않습니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [멤버 디자인 지침](../../../docs/standard/design-guidelines/member.md)  
- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)
