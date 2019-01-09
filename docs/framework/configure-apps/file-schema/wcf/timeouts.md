---
title: '&lt;시간 제한&gt;'
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: e39deeb251865b87eb7734e4447088ca2f221d1d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148333"
---
# <a name="lttimeoutsgt"></a><span data-ttu-id="2bce2-102">&lt;시간 제한&gt;</span><span class="sxs-lookup"><span data-stu-id="2bce2-102">&lt;timeOuts&gt;</span></span>
<span data-ttu-id="2bce2-103">서비스 호스트가 열리거나 닫히는 데 허용되는 시간 간격을 지정하는 구성 요소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2bce2-103">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
 <span data-ttu-id="2bce2-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2bce2-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="2bce2-105">\<client></span><span class="sxs-lookup"><span data-stu-id="2bce2-105">\<client></span></span>  
<span data-ttu-id="2bce2-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="2bce2-106">\<endpoint></span></span>  
<span data-ttu-id="2bce2-107">\<호스트 ></span><span class="sxs-lookup"><span data-stu-id="2bce2-107">\<host></span></span>  
<span data-ttu-id="2bce2-108">\<시간 ></span><span class="sxs-lookup"><span data-stu-id="2bce2-108">\<timeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2bce2-109">구문</span><span class="sxs-lookup"><span data-stu-id="2bce2-109">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2bce2-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="2bce2-110">Attributes and Elements</span></span>  
 <span data-ttu-id="2bce2-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2bce2-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2bce2-112">특성</span><span class="sxs-lookup"><span data-stu-id="2bce2-112">Attributes</span></span>  
  
|<span data-ttu-id="2bce2-113">특성</span><span class="sxs-lookup"><span data-stu-id="2bce2-113">Attribute</span></span>|<span data-ttu-id="2bce2-114">설명</span><span class="sxs-lookup"><span data-stu-id="2bce2-114">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="2bce2-115">서비스 호스트를 닫는 데 허용되는 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2bce2-115">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="2bce2-116">서비스 호스트를 여는 데 허용되는 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2bce2-116">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2bce2-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="2bce2-117">Child Elements</span></span>  
 <span data-ttu-id="2bce2-118">없음</span><span class="sxs-lookup"><span data-stu-id="2bce2-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2bce2-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="2bce2-119">Parent Elements</span></span>  
  
|<span data-ttu-id="2bce2-120">요소</span><span class="sxs-lookup"><span data-stu-id="2bce2-120">Element</span></span>|<span data-ttu-id="2bce2-121">설명</span><span class="sxs-lookup"><span data-stu-id="2bce2-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2bce2-122">\<호스트 ></span><span class="sxs-lookup"><span data-stu-id="2bce2-122">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="2bce2-123">서비스 호스트의 설정을 지정하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="2bce2-123">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2bce2-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2bce2-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 [<span data-ttu-id="2bce2-125">호스팅</span><span class="sxs-lookup"><span data-stu-id="2bce2-125">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
