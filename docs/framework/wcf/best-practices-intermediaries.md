---
title: '모범 사례: 중간'
ms.date: 03/30/2017
ms.assetid: 2d41b337-8132-4ac2-bea2-6e9ae2f00f8d
ms.openlocfilehash: 8a95bd555e6c1acf896daa77e93d7c735d1f091c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663624"
---
# <a name="best-practices-intermediaries"></a><span data-ttu-id="4d2b0-102">모범 사례: 중간</span><span class="sxs-lookup"><span data-stu-id="4d2b0-102">Best Practices: Intermediaries</span></span>
<span data-ttu-id="4d2b0-103">매개자의 서비스 쪽 채널이 올바르게 닫히도록 하려면 매개자를 호출할 때 오류를 올바르게 처리하도록 주의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-103">Care must be taken to handle faults correctly when calling intermediaries to make sure service side channels on the intermediary are closed properly.</span></span>  
  
 <span data-ttu-id="4d2b0-104">다음과 같은 시나리오를 생각해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-104">Consider the following scenario.</span></span> <span data-ttu-id="4d2b0-105">클라이언트가 매개자를 호출하고 매개자는 백 엔드 서비스를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-105">A client makes a call to an intermediary which then calls a back-end service.</span></span>  <span data-ttu-id="4d2b0-106">백 엔드 서비스는 아무 오류 계약도 정의하지 않으므로, 이 서비스에서 throw되는 모든 오류는 형식화되지 않은 오류로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-106">The back-end service defines no fault contract, so any fault thrown from that service will be treated as an un-typed fault.</span></span>  <span data-ttu-id="4d2b0-107">백 엔드 서비스 throw는 <xref:System.ApplicationException> 를 WCF 서비스 쪽 채널을 잘못 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-107">The back-end service throws an <xref:System.ApplicationException> and WCF correctly aborts the service-side channel.</span></span> <span data-ttu-id="4d2b0-108">그런 다음 <xref:System.ApplicationException>은 매개자에 throw된 <xref:System.ServiceModel.FaultException>으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-108">The <xref:System.ApplicationException> then surfaces as a <xref:System.ServiceModel.FaultException> that is thrown to the intermediary.</span></span> <span data-ttu-id="4d2b0-109">매개자는 <xref:System.ApplicationException>을 다시 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-109">The intermediary re-throws the <xref:System.ApplicationException>.</span></span> <span data-ttu-id="4d2b0-110">WCF는 이를 매개자에서 발생한 형식화되지 않은 오류로 해석하고 이를 클라이언트에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-110">WCF interprets this as an un-typed fault from the intermediary and forwards it on to the client.</span></span> <span data-ttu-id="4d2b0-111">오류를 수신한 매개자와 클라이언트는 클라이언트 쪽 채널에서 오류를 발생시킵니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-111">Upon receiving the fault, both the intermediary and the client fault their client-side channels.</span></span> <span data-ttu-id="4d2b0-112">하지만 WCF에서 이 오류가 치명적인 오류로 인식되지 않기 때문에 매개자의 서비스 쪽 채널은 계속 열린 상태로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-112">The intermediary’s service-side channel however remains open because WCF doesn’t know the fault is fatal.</span></span>  
  
 <span data-ttu-id="4d2b0-113">이 시나리오에서 가장 좋은 방법은 서비스에서 발생한 오류가 치명적인지 확인하고, 치명적인 오류인 경우 다음 코드 조각에 표시된 것처럼 매개자가 해당 서비스 쪽 채널에 오류를 발생시키는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-113">The best practice in this scenario is to detect if the fault coming from the service is fatal and if so the intermediary should fault its service-side channel as shown in the following code snippet.</span></span>  
  
```csharp  
catch (Exception e)  
{  
    bool faulted = service.State == CommunicationState.Faulted;  
    service.Abort();  
    if (faulted)  
    {  
        throw new ApplicationException(e.Message);  
    }  
    else  
    {  
        throw;  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="4d2b0-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="4d2b0-114">See also</span></span>
- [<span data-ttu-id="4d2b0-115">WCF 오류 처리</span><span class="sxs-lookup"><span data-stu-id="4d2b0-115">WCF Error Handling</span></span>](../../../docs/framework/wcf/wcf-error-handling.md)
- [<span data-ttu-id="4d2b0-116">계약 및 서비스에서 오류 지정 및 처리</span><span class="sxs-lookup"><span data-stu-id="4d2b0-116">Specifying and Handling Faults in Contracts and Services</span></span>](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
