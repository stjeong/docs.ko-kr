---
title: '&lt;항목&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: 8c442990ee736c17b71b625e06d961230a8ceed2
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146435"
---
# <a name="ltentriesgt"></a><span data-ttu-id="8aa0d-102">&lt;항목&gt;</span><span class="sxs-lookup"><span data-stu-id="8aa0d-102">&lt;entries&gt;</span></span>
<span data-ttu-id="8aa0d-103">필터가 일치할 때 메시지를 보내기 위한 라우팅 필터와 대상 엔드포인트 간의 매핑을 포함하는 라우팅 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-103">A routing entry that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="8aa0d-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="8aa0d-104">\<system.serviceModel></span></span>  
<span data-ttu-id="8aa0d-105">\<라우팅 ></span><span class="sxs-lookup"><span data-stu-id="8aa0d-105">\<routing></span></span>  
<span data-ttu-id="8aa0d-106">\<routingTables ></span><span class="sxs-lookup"><span data-stu-id="8aa0d-106">\<routingTables></span></span>  
<span data-ttu-id="8aa0d-107">\<테이블 ></span><span class="sxs-lookup"><span data-stu-id="8aa0d-107">\<table></span></span>  
<span data-ttu-id="8aa0d-108">\<항목 ></span><span class="sxs-lookup"><span data-stu-id="8aa0d-108">\<entries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8aa0d-109">구문</span><span class="sxs-lookup"><span data-stu-id="8aa0d-109">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
    <filterTable name="String">
      <entries>
        <add backupList="String"
             endpointName="String"
             filterName="String"
             priority="Integer" />
      </entries>
    </filterTable>
  </filterTables>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8aa0d-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="8aa0d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="8aa0d-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8aa0d-112">특성</span><span class="sxs-lookup"><span data-stu-id="8aa0d-112">Attributes</span></span>  
 <span data-ttu-id="8aa0d-113">없음</span><span class="sxs-lookup"><span data-stu-id="8aa0d-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8aa0d-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="8aa0d-114">Child Elements</span></span>  
  
|<span data-ttu-id="8aa0d-115">요소</span><span class="sxs-lookup"><span data-stu-id="8aa0d-115">Element</span></span>|<span data-ttu-id="8aa0d-116">설명</span><span class="sxs-lookup"><span data-stu-id="8aa0d-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8aa0d-117">\<필터></span><span class="sxs-lookup"><span data-stu-id="8aa0d-117">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="8aa0d-118">이전에 정의된 클라이언트 엔드포인트에 필터를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-118">Maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="8aa0d-119">이 필터와 일치하는 메시지가 해당 대상으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-119">Messages matching this filter will be sent to this destination.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8aa0d-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="8aa0d-120">Parent Elements</span></span>  
  
|<span data-ttu-id="8aa0d-121">요소</span><span class="sxs-lookup"><span data-stu-id="8aa0d-121">Element</span></span>|<span data-ttu-id="8aa0d-122">설명</span><span class="sxs-lookup"><span data-stu-id="8aa0d-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8aa0d-123">\<라우팅 ></span><span class="sxs-lookup"><span data-stu-id="8aa0d-123">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="8aa0d-124">라우팅 테이블을 포함하는 구성 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-124">A configuration section that contains a routing table.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8aa0d-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8aa0d-125">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>    
