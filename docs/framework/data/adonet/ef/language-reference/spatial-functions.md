---
title: 공간 함수
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: ad6b722e84aae40354e30434b107752d02352645
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43776949"
---
# <a name="spatial-functions"></a>공간 함수
공간 형식의 경우 리터럴 형식이 없습니다. 그러나 WKT(Well Known Text) 형식의 문자열을 사용하여 호출하는 정식 Entity Framework 함수를 사용할 수 있습니다. 예를 들어 다음 함수 호출은 기하 도형 점을 만듭니다.  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 합니다 [SpatialEdmFunctions 메서드](https://msdn.microsoft.com/library/hh749531.aspx) 페이지에는 모든 공간 정식 Entity Framework 메서드가 나열 합니다. 함수에 전달해야 하는 매개 변수를 보려면 해당 메서드를 클릭하세요.
