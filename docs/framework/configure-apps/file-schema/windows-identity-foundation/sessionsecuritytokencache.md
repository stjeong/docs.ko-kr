---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: 024375cb114bb080c576ea033e5588526350ecdf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510093"
---
# <a name="ltsessionsecuritytokencachegt"></a><span data-ttu-id="81e69-102">&lt;sessionSecurityTokenCache&gt;</span><span class="sxs-lookup"><span data-stu-id="81e69-102">&lt;sessionSecurityTokenCache&gt;</span></span>
<span data-ttu-id="81e69-103">서비스 또는 보안 토큰 처리기 컬렉션을 사용 하 여 세션 토큰에 대 한 캐시를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="81e69-103">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="81e69-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="81e69-104">\<system.identityModel></span></span>  
<span data-ttu-id="81e69-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="81e69-105">\<identityConfiguration></span></span>  
<span data-ttu-id="81e69-106">\<caches></span><span class="sxs-lookup"><span data-stu-id="81e69-106">\<caches></span></span>  
<span data-ttu-id="81e69-107">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="81e69-107">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81e69-108">구문</span><span class="sxs-lookup"><span data-stu-id="81e69-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <sessionSecurityTokenCache type=xs:string>  
      </sessionSecurityTokenCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="81e69-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="81e69-109">Attributes and Elements</span></span>  
 <span data-ttu-id="81e69-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="81e69-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="81e69-111">특성</span><span class="sxs-lookup"><span data-stu-id="81e69-111">Attributes</span></span>  
  
|<span data-ttu-id="81e69-112">특성</span><span class="sxs-lookup"><span data-stu-id="81e69-112">Attribute</span></span>|<span data-ttu-id="81e69-113">설명</span><span class="sxs-lookup"><span data-stu-id="81e69-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="81e69-114">형식</span><span class="sxs-lookup"><span data-stu-id="81e69-114">type</span></span>|<span data-ttu-id="81e69-115">형식에서 파생 되는 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="81e69-115">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="81e69-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="81e69-116">Child Elements</span></span>  
 <span data-ttu-id="81e69-117">없음</span><span class="sxs-lookup"><span data-stu-id="81e69-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="81e69-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="81e69-118">Parent Elements</span></span>  
  
|<span data-ttu-id="81e69-119">요소</span><span class="sxs-lookup"><span data-stu-id="81e69-119">Element</span></span>|<span data-ttu-id="81e69-120">설명</span><span class="sxs-lookup"><span data-stu-id="81e69-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="81e69-121">\<caches></span><span class="sxs-lookup"><span data-stu-id="81e69-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="81e69-122">서비스 또는 보안 토큰 처리기 컬렉션을 사용 하는 캐시를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e69-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="81e69-123">예제</span><span class="sxs-lookup"><span data-stu-id="81e69-123">Example</span></span>  
 <span data-ttu-id="81e69-124">다음 XML 세션 보안 토큰을 보관 하기 위한 사용자 지정 캐시 구성을 보여 줍니다 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="81e69-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="81e69-125">구성에서 가져온 것은 `ClaimsAwareWebFarm` 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="81e69-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="81e69-126">이 샘플에 대 한 자세한 내용은 참조 하세요. [WIF 코드 샘플 인덱스](../../../../../docs/framework/security/wif-code-sample-index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="81e69-126">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="81e69-127">참고자료</span><span class="sxs-lookup"><span data-stu-id="81e69-127">See also</span></span>
- <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
