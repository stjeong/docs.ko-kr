---
title: '&lt;resolver&gt;'
ms.date: 03/30/2017
ms.assetid: 0c00200c-f135-4e5c-a024-76b72bcbc021
ms.openlocfilehash: 48b6b6ca315f7ab63a8f7a64b97167fa04fe1e4e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44180802"
---
# <a name="ltresolvergt"></a><span data-ttu-id="f001a-102">&lt;resolver&gt;</span><span class="sxs-lookup"><span data-stu-id="f001a-102">&lt;resolver&gt;</span></span>
<span data-ttu-id="f001a-103">피어 메시 ID를 확인하는 데 사용되는 피어 확인자를 메시에 참여하는 몇 개의 노드를 나타내는 피어 노드 주소 집합에 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-103">Specifies a peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>  
  
 <span data-ttu-id="f001a-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f001a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f001a-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="f001a-105">\<bindings></span></span>  
<span data-ttu-id="f001a-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="f001a-106">\<netPeerBinding></span></span>  
<span data-ttu-id="f001a-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="f001a-107">\<binding></span></span>  
<span data-ttu-id="f001a-108">\<resolver></span><span class="sxs-lookup"><span data-stu-id="f001a-108">\<resolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f001a-109">구문</span><span class="sxs-lookup"><span data-stu-id="f001a-109">Syntax</span></span>  
  
```xml  
<resolver mode="Auto/Custom/Pnrp"  
   referralPolicy="DoNotShare/Service/Share">  
</resolver>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f001a-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="f001a-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f001a-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f001a-112">특성</span><span class="sxs-lookup"><span data-stu-id="f001a-112">Attributes</span></span>  
  
|<span data-ttu-id="f001a-113">특성</span><span class="sxs-lookup"><span data-stu-id="f001a-113">Attribute</span></span>|<span data-ttu-id="f001a-114">설명</span><span class="sxs-lookup"><span data-stu-id="f001a-114">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="f001a-115">이 서비스와 연결된 피어 확인자 인스턴스가 PNRP 관련 사용자 지정 확인자인지 아니면 자동으로 결정되는지 여부를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-115">A string that specifies whether the peer resolver instance associated with this service is either PNRP-specific, a custom resolver, or automatically determined.</span></span> <span data-ttu-id="f001a-116">이 특성은 <xref:System.ServiceModel.PeerResolvers.PeerResolverMode> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-116">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span></span>|  
|`referralPolicy`|<span data-ttu-id="f001a-117">피어 간에 조회를 공유하는 방법을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-117">A string that specifies the way referrals are shared among peers.</span></span> <span data-ttu-id="f001a-118">이 특성은 <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-118">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f001a-119">자식 요소</span><span class="sxs-lookup"><span data-stu-id="f001a-119">Child Elements</span></span>  
  
|<span data-ttu-id="f001a-120">요소</span><span class="sxs-lookup"><span data-stu-id="f001a-120">Element</span></span>|<span data-ttu-id="f001a-121">설명</span><span class="sxs-lookup"><span data-stu-id="f001a-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f001a-122">\<headers></span><span class="sxs-lookup"><span data-stu-id="f001a-122">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="f001a-123">사용자 지정 피어 확인자 서비스의 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-123">Specifies settings for a custom peer resolver service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f001a-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="f001a-124">Parent Elements</span></span>  
  
|<span data-ttu-id="f001a-125">요소</span><span class="sxs-lookup"><span data-stu-id="f001a-125">Element</span></span>|<span data-ttu-id="f001a-126">설명</span><span class="sxs-lookup"><span data-stu-id="f001a-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f001a-127">\<binding></span><span class="sxs-lookup"><span data-stu-id="f001a-127">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="f001a-128">모든 바인딩 기능을 정의 합니다 [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-128">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f001a-129">설명</span><span class="sxs-lookup"><span data-stu-id="f001a-129">Remarks</span></span>  
 <span data-ttu-id="f001a-130">피어 이름 확인자는 피어 메시에 참여하는 피어 노드를 찾기 위해 피어 채널에서 사용하는 검색 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-130">A peer name resolver is a discovery service used by peer channels to find peer nodes that participate in a peer mesh.</span></span> <span data-ttu-id="f001a-131">또한 이 확인자는 피어 노드가 알려지고 피어 메시에서 사용할 수 있게 되는 메커니즘인 피어 메시를 통해 노드를 "등록"하는 데에도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-131">It is also used to "register" a node with a peer mesh, the mechanism by which the peer node becomes known and available from the peer mesh.</span></span> <span data-ttu-id="f001a-132">피어 확인자에 대 한 자세한 내용은 참조 하세요. [피어 확인 자의](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="f001a-132">For more information on peer resolvers, see [Peer Resolvers](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f001a-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f001a-133">See Also</span></span>  
 <xref:System.ServiceModel.PeerResolver>  
 <xref:System.ServiceModel.PeerResolvers.PeerResolverSettings>  
 <xref:System.ServiceModel.NetPeerTcpBinding.Resolver%2A>  
 <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Resolver%2A>  
 <xref:System.ServiceModel.Configuration.PeerResolverElement>  
 [<span data-ttu-id="f001a-134">피어 확인자</span><span class="sxs-lookup"><span data-stu-id="f001a-134">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)  
 [<span data-ttu-id="f001a-135">PeerChannel 응용 프로그램에 사용자 지정 확인자 추가</span><span class="sxs-lookup"><span data-stu-id="f001a-135">Adding a Custom Resolver to a PeerChannel Application</span></span>](https://msdn.microsoft.com/library/12aa3787-2962-439c-ad27-46523c8b0419)
