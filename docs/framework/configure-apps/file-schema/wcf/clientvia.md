---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 48e56b79f47e84122ddd4d7f55d50044510bfa66
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149061"
---
# <a name="ltclientviagt"></a><span data-ttu-id="53cfd-102">&lt;clientVia&gt;</span><span class="sxs-lookup"><span data-stu-id="53cfd-102">&lt;clientVia&gt;</span></span>
<span data-ttu-id="53cfd-103">전송 채널을 만들어야 하는 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53cfd-103">Specifies the URI for which the transport channel should be created.</span></span> <span data-ttu-id="53cfd-104">자세한 내용은 <xref:System.ServiceModel.Description.ClientViaBehavior>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="53cfd-104">For more information, see <xref:System.ServiceModel.Description.ClientViaBehavior>.</span></span>  
  
 <span data-ttu-id="53cfd-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="53cfd-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="53cfd-106">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="53cfd-106">\<behaviors></span></span>  
<span data-ttu-id="53cfd-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="53cfd-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="53cfd-108">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="53cfd-108">\<behavior></span></span>  
<span data-ttu-id="53cfd-109">\<clientVia ></span><span class="sxs-lookup"><span data-stu-id="53cfd-109">\<clientVia></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53cfd-110">구문</span><span class="sxs-lookup"><span data-stu-id="53cfd-110">Syntax</span></span>  
  
```xml  
<clientVia viaUri="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="53cfd-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="53cfd-111">Attributes and Elements</span></span>  
 <span data-ttu-id="53cfd-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="53cfd-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="53cfd-113">특성</span><span class="sxs-lookup"><span data-stu-id="53cfd-113">Attributes</span></span>  
  
|<span data-ttu-id="53cfd-114">특성</span><span class="sxs-lookup"><span data-stu-id="53cfd-114">Attribute</span></span>|<span data-ttu-id="53cfd-115">설명</span><span class="sxs-lookup"><span data-stu-id="53cfd-115">Description</span></span>|  
|---------------|-----------------|  
|`viaUri`|<span data-ttu-id="53cfd-116">메시지가 이동할 경로를 나타내는 URI를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="53cfd-116">A string that specifies a URI that indicates the route a message should take.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="53cfd-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="53cfd-117">Child Elements</span></span>  
 <span data-ttu-id="53cfd-118">없음</span><span class="sxs-lookup"><span data-stu-id="53cfd-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="53cfd-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="53cfd-119">Parent Elements</span></span>  
  
|<span data-ttu-id="53cfd-120">요소</span><span class="sxs-lookup"><span data-stu-id="53cfd-120">Element</span></span>|<span data-ttu-id="53cfd-121">설명</span><span class="sxs-lookup"><span data-stu-id="53cfd-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="53cfd-122">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="53cfd-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="53cfd-123">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53cfd-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="53cfd-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="53cfd-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ClientViaElement>  
 <xref:System.ServiceModel.Description.ClientViaBehavior>
