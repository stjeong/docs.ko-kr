---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: 27402017e5e79194578719fd0c921dfc1e047b80
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43407919"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a><span data-ttu-id="916ef-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span><span class="sxs-lookup"><span data-stu-id="916ef-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span></span>
<span data-ttu-id="916ef-103">포이즌 메시지가 거부되었습니다.</span><span class="sxs-lookup"><span data-stu-id="916ef-103">Poison message rejected.</span></span>  
  
## <a name="description"></a><span data-ttu-id="916ef-104">설명</span><span class="sxs-lookup"><span data-stu-id="916ef-104">Description</span></span>  
 <span data-ttu-id="916ef-105">이 추적은 포이즌 메시지가 발생되어 거부되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="916ef-105">The trace indicates that a poison message was encountered and subsequently rejected.</span></span> <span data-ttu-id="916ef-106">이는 NetMsmqBinding 또는 MsmqIntegrationBinding의 `ReceiveErrorHandling` 속성을 `Reject`로 설정할 경우 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="916ef-106">This occurs when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="916ef-107">거부 된 메시지를 보낸 사람에 게 배달 됩니다 [배달 못 한 편지 큐](https://go.microsoft.com/fwlink/?LinkId=99544)합니다.</span><span class="sxs-lookup"><span data-stu-id="916ef-107">A rejected message is delivered back to the sender’s [Dead-Letter Queue](https://go.microsoft.com/fwlink/?LinkId=99544).</span></span>  
  
 <span data-ttu-id="916ef-108">참조 [포이즌 메시지 처리](https://go.microsoft.com/fwlink/?LinkId=99546) 메시지는 포이즌 메시지가 될 경우 및이 적절히 처리 하도록 서비스를 구성 하는 방법에 대 한 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="916ef-108">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkId=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span> <span data-ttu-id="916ef-109">참조 [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) MSMQ에서 거부 된 메시지가 의미 하는 바를 대 한 자세한 내용은 합니다.</span><span class="sxs-lookup"><span data-stu-id="916ef-109">See [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) for more details on what a rejected message means in MSMQ.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="916ef-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="916ef-110">See Also</span></span>  
 [<span data-ttu-id="916ef-111">추적</span><span class="sxs-lookup"><span data-stu-id="916ef-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="916ef-112">추적을 사용하여 응용 프로그램 문제 해결</span><span class="sxs-lookup"><span data-stu-id="916ef-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="916ef-113">관리 및 진단</span><span class="sxs-lookup"><span data-stu-id="916ef-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)  
 [<span data-ttu-id="916ef-114">포이즌 메시지 처리</span><span class="sxs-lookup"><span data-stu-id="916ef-114">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkId=99546)  
 [<span data-ttu-id="916ef-115">MQMarkMessageRejected</span><span class="sxs-lookup"><span data-stu-id="916ef-115">MQMarkMessageRejected</span></span>](https://go.microsoft.com/fwlink/?LinkId=99548)
