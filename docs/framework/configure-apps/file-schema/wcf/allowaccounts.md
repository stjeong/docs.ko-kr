---
title: '&lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: c1c4630e6191dbbe02688a4e4a9db9e18b8d36d2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508420"
---
# <a name="ltallowaccountsgt"></a><span data-ttu-id="de53e-102">&lt;allowAccounts&gt;</span><span class="sxs-lookup"><span data-stu-id="de53e-102">&lt;allowAccounts&gt;</span></span>
<span data-ttu-id="de53e-103">사용자 호스트 하는 Windows Communication Foundation (WCF) 서비스 프로세스에 대 한 계정 및 공유 서비스에 대 한 연결 액세스를 부여 하는 지정 하는 구성 요소의 컬렉션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="de53e-103">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="de53e-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="de53e-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de53e-105">구문</span><span class="sxs-lookup"><span data-stu-id="de53e-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="de53e-106">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="de53e-106">Attributes and Elements</span></span>  
 <span data-ttu-id="de53e-107">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="de53e-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="de53e-108">특성</span><span class="sxs-lookup"><span data-stu-id="de53e-108">Attributes</span></span>  
 <span data-ttu-id="de53e-109">없음</span><span class="sxs-lookup"><span data-stu-id="de53e-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="de53e-110">자식 요소</span><span class="sxs-lookup"><span data-stu-id="de53e-110">Child Elements</span></span>  
  
|<span data-ttu-id="de53e-111">특성</span><span class="sxs-lookup"><span data-stu-id="de53e-111">Attribute</span></span>|<span data-ttu-id="de53e-112">설명</span><span class="sxs-lookup"><span data-stu-id="de53e-112">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="de53e-113">\<add></span><span class="sxs-lookup"><span data-stu-id="de53e-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="de53e-114">WCF 서비스를 호스팅하고 공유 서비스에 대 한 연결 액세스 권한이 부여 된 프로세스에 대 한 사용자 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="de53e-114">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="de53e-115">부모 요소</span><span class="sxs-lookup"><span data-stu-id="de53e-115">Parent Elements</span></span>  
  
|<span data-ttu-id="de53e-116">요소</span><span class="sxs-lookup"><span data-stu-id="de53e-116">Element</span></span>|<span data-ttu-id="de53e-117">설명</span><span class="sxs-lookup"><span data-stu-id="de53e-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="de53e-118">[\<net. pipe >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) 나 [ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="de53e-118">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="de53e-119">Net Pipe 또는 TCP 공유 서비스의 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de53e-119">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="de53e-120">참고자료</span><span class="sxs-lookup"><span data-stu-id="de53e-120">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
