---
title: <persistenceProvider>
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: 054991687a54ecbf95cc18f58717a4ed3e36f050
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260803"
---
# <a name="persistenceprovider"></a><span data-ttu-id="cd444-101">\<persistenceProvider></span><span class="sxs-lookup"><span data-stu-id="cd444-101">\<persistenceProvider></span></span>
<span data-ttu-id="cd444-102">사용할 지속성 공급자 구현 형식 및 지속성 작업에 사용할 제한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-102">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="cd444-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="cd444-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="cd444-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="cd444-104">\<behaviors></span></span>  
<span data-ttu-id="cd444-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="cd444-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="cd444-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cd444-106">\<behavior></span></span>  
<span data-ttu-id="cd444-107">\<persistenceProvider></span><span class="sxs-lookup"><span data-stu-id="cd444-107">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd444-108">구문</span><span class="sxs-lookup"><span data-stu-id="cd444-108">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cd444-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="cd444-109">Attributes and Elements</span></span>  
 <span data-ttu-id="cd444-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cd444-111">특성</span><span class="sxs-lookup"><span data-stu-id="cd444-111">Attributes</span></span>  
  
|<span data-ttu-id="cd444-112">특성</span><span class="sxs-lookup"><span data-stu-id="cd444-112">Attribute</span></span>|<span data-ttu-id="cd444-113">설명</span><span class="sxs-lookup"><span data-stu-id="cd444-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cd444-114">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="cd444-114">persistenceOperationTimeout</span></span>|<span data-ttu-id="cd444-115">지속성 작업에 사용되는 제한 시간을 지정하는 <xref:System.TimeSpan> 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-115">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="cd444-116">기본값은 "00: 00:30"입니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-116">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="cd444-117">형식</span><span class="sxs-lookup"><span data-stu-id="cd444-117">type</span></span>|<span data-ttu-id="cd444-118">사용할 지속성 공급자 팩터리의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-118">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cd444-119">자식 요소</span><span class="sxs-lookup"><span data-stu-id="cd444-119">Child Elements</span></span>  
 <span data-ttu-id="cd444-120">없음</span><span class="sxs-lookup"><span data-stu-id="cd444-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cd444-121">부모 요소</span><span class="sxs-lookup"><span data-stu-id="cd444-121">Parent Elements</span></span>  
  
|<span data-ttu-id="cd444-122">요소</span><span class="sxs-lookup"><span data-stu-id="cd444-122">Element</span></span>|<span data-ttu-id="cd444-123">설명</span><span class="sxs-lookup"><span data-stu-id="cd444-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cd444-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cd444-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="cd444-125">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-125">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd444-126">설명</span><span class="sxs-lookup"><span data-stu-id="cd444-126">Remarks</span></span>  
 <span data-ttu-id="cd444-127">이 요소는 WCF 서비스의 상태를 serialize하는 데 사용되는 지속성 공급자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-127">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="cd444-128">이 요소는 HTTP 헤더에서 상태 정보를 전달하는 `wsHttpContextBinding`과 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd444-128">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd444-129">참고자료</span><span class="sxs-lookup"><span data-stu-id="cd444-129">See also</span></span>
- <xref:System.ServiceModel.Configuration.PersistenceProviderElement>
- <xref:System.ServiceModel.Persistence.PersistenceProvider>
