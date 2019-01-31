---
title: <useManagedPresentation>
ms.date: 03/30/2017
ms.assetid: 17a0dd77-af54-41db-a9d0-4b17ff42878f
ms.openlocfilehash: 1134c4d5f18f60bb2986f4239a788b836fa9113e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55287250"
---
# <a name="usemanagedpresentation"></a><span data-ttu-id="8b54d-101">\<useManagedPresentation></span><span class="sxs-lookup"><span data-stu-id="8b54d-101">\<useManagedPresentation></span></span>
<span data-ttu-id="8b54d-102">WS-Trust의 CardSpace 프로필을 지원하는 CardSpace 보안 토큰 서비스와 통신하는 데 사용되는 바인딩 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="8b54d-102">A binding element used to communicate with a CardSpace Security Token Service that supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="8b54d-103">이 요소는 특성이 없고 빈 스위치로 존재합니다.</span><span class="sxs-lookup"><span data-stu-id="8b54d-103">This element has no attribute and is present as an empty switch.</span></span>  
  
 <span data-ttu-id="8b54d-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="8b54d-104">\<system.serviceModel></span></span>  
<span data-ttu-id="8b54d-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="8b54d-105">\<bindings></span></span>  
<span data-ttu-id="8b54d-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="8b54d-106">\<customBinding></span></span>  
<span data-ttu-id="8b54d-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="8b54d-107">\<binding></span></span>  
<span data-ttu-id="8b54d-108">\<useManagedPresentation></span><span class="sxs-lookup"><span data-stu-id="8b54d-108">\<useManagedPresentation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b54d-109">구문</span><span class="sxs-lookup"><span data-stu-id="8b54d-109">Syntax</span></span>  
  
```xml  
<useManagedPresentation />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8b54d-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="8b54d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="8b54d-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8b54d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8b54d-112">특성</span><span class="sxs-lookup"><span data-stu-id="8b54d-112">Attributes</span></span>  
 <span data-ttu-id="8b54d-113">없음</span><span class="sxs-lookup"><span data-stu-id="8b54d-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="8b54d-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="8b54d-114">Child Elements</span></span>  
 <span data-ttu-id="8b54d-115">없음</span><span class="sxs-lookup"><span data-stu-id="8b54d-115">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8b54d-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="8b54d-116">Parent Elements</span></span>  
  
|<span data-ttu-id="8b54d-117">요소</span><span class="sxs-lookup"><span data-stu-id="8b54d-117">Element</span></span>|<span data-ttu-id="8b54d-118">설명</span><span class="sxs-lookup"><span data-stu-id="8b54d-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8b54d-119">\<binding></span><span class="sxs-lookup"><span data-stu-id="8b54d-119">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="8b54d-120">사용자 지정 바인딩의 모든 바인딩 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="8b54d-120">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8b54d-121">설명</span><span class="sxs-lookup"><span data-stu-id="8b54d-121">Remarks</span></span>  
 <span data-ttu-id="8b54d-122">이 요소는 ID 공급자가 정책에서 WS-Trust의 CardSpace 프로필을 지원함을 나타내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b54d-122">This element is used by an identity provider to express in its policy the fact that it supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="8b54d-123">그러한 정책 어설션을 게시하는 ID 공급자는 해당 CardSpace 프로필을 기반으로 토큰을 발급할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b54d-123">Identity providers that publish such a policy assertion should be able to issue tokens based on that CardSpace profile.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b54d-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="8b54d-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.UseManagedPresentationElement>
- <xref:System.ServiceModel.Channels.UseManagedPresentationBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="8b54d-125">바인딩</span><span class="sxs-lookup"><span data-stu-id="8b54d-125">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="8b54d-126">바인딩 확장</span><span class="sxs-lookup"><span data-stu-id="8b54d-126">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="8b54d-127">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="8b54d-127">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="8b54d-128">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="8b54d-128">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
