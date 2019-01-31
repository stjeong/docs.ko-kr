---
title: <add>의 <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 1bd7426f-5f4f-43fc-b8e9-de842219aa32
ms.openlocfilehash: d66be51fa2626283063c250905efdb7d47babfb0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279944"
---
# <a name="add-of-baseaddresses"></a><span data-ttu-id="00ff3-102">\<추가 >의 \<baseAddresses ></span><span class="sxs-lookup"><span data-stu-id="00ff3-102">\<add> of \<baseAddresses></span></span>
<span data-ttu-id="00ff3-103">서비스 호스트에서 사용하는 기본 주소를 지정하는 구성 요소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00ff3-103">Represents a configuration element that specifies the base addresses used by the service host.</span></span>  
  
 <span data-ttu-id="00ff3-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="00ff3-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="00ff3-105">\<client></span><span class="sxs-lookup"><span data-stu-id="00ff3-105">\<client></span></span>  
<span data-ttu-id="00ff3-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="00ff3-106">\<endpoint></span></span>  
<span data-ttu-id="00ff3-107">\<host></span><span class="sxs-lookup"><span data-stu-id="00ff3-107">\<host></span></span>  
<span data-ttu-id="00ff3-108">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="00ff3-108">\<baseAddresses></span></span>  
<span data-ttu-id="00ff3-109">\<baseAddress></span><span class="sxs-lookup"><span data-stu-id="00ff3-109">\<baseAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00ff3-110">구문</span><span class="sxs-lookup"><span data-stu-id="00ff3-110">Syntax</span></span>  
  
```xml  
<add baseAddress="string" />
```  
  
## <a name="type"></a><span data-ttu-id="00ff3-111">형식</span><span class="sxs-lookup"><span data-stu-id="00ff3-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="00ff3-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="00ff3-112">Attributes and Elements</span></span>  
 <span data-ttu-id="00ff3-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="00ff3-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="00ff3-114">특성</span><span class="sxs-lookup"><span data-stu-id="00ff3-114">Attributes</span></span>  
  
|<span data-ttu-id="00ff3-115">특성</span><span class="sxs-lookup"><span data-stu-id="00ff3-115">Attribute</span></span>|<span data-ttu-id="00ff3-116">설명</span><span class="sxs-lookup"><span data-stu-id="00ff3-116">Description</span></span>|  
|---------------|-----------------|  
|`baseAddress`|<span data-ttu-id="00ff3-117">서비스 호스트에서 사용하는 기본 주소를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="00ff3-117">A string that specifies a base address used by the service host.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="00ff3-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="00ff3-118">Child Elements</span></span>  
 <span data-ttu-id="00ff3-119">없음</span><span class="sxs-lookup"><span data-stu-id="00ff3-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="00ff3-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="00ff3-120">Parent Elements</span></span>  
  
|<span data-ttu-id="00ff3-121">요소</span><span class="sxs-lookup"><span data-stu-id="00ff3-121">Element</span></span>|<span data-ttu-id="00ff3-122">설명</span><span class="sxs-lookup"><span data-stu-id="00ff3-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="00ff3-123">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="00ff3-123">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="00ff3-124">`baseAddress` 요소의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="00ff3-124">A collection of `baseAddress` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="00ff3-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="00ff3-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="00ff3-126">호스팅</span><span class="sxs-lookup"><span data-stu-id="00ff3-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
