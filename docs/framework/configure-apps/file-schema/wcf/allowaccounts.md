---
title: '&lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: 61310d530cfec2862fb64155777cd0e88132f748
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145941"
---
# <a name="ltallowaccountsgt"></a><span data-ttu-id="edaee-102">&lt;allowAccounts&gt;</span><span class="sxs-lookup"><span data-stu-id="edaee-102">&lt;allowAccounts&gt;</span></span>
<span data-ttu-id="edaee-103">사용자 호스트 하는 Windows Communication Foundation (WCF) 서비스 프로세스에 대 한 계정 및 공유 서비스에 대 한 연결 액세스를 부여 하는 지정 하는 구성 요소의 컬렉션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="edaee-103">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="edaee-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="edaee-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="edaee-105">구문</span><span class="sxs-lookup"><span data-stu-id="edaee-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="edaee-106">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="edaee-106">Attributes and Elements</span></span>  
 <span data-ttu-id="edaee-107">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="edaee-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="edaee-108">특성</span><span class="sxs-lookup"><span data-stu-id="edaee-108">Attributes</span></span>  
 <span data-ttu-id="edaee-109">없음</span><span class="sxs-lookup"><span data-stu-id="edaee-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="edaee-110">자식 요소</span><span class="sxs-lookup"><span data-stu-id="edaee-110">Child Elements</span></span>  
  
|<span data-ttu-id="edaee-111">특성</span><span class="sxs-lookup"><span data-stu-id="edaee-111">Attribute</span></span>|<span data-ttu-id="edaee-112">설명</span><span class="sxs-lookup"><span data-stu-id="edaee-112">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="edaee-113">\<add></span><span class="sxs-lookup"><span data-stu-id="edaee-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="edaee-114">WCF 서비스를 호스팅하고 공유 서비스에 대 한 연결 액세스 권한이 부여 된 프로세스에 대 한 사용자 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="edaee-114">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="edaee-115">부모 요소</span><span class="sxs-lookup"><span data-stu-id="edaee-115">Parent Elements</span></span>  
  
|<span data-ttu-id="edaee-116">요소</span><span class="sxs-lookup"><span data-stu-id="edaee-116">Element</span></span>|<span data-ttu-id="edaee-117">설명</span><span class="sxs-lookup"><span data-stu-id="edaee-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="edaee-118">[\<net. pipe >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) 나 [ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="edaee-118">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="edaee-119">Net Pipe 또는 TCP 공유 서비스의 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="edaee-119">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="edaee-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="edaee-120">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
