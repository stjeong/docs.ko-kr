---
title: '&lt;호스트&gt;'
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: 1fb35058d407d0fbae78092bb4ccd45b0aaa40e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702030"
---
# <a name="lthostgt"></a><span data-ttu-id="d528c-102">&lt;호스트&gt;</span><span class="sxs-lookup"><span data-stu-id="d528c-102">&lt;host&gt;</span></span>
<span data-ttu-id="d528c-103">서비스 호스트의 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d528c-103">Specifies settings for a service host.</span></span>  
  
 <span data-ttu-id="d528c-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d528c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="d528c-105">\<services></span><span class="sxs-lookup"><span data-stu-id="d528c-105">\<services></span></span>  
<span data-ttu-id="d528c-106">\<service></span><span class="sxs-lookup"><span data-stu-id="d528c-106">\<service></span></span>  
<span data-ttu-id="d528c-107">\<host></span><span class="sxs-lookup"><span data-stu-id="d528c-107">\<host></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d528c-108">구문</span><span class="sxs-lookup"><span data-stu-id="d528c-108">Syntax</span></span>  
  
```xml  
<host>
  <baseAddresses>
    <add baseAddress="string" />
  </baseAddresses>
  <timeOuts closeTimeout="TimeSpan"
            openTimeout="TimeSpan" />
</host>
```  
  
## <a name="type"></a><span data-ttu-id="d528c-109">형식</span><span class="sxs-lookup"><span data-stu-id="d528c-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d528c-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="d528c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="d528c-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d528c-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d528c-112">특성</span><span class="sxs-lookup"><span data-stu-id="d528c-112">Attributes</span></span>  
 <span data-ttu-id="d528c-113">없음</span><span class="sxs-lookup"><span data-stu-id="d528c-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d528c-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="d528c-114">Child Elements</span></span>  
  
|<span data-ttu-id="d528c-115">요소</span><span class="sxs-lookup"><span data-stu-id="d528c-115">Element</span></span>|<span data-ttu-id="d528c-116">설명</span><span class="sxs-lookup"><span data-stu-id="d528c-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d528c-117">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="d528c-117">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="d528c-118">서비스 호스트에서 사용하는 기본 주소를 지정하는 `baseAddress` 요소 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="d528c-118">A collection of `baseAddress` elements that specifies the base addresses used by the service host.</span></span>|  
|[<span data-ttu-id="d528c-119">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="d528c-119">\<timeOuts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|<span data-ttu-id="d528c-120">서비스 호스트가 열리거나 닫히는 데 허용되는 시간 간격을 지정하는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d528c-120">A configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d528c-121">부모 요소</span><span class="sxs-lookup"><span data-stu-id="d528c-121">Parent Elements</span></span>  
  
|<span data-ttu-id="d528c-122">요소</span><span class="sxs-lookup"><span data-stu-id="d528c-122">Element</span></span>|<span data-ttu-id="d528c-123">설명</span><span class="sxs-lookup"><span data-stu-id="d528c-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d528c-124">\<service></span><span class="sxs-lookup"><span data-stu-id="d528c-124">\<service></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|<span data-ttu-id="d528c-125">Windows Communication Foundation (WCF) 서비스에 대 한 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d528c-125">Specifies the settings for a Windows Communication Foundation (WCF) service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d528c-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="d528c-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="d528c-127">호스팅</span><span class="sxs-lookup"><span data-stu-id="d528c-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
