---
title: 매개 변수 이름 지정
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- parameters, names
- names [.NET Framework], parameters
ms.assetid: ca3c956e-725a-441b-b4e3-eab5d472f41c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8e6a8a1dcdcb8fa3311b040c72987f0f76e681fc
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44086474"
---
# <a name="naming-parameters"></a>매개 변수 이름 지정
가독성의 이유를 초과 비주얼 디자인 도구 Intellisense 및 검색 기능을 하는 클래스를 제공 하는 경우 매개 변수는 문서에 디자이너에 표시 되기 때문에 매개 변수 이름에 대 한 지침을 따르는 것이 반드시 합니다.  
  
 **✓ DO** camelCasing 매개 변수 이름에 사용할 수 있습니다.  
  
 **✓ DO** 설명이 포함 된 매개 변수 이름을 사용 합니다.  
  
 **✓ CONSIDER** 매개 변수의 형식 보다는 매개 변수의 의미에 따라 이름을 사용 합니다.  
  
### <a name="naming-operator-overload-parameters"></a>연산자 오버 로드 매개 변수 이름 지정  
 **✓ DO** 사용 `left` 및 `right` 이항 연산자 오버 로드 매개 변수 이름은 매개 변수를 아무 의미가 없는 경우에 대 한 합니다.  
  
 **✓ DO** 사용 `value` 에 대 한 단항 연산자 오버 로드 매개 변수 이름은 매개 변수를 아무 의미가 없는 경우.  
  
 **✓ CONSIDER** 연산자에 대 한 의미 있는 이름을 추가 되므로 중요 한 가치 경우 매개 변수를 재정의 합니다.  
  
 **X DO NOT** 오버 로드 매개 변수 이름을 사용 하 여 약어 또는 연산자에 대 한 숫자 인덱스입니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [명명 지침](../../../docs/standard/design-guidelines/naming-guidelines.md)
