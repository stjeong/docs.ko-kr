---
title: '&lt;ClaimType&gt;'
ms.date: 03/30/2017
ms.assetid: d17b5831-9a2c-45c4-b0d1-68f48e72e861
author: BrucePerlerMS
ms.openlocfilehash: 805377565b6e835fd9ffba915a003bc56529a3b6
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47234964"
---
# <a name="ltclaimtypegt"></a><span data-ttu-id="7d315-102">&lt;ClaimType&gt;</span><span class="sxs-lookup"><span data-stu-id="7d315-102">&lt;claimType&gt;</span></span>
<span data-ttu-id="7d315-103">들어오는 보안 토큰에 대 한 단일 옵션 또는 필요한 클레임을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-103">Specifies a single optional or required claim for incoming security tokens.</span></span>  
  
 <span data-ttu-id="7d315-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="7d315-104">\<system.identityModel></span></span>  
<span data-ttu-id="7d315-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="7d315-105">\<identityConfiguration></span></span>  
<span data-ttu-id="7d315-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="7d315-106">\<claimTypeRequired></span></span>  
<span data-ttu-id="7d315-107">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="7d315-107">\<claimType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d315-108">구문</span><span class="sxs-lookup"><span data-stu-id="7d315-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
      <claimType type=URI optional=xs:boolean >  
      </claimType>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7d315-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="7d315-109">Attributes and Elements</span></span>  
 <span data-ttu-id="7d315-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7d315-111">특성</span><span class="sxs-lookup"><span data-stu-id="7d315-111">Attributes</span></span>  
  
|<span data-ttu-id="7d315-112">특성</span><span class="sxs-lookup"><span data-stu-id="7d315-112">Attribute</span></span>|<span data-ttu-id="7d315-113">설명</span><span class="sxs-lookup"><span data-stu-id="7d315-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7d315-114">type</span><span class="sxs-lookup"><span data-stu-id="7d315-114">type</span></span>|<span data-ttu-id="7d315-115">클레임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-115">The claim type.</span></span> <span data-ttu-id="7d315-116">일반적으로 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-116">Typically a URI.</span></span> <span data-ttu-id="7d315-117">필수.</span><span class="sxs-lookup"><span data-stu-id="7d315-117">Required.</span></span>|  
|<span data-ttu-id="7d315-118">선택적</span><span class="sxs-lookup"><span data-stu-id="7d315-118">optional</span></span>|<span data-ttu-id="7d315-119">클레임 형식이 선택 사항 인지 여부를 지정 하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-119">A boolean value that specifies whether the claim type is optional.</span></span> <span data-ttu-id="7d315-120">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-120">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7d315-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="7d315-121">Child Elements</span></span>  
 <span data-ttu-id="7d315-122">없음</span><span class="sxs-lookup"><span data-stu-id="7d315-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7d315-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="7d315-123">Parent Elements</span></span>  
  
|<span data-ttu-id="7d315-124">요소</span><span class="sxs-lookup"><span data-stu-id="7d315-124">Element</span></span>|<span data-ttu-id="7d315-125">설명</span><span class="sxs-lookup"><span data-stu-id="7d315-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7d315-126">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="7d315-126">\<claimTypeRequired></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtyperequired.md)|<span data-ttu-id="7d315-127">들어오는 보안 토큰에 대 한 필수 클레임 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d315-127">Specifies the set of required claims for incoming security tokens.</span></span>|
