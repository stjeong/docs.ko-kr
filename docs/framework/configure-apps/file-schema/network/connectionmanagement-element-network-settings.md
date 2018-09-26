---
title: '&lt;connectionManagement&gt; 요소 (네트워크 설정)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/connectionManagement
- http://schemas.microsoft.com/.NetConfiguration/v2.0#connectionManagement
helpviewer_keywords:
- <connectionManagement> element
- connectionManagement element
ms.assetid: bedccaab-12a2-4511-8f67-e961f249aec6
author: mcleblanc
ms.author: markl
ms.openlocfilehash: bc0b75db5b3f35087df70c9155a1ba3b39ceae4d
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47205985"
---
# <a name="ltconnectionmanagementgt-element-network-settings"></a><span data-ttu-id="22f6b-102">&lt;connectionManagement&gt; 요소 (네트워크 설정)</span><span class="sxs-lookup"><span data-stu-id="22f6b-102">&lt;connectionManagement&gt; Element (Network Settings)</span></span>
<span data-ttu-id="22f6b-103">네트워크 호스트에 대한 최대 연결 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-103">Specifies the maximum number of connections to a network host.</span></span>  
  
 <span data-ttu-id="22f6b-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="22f6b-104">\<configuration></span></span>  
<span data-ttu-id="22f6b-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="22f6b-105">\<system.net></span></span>  
<span data-ttu-id="22f6b-106">\<connectionManagement ></span><span class="sxs-lookup"><span data-stu-id="22f6b-106">\<connectionManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22f6b-107">구문</span><span class="sxs-lookup"><span data-stu-id="22f6b-107">Syntax</span></span>  
  
```xml  
<connectionManagement>   
</connectionManagement>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="22f6b-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="22f6b-108">Attributes and Elements</span></span>  
 <span data-ttu-id="22f6b-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="22f6b-110">특성</span><span class="sxs-lookup"><span data-stu-id="22f6b-110">Attributes</span></span>  
 <span data-ttu-id="22f6b-111">없음</span><span class="sxs-lookup"><span data-stu-id="22f6b-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="22f6b-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="22f6b-112">Child Elements</span></span>  
  
|<span data-ttu-id="22f6b-113">**요소**</span><span class="sxs-lookup"><span data-stu-id="22f6b-113">**Element**</span></span>|<span data-ttu-id="22f6b-114">**설명**</span><span class="sxs-lookup"><span data-stu-id="22f6b-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="22f6b-115">add</span><span class="sxs-lookup"><span data-stu-id="22f6b-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="22f6b-116">연결 관리 목록에 IP 주소 또는 DNS 이름을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-116">Adds an IP address or DNS name to the connection management list.</span></span>|  
|[<span data-ttu-id="22f6b-117">clear</span><span class="sxs-lookup"><span data-stu-id="22f6b-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="22f6b-118">연결 관리 목록을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-118">Clears the connection management list.</span></span>|  
|[<span data-ttu-id="22f6b-119">remove</span><span class="sxs-lookup"><span data-stu-id="22f6b-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="22f6b-120">연결 관리 목록에서 IP 주소 또는 DNS 이름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-120">Removes an IP address or DNS name from the connection management list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="22f6b-121">부모 요소</span><span class="sxs-lookup"><span data-stu-id="22f6b-121">Parent Elements</span></span>  
  
|<span data-ttu-id="22f6b-122">**요소**</span><span class="sxs-lookup"><span data-stu-id="22f6b-122">**Element**</span></span>|<span data-ttu-id="22f6b-123">**설명**</span><span class="sxs-lookup"><span data-stu-id="22f6b-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="22f6b-124">system.net</span><span class="sxs-lookup"><span data-stu-id="22f6b-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="22f6b-125">.NET Framework의 네트워크 연결 방법을 지정하는 설정을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="22f6b-126">설명</span><span class="sxs-lookup"><span data-stu-id="22f6b-126">Remarks</span></span>  
 <span data-ttu-id="22f6b-127">`connectionManagement` 요소 서버나 서버 그룹을 연결의 최대 수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-127">The `connectionManagement` element defines the maximum number of connections to a server or group of servers.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="22f6b-128">구성 파일</span><span class="sxs-lookup"><span data-stu-id="22f6b-128">Configuration Files</span></span>  
 <span data-ttu-id="22f6b-129">이 요소는 응용 프로그램 구성 파일 또는 컴퓨터 구성 파일(Machine.config)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="22f6b-130">예제</span><span class="sxs-lookup"><span data-stu-id="22f6b-130">Example</span></span>  
 <span data-ttu-id="22f6b-131">다음 예제에서는 www.contoso.com 서버에 대 한 연결 4 및 다른 모든 서버에 두 개의 연결을 사용 하도록 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6b-131">The following example configures an application to use four connections to the server www.contoso.com and two connections to all other servers.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <connectionManagement>  
      <add address = "http://www.contoso.com" maxconnection = "4" />  
      <add address = "*" maxconnection = "2" />  
    </connectionManagement>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="22f6b-132">참고 항목</span><span class="sxs-lookup"><span data-stu-id="22f6b-132">See Also</span></span>  
 <xref:System.Net.ServicePoint>  
 <xref:System.Net.ServicePointManager>  
 [<span data-ttu-id="22f6b-133">네트워크 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="22f6b-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
