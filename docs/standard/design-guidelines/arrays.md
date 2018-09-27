---
title: 배열
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], arrays
- arrays [.NET Framework], usage guidelines
- empty arrays
ms.assetid: 66a1b3d8-6f3f-4715-b235-e1ff95e32d8e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ac7e28c3172f2ed68d402e1d04a1664644c7f25
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47399692"
---
# <a name="arrays"></a>배열
**✓ DO** 공용 Api에서 배열을 통해 컬렉션을 사용 하는 것을 선호 합니다. 합니다 [컬렉션](../../../docs/standard/design-guidelines/guidelines-for-collections.md) 섹션에서는 컬렉션 및 배열 중에서 선택 하는 방법에 대 한 세부 정보를 제공 합니다.  
  
 **X DO NOT** 읽기 전용 배열 필드를 사용 합니다. 필드 자체 읽기 전용 이며 변경할 수 없습니다. 하지만 배열의 요소를 변경할 수 있습니다.  
  
 **✓ CONSIDER** 다차원 배열 대신 가변된 배열을 사용 합니다.  
  
 가변된 배열에 있는 배열 요소를 사용 하 여 배열이입니다. 요소를 구성 하는 배열의 앞에 공간을 절약할 일부 (예: 스파스 행렬) 데이터 집합에 대 한 다차원 배열에 비해 다양 한 일 수 있습니다. 또한 CLR 하므로 일부 시나리오에서는 런타임 성능이 향상을 나타낼 수 있습니다 이러한 가변된 배열에서 인덱스 작업을 최적화 합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*  
  
## <a name="see-also"></a>참고자료

- <xref:System.Array>  
- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [사용 지침](../../../docs/standard/design-guidelines/usage-guidelines.md)
