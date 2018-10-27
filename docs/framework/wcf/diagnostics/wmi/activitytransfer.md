---
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 936e870c1ec991e2e33acf8a08ccc93975989679
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50034431"
---
# <a name="activitytransfer"></a><span data-ttu-id="e59a7-102">ActivityTransfer</span><span class="sxs-lookup"><span data-stu-id="e59a7-102">ActivityTransfer</span></span>
<span data-ttu-id="e59a7-103">활동 전송 이벤트</span><span class="sxs-lookup"><span data-stu-id="e59a7-103">Activity Transfer Event</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e59a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e59a7-104">Syntax</span></span>  
  
```csharp
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e59a7-105">메서드</span><span class="sxs-lookup"><span data-stu-id="e59a7-105">Methods</span></span>  
 <span data-ttu-id="e59a7-106">ActivityTransfer 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a7-106">The ActivityTransfer class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e59a7-107">속성</span><span class="sxs-lookup"><span data-stu-id="e59a7-107">Properties</span></span>  
 <span data-ttu-id="e59a7-108">ActivityTransfer 클래스에는 다음 속성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a7-108">The ActivityTransfer class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="e59a7-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="e59a7-109">ActivityID</span></span>  
  
-   <span data-ttu-id="e59a7-110">데이터 형식: object</span><span class="sxs-lookup"><span data-stu-id="e59a7-110">Data type: object</span></span>  
    <span data-ttu-id="e59a7-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="e59a7-111">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="e59a7-112">활동 ID</span><span class="sxs-lookup"><span data-stu-id="e59a7-112">Activity ID</span></span>  
  
### <a name="relatedactivityid"></a><span data-ttu-id="e59a7-113">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="e59a7-113">RelatedActivityID</span></span>  
  
-   <span data-ttu-id="e59a7-114">데이터 형식: object</span><span class="sxs-lookup"><span data-stu-id="e59a7-114">Data type: object</span></span>  
    <span data-ttu-id="e59a7-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="e59a7-115">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="e59a7-116">관련 활동 ID</span><span class="sxs-lookup"><span data-stu-id="e59a7-116">Related Activity ID</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e59a7-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e59a7-117">Requirements</span></span>  
  
|<span data-ttu-id="e59a7-118">MOF</span><span class="sxs-lookup"><span data-stu-id="e59a7-118">MOF</span></span>|<span data-ttu-id="e59a7-119">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a7-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e59a7-120">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="e59a7-120">Namespace</span></span>|<span data-ttu-id="e59a7-121">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a7-121">Defined in root\ServiceModel.</span></span>|
