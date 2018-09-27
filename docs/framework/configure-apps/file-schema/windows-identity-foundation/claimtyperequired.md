---
title: '&lt;claimTypeRequired&gt;'
ms.date: 03/30/2017
ms.assetid: c469d71f-6c77-4a24-97aa-53efa126ceef
author: BrucePerlerMS
ms.openlocfilehash: df4494de6b76943849db2bedef8f43ad894b6bd1
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47399413"
---
# <a name="ltclaimtyperequiredgt"></a><span data-ttu-id="2fcf2-102">&lt;claimTypeRequired&gt;</span><span class="sxs-lookup"><span data-stu-id="2fcf2-102">&lt;claimTypeRequired&gt;</span></span>
<span data-ttu-id="2fcf2-103">들어오는 보안 토큰에 대 한 필수 클레임 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fcf2-103">Specifies the set of required claims for incoming security tokens.</span></span>  
  
 <span data-ttu-id="2fcf2-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="2fcf2-104">\<system.identityModel></span></span>  
<span data-ttu-id="2fcf2-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="2fcf2-105">\<identityConfiguration></span></span>  
<span data-ttu-id="2fcf2-106">\<claimTypeRequired ></span><span class="sxs-lookup"><span data-stu-id="2fcf2-106">\<claimTypeRequired></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2fcf2-107">구문</span><span class="sxs-lookup"><span data-stu-id="2fcf2-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2fcf2-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="2fcf2-108">Attributes and Elements</span></span>  
 <span data-ttu-id="2fcf2-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2fcf2-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2fcf2-110">특성</span><span class="sxs-lookup"><span data-stu-id="2fcf2-110">Attributes</span></span>  
 <span data-ttu-id="2fcf2-111">없음</span><span class="sxs-lookup"><span data-stu-id="2fcf2-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2fcf2-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="2fcf2-112">Child Elements</span></span>  
  
|<span data-ttu-id="2fcf2-113">요소</span><span class="sxs-lookup"><span data-stu-id="2fcf2-113">Element</span></span>|<span data-ttu-id="2fcf2-114">설명</span><span class="sxs-lookup"><span data-stu-id="2fcf2-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2fcf2-115">\<claimType ></span><span class="sxs-lookup"><span data-stu-id="2fcf2-115">\<claimType></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtype.md)|<span data-ttu-id="2fcf2-116">들어오는 보안 토큰에 대 한 단일 옵션 또는 필요한 클레임을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2fcf2-116">Specifies a single optional or required claim for incoming security tokens.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2fcf2-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="2fcf2-117">Parent Elements</span></span>  
  
|<span data-ttu-id="2fcf2-118">요소</span><span class="sxs-lookup"><span data-stu-id="2fcf2-118">Element</span></span>|<span data-ttu-id="2fcf2-119">설명</span><span class="sxs-lookup"><span data-stu-id="2fcf2-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2fcf2-120">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="2fcf2-120">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="2fcf2-121">서비스 수준 id 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2fcf2-121">Specifies service-level identity settings.</span></span>|
