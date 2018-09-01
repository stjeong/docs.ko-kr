---
title: Instances Per Second
ms.date: 03/30/2017
ms.assetid: 74579397-1058-4278-80cf-2d00854a480f
ms.openlocfilehash: f0797c38a5eb7399817eaf6aad9fb5b6ecbfab89
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43387909"
---
# <a name="instances-per-second"></a>Instances Per Second
카운터 이름: Instances Created Per Second  
  
## <a name="description"></a>설명  
 초당 만들어진 총 서비스 인스턴스 수입니다.  
  
 이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
