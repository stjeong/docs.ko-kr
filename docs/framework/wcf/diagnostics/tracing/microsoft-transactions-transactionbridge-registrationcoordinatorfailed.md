---
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed
ms.date: 03/30/2017
ms.assetid: 96474056-0418-41e4-8c75-bbc0a853eaba
ms.openlocfilehash: 5c8592ac34375445964b3dbcbbd4800c47e53850
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515052"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfailed"></a><span data-ttu-id="cc075-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span><span class="sxs-lookup"><span data-stu-id="cc075-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span></span>
<span data-ttu-id="cc075-103">WS-AT 프로토콜 서비스가 코디네이터에게 Register 메시지를 보내지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="cc075-103">The WS-AT protocol service failed to send a Register message to its coordinator</span></span>  
  
## <a name="description"></a><span data-ttu-id="cc075-104">설명</span><span class="sxs-lookup"><span data-stu-id="cc075-104">Description</span></span>  
 <span data-ttu-id="cc075-105">로컬 TransactionManager가 메시지를 보낼 수 없기 때문에 상위 TransactionManager를 등록할 수 없는 경우 추적됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc075-105">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to the inability to send a message.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="cc075-106">문제 해결</span><span class="sxs-lookup"><span data-stu-id="cc075-106">Troubleshooting</span></span>  
 <span data-ttu-id="cc075-107">메시지 보내기 오류의 원인인 예외에 대한 추적 메시지를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="cc075-107">Inspect the trace message for the exception causing the message send failure</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc075-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="cc075-108">See also</span></span>
- [<span data-ttu-id="cc075-109">추적</span><span class="sxs-lookup"><span data-stu-id="cc075-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="cc075-110">추적을 사용하여 애플리케이션 문제 해결</span><span class="sxs-lookup"><span data-stu-id="cc075-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="cc075-111">관리 및 진단</span><span class="sxs-lookup"><span data-stu-id="cc075-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
