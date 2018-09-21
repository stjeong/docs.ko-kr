---
title: 리소스 이름 지정
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], localized resources
- localization, naming guidelines
- resource names
- global applications, naming guidelines
- international applications, naming guidelines
ms.assetid: 8b0e97f3-7877-44fd-bc76-e05d36d5d79c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5b53fc383e6fc9a5f056bab4eabde9979cd734b
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46493063"
---
# <a name="naming-resources"></a>리소스 이름 지정
지역화할 수 있는 리소스 속성 처럼 특정 개체를 통해 참조할 수, 있으므로 리소스에 대 한 명명 지침 속성 지침 비슷합니다.  
  
 **✓ DO** PascalCasing 리소스 키에 사용 합니다.  
  
 **✓ DO** 설명 하는 대신 짧은 식별자를 제공 합니다.  
  
 **X DO NOT** 주 CLR 언어의 언어 관련 키워드를 사용 합니다.  
  
 **✓ DO** 영숫자 문자와 밑줄 리소스 이름 지정 시에 사용 합니다.  
  
 **✓ DO** 예외 메시지 리소스에 대 한 다음과 같은 명명 규칙을 사용 합니다.  
  
 예외 형식 이름 및 예외 짧은 식별자 리소스 식별자 여야 합니다.  
  
 `ArgumentExceptionIllegalCharacters`  
 `ArgumentExceptionInvalidName`  
 `ArgumentExceptionFileNameIsMalformed`  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [명명 지침](../../../docs/standard/design-guidelines/naming-guidelines.md)
