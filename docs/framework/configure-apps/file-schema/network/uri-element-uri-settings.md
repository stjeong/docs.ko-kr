---
title: '&lt;Uri&gt; 요소 (Uri 설정)'
ms.date: 03/30/2017
ms.assetid: c22bab8b-477c-4ae4-8498-65ad409e0847
ms.openlocfilehash: 3663fdc995be216351a1ce49ae86e5067d64144f
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50035868"
---
# <a name="lturigt-element-uri-settings"></a><span data-ttu-id="a44a2-102">&lt;Uri&gt; 요소 (Uri 설정)</span><span class="sxs-lookup"><span data-stu-id="a44a2-102">&lt;Uri&gt; Element (Uri Settings)</span></span>
<span data-ttu-id="a44a2-103">.NET Framework uniform resource identifier (Uri)를 사용 하 여 표현 하는 웹 주소를 처리 하는 방법을 지정 하는 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-103">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>  
  
## <a name="schema-hierarchy"></a><span data-ttu-id="a44a2-104">스키마 계층 구조</span><span class="sxs-lookup"><span data-stu-id="a44a2-104">Schema Hierarchy</span></span>  
 [<span data-ttu-id="a44a2-105">\<configuration> 요소</span><span class="sxs-lookup"><span data-stu-id="a44a2-105">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="a44a2-106">\<uri ></span><span class="sxs-lookup"><span data-stu-id="a44a2-106">\<uri></span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
## <a name="syntax"></a><span data-ttu-id="a44a2-107">구문</span><span class="sxs-lookup"><span data-stu-id="a44a2-107">Syntax</span></span>  
  
```xml  
<uri>  
</uri>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a44a2-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a44a2-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a44a2-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a44a2-110">특성</span><span class="sxs-lookup"><span data-stu-id="a44a2-110">Attributes</span></span>  
 <span data-ttu-id="a44a2-111">없음</span><span class="sxs-lookup"><span data-stu-id="a44a2-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a44a2-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a44a2-112">Child Elements</span></span>  
  
|<span data-ttu-id="a44a2-113">**요소**</span><span class="sxs-lookup"><span data-stu-id="a44a2-113">**Element**</span></span>|<span data-ttu-id="a44a2-114">**설명**</span><span class="sxs-lookup"><span data-stu-id="a44a2-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="a44a2-115">idn</span><span class="sxs-lookup"><span data-stu-id="a44a2-115">idn</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/idn-element-uri-settings.md)|<span data-ttu-id="a44a2-116">IDN(Internationalized Domain Name) 구문 분석이 도메인 이름에 적용되는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-116">Specifies if Internationalized Domain Name (IDN) parsing is applied to domain names.</span></span>|  
|[<span data-ttu-id="a44a2-117">iriParsing</span><span class="sxs-lookup"><span data-stu-id="a44a2-117">iriParsing</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/iriparsing-element-uri-settings.md)|<span data-ttu-id="a44a2-118">식별자 IRI (International Resource) 구문 분석에 적용 됩니다 지정 <xref:System.Uri> IRI 구문 분석 규칙을 적용 해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-118">Specifies if International Resource Identifier (IRI) parsing is applied to <xref:System.Uri> and whether IRI parsing rules should be applied.</span></span>|  
|[<span data-ttu-id="a44a2-119">schemeSettings</span><span class="sxs-lookup"><span data-stu-id="a44a2-119">schemeSettings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|<span data-ttu-id="a44a2-120">특정 체계에 대해 <xref:System.Uri>가 구문 분석되는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-120">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a44a2-121">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a44a2-121">Parent Elements</span></span>  
  
|<span data-ttu-id="a44a2-122">**요소**</span><span class="sxs-lookup"><span data-stu-id="a44a2-122">**Element**</span></span>|<span data-ttu-id="a44a2-123">**설명**</span><span class="sxs-lookup"><span data-stu-id="a44a2-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="a44a2-124">구성</span><span class="sxs-lookup"><span data-stu-id="a44a2-124">configuration</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="a44a2-125">모든 네임 스페이스에 대 한 설정을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-125">Contains settings for all namespaces.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a44a2-126">설명</span><span class="sxs-lookup"><span data-stu-id="a44a2-126">Remarks</span></span>  
 <span data-ttu-id="a44a2-127">`uri` 요소 멤버에 대 한 설정을 포함 합니다 <xref:System.Uri> 클래스에 의해 사용 되는 클래스는 <xref:System.Net> 네임 스페이스.</span><span class="sxs-lookup"><span data-stu-id="a44a2-127">The `uri` element contains settings for members of the <xref:System.Uri> class used by classes in the <xref:System.Net> namespace.</span></span> <span data-ttu-id="a44a2-128">이 설정은 IRI 및 IDN에 대 한 지원을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-128">The settings configure support for IRI and IDN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a44a2-129">예제</span><span class="sxs-lookup"><span data-stu-id="a44a2-129">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="a44a2-130">설명</span><span class="sxs-lookup"><span data-stu-id="a44a2-130">Description</span></span>  
 <span data-ttu-id="a44a2-131">다음 예제에서 사용 하는 구성을 보여 줍니다는 <xref:System.Uri> IRI 구문 분석 및 IDN 이름이 지원 되는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-131">The following example shows a configuration used by the <xref:System.Uri> class to support IRI parsing and IDN names.</span></span> <span data-ttu-id="a44a2-132">이 예제에서는 모든 스키마 설정을 지웁니다 및 http 체계에 대 한 백분율로 인코딩된 경로 구분 기호를 이스케이프 하지 않아도 되도록 하는 것에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a44a2-132">The example also clears all scheme settings and then adds support for not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
### <a name="code"></a><span data-ttu-id="a44a2-133">코드</span><span class="sxs-lookup"><span data-stu-id="a44a2-133">Code</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
    <schemeSettings>  
      <clear/>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a44a2-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a44a2-134">See Also</span></span>  
 [<span data-ttu-id="a44a2-135">네트워크 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="a44a2-135">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
