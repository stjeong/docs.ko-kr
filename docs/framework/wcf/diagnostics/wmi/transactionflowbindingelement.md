---
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: 027ace6ea9fc2a0e5ce63efa84e1a49c0ed2cd0a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188029"
---
# <a name="transactionflowbindingelement"></a>TransactionFlowBindingElement
TransactionFlowBindingElement  
  
## <a name="syntax"></a>구문  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a>메서드  
 TransactionFlowBindingElement 클래스는 메서드를 정의하지 않습니다.  
  
## <a name="properties"></a>속성  
 TransactionFlowBindingElement 클래스에는 다음과 같은 속성이 있습니다.  
  
### <a name="issuedtokens"></a>IssuedTokens  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 발급된 보안 토큰 헤더(WS-Trust의 IssuedTokens)의 요구 사항을 지정합니다.  
  
### <a name="transactionprotocol"></a>TransactionProtocol  
 데이터 형식: string  
  
 액세스 형식: 읽기 전용  
  
 서비스에서 트랜잭션을 이동하는 데 사용하는 트랜잭션 프로토콜입니다.  
  
### <a name="transactions"></a>트랜잭션  
 데이터 형식: boolean  
  
 액세스 형식: 읽기 전용  
  
 들어오는 트랜잭션이 지원되는지 여부를 나타냅니다.  
  
## <a name="requirements"></a>요구 사항  
  
|MOF|Servicemodel.mof에 선언되어 있습니다.|  
|---------|-----------------------------------|  
|네임스페이스|root\ServiceModel에 정의되어 있습니다.|  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
