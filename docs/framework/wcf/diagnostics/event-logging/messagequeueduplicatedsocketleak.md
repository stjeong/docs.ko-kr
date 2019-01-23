---
title: MessageQueueDuplicatedSocketLeak
ms.date: 03/30/2017
ms.assetid: 9721a463-15d1-43dc-8e3a-cae44448de91
ms.openlocfilehash: 07712104a8dac002d46aee2ba6637bbbc9d850b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532342"
---
# <a name="messagequeueduplicatedsocketleak"></a><span data-ttu-id="88b52-102">MessageQueueDuplicatedSocketLeak</span><span class="sxs-lookup"><span data-stu-id="88b52-102">MessageQueueDuplicatedSocketLeak</span></span>
<span data-ttu-id="88b52-103">ID: 165</span><span class="sxs-lookup"><span data-stu-id="88b52-103">Id: 165</span></span>  
  
 <span data-ttu-id="88b52-104">심각도: Error</span><span class="sxs-lookup"><span data-stu-id="88b52-104">Severity: Error</span></span>  
  
 <span data-ttu-id="88b52-105">범주: SMSvcHost</span><span class="sxs-lookup"><span data-stu-id="88b52-105">Category: SMSvcHost</span></span>  
  
## <a name="description"></a><span data-ttu-id="88b52-106">설명</span><span class="sxs-lookup"><span data-stu-id="88b52-106">Description</span></span>  
 <span data-ttu-id="88b52-107">이 이벤트는 중복 소켓을 발송하는 동안 발생한 오류를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="88b52-107">This event indicates that an error occurred while dispatching a duplicated socket.</span></span> <span data-ttu-id="88b52-108">현재 이 핸들은 프로세스에서 누락됩니다.</span><span class="sxs-lookup"><span data-stu-id="88b52-108">This handle is now leaked in the process.</span></span> <span data-ttu-id="88b52-109">이 이벤트는 소스, 예외, 프로세스 이름 및 프로세스 ID를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="88b52-109">The event lists the Source, Exception, Process Name and Process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88b52-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="88b52-110">See also</span></span>
- [<span data-ttu-id="88b52-111">이벤트 로깅</span><span class="sxs-lookup"><span data-stu-id="88b52-111">Event Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md)
- [<span data-ttu-id="88b52-112">이벤트 일반 참조</span><span class="sxs-lookup"><span data-stu-id="88b52-112">Events General Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/events-general-reference.md)
