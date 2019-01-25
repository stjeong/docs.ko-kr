---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 6491411d8cfe5c7a5a944f3b1cd728c9f0a4b852
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54641215"
---
# <a name="ltclientviagt"></a><span data-ttu-id="514b4-102">&lt;clientVia&gt;</span><span class="sxs-lookup"><span data-stu-id="514b4-102">&lt;clientVia&gt;</span></span>
<span data-ttu-id="514b4-103">전송 채널을 만들어야 하는 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="514b4-103">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="514b4-104">자세한 내용은 <xref:System.ServiceModel.Description.ClientViaBehavior>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="514b4-104">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="514b4-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="514b4-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="514b4-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="514b4-106">\<behaviors></span></span>  
<span data-ttu-id="514b4-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="514b4-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="514b4-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="514b4-108">\<behavior></span></span>  
<span data-ttu-id="514b4-109">\<clientVia></span><span class="sxs-lookup"><span data-stu-id="514b4-109">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="514b4-110">구문</span><span class="sxs-lookup"><span data-stu-id="514b4-110">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="514b4-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="514b4-111">Attributes and Elements</span></span>  
 <span data-ttu-id="514b4-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="514b4-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="514b4-113">특성</span><span class="sxs-lookup"><span data-stu-id="514b4-113">Attributes</span></span>  
  
|<span data-ttu-id="514b4-114">특성</span><span class="sxs-lookup"><span data-stu-id="514b4-114">Attribute</span></span>|<span data-ttu-id="514b4-115">설명</span><span class="sxs-lookup"><span data-stu-id="514b4-115">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="514b4-116">메시지가 이동할 경로를 나타내는 URI를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="514b4-116">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="514b4-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="514b4-117">Child Elements</span></span>  
 <span data-ttu-id="514b4-118">없음</span><span class="sxs-lookup"><span data-stu-id="514b4-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="514b4-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="514b4-119">Parent Elements</span></span>  
  
|<span data-ttu-id="514b4-120">요소</span><span class="sxs-lookup"><span data-stu-id="514b4-120">Element</span></span>|<span data-ttu-id="514b4-121">설명</span><span class="sxs-lookup"><span data-stu-id="514b4-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="514b4-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="514b4-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="514b4-123">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="514b4-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="514b4-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="514b4-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.ClientViaElement>
- <xref:System.ServiceModel.Description.ClientViaBehavior>
