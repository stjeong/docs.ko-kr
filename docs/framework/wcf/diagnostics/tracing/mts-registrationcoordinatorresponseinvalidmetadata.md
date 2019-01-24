---
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorResponseInvalidMetadata
ms.date: 03/30/2017
ms.assetid: a174bbf5-0ffe-4fda-969d-e7fbd1996123
ms.openlocfilehash: 3bc093e6f348243932f64dd454643ae214a69713
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589440"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorresponseinvalidmetadata"></a><span data-ttu-id="093fa-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorResponseInvalidMetadata</span><span class="sxs-lookup"><span data-stu-id="093fa-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorResponseInvalidMetadata</span></span>
<span data-ttu-id="093fa-103">WS-Atomic Transaction 프로토콜 서비스에서 잘못되었거나 호환되지 않는 메타데이터가 있는 엔드포인트 참조를 포함한 RegisterResponse 메시지를 코디네이터로부터 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-103">The WS-Atomic Transaction protocol service received a RegisterResponse message from its coordinator that contains an endpoint reference with invalid or incompatible metadata.</span></span>  
  
## <a name="description"></a><span data-ttu-id="093fa-104">설명</span><span class="sxs-lookup"><span data-stu-id="093fa-104">Description</span></span>  
 <span data-ttu-id="093fa-105">로컬 트랜잭션 관리자에서 상위 트랜잭션 관리자에 등록하려고 하는 경우 상위에서 RegisterResponse 메시지에 잘못된 주소를 반환하면 추적됩니다.</span><span class="sxs-lookup"><span data-stu-id="093fa-105">Traced when the local Transaction Manager tries to register with its superior Transaction Manager and the superior returns an invalid address within the RegisterResponse message.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="093fa-106">참고자료</span><span class="sxs-lookup"><span data-stu-id="093fa-106">See also</span></span>
- [<span data-ttu-id="093fa-107">추적</span><span class="sxs-lookup"><span data-stu-id="093fa-107">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="093fa-108">추적을 사용하여 애플리케이션 문제 해결</span><span class="sxs-lookup"><span data-stu-id="093fa-108">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="093fa-109">관리 및 진단</span><span class="sxs-lookup"><span data-stu-id="093fa-109">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
