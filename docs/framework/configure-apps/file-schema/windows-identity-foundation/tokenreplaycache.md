---
title: <tokenReplayCache>
ms.date: 03/30/2017
ms.assetid: 1572ab23-6933-41b5-bfb4-0c4548145500
author: BrucePerlerMS
ms.openlocfilehash: dfa6c0d84582d55595f00f149adfdcaa9d554d6b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271952"
---
# <a name="tokenreplaycache"></a><span data-ttu-id="fb0e4-101">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="fb0e4-101">\<tokenReplayCache></span></span>
<span data-ttu-id="fb0e4-102">서비스 또는 보안 토큰 처리기 컬렉션을 사용 하 여 토큰 재생 캐시를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-102">Registers a token replay cache with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="fb0e4-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="fb0e4-103">\<system.identityModel></span></span>  
<span data-ttu-id="fb0e4-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="fb0e4-104">\<identityConfiguration></span></span>  
<span data-ttu-id="fb0e4-105">\<caches></span><span class="sxs-lookup"><span data-stu-id="fb0e4-105">\<caches></span></span>  
<span data-ttu-id="fb0e4-106">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="fb0e4-106">\<tokenReplayCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb0e4-107">구문</span><span class="sxs-lookup"><span data-stu-id="fb0e4-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <tokenReplayCache type=xs:string>  
      </tokenReplayCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fb0e4-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="fb0e4-108">Attributes and Elements</span></span>  
 <span data-ttu-id="fb0e4-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fb0e4-110">특성</span><span class="sxs-lookup"><span data-stu-id="fb0e4-110">Attributes</span></span>  
  
|<span data-ttu-id="fb0e4-111">특성</span><span class="sxs-lookup"><span data-stu-id="fb0e4-111">Attribute</span></span>|<span data-ttu-id="fb0e4-112">설명</span><span class="sxs-lookup"><span data-stu-id="fb0e4-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fb0e4-113">형식</span><span class="sxs-lookup"><span data-stu-id="fb0e4-113">type</span></span>|<span data-ttu-id="fb0e4-114">형식에서 파생 되는 <xref:System.IdentityModel.Tokens.TokenReplayCache> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-114">A type that derives from the <xref:System.IdentityModel.Tokens.TokenReplayCache> class.</span></span> <span data-ttu-id="fb0e4-115">사용자 지정 하는 방법에 대 한 자세한 내용은 `type`, [사용자 지정 형식 참조]를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-115">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb0e4-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="fb0e4-116">Child Elements</span></span>  
 <span data-ttu-id="fb0e4-117">없음</span><span class="sxs-lookup"><span data-stu-id="fb0e4-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fb0e4-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="fb0e4-118">Parent Elements</span></span>  
  
|<span data-ttu-id="fb0e4-119">요소</span><span class="sxs-lookup"><span data-stu-id="fb0e4-119">Element</span></span>|<span data-ttu-id="fb0e4-120">설명</span><span class="sxs-lookup"><span data-stu-id="fb0e4-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fb0e4-121">\<caches></span><span class="sxs-lookup"><span data-stu-id="fb0e4-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="fb0e4-122">서비스 또는 보안 토큰 처리기 컬렉션을 사용 하는 캐시를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fb0e4-123">설명</span><span class="sxs-lookup"><span data-stu-id="fb0e4-123">Remarks</span></span>  
 <span data-ttu-id="fb0e4-124">재생 된 토큰을 검색 하는 토큰 재생 캐시가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-124">The token replay cache is used to detect replayed tokens.</span></span> <span data-ttu-id="fb0e4-125">토큰 재생 검색이 사용 되는 [ \<tokenReplayDetection >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md) 도 토큰에 대 한 최대 만료 시간을 지정 하는 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-125">Token replay detection is enabled by the [\<tokenReplayDetection>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md) element, which also specifies the maximum expiration time for tokens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fb0e4-126">예제</span><span class="sxs-lookup"><span data-stu-id="fb0e4-126">Example</span></span>  
 <span data-ttu-id="fb0e4-127">다음 XML 재생 된 토큰을 검색 하는 것에 대 한 사용자 지정 캐시의 구성을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb0e4-127">The following XML shows the configuration of a custom cache for detecting replayed tokens.</span></span>  
  
```xml  
<caches>  
  <tokenReplayCache type="MyCacheLibrary.MyTokenReplayCache, MyCacheLibrary">  
  </tokenReplayCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fb0e4-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="fb0e4-128">See also</span></span>
- <xref:System.IdentityModel.Tokens.TokenReplayCache>
- [<span data-ttu-id="fb0e4-129">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="fb0e4-129">\<tokenReplayDetection></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)
