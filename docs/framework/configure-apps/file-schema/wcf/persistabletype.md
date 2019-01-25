---
title: '&lt;persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: b9d61a736a2f8650c543433931d57e156d115018
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706854"
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="1b116-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="1b116-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="1b116-103">모든 지속 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b116-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="1b116-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1b116-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="1b116-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="1b116-105">\<comContracts></span></span>  
<span data-ttu-id="1b116-106">\<comContract></span><span class="sxs-lookup"><span data-stu-id="1b116-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b116-107">구문</span><span class="sxs-lookup"><span data-stu-id="1b116-107">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <persistableTypes>
      <persistableType id="String"
                       name="String">
      </persistableType>
    </persistableTypes>
  </comContract>
</comContracts>
```  
  
## <a name="type"></a><span data-ttu-id="1b116-108">형식</span><span class="sxs-lookup"><span data-stu-id="1b116-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1b116-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="1b116-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1b116-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1b116-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1b116-111">특성</span><span class="sxs-lookup"><span data-stu-id="1b116-111">Attributes</span></span>  
  
|<span data-ttu-id="1b116-112">특성</span><span class="sxs-lookup"><span data-stu-id="1b116-112">Attribute</span></span>|<span data-ttu-id="1b116-113">설명</span><span class="sxs-lookup"><span data-stu-id="1b116-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1b116-114">id</span><span class="sxs-lookup"><span data-stu-id="1b116-114">id</span></span>|<span data-ttu-id="1b116-115">지속 형식에 대한 고유 식별자를 지정하는 문자열이 포함된 필수적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="1b116-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="1b116-116">name</span><span class="sxs-lookup"><span data-stu-id="1b116-116">name</span></span>|<span data-ttu-id="1b116-117">지속 형식의 이름을 지정하는 문자열이 포함된 선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="1b116-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1b116-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="1b116-118">Child Elements</span></span>  
 <span data-ttu-id="1b116-119">없음</span><span class="sxs-lookup"><span data-stu-id="1b116-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1b116-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="1b116-120">Parent Elements</span></span>  
  
|<span data-ttu-id="1b116-121">요소</span><span class="sxs-lookup"><span data-stu-id="1b116-121">Element</span></span>|<span data-ttu-id="1b116-122">설명</span><span class="sxs-lookup"><span data-stu-id="1b116-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1b116-123">\<persistableTypes></span><span class="sxs-lookup"><span data-stu-id="1b116-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="1b116-124">`persistableType` 요소의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="1b116-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1b116-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="1b116-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>
- [<span data-ttu-id="1b116-126">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="1b116-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)
- [<span data-ttu-id="1b116-127">COM+ 애플리케이션과 통합</span><span class="sxs-lookup"><span data-stu-id="1b116-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="1b116-128">방법: COM + 서비스 설정 구성</span><span class="sxs-lookup"><span data-stu-id="1b116-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
