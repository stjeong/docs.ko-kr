---
title: '&lt;persistenceProvider&gt;'
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: ba02977a7df44931ae195040949e9a8eb0c141b5
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152023"
---
# <a name="ltpersistenceprovidergt"></a><span data-ttu-id="c2e4e-102">&lt;persistenceProvider&gt;</span><span class="sxs-lookup"><span data-stu-id="c2e4e-102">&lt;persistenceProvider&gt;</span></span>
<span data-ttu-id="c2e4e-103">사용할 지속성 공급자 구현 형식 및 지속성 작업에 사용할 제한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-103">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="c2e4e-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c2e4e-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c2e4e-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="c2e4e-105">\<behaviors></span></span>  
<span data-ttu-id="c2e4e-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="c2e4e-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="c2e4e-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="c2e4e-107">\<behavior></span></span>  
<span data-ttu-id="c2e4e-108">\<persistenceProvider ></span><span class="sxs-lookup"><span data-stu-id="c2e4e-108">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2e4e-109">구문</span><span class="sxs-lookup"><span data-stu-id="c2e4e-109">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c2e4e-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="c2e4e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="c2e4e-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c2e4e-112">특성</span><span class="sxs-lookup"><span data-stu-id="c2e4e-112">Attributes</span></span>  
  
|<span data-ttu-id="c2e4e-113">특성</span><span class="sxs-lookup"><span data-stu-id="c2e4e-113">Attribute</span></span>|<span data-ttu-id="c2e4e-114">설명</span><span class="sxs-lookup"><span data-stu-id="c2e4e-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c2e4e-115">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="c2e4e-115">persistenceOperationTimeout</span></span>|<span data-ttu-id="c2e4e-116">지속성 작업에 사용되는 제한 시간을 지정하는 <xref:System.TimeSpan> 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-116">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="c2e4e-117">기본값은 "00: 00:30"입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-117">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="c2e4e-118">형식</span><span class="sxs-lookup"><span data-stu-id="c2e4e-118">type</span></span>|<span data-ttu-id="c2e4e-119">사용할 지속성 공급자 팩터리의 형식을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-119">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c2e4e-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="c2e4e-120">Child Elements</span></span>  
 <span data-ttu-id="c2e4e-121">없음</span><span class="sxs-lookup"><span data-stu-id="c2e4e-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c2e4e-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="c2e4e-122">Parent Elements</span></span>  
  
|<span data-ttu-id="c2e4e-123">요소</span><span class="sxs-lookup"><span data-stu-id="c2e4e-123">Element</span></span>|<span data-ttu-id="c2e4e-124">설명</span><span class="sxs-lookup"><span data-stu-id="c2e4e-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c2e4e-125">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="c2e4e-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="c2e4e-126">동작 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-126">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2e4e-127">설명</span><span class="sxs-lookup"><span data-stu-id="c2e4e-127">Remarks</span></span>  
 <span data-ttu-id="c2e4e-128">이 요소는 WCF 서비스의 상태를 serialize하는 데 사용되는 지속성 공급자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-128">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="c2e4e-129">이 요소는 HTTP 헤더에서 상태 정보를 전달하는 `wsHttpContextBinding`과 함께 사용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e4e-129">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2e4e-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c2e4e-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PersistenceProviderElement>  
 <xref:System.ServiceModel.Persistence.PersistenceProvider>
