---
title: 신뢰할 수 있는 세션
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 1d87f6f4d94763dc8f6ac7e929c22b17940097ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735427"
---
# <a name="reliable-sessions"></a>신뢰할 수 있는 세션

이 섹션에서는 무엇을 Windows Communication Foundation (WCF) 신뢰할 수 있는 세션, 용도, 방법 및 경우 하나를 사용 하려면 바인딩 구성, 지원 및 모범 사례에 대 한 포인터를 설명 합니다. 다음 표에서는 이 단원의 필수 사항 및 관련 항목에 대한 세부 정보를 요약하여 설명합니다.

신뢰할 수 있는 세션 WCF 끝점 간에 보내진 메시지가 SOAP 또는 전송 매개 자를 통해 전송 되 고 전송 된 동일한 순서로 한 번만 있고, 선택적으로 배달 하는 기능을 제공 합니다.

WCF 응용 프로그램에서 신뢰할 수 있는 세션을 사용 하려면 기본적으로 또는 필요에 따라 신뢰할 수 있는 세션을 지 원하는 WCF의 시스템 제공 바인딩 중 하나를 사용 하거나 세션을 지 원하는 고유한 사용자 지정 바인딩을 만듭니다.

## <a name="in-this-section"></a>섹션 내용

[신뢰할 수 있는 세션 개요](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md)   
신뢰할 수 있는 세션, 사용 시기, 신뢰할 수 있는 세션을 지원하는 다른 바인딩 및 그러한 바인딩의 작동 방식에 대해 설명합니다.

[방법: 신뢰할 수 있는 세션 내에서 메시지 교환](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md)   
구성에 지정된 사용자 지정 바인딩을 사용하여 HTTP를 통해 신뢰할 수 있는 세션을 만드는 방법에 대해 설명합니다.

[방법: 신뢰할 수 있는 세션 내에서 메시지 보안](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md)   
신뢰할 수 있는 세션의 보안을 유지하는 방법에 대해 설명합니다.

[방법: HTTPS를 사용 하 여 사용자 지정 신뢰할 수 있는 세션 바인딩 만들기](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md)   
HTTPS를 통해 신뢰할 수 있는 세션을 만드는 방법에 대해 설명합니다.

[신뢰할 수 있는 세션에 대 한 모범 사례](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md)   
신뢰할 수 있는 세션 사용과 관련된 몇 가지 최선의 방법에 대해 설명합니다.

## <a name="reference"></a>참조

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a>참고자료

- [큐 및 신뢰할 수 있는 세션](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
- [세션, 인스턴스 및 동시성](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
