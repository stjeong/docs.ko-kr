---
title: '&lt;filterTables&gt;'
ms.date: 03/30/2017
ms.assetid: 41f1ac35-f559-473a-b2c3-8cc83a6a3831
ms.openlocfilehash: d73a3c25dbb4d2de41007149ef5864fcf37ad883
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573061"
---
# <a name="ltfiltertablesgt"></a><span data-ttu-id="030bc-102">&lt;filterTables&gt;</span><span class="sxs-lookup"><span data-stu-id="030bc-102">&lt;filterTables&gt;</span></span>
<span data-ttu-id="030bc-103">필터가 일치할 때 메시지를 보내기 위한 라우팅 필터와 대상 엔드포인트 간의 매핑을 포함하는 라우팅 테이블을 정의하기 위한 구성 섹션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="030bc-103">Represents a configuration section for defining routing tables that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
 <span data-ttu-id="030bc-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="030bc-104">\<system.serviceModel></span></span>  
<span data-ttu-id="030bc-105">\<라우팅 ></span><span class="sxs-lookup"><span data-stu-id="030bc-105">\<routing></span></span>  
<span data-ttu-id="030bc-106">\<routingTables></span><span class="sxs-lookup"><span data-stu-id="030bc-106">\<routingTables></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="030bc-107">구문</span><span class="sxs-lookup"><span data-stu-id="030bc-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="030bc-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="030bc-108">Attributes and Elements</span></span>  
 <span data-ttu-id="030bc-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="030bc-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="030bc-110">특성</span><span class="sxs-lookup"><span data-stu-id="030bc-110">Attributes</span></span>  
 <span data-ttu-id="030bc-111">없음</span><span class="sxs-lookup"><span data-stu-id="030bc-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="030bc-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="030bc-112">Child Elements</span></span>  
  
|<span data-ttu-id="030bc-113">요소</span><span class="sxs-lookup"><span data-stu-id="030bc-113">Element</span></span>|<span data-ttu-id="030bc-114">설명</span><span class="sxs-lookup"><span data-stu-id="030bc-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="030bc-115">\<필터></span><span class="sxs-lookup"><span data-stu-id="030bc-115">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="030bc-116">필터가 일치할 때 메시지를 보내기 위한 라우팅 필터와 대상 엔드포인트 간의 매핑을 포함하는 라우팅 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="030bc-116">A routing table that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="030bc-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="030bc-117">Parent Elements</span></span>  
  
|<span data-ttu-id="030bc-118">요소</span><span class="sxs-lookup"><span data-stu-id="030bc-118">Element</span></span>|<span data-ttu-id="030bc-119">설명</span><span class="sxs-lookup"><span data-stu-id="030bc-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="030bc-120">\<routing></span><span class="sxs-lookup"><span data-stu-id="030bc-120">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="030bc-121">라우팅 필터와 라우팅 테이블을 포함하는 구성 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="030bc-121">A configuration section that contains routing filters and routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="030bc-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="030bc-122">See also</span></span>
- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableCollection?displayProperty=nameWithType>
