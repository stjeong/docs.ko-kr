---
title: System.ServiceModel.MessageClosedAgain
ms.date: 03/30/2017
ms.assetid: 24c274d4-65cd-4c91-9869-bc6eb34ef979
ms.openlocfilehash: bcac4683655476c6aa868232b0483336b815b6cc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54705984"
---
# <a name="systemservicemodelmessageclosedagain"></a><span data-ttu-id="0b9f7-102">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="0b9f7-102">System.ServiceModel.MessageClosedAgain</span></span>
<span data-ttu-id="0b9f7-103">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="0b9f7-103">System.ServiceModel.MessageClosedAgain</span></span>  
  
## <a name="description"></a><span data-ttu-id="0b9f7-104">설명</span><span class="sxs-lookup"><span data-stu-id="0b9f7-104">Description</span></span>  
 <span data-ttu-id="0b9f7-105">메시지가 다시 닫혔습니다.</span><span class="sxs-lookup"><span data-stu-id="0b9f7-105">A message was closed again.</span></span>  
  
 <span data-ttu-id="0b9f7-106">메시지는 한 번만 닫혀야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9f7-106">A message should be closed only once.</span></span> <span data-ttu-id="0b9f7-107">사용자 확장 코드에서 이 추적을 내보낸다는 것은 사용자 확장 코드가 이미 닫힌 메시지를 닫고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0b9f7-107">If this trace is being emitted in user extension code, it indicates that the user extension code is closing a message that has already been closed.</span></span> <span data-ttu-id="0b9f7-108">제품 코드를 통해 이 추적을 내보낸다는 것은 사용자 확장명 코드가 메시지를 너무 일찍 닫을 가능성이 있다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0b9f7-108">If this trace is being emitted through product code, it indicates that the user extension code could potentially be closing a message too early.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b9f7-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="0b9f7-109">See also</span></span>
- [<span data-ttu-id="0b9f7-110">추적</span><span class="sxs-lookup"><span data-stu-id="0b9f7-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="0b9f7-111">추적을 사용하여 애플리케이션 문제 해결</span><span class="sxs-lookup"><span data-stu-id="0b9f7-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="0b9f7-112">관리 및 진단</span><span class="sxs-lookup"><span data-stu-id="0b9f7-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
