---
title: '&lt;allowAccounts&gt;의 &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 763c7b1f-e7b0-4d99-a42c-4506fcb8da00
ms.openlocfilehash: 63f8e678b81838a25664180888e9e7a8eabd043d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722006"
---
# <a name="ltaddgt-of-ltallowaccountsgt"></a><span data-ttu-id="4d1af-102">&lt;allowAccounts&gt;의 &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="4d1af-102">&lt;add&gt; of &lt;allowAccounts&gt;</span></span>
<span data-ttu-id="4d1af-103">WCF 서비스를 호스팅하고 공유 서비스에 대 한 연결 액세스 권한이 부여 된 프로세스에 대 한 사용자 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1af-103">Specifies a user account for processes that host WCF services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="4d1af-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="4d1af-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d1af-105">구문</span><span class="sxs-lookup"><span data-stu-id="4d1af-105">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4d1af-106">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4d1af-106">Attributes and Elements</span></span>  
 <span data-ttu-id="4d1af-107">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1af-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4d1af-108">특성</span><span class="sxs-lookup"><span data-stu-id="4d1af-108">Attributes</span></span>  
  
|<span data-ttu-id="4d1af-109">특성</span><span class="sxs-lookup"><span data-stu-id="4d1af-109">Attribute</span></span>|<span data-ttu-id="4d1af-110">설명</span><span class="sxs-lookup"><span data-stu-id="4d1af-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4d1af-111">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="4d1af-111">securityIdentifier</span></span>|<span data-ttu-id="4d1af-112">사용자 계정을 식별하는 데 사용하는 고유 식별자를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1af-112">A string that specifies a unique identifier used to identify a user account.</span></span> <span data-ttu-id="4d1af-113">반환되는 기본값은 LocalSystem, Administrators, NS, LS 및 IIS_USRS입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1af-113">The default values are LocalSystem, Administrators, NS, LS, and IIS_USRS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4d1af-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4d1af-114">Child Elements</span></span>  
 <span data-ttu-id="4d1af-115">없음</span><span class="sxs-lookup"><span data-stu-id="4d1af-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4d1af-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4d1af-116">Parent Elements</span></span>  
  
|<span data-ttu-id="4d1af-117">요소</span><span class="sxs-lookup"><span data-stu-id="4d1af-117">Element</span></span>|<span data-ttu-id="4d1af-118">설명</span><span class="sxs-lookup"><span data-stu-id="4d1af-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4d1af-119">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="4d1af-119">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="4d1af-120">포함 된 구성 요소의 컬렉션을 `securityIdentifier` WCF 서비스를 호스팅하고 공유 서비스에 대 한 연결 액세스 권한이 부여 된 프로세스에 대 한 사용자 계정을 지정 하는 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="4d1af-120">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="4d1af-121">예제</span><span class="sxs-lookup"><span data-stu-id="4d1af-121">Example</span></span>  
 <span data-ttu-id="4d1af-122">다음 구성 예제에서는 사용자 계정에 대한 다섯 가지 기본 식별자를 이 컬렉션에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4d1af-122">The following configuration example adds the five default identifiers for user accounts to this collection.</span></span>  
  
```xml  
<allowAccounts>
  <!-- LocalSystem account -->
  <add securityIdentifier="S-1-5-18" />
  <!-- LocalService account -->
  <add securityIdentifier="S-1-5-19" />
  <!-- Administrators account -->
  <add securityIdentifier="S-1-5-20" />
  <!-- Network Service account -->
  <add securityIdentifier="S-1-5-32-544" />
  <!-- IIS_IUSRS account (Vista only) -->
  <add securityIdentifier="S-1-5-32-568" />
</allowAccounts>
```  
  
## <a name="see-also"></a><span data-ttu-id="4d1af-123">참고자료</span><span class="sxs-lookup"><span data-stu-id="4d1af-123">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
