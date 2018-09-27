---
title: '&lt;제거&gt; bypasslist (네트워크 설정)에 대 한 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- <bypasslist>, remove element
- remove elemment, bypasslist
- bypasslist, remove element
- remove element, bypasslist
ms.assetid: 61dcfb4a-e3d9-4abf-a2cd-7d685fe2f64b
author: mcleblanc
ms.author: markl
ms.openlocfilehash: b6c72d9780088fddcaa59e644ff8069afbb4e43d
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47397100"
---
# <a name="ltremovegt-element-for-bypasslist-network-settings"></a><span data-ttu-id="50dfa-102">&lt;제거&gt; bypasslist (네트워크 설정)에 대 한 요소</span><span class="sxs-lookup"><span data-stu-id="50dfa-102">&lt;remove&gt; Element for bypasslist (Network Settings)</span></span>
<span data-ttu-id="50dfa-103">프록시 무시 목록에서 IP 주소 또는 DNS 이름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-103">Removes an IP address or DNS name from the proxy bypass list.</span></span>  
  
 <span data-ttu-id="50dfa-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="50dfa-104">\<configuration></span></span>  
<span data-ttu-id="50dfa-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="50dfa-105">\<system.net></span></span>  
<span data-ttu-id="50dfa-106">\<defaultProxy ></span><span class="sxs-lookup"><span data-stu-id="50dfa-106">\<defaultProxy></span></span>  
<span data-ttu-id="50dfa-107">\<bypasslist ></span><span class="sxs-lookup"><span data-stu-id="50dfa-107">\<bypasslist></span></span>  
<span data-ttu-id="50dfa-108">\<remove></span><span class="sxs-lookup"><span data-stu-id="50dfa-108">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50dfa-109">구문</span><span class="sxs-lookup"><span data-stu-id="50dfa-109">Syntax</span></span>  
  
```xml  
<remove   
  address="regular expression"   
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="50dfa-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="50dfa-110">Attributes and Elements</span></span>  
 <span data-ttu-id="50dfa-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="50dfa-112">특성</span><span class="sxs-lookup"><span data-stu-id="50dfa-112">Attributes</span></span>  
  
|<span data-ttu-id="50dfa-113">**특성**</span><span class="sxs-lookup"><span data-stu-id="50dfa-113">**Attribute**</span></span>|<span data-ttu-id="50dfa-114">**설명**</span><span class="sxs-lookup"><span data-stu-id="50dfa-114">**Description**</span></span>|  
|-------------------|---------------------|  
|`address`|<span data-ttu-id="50dfa-115">IP 주소 또는 DNS 이름을 설명 하는 정규식입니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-115">A regular expression describing an IP address or DNS name.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="50dfa-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="50dfa-116">Child Elements</span></span>  
 <span data-ttu-id="50dfa-117">없음</span><span class="sxs-lookup"><span data-stu-id="50dfa-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="50dfa-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="50dfa-118">Parent Elements</span></span>  
  
|<span data-ttu-id="50dfa-119">**요소**</span><span class="sxs-lookup"><span data-stu-id="50dfa-119">**Element**</span></span>|<span data-ttu-id="50dfa-120">**설명**</span><span class="sxs-lookup"><span data-stu-id="50dfa-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="50dfa-121">bypasslist</span><span class="sxs-lookup"><span data-stu-id="50dfa-121">bypasslist</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|<span data-ttu-id="50dfa-122">프록시를 사용 하지 않는 주소를 설명 하는 정규식 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-122">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="50dfa-123">설명</span><span class="sxs-lookup"><span data-stu-id="50dfa-123">Remarks</span></span>  
 <span data-ttu-id="50dfa-124">`remove` 요소 IP 주소 또는 프록시 서버를 바이패스 하는 주소 목록에서 DNS 서버 이름을 설명 하는 정규식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-124">The `remove` element removes regular expressions describing IP addresses or DNS server names from the list of addresses that bypass a proxy server.</span></span> <span data-ttu-id="50dfa-125">구성 계층 구조의 상위 수준 또는 구성 파일에서 주소를 이전 정의 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-125">The addresses were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
 <span data-ttu-id="50dfa-126">에 대 한 값을 `address` 특성에는 IP 주소 또는 호스트 이름 집합을 설명 하는 정규식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-126">The value for the `address` attribute should be a regular expression that describes a set of IP addresses or host names.</span></span>  
  
 <span data-ttu-id="50dfa-127">정규식에 대 한 자세한 내용은 다음을 참조 하세요. [.NET framework 정규식](../../../../../docs/standard/base-types/regular-expressions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-127">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../../docs/standard/base-types/regular-expressions.md).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="50dfa-128">구성 파일</span><span class="sxs-lookup"><span data-stu-id="50dfa-128">Configuration Files</span></span>  
 <span data-ttu-id="50dfa-129">이 요소는 응용 프로그램 구성 파일 또는 컴퓨터 구성 파일(Machine.config)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="50dfa-130">예제</span><span class="sxs-lookup"><span data-stu-id="50dfa-130">Example</span></span>  
 <span data-ttu-id="50dfa-131">Adventure-works.com 도메인에 대 한 이전 정의 제거 하 고 바이패스 목록에 contoso.com 도메인을 추가 하는 다음 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="50dfa-131">The following example removes any previous definition for the adventure-works.com domain, and then adds the contoso.com domain to the bypass list.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
        <remove address="[a-z]+\.adventure-works\.com$" />  
        <add address="[a-z]+\.contoso\.com$" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="50dfa-132">참고 항목</span><span class="sxs-lookup"><span data-stu-id="50dfa-132">See Also</span></span>  
 <xref:System.Net.WebProxy?displayProperty=nameWithType>  
 [<span data-ttu-id="50dfa-133">네트워크 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="50dfa-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
