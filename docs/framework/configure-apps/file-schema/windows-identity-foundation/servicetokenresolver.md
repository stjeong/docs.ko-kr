---
title: '&lt;serviceTokenResolver&gt;'
ms.date: 03/30/2017
ms.assetid: 6e9001e1-e064-4f47-84b2-46225c177746
author: BrucePerlerMS
ms.openlocfilehash: d4b64e2c88e153834b7cf5a83bd6258b6dfd471f
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075308"
---
# <a name="ltservicetokenresolvergt"></a><span data-ttu-id="606cb-102">&lt;serviceTokenResolver&gt;</span><span class="sxs-lookup"><span data-stu-id="606cb-102">&lt;serviceTokenResolver&gt;</span></span>
<span data-ttu-id="606cb-103">토큰 처리기 컬렉션의 처리기에서 사용 되는 서비스 토큰 확인자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-103">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="606cb-104">서비스 토큰 확인자는 들어오는 토큰에 메시지 암호화 토큰을 확인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-104">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span>  
  
 <span data-ttu-id="606cb-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="606cb-105">\<system.identityModel></span></span>  
<span data-ttu-id="606cb-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="606cb-106">\<identityConfiguration></span></span>  
<span data-ttu-id="606cb-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="606cb-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="606cb-108">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="606cb-108">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="606cb-109">\<serviceTokenResolver ></span><span class="sxs-lookup"><span data-stu-id="606cb-109">\<serviceTokenResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="606cb-110">구문</span><span class="sxs-lookup"><span data-stu-id="606cb-110">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <serviceTokenResolver type=xs:string>  
        </serviceTokenResolver>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="606cb-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="606cb-111">Attributes and Elements</span></span>  
 <span data-ttu-id="606cb-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="606cb-113">특성</span><span class="sxs-lookup"><span data-stu-id="606cb-113">Attributes</span></span>  
  
|<span data-ttu-id="606cb-114">특성</span><span class="sxs-lookup"><span data-stu-id="606cb-114">Attribute</span></span>|<span data-ttu-id="606cb-115">설명</span><span class="sxs-lookup"><span data-stu-id="606cb-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="606cb-116">type</span><span class="sxs-lookup"><span data-stu-id="606cb-116">type</span></span>|<span data-ttu-id="606cb-117">서비스 토큰 확인자 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-117">Specifies the type of the service token resolver.</span></span> <span data-ttu-id="606cb-118">중 하나는 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 형식 또는 형식에서 파생 되는 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-118">Either the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> type or a type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span> <span data-ttu-id="606cb-119">지정 하는 방법에 대 한 자세한 내용은 `type` 특성 [사용자 지정 형식 참조]를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="606cb-119">For more information about how to specify the `type` attribute, see [Custom Type References].</span></span> <span data-ttu-id="606cb-120">필수.</span><span class="sxs-lookup"><span data-stu-id="606cb-120">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="606cb-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="606cb-121">Child Elements</span></span>  
 <span data-ttu-id="606cb-122">없음</span><span class="sxs-lookup"><span data-stu-id="606cb-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="606cb-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="606cb-123">Parent Elements</span></span>  
  
|<span data-ttu-id="606cb-124">요소</span><span class="sxs-lookup"><span data-stu-id="606cb-124">Element</span></span>|<span data-ttu-id="606cb-125">설명</span><span class="sxs-lookup"><span data-stu-id="606cb-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="606cb-126">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="606cb-126">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="606cb-127">구성 컬렉션의 보안 토큰 처리기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-127">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="606cb-128">설명</span><span class="sxs-lookup"><span data-stu-id="606cb-128">Remarks</span></span>  
 <span data-ttu-id="606cb-129">들어오는 토큰에 메시지 암호화 토큰을 확인 하려면 서비스 토큰 확인자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-129">The service token resolver can be used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="606cb-130">들어오는 토큰 암호 해독에 사용 해야 하는 키를 검색 하는 것이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-130">It is used to retrieve the key that should be used to decrypt incoming tokens.</span></span> <span data-ttu-id="606cb-131">지정 해야 합니다 `type` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-131">You must specify the `type` attribute.</span></span> <span data-ttu-id="606cb-132">지정 된 형식의 일 수 있습니다 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 또는 사용자 지정 형식에서 파생 되는 <xref:System.IdentityModel.Selectors.SecurityTokenResolver> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-132">The type specified can be either <xref:System.IdentityModel.Selectors.SecurityTokenResolver> or a custom type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span>  
  
 <span data-ttu-id="606cb-133">일부 토큰 처리기를 사용 하면 구성에서 서비스 토큰 확인자 설정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-133">Some token handlers allow you to specify service token resolver settings in configuration.</span></span> <span data-ttu-id="606cb-134">개별 토큰 처리기에 설정 된 보안 토큰 처리기 컬렉션에서 지정 된 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-134">Settings on individual token handlers override those specified on the security token handler collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="606cb-135">지정 된 `<serviceTokenResolver>` 의 자식 요소로 요소를 [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) 요소에 사용 되지 않지만 이전 버전과 호환성을 위해 계속 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-135">Specifying the `<serviceTokenResolver>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="606cb-136">설정 합니다 `<securityTokenHandlerConfiguration>` 요소에 있는 구성을 재정의 `<identityConfiguration>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="606cb-136">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="606cb-137">예제</span><span class="sxs-lookup"><span data-stu-id="606cb-137">Example</span></span>  
  
```xml  
<serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
```
