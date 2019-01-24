---
title: '&lt;pnrpPeerResolver&gt;'
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: cefd46d7810149264f9c431a212da0f3f51f8186
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577648"
---
# <a name="ltpnrppeerresolvergt"></a><span data-ttu-id="c9409-102">&lt;pnrpPeerResolver&gt;</span><span class="sxs-lookup"><span data-stu-id="c9409-102">&lt;pnrpPeerResolver&gt;</span></span>
<span data-ttu-id="c9409-103">PNRP(피어 이름 확인 프로토콜)가 확인자로 사용되도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-103">Specifies that the PNRP (Peer Name Resolution Protocol) resolver is to be used as a resolver.</span></span> <span data-ttu-id="c9409-104">PNRP가 기본 확인자이므로 이 요소는 선택적입니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-104">This element is optional because PNRP is the default resolver.</span></span>  
  
 <span data-ttu-id="c9409-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="c9409-105">\<system.serviceModel></span></span>  
<span data-ttu-id="c9409-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="c9409-106">\<bindings></span></span>  
<span data-ttu-id="c9409-107">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="c9409-107">\<customBinding></span></span>  
<span data-ttu-id="c9409-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="c9409-108">\<binding></span></span>  
<span data-ttu-id="c9409-109">\<pnrpResolver></span><span class="sxs-lookup"><span data-stu-id="c9409-109">\<pnrpResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9409-110">구문</span><span class="sxs-lookup"><span data-stu-id="c9409-110">Syntax</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c9409-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="c9409-111">Attributes and Elements</span></span>  
 <span data-ttu-id="c9409-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c9409-113">특성</span><span class="sxs-lookup"><span data-stu-id="c9409-113">Attributes</span></span>  
  
|<span data-ttu-id="c9409-114">특성</span><span class="sxs-lookup"><span data-stu-id="c9409-114">Attribute</span></span>|<span data-ttu-id="c9409-115">설명</span><span class="sxs-lookup"><span data-stu-id="c9409-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c9409-116">resolverType</span><span class="sxs-lookup"><span data-stu-id="c9409-116">resolverType</span></span>|<span data-ttu-id="c9409-117">사용할 확인자를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-117">A string that specifies the resolver to be used.</span></span> <span data-ttu-id="c9409-118">이 특성은 선택적 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-118">This attribute is optional.</span></span> <span data-ttu-id="c9409-119">이 특성을 설정하지 않거나 빈 문자열로 설정하면 PNRP가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-119">If it is not set, or if it is set to an empty string, PNRP is used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c9409-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="c9409-120">Child Elements</span></span>  
 <span data-ttu-id="c9409-121">없음</span><span class="sxs-lookup"><span data-stu-id="c9409-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c9409-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="c9409-122">Parent Elements</span></span>  
  
|<span data-ttu-id="c9409-123">요소</span><span class="sxs-lookup"><span data-stu-id="c9409-123">Element</span></span>|<span data-ttu-id="c9409-124">설명</span><span class="sxs-lookup"><span data-stu-id="c9409-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c9409-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="c9409-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="c9409-126">사용자 지정 바인딩의 모든 바인딩 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c9409-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c9409-127">예제</span><span class="sxs-lookup"><span data-stu-id="c9409-127">Example</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="see-also"></a><span data-ttu-id="c9409-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="c9409-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>
- <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="c9409-129">바인딩</span><span class="sxs-lookup"><span data-stu-id="c9409-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="c9409-130">바인딩 확장</span><span class="sxs-lookup"><span data-stu-id="c9409-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="c9409-131">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="c9409-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="c9409-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="c9409-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="c9409-133">피어 확인자</span><span class="sxs-lookup"><span data-stu-id="c9409-133">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
