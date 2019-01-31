---
title: <mexEndpoint>
ms.date: 03/30/2017
ms.assetid: c9823060-0a5d-4f9d-99d4-4d113b758247
ms.openlocfilehash: 8fffcc05d5f53f719efce182083fbf103b1230ff
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271696"
---
# <a name="mexendpoint"></a><span data-ttu-id="db7d4-101">\<mexEndpoint></span><span class="sxs-lookup"><span data-stu-id="db7d4-101">\<mexEndpoint></span></span>
<span data-ttu-id="db7d4-102">이 구성 요소는 고정 IMetadataExchange 계약을 사용하여 표준 엔드포인트를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="db7d4-102">This configuration element defines a standard endpoint with a fixed IMetadataExchange contract.</span></span> <span data-ttu-id="db7d4-103">모든 메타데이터 교환 엔드포인트가 IMetadataExchange를 계약으로 지정하므로 고유의 엔드포인트를 정의하는 대신 이 표준 지점을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db7d4-103">Since all metadata exchange endpoints specify IMetadataExchange as their contract, you can use this standard point instead of defining one for yourself.</span></span>  
  
 <span data-ttu-id="db7d4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="db7d4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="db7d4-105">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="db7d4-105">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db7d4-106">구문</span><span class="sxs-lookup"><span data-stu-id="db7d4-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <mexEndpoint>
      <standardEndpoint name="String" />
    </mexEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="db7d4-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="db7d4-107">Attributes and Elements</span></span>  
 <span data-ttu-id="db7d4-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="db7d4-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="db7d4-109">특성</span><span class="sxs-lookup"><span data-stu-id="db7d4-109">Attributes</span></span>  
  
|<span data-ttu-id="db7d4-110">특성</span><span class="sxs-lookup"><span data-stu-id="db7d4-110">Attribute</span></span>|<span data-ttu-id="db7d4-111">설명</span><span class="sxs-lookup"><span data-stu-id="db7d4-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="db7d4-112">name</span><span class="sxs-lookup"><span data-stu-id="db7d4-112">name</span></span>|<span data-ttu-id="db7d4-113">표준 끝점의 구성 이름을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="db7d4-113">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="db7d4-114">이 이름은 서비스 엔드포인트의 `endpointConfiguration` 특성에서 표준 엔드포인트를 해당 구성에 연결하기 위해 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="db7d4-114">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="db7d4-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="db7d4-115">Child Elements</span></span>  
 <span data-ttu-id="db7d4-116">없음</span><span class="sxs-lookup"><span data-stu-id="db7d4-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="db7d4-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="db7d4-117">Parent Elements</span></span>  
  
|<span data-ttu-id="db7d4-118">요소</span><span class="sxs-lookup"><span data-stu-id="db7d4-118">Element</span></span>|<span data-ttu-id="db7d4-119">설명</span><span class="sxs-lookup"><span data-stu-id="db7d4-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="db7d4-120">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="db7d4-120">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="db7d4-121">하나 이상의 속성(주소, 바인딩, 계약)이 고정된 미리 정의된 엔드포인트인 표준 엔드포인트의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="db7d4-121">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|
