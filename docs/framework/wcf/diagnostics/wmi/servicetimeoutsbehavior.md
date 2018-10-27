---
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 1a5284915de739e95325234318842a4d1ab607be
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/26/2018
ms.locfileid: "50135247"
---
# <a name="servicetimeoutsbehavior"></a><span data-ttu-id="0b816-102">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="0b816-102">ServiceTimeoutsBehavior</span></span>
<span data-ttu-id="0b816-103">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="0b816-103">ServiceTimeoutsBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b816-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b816-104">Syntax</span></span>  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0b816-105">메서드</span><span class="sxs-lookup"><span data-stu-id="0b816-105">Methods</span></span>  
 <span data-ttu-id="0b816-106">ServiceTimeoutsBehavior 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b816-106">The ServiceTimeoutsBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0b816-107">속성</span><span class="sxs-lookup"><span data-stu-id="0b816-107">Properties</span></span>  
 <span data-ttu-id="0b816-108">ServiceTimeoutsBehavior 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b816-108">The ServiceTimeoutsBehavior class has the following property:</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="0b816-109">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="0b816-109">TransactionTimeout</span></span>  
 <span data-ttu-id="0b816-110">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="0b816-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="0b816-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="0b816-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0b816-112">트랜잭션을 완료해야 하는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="0b816-112">The period within which a transaction must complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b816-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="0b816-113">Requirements</span></span>  
  
|<span data-ttu-id="0b816-114">MOF</span><span class="sxs-lookup"><span data-stu-id="0b816-114">MOF</span></span>|<span data-ttu-id="0b816-115">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b816-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0b816-116">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="0b816-116">Namespace</span></span>|<span data-ttu-id="0b816-117">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b816-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0b816-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0b816-118">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
