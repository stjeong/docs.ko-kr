---
title: '&lt;프록시&gt; 요소 (네트워크 설정)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/proxy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#proxy
helpviewer_keywords:
- <proxy> element
- proxy element
ms.assetid: 37a548d8-fade-4ac5-82ec-b49b6c6cb22a
author: mcleblanc
ms.author: markl
ms.openlocfilehash: f4ab3d4e7ce6686a43e4c5258a56e72203c38ebd
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47209477"
---
# <a name="ltproxygt-element-network-settings"></a><span data-ttu-id="58793-102">&lt;프록시&gt; 요소 (네트워크 설정)</span><span class="sxs-lookup"><span data-stu-id="58793-102">&lt;proxy&gt; Element (Network Settings)</span></span>
<span data-ttu-id="58793-103">프록시 서버를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-103">Defines a proxy server.</span></span>  
  
 <span data-ttu-id="58793-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="58793-104">\<configuration></span></span>  
<span data-ttu-id="58793-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="58793-105">\<system.net></span></span>  
<span data-ttu-id="58793-106">\<defaultProxy ></span><span class="sxs-lookup"><span data-stu-id="58793-106">\<defaultProxy></span></span>  
<span data-ttu-id="58793-107">\<프록시 ></span><span class="sxs-lookup"><span data-stu-id="58793-107">\<proxy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58793-108">구문</span><span class="sxs-lookup"><span data-stu-id="58793-108">Syntax</span></span>  
  
```xml  
<proxy
  autoDetect="true|false|unspecified" 
  bypassonlocal="true|false|unspecified"
  proxyaddress="uriString"
  scriptLocation="uriString"
  usesystemdefault="true|false|unspecified"
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="58793-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="58793-109">Attributes and Elements</span></span>  
 <span data-ttu-id="58793-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="58793-111">특성</span><span class="sxs-lookup"><span data-stu-id="58793-111">Attributes</span></span>  
  
|<span data-ttu-id="58793-112">**특성**</span><span class="sxs-lookup"><span data-stu-id="58793-112">**Attribute**</span></span>|<span data-ttu-id="58793-113">**설명**</span><span class="sxs-lookup"><span data-stu-id="58793-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`autoDetect`|<span data-ttu-id="58793-114">프록시를 자동으로 검색 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-114">Specifies whether the proxy is automatically detected.</span></span> <span data-ttu-id="58793-115">기본값은 `unspecified`입니다.</span><span class="sxs-lookup"><span data-stu-id="58793-115">The default value is `unspecified`.</span></span>|  
|`bypassonlocal`|<span data-ttu-id="58793-116">로컬 리소스에 대 한 프록시를 바이패스 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-116">Specifies whether the proxy is bypassed for local resources.</span></span> <span data-ttu-id="58793-117">로컬 서버를 포함 하는 로컬 리소스 (`http://localhost`, `http://loopback`, 또는 `http://127.0.0.1`) 및 마침표가 없는 URI (`http://webserver`).</span><span class="sxs-lookup"><span data-stu-id="58793-117">Local resources include the local server (`http://localhost`, `http://loopback`, or `http://127.0.0.1`) and a URI without a period (`http://webserver`).</span></span> <span data-ttu-id="58793-118">기본값은 `unspecified`입니다.</span><span class="sxs-lookup"><span data-stu-id="58793-118">The default value is `unspecified`.</span></span>|  
|`proxyaddress`|<span data-ttu-id="58793-119">프록시를 사용 하는 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-119">Specifies the proxy URI to use.</span></span>|  
|`scriptLocation`|<span data-ttu-id="58793-120">구성 스크립트의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-120">Specifies the location of the configuration script.</span></span> <span data-ttu-id="58793-121">사용 하지 마십시오는 `bypassonlocal` 이 특성을 사용 하 여 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="58793-121">Do not use the `bypassonlocal` attribute with this attribute.</span></span> |  
|`usesystemdefault`|<span data-ttu-id="58793-122">Internet Explorer 프록시 설정을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-122">Specifies whether to use Internet Explorer proxy settings.</span></span> <span data-ttu-id="58793-123">경우 설정 `true`, 후속 특성에는 Internet Explorer 프록시 설정이 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58793-123">If set to `true`, subsequent attributes will override Internet Explorer proxy settings.</span></span> <span data-ttu-id="58793-124">기본값은 `unspecified`입니다.</span><span class="sxs-lookup"><span data-stu-id="58793-124">The default value is `unspecified`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="58793-125">자식 요소</span><span class="sxs-lookup"><span data-stu-id="58793-125">Child Elements</span></span>  
 <span data-ttu-id="58793-126">없음</span><span class="sxs-lookup"><span data-stu-id="58793-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="58793-127">부모 요소</span><span class="sxs-lookup"><span data-stu-id="58793-127">Parent Elements</span></span>  
  
