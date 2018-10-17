---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: edc154fcce0058455f1376a2a45807c92f7f2457
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373705"
---
# <a name="servicethrottlingbehavior"></a><span data-ttu-id="445c7-102">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="445c7-102">ServiceThrottlingBehavior</span></span>
<span data-ttu-id="445c7-103">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="445c7-103">ServiceThrottlingBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="445c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="445c7-104">Syntax</span></span>  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="445c7-105">메서드</span><span class="sxs-lookup"><span data-stu-id="445c7-105">Methods</span></span>  
 <span data-ttu-id="445c7-106">ServiceThrottlingBehavior 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-106">The ServiceThrottlingBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="445c7-107">속성</span><span class="sxs-lookup"><span data-stu-id="445c7-107">Properties</span></span>  
 <span data-ttu-id="445c7-108">ServiceThrottlingBehavior 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-108">The ServiceThrottlingBehavior class has the following properties:</span></span>  
  
### <a name="maxconcurrentcalls"></a><span data-ttu-id="445c7-109">MaxConcurrentCalls</span><span class="sxs-lookup"><span data-stu-id="445c7-109">MaxConcurrentCalls</span></span>  
 <span data-ttu-id="445c7-110">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="445c7-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="445c7-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="445c7-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="445c7-112">ServiceHost의 모든 디스패처 개체에서 동시에 처리하는 최대 메시지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-112">The maximum number of messages actively processing across all dispatcher objects in a ServiceHost.</span></span>  
  
### <a name="maxconcurrentinstances"></a><span data-ttu-id="445c7-113">MaxConcurrentInstances</span><span class="sxs-lookup"><span data-stu-id="445c7-113">MaxConcurrentInstances</span></span>  
 <span data-ttu-id="445c7-114">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="445c7-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="445c7-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="445c7-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="445c7-116">한 번에 실행할 수 있는 최대 서비스 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-116">The maximum number of service objects that can execute at one time.</span></span>  
  
### <a name="maxconcurrentsessions"></a><span data-ttu-id="445c7-117">MaxConcurrentSessions</span><span class="sxs-lookup"><span data-stu-id="445c7-117">MaxConcurrentSessions</span></span>  
 <span data-ttu-id="445c7-118">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="445c7-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="445c7-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="445c7-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="445c7-120">호스트가 한 번에 수락할 수 있는 최대 세션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-120">The maximum number of sessions a host can accept at one time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="445c7-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="445c7-121">Requirements</span></span>  
  
|<span data-ttu-id="445c7-122">MOF</span><span class="sxs-lookup"><span data-stu-id="445c7-122">MOF</span></span>|<span data-ttu-id="445c7-123">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="445c7-124">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="445c7-124">Namespace</span></span>|<span data-ttu-id="445c7-125">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="445c7-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="445c7-126">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
