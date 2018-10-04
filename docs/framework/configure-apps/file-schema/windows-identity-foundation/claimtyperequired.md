---
title: '&lt;claimTypeRequired&gt;'
ms.date: 03/30/2017
ms.assetid: c469d71f-6c77-4a24-97aa-53efa126ceef
author: BrucePerlerMS
ms.openlocfilehash: df4494de6b76943849db2bedef8f43ad894b6bd1
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48780663"
---
# <a name="ltclaimtyperequiredgt"></a><span data-ttu-id="3084d-102">&lt;claimTypeRequired&gt;</span><span class="sxs-lookup"><span data-stu-id="3084d-102">&lt;claimTypeRequired&gt;</span></span>
<span data-ttu-id="3084d-103">들어오는 보안 토큰에 대 한 필수 클레임 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3084d-103">Specifies the set of required claims for incoming security tokens.</span></span>  
  
 <span data-ttu-id="3084d-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="3084d-104">\<system.identityModel></span></span>  
<span data-ttu-id="3084d-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="3084d-105">\<identityConfiguration></span></span>  
<span data-ttu-id="3084d-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="3084d-106">\<claimTypeRequired></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3084d-107">구문</span><span class="sxs-lookup"><span data-stu-id="3084d-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3084d-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="3084d-108">Attributes and Elements</span></span>  
 <span data-ttu-id="3084d-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3084d-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3084d-110">특성</span><span class="sxs-lookup"><span data-stu-id="3084d-110">Attributes</span></span>  
 <span data-ttu-id="3084d-111">없음</span><span class="sxs-lookup"><span data-stu-id="3084d-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="3084d-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="3084d-112">Child Elements</span></span>  
  
|<span data-ttu-id="3084d-113">요소</span><span class="sxs-lookup"><span data-stu-id="3084d-113">Element</span></span>|<span data-ttu-id="3084d-114">설명</span><span class="sxs-lookup"><span data-stu-id="3084d-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3084d-115">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="3084d-115">\<claimType></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtype.md)|<span data-ttu-id="3084d-116">들어오는 보안 토큰에 대 한 단일 옵션 또는 필요한 클레임을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3084d-116">Specifies a single optional or required claim for incoming security tokens.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3084d-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="3084d-117">Parent Elements</span></span>  
  
|<span data-ttu-id="3084d-118">요소</span><span class="sxs-lookup"><span data-stu-id="3084d-118">Element</span></span>|<span data-ttu-id="3084d-119">설명</span><span class="sxs-lookup"><span data-stu-id="3084d-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3084d-120">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="3084d-120">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="3084d-121">서비스 수준 id 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3084d-121">Specifies service-level identity settings.</span></span>|
