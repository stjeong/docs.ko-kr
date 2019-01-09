---
title: '&lt;serviceTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
ms.openlocfilehash: 4cb4b4ae6fe01430989d9ee5f3d94b16778595aa
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148476"
---
# <a name="ltservicetimeoutsgt"></a><span data-ttu-id="3cafd-102">&lt;serviceTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="3cafd-102">&lt;serviceTimeouts&gt;</span></span>
<span data-ttu-id="3cafd-103">서비스에 대한 제한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cafd-103">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="3cafd-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3cafd-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3cafd-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="3cafd-105">\<behaviors></span></span>  
<span data-ttu-id="3cafd-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="3cafd-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="3cafd-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="3cafd-107">\<behavior></span></span>  
<span data-ttu-id="3cafd-108">\<serviceTimeouts ></span><span class="sxs-lookup"><span data-stu-id="3cafd-108">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cafd-109">구문</span><span class="sxs-lookup"><span data-stu-id="3cafd-109">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="3cafd-110">형식</span><span class="sxs-lookup"><span data-stu-id="3cafd-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3cafd-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="3cafd-111">Attributes and Elements</span></span>  
 <span data-ttu-id="3cafd-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3cafd-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3cafd-113">특성</span><span class="sxs-lookup"><span data-stu-id="3cafd-113">Attributes</span></span>  
  
|<span data-ttu-id="3cafd-114">특성</span><span class="sxs-lookup"><span data-stu-id="3cafd-114">Attribute</span></span>|<span data-ttu-id="3cafd-115">설명</span><span class="sxs-lookup"><span data-stu-id="3cafd-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="3cafd-116">클라이언트에서 서버로 트랜잭션을 전달해야 하는 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3cafd-116">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="3cafd-117">기본값은 "00: 00:00"입니다.</span><span class="sxs-lookup"><span data-stu-id="3cafd-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3cafd-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="3cafd-118">Child Elements</span></span>  
 <span data-ttu-id="3cafd-119">없음</span><span class="sxs-lookup"><span data-stu-id="3cafd-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3cafd-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="3cafd-120">Parent Elements</span></span>  
  
|<span data-ttu-id="3cafd-121">요소</span><span class="sxs-lookup"><span data-stu-id="3cafd-121">Element</span></span>|<span data-ttu-id="3cafd-122">설명</span><span class="sxs-lookup"><span data-stu-id="3cafd-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3cafd-123">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="3cafd-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="3cafd-124">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cafd-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3cafd-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3cafd-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
