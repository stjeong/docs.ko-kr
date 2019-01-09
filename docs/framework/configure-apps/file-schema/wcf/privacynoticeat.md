---
title: '&lt;privacyNoticeAt&gt;'
ms.date: 03/30/2017
ms.assetid: 4cc96942-4eb9-4241-b2fd-45aa239915e8
ms.openlocfilehash: 104b2b6399ea31273045e43be716947db110715d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147319"
---
# <a name="ltprivacynoticeatgt"></a><span data-ttu-id="50c8f-102">&lt;privacyNoticeAt&gt;</span><span class="sxs-lookup"><span data-stu-id="50c8f-102">&lt;privacyNoticeAt&gt;</span></span>
<span data-ttu-id="50c8f-103">`wsFederationHttp` 바인딩에 사용되는 개인 정보 알림을 지정하는 구성 요소를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="50c8f-103">Represents a configuration element that specifies a privacy notice used in `wsFederationHttp` binding.</span></span>  
  
 <span data-ttu-id="50c8f-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="50c8f-104">\<system.serviceModel></span></span>  
<span data-ttu-id="50c8f-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="50c8f-105">\<bindings></span></span>  
<span data-ttu-id="50c8f-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="50c8f-106">\<customBinding></span></span>  
<span data-ttu-id="50c8f-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="50c8f-107">\<binding></span></span>  
<span data-ttu-id="50c8f-108">\<privacyNotice ></span><span class="sxs-lookup"><span data-stu-id="50c8f-108">\<privacyNotice></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50c8f-109">구문</span><span class="sxs-lookup"><span data-stu-id="50c8f-109">Syntax</span></span>  
  
```xml  
<privacyNotice url="String"
               version="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="50c8f-110">형식</span><span class="sxs-lookup"><span data-stu-id="50c8f-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="50c8f-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="50c8f-111">Attributes and Elements</span></span>  
 <span data-ttu-id="50c8f-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="50c8f-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="50c8f-113">특성</span><span class="sxs-lookup"><span data-stu-id="50c8f-113">Attributes</span></span>  
  
|<span data-ttu-id="50c8f-114">특성</span><span class="sxs-lookup"><span data-stu-id="50c8f-114">Attribute</span></span>|<span data-ttu-id="50c8f-115">설명</span><span class="sxs-lookup"><span data-stu-id="50c8f-115">Description</span></span>|  
|---------------|-----------------|  
|`url`|<span data-ttu-id="50c8f-116">개인 정보 알림이 있는 URI를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="50c8f-116">A string that specifies the URI at which the privacy notice is located.</span></span>|  
|`version`|<span data-ttu-id="50c8f-117">이 개인 정보 알림의 버전을 지정하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="50c8f-117">An integer that specifies the version of this privacy notice.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="50c8f-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="50c8f-118">Child Elements</span></span>  
 <span data-ttu-id="50c8f-119">없음</span><span class="sxs-lookup"><span data-stu-id="50c8f-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="50c8f-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="50c8f-120">Parent Elements</span></span>  
  
|<span data-ttu-id="50c8f-121">요소</span><span class="sxs-lookup"><span data-stu-id="50c8f-121">Element</span></span>|<span data-ttu-id="50c8f-122">설명</span><span class="sxs-lookup"><span data-stu-id="50c8f-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="50c8f-123">\<binding></span><span class="sxs-lookup"><span data-stu-id="50c8f-123">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="50c8f-124">사용자 지정 바인딩의 모든 바인딩 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="50c8f-124">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="50c8f-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="50c8f-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PrivacyNoticeElement>  
 <xref:System.ServiceModel.Channels.PrivacyNoticeBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="50c8f-126">바인딩</span><span class="sxs-lookup"><span data-stu-id="50c8f-126">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="50c8f-127">바인딩 확장</span><span class="sxs-lookup"><span data-stu-id="50c8f-127">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="50c8f-128">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="50c8f-128">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="50c8f-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="50c8f-129">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