|<span data-ttu-id="58793-128">**요소**</span><span class="sxs-lookup"><span data-stu-id="58793-128">**Element**</span></span>|<span data-ttu-id="58793-129">**설명**</span><span class="sxs-lookup"><span data-stu-id="58793-129">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="58793-130">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="58793-130">defaultProxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|<span data-ttu-id="58793-131">HTTP(Hypertext Transfer Protocol) 프록시 서버를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-131">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
  
## <a name="text-value"></a><span data-ttu-id="58793-132">텍스트 값</span><span class="sxs-lookup"><span data-stu-id="58793-132">Text Value</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58793-133">설명</span><span class="sxs-lookup"><span data-stu-id="58793-133">Remarks</span></span>  
 <span data-ttu-id="58793-134">`proxy` 요소는 응용 프로그램에 대 한 프록시 서버를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-134">The `proxy` element defines a proxy server for an application.</span></span> <span data-ttu-id="58793-135">이 요소가 구성 파일에서 누락 된.NET Framework Internet Explorer에서 프록시 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-135">If this element is missing from the configuration file, then the .NET Framework will use the proxy settings in Internet Explorer.</span></span>  
  
 <span data-ttu-id="58793-136">값을 `proxyaddress` 특성을 제대로 구성 된 리소스 URI (Uniform Indicator) 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-136">The value for the `proxyaddress` attribute should be a well-formed Uniform Resource Indicator (URI).</span></span>  
  
 <span data-ttu-id="58793-137">`scriptLocation` 특성이 프록시 구성 스크립트의 자동 검색을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-137">The `scriptLocation` attribute refers to the automatic detection of proxy configuration scripts.</span></span> <span data-ttu-id="58793-138"><xref:System.Net.WebProxy> 클래스는 구성 스크립트 (일반적으로 명명 된 Wpad.dat)를 경우 찾으려고 시도 합니다 **자동 구성 스크립트를 사용 하 여** Internet Explorer에서 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-138">The <xref:System.Net.WebProxy> class will attempt to locate a configuration script (usually named Wpad.dat) when the **Use automatic configuration script** option is selected in Internet Explorer.</span></span> <span data-ttu-id="58793-139">하는 경우 `bypassonlocal` 모든 값으로 설정 되어 `scriptLocation` 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58793-139">If `bypassonlocal` is set to any value, `scriptLocation` is ignored.</span></span>
  
 <span data-ttu-id="58793-140">사용 된 `usesystemdefault` 버전 2.0으로 마이그레이션 중인.NET Framework 버전 1.1 응용 프로그램에 대 한 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="58793-140">Use the `usesystemdefault` attribute for .NET Framework version 1.1 applications that are migrating to version 2.0.</span></span>  
  
 <span data-ttu-id="58793-141">예외가 발생 하는 경우는 `proxyaddress` 특성에 잘못 된 기본 프록시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-141">An exception is thrown if the `proxyaddress` attribute specifies an invalid default proxy.</span></span> <span data-ttu-id="58793-142">예외의 <xref:System.Exception.InnerException%2A> 속성에는 오류의 근본 원인에 대한 추가 정보가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-142">The <xref:System.Exception.InnerException%2A> property on the exception should have more information about the root cause of the error.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="58793-143">구성 파일</span><span class="sxs-lookup"><span data-stu-id="58793-143">Configuration Files</span></span>  
 <span data-ttu-id="58793-144">이 요소는 응용 프로그램 구성 파일 또는 컴퓨터 구성 파일(Machine.config)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58793-144">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="58793-145">예제</span><span class="sxs-lookup"><span data-stu-id="58793-145">Example</span></span>  
 <span data-ttu-id="58793-146">다음 예제에서는 Internet Explorer 프록시의 기본값을 사용 하 여 프록시 주소를 지정 하며 로컬 액세스에 대 한 프록시를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58793-146">The following example uses the defaults from the Internet Explorer proxy, specifies the proxy address, and bypasses the proxy for local access.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <proxy  
        usesystemdefault="true"  
        proxyaddress="http://192.168.1.10:3128"  
        bypassonlocal="true"  
      />  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="58793-147">참고 항목</span><span class="sxs-lookup"><span data-stu-id="58793-147">See Also</span></span>  
 <xref:System.Net.WebProxy?displayProperty=nameWithType>  
 [<span data-ttu-id="58793-148">네트워크 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="58793-148">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
