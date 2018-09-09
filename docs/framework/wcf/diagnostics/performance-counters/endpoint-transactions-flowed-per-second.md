---
title: '엔드포인트: Transactions Flowed Per Second'
ms.date: 03/30/2017
ms.assetid: 0f370ff1-a913-450b-bccb-c279ad165b3d
ms.openlocfilehash: 79f50b6706facd040ec2d325c676f210d5327bf8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44227144"
---
# <a name="endpoint-transactions-flowed-per-second"></a>엔드포인트: Transactions Flowed Per Second
카운터 이름: Transactions Flowed Per Second  
  
## <a name="description"></a>설명  
 이 엔드포인트에서 작업에 적용된 초당 트랜잭션의 수입니다. 엔드포인트에 전송된 메시지에 트랜잭션 ID가 있을 때마다 이 카운터가 증가합니다.  
  
 이 카운터는 성능 카운터 형식 [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), 값은 다음 수식을 사용 하 여 계산 됩니다.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
