---
title: 같음 연산자
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], Equals method
- class library design guidelines [.NET Framework], equality operator
- equality operator (==) [.NET Framework]
- Equals method
- == operator (equality) [.NET Framework]
ms.assetid: bc496a91-fefb-4ce0-ab4c-61f09964119a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27550a8fd8292029cad9c2e699374a190b1a532e
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46287024"
---
# <a name="equality-operators"></a>같음 연산자
이 섹션에서는 같음 연산자를 오버 로드에 대해 설명 하 고 가리킵니다 `operator==` 고 `operator!=` 같음 연산자입니다.  
  
 **X DO NOT** 같음 연산자 있고 다른 선언 중 하나를 오버 로드 합니다.  
  
 **✓ DO** 되도록 <xref:System.Object.Equals%2A?displayProperty=nameWithType> 및 같음 연산자는 정확히 동일한 의미 체계와 비슷한 성능 특성입니다.  
  
 자주 따라서 `Object.Equals` 같음 연산자를 오버 로드 하는 경우 재정의 해야 합니다.  
  
 **X AVOID** 같음 연산자에서 예외를 throw 합니다.  
  
 예를 들어 인수 중 하나를 throw 하지 않고 null 이면 false를 반환 `NullReferenceException`합니다.  
  
## <a name="equality-operators-on-value-types"></a>값 형식에 같음 연산자  
 **✓ DO** 같음이 의미가 있을 경우에 값 형식에 같음 연산자를 오버 로드 합니다.  
  
 대부분의 프로그래밍 언어에서은의 기본 구현이 없는 `operator==` 값 형식에 대 한 합니다.  
  
## <a name="equality-operators-on-reference-types"></a>참조 형식에 같음 연산자  
 **X AVOID** 변경 가능한 참조 형식에 같음 연산자를 오버 로드 합니다.  
  
 다양 한 언어 참조 형식에 대 한 기본 같음 연산자가 있는 경우. 기본 제공 연산자에는 일반적으로 참조 같음 구현 하 고 값이 같은지를 기본 동작이 변경 될 때 많은 개발자가 알고 계십니까 키를 누릅니다.  
  
 이 문제는 불변성을 사용 하면 값이 같은지 참조 같음 사이의 차이점을 확인 하기가 훨씬 변경할 수 없는 참조 형식에 대 한 완화 됩니다.  
  
 **X AVOID** 참조 일치 하는 것 보다 크게 느려지지 구현 되는 경우에 참조 형식에 같음 연산자를 오버 로드 합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [사용 지침](../../../docs/standard/design-guidelines/usage-guidelines.md)
