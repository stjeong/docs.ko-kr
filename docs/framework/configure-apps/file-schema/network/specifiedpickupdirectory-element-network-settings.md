---
title: '&lt;specifiedPickupDirectory&gt; 요소 (네트워크 설정)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#specifiedPickupDirectory
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp/specifiedPickupDirectory
helpviewer_keywords:
- specifiedPickupDirectory element
- <specifiedPickupDirectory> element
ms.assetid: 0121f49d-bff2-4bc6-af06-f1628dcd61f1
author: mcleblanc
ms.author: markl
ms.openlocfilehash: b62dc1a9118f7d4f1f693ade36626deaecd23999
ms.sourcegitcommit: daa8788af67ac2d1cecd24f9f3409babb2f978c9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47863652"
---
# <a name="ltspecifiedpickupdirectorygt-element-network-settings"></a><span data-ttu-id="dad50-102">&lt;specifiedPickupDirectory&gt; 요소 (네트워크 설정)</span><span class="sxs-lookup"><span data-stu-id="dad50-102">&lt;specifiedPickupDirectory&gt; Element (Network Settings)</span></span>
<span data-ttu-id="dad50-103">전송 프로토콜 SMTP (Simple Mail) 서버에 대 한 로컬 디렉터리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="dad50-103">Configures the local directory for a Simple Mail Transport Protocol (SMTP) server.</span></span>  
  
 <span data-ttu-id="dad50-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dad50-104">\<configuration></span></span>  
<span data-ttu-id="dad50-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="dad50-105">\<system.net></span></span>  
<span data-ttu-id="dad50-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="dad50-106">\<mailSettings></span></span>  
<span data-ttu-id="dad50-107">\<smtp></span><span class="sxs-lookup"><span data-stu-id="dad50-107">\<smtp></span></span>  
<span data-ttu-id="dad50-108">\<specifiedPickupDirectory></span><span class="sxs-lookup"><span data-stu-id="dad50-108">\<specifiedPickupDirectory></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dad50-109">구문</span><span class="sxs-lookup"><span data-stu-id="dad50-109">Syntax</span></span>  
  
```xml  
<specifiedPickupDirectory  
  pickupDirectoryLocation="directory"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dad50-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="dad50-110">Attributes and Elements</span></span>  
 <span data-ttu-id="dad50-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dad50-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dad50-112">특성</span><span class="sxs-lookup"><span data-stu-id="dad50-112">Attributes</span></span>  
  
|<span data-ttu-id="dad50-113">특성</span><span class="sxs-lookup"><span data-stu-id="dad50-113">Attribute</span></span>|<span data-ttu-id="dad50-114">설명</span><span class="sxs-lookup"><span data-stu-id="dad50-114">Description</span></span>|  
|---------------|-----------------|  
|`pickupDirectoryLocation`|<span data-ttu-id="dad50-115">응용 프로그램에서 SMTP 서버에서 나중에 처리할 전자 메일을 저장할 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="dad50-115">The directory where applications save email for later processing by the SMTP server.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dad50-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="dad50-116">Child Elements</span></span>  
 <span data-ttu-id="dad50-117">없음</span><span class="sxs-lookup"><span data-stu-id="dad50-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dad50-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="dad50-118">Parent Elements</span></span>  
  
|<span data-ttu-id="dad50-119">요소</span><span class="sxs-lookup"><span data-stu-id="dad50-119">Element</span></span>|<span data-ttu-id="dad50-120">설명</span><span class="sxs-lookup"><span data-stu-id="dad50-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dad50-121">\<smtp > 요소 (네트워크 설정)</span><span class="sxs-lookup"><span data-stu-id="dad50-121">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="dad50-122">단순 메일 전송 프로토콜 (SMTP) 메일 보내기 옵션을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad50-122">Configures Simple Mail Transport Protocol (SMTP) mail sending options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dad50-123">설명</span><span class="sxs-lookup"><span data-stu-id="dad50-123">Remarks</span></span>  
 <span data-ttu-id="dad50-124">`specifiedPickupDirectory` 특성은 응용 프로그램이 SMTP 서버에서 처리할 수 있도록 메일 메시지를 저장하는 디렉터리를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad50-124">The `specifiedPickupDirectory` attribute sets the directory where applications save mail messages to be processed by the SMTP server.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dad50-125">예제</span><span class="sxs-lookup"><span data-stu-id="dad50-125">Example</span></span>  
 <span data-ttu-id="dad50-126">다음 예제에서는 메일 픽업 디렉터리로 c:\maildrop를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dad50-126">The following example specifies c:\maildrop as the mail pickup directory.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="SpecifiedPickupDirectory">  
        <specifiedPickupDirectory  
          pickupDirectoryLocation="c:\maildrop"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dad50-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dad50-127">See Also</span></span>  
 <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.SmtpSpecifiedPickupDirectoryElement?displayProperty=nameWithType>  
 [<span data-ttu-id="dad50-128">네트워크 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="dad50-128">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
