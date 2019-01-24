---
title: '&lt;policyImporter&gt;'
ms.date: 03/30/2017
ms.assetid: b0d03456-546f-44bb-ab12-1b2ce7f98fca
ms.openlocfilehash: 4075f7fcb1c65da3d9e2e5e5dab52452ca2c9b60
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632168"
---
# <a name="ltpolicyimportergt"></a><span data-ttu-id="10b92-102">&lt;policyImporter&gt;</span><span class="sxs-lookup"><span data-stu-id="10b92-102">&lt;policyImporter&gt;</span></span>
<span data-ttu-id="10b92-103">바인딩에 대한 사용자 지정 정책 어설션의 가져오기를 제어하는 정책 가져오기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10b92-103">Specifies a policy importer that controls the import of custom policy assertions about bindings.</span></span>  
  
 <span data-ttu-id="10b92-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="10b92-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="10b92-105">\<client></span><span class="sxs-lookup"><span data-stu-id="10b92-105">\<client></span></span>  
<span data-ttu-id="10b92-106">\<metadata></span><span class="sxs-lookup"><span data-stu-id="10b92-106">\<metadata></span></span>  
<span data-ttu-id="10b92-107">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="10b92-107">\<policyImporters></span></span>  
<span data-ttu-id="10b92-108">\<policyImporter></span><span class="sxs-lookup"><span data-stu-id="10b92-108">\<policyImporter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10b92-109">구문</span><span class="sxs-lookup"><span data-stu-id="10b92-109">Syntax</span></span>  
  
```xml  
<metadata>
  <policyImporters>
    <policyImporter type="String" />
  </policyImporters>
</metadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="10b92-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="10b92-110">Attributes and Elements</span></span>  
 <span data-ttu-id="10b92-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="10b92-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="10b92-112">특성</span><span class="sxs-lookup"><span data-stu-id="10b92-112">Attributes</span></span>  
  
|<span data-ttu-id="10b92-113">특성</span><span class="sxs-lookup"><span data-stu-id="10b92-113">Attribute</span></span>|<span data-ttu-id="10b92-114">설명</span><span class="sxs-lookup"><span data-stu-id="10b92-114">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="10b92-115">이 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="10b92-115">The type of this element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="10b92-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="10b92-116">Child Elements</span></span>  
 <span data-ttu-id="10b92-117">없음</span><span class="sxs-lookup"><span data-stu-id="10b92-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="10b92-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="10b92-118">Parent Elements</span></span>  
  
|<span data-ttu-id="10b92-119">요소</span><span class="sxs-lookup"><span data-stu-id="10b92-119">Element</span></span>|<span data-ttu-id="10b92-120">설명</span><span class="sxs-lookup"><span data-stu-id="10b92-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="10b92-121">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="10b92-121">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="10b92-122">바인딩에 대한 사용자 지정 정책 어설션의 가져오기를 제어하는 모든 정책 가져오기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10b92-122">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="10b92-123">설명</span><span class="sxs-lookup"><span data-stu-id="10b92-123">Remarks</span></span>  
 <span data-ttu-id="10b92-124">정책 가져오기는, 바인딩 기능에 대한 사용자 지정 정책 어설션을 검색하거나 어설션에서 요구하는 기능을 구현하는 사용자 지정 바인딩 요소를 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="10b92-124">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="10b92-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="10b92-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.PolicyImporterElement>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Description.MetadataImporter>
- [<span data-ttu-id="10b92-126">WCF 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="10b92-126">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="10b92-127">클라이언트</span><span class="sxs-lookup"><span data-stu-id="10b92-127">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
