---
title: 상관 관계
ms.date: 03/30/2017
ms.assetid: 60151f6c-19b7-47af-9cdc-76c2ac95f301
ms.openlocfilehash: e72f462a9b8777fbeadb306c7fea8354f64ffe8c
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216580"
---
# <a name="correlation"></a><span data-ttu-id="11ffd-102">상관 관계</span><span class="sxs-lookup"><span data-stu-id="11ffd-102">Correlation</span></span>
<span data-ttu-id="11ffd-103">워크플로 서비스 응용 프로그램이 다른 서비스와 통신할 때는 둘 사이의 메시지가 적절한 워크플로 인스턴스에 디스패치되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-103">When workflow service applications communicate with other services, it is important that messages between them are dispatched to the appropriate workflow instance.</span></span> <span data-ttu-id="11ffd-104">상관 관계는 이를 위한 메커니즘을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-104">Correlation provides the mechanism for this.</span></span> <span data-ttu-id="11ffd-105">이 단원의 항목에서는 상관 관계의 개요를 제공하고 다양한 워크플로 서비스 시나리오에서 상관 관계를 사용하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-105">The topics in this section provide an overview of correlation and how to use it in different workflow service scenarios.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="11ffd-106">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="11ffd-106">In This Section</span></span>  
 [<span data-ttu-id="11ffd-107">상관 관계 개요</span><span class="sxs-lookup"><span data-stu-id="11ffd-107">Correlation Overview</span></span>](../../../../docs/framework/wcf/feature-details/correlation-overview.md)  
 <span data-ttu-id="11ffd-108">[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)]에서 사용할 수 있는 상관 관계의 형식에 대해 간략하게 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-108">Provides an overview of the types of correlation available in [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)].</span></span>  
  
 [<span data-ttu-id="11ffd-109">영속 이중</span><span class="sxs-lookup"><span data-stu-id="11ffd-109">Durable Duplex</span></span>](../../../../docs/framework/wcf/feature-details/durable-duplex-correlation.md)  
 <span data-ttu-id="11ffd-110">영속 이중 상관 관계에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-110">Describes durable duplex correlation.</span></span>
  
 [<span data-ttu-id="11ffd-111">요청-회신</span><span class="sxs-lookup"><span data-stu-id="11ffd-111">Request-Reply</span></span>](../../../../docs/framework/wcf/feature-details/request-reply-correlation.md)  
 <span data-ttu-id="11ffd-112">요청-회신 상관 관계에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-112">Describes request-reply correlation.</span></span>  
  
 [<span data-ttu-id="11ffd-113">상관 관계 문제 해결</span><span class="sxs-lookup"><span data-stu-id="11ffd-113">Troubleshooting Correlation</span></span>](../../../../docs/framework/wcf/feature-details/troubleshooting-correlation.md)  
 <span data-ttu-id="11ffd-114">상관 관계 문제를 해결하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="11ffd-114">Provides methods for troubleshooting correlation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11ffd-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="11ffd-115">See Also</span></span>  
 <xref:System.ServiceModel.Activities.CorrelationHandle>  
 <xref:System.ServiceModel.Activities.Send>  
 <xref:System.ServiceModel.Activities.Receive>  
 <xref:System.ServiceModel.CorrelationQuery>  
 [<span data-ttu-id="11ffd-116">내용 기반 상관 관계</span><span class="sxs-lookup"><span data-stu-id="11ffd-116">Content-Based Correlation</span></span>](../../../../docs/framework/windows-workflow-foundation/samples/content-based-correlation.md)  
 [<span data-ttu-id="11ffd-117">상호 관련된 계산기</span><span class="sxs-lookup"><span data-stu-id="11ffd-117">Correlated Calculator</span></span>](../../../../docs/framework/windows-workflow-foundation/samples/correlated-calculator.md)
