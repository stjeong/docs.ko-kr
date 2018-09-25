---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: b812673ac1c015adde357d3c0707d85643aad3e9
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084334"
---
# <a name="ltsessionsecuritytokencachegt"></a><span data-ttu-id="f5657-102">&lt;sessionSecurityTokenCache&gt;</span><span class="sxs-lookup"><span data-stu-id="f5657-102">&lt;sessionSecurityTokenCache&gt;</span></span>
<span data-ttu-id="f5657-103">서비스 또는 보안 토큰 처리기 컬렉션을 사용 하 여 세션 토큰에 대 한 캐시를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="f5657-103">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="f5657-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="f5657-104">\<system.identityModel></span></span>  
<span data-ttu-id="f5657-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="f5657-105">\<identityConfiguration></span></span>  
<span data-ttu-id="f5657-106">\<캐시 ></span><span class="sxs-lookup"><span data-stu-id="f5657-106">\<caches></span></span>  
<span data-ttu-id="f5657-107">\<sessionSecurityTokenCache ></span><span class="sxs-lookup"><span data-stu-id="f5657-107">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5657-108">구문</span><span class="sxs-lookup"><span data-stu-id="f5657-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f5657-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="f5657-109">Attributes and Elements</span></span>  
 <span data-ttu-id="f5657-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f5657-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f5657-111">특성</span><span class="sxs-lookup"><span data-stu-id="f5657-111">Attributes</span></span>  
  
|<span data-ttu-id="f5657-112">특성</span><span class="sxs-lookup"><span data-stu-id="f5657-112">Attribute</span></span>|<span data-ttu-id="f5657-113">설명</span><span class="sxs-lookup"><span data-stu-id="f5657-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f5657-114">type</span><span class="sxs-lookup"><span data-stu-id="f5657-114">type</span></span>|<span data-ttu-id="f5657-115">형식에서 파생 되는 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="f5657-115">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f5657-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="f5657-116">Child Elements</span></span>  
 <span data-ttu-id="f5657-117">없음</span><span class="sxs-lookup"><span data-stu-id="f5657-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f5657-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="f5657-118">Parent Elements</span></span>  
  
|<span data-ttu-id="f5657-119">요소</span><span class="sxs-lookup"><span data-stu-id="f5657-119">Element</span></span>|<span data-ttu-id="f5657-120">설명</span><span class="sxs-lookup"><span data-stu-id="f5657-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f5657-121">\<캐시 ></span><span class="sxs-lookup"><span data-stu-id="f5657-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="f5657-122">서비스 또는 보안 토큰 처리기 컬렉션을 사용 하는 캐시를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5657-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f5657-123">예제</span><span class="sxs-lookup"><span data-stu-id="f5657-123">Example</span></span>  
 <span data-ttu-id="f5657-124">다음 XML 세션 보안 토큰을 보관 하기 위한 사용자 지정 캐시 구성을 보여 줍니다 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="f5657-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="f5657-125">구성에서 가져온 것은 `ClaimsAwareWebFarm` 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="f5657-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="f5657-126">이 샘플에 대 한 자세한 내용은 참조 하세요. [WIF 코드 샘플 인덱스](../../../../../docs/framework/security/wif-code-sample-index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="f5657-126">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f5657-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f5657-127">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
