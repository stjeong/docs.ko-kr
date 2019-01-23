---
title: 인스턴스
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 1b2801b5df3a5d2ca6d7fd03299ecdf4b7df426a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520275"
---
# <a name="instances"></a><span data-ttu-id="3f7b7-102">인스턴스</span><span class="sxs-lookup"><span data-stu-id="3f7b7-102">Instances</span></span>
<span data-ttu-id="3f7b7-103">카운터 이름: 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7b7-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="3f7b7-104">설명</span><span class="sxs-lookup"><span data-stu-id="3f7b7-104">Description</span></span>  
 <span data-ttu-id="3f7b7-105">현재 서비스에 포함된 인스턴스 컨텍스트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7b7-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="3f7b7-106">대체로 인스턴스 컨텍스트 수는 인스턴스 수와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3f7b7-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="3f7b7-107">그러나 다음 시나리오는 이 규칙의 예외입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7b7-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="3f7b7-108">서비스 메서드가 명시적으로 <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7b7-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="3f7b7-109"><xref:System.ServiceModel.ReleaseInstanceMode>가 <xref:System.ServiceModel.OperationBehaviorAttribute> 인스턴스에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f7b7-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f7b7-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="3f7b7-110">See also</span></span>
- <xref:System.ServiceModel.OperationBehaviorAttribute>
