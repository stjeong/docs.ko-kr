---
title: <sessionTokenRequirement>
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 0c575e02862884e8f7ecf062138c36fe731f8e19
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271904"
---
# <a name="sessiontokenrequirement"></a><span data-ttu-id="da465-101">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="da465-101">\<sessionTokenRequirement></span></span>
<span data-ttu-id="da465-102">에 대 한 구성을 제공 합니다 <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> 클래스나 파생된 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="da465-102">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="da465-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="da465-103">\<system.identityModel></span></span>  
<span data-ttu-id="da465-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="da465-104">\<identityConfiguration></span></span>  
<span data-ttu-id="da465-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="da465-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="da465-106">\<add></span><span class="sxs-lookup"><span data-stu-id="da465-106">\<add></span></span>  
<span data-ttu-id="da465-107">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="da465-107">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da465-108">구문</span><span class="sxs-lookup"><span data-stu-id="da465-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">  
        <sessionTokenRequirement lifetime=TimeSpan >  
        </sessionTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="da465-109">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="da465-109">Attributes and Elements</span></span>  
 <span data-ttu-id="da465-110">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="da465-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="da465-111">특성</span><span class="sxs-lookup"><span data-stu-id="da465-111">Attributes</span></span>  
  
|<span data-ttu-id="da465-112">특성</span><span class="sxs-lookup"><span data-stu-id="da465-112">Attribute</span></span>|<span data-ttu-id="da465-113">설명</span><span class="sxs-lookup"><span data-stu-id="da465-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="da465-114">수명(lifetime)</span><span class="sxs-lookup"><span data-stu-id="da465-114">lifetime</span></span>|<span data-ttu-id="da465-115">세션 토큰의 수명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="da465-115">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="da465-116">자식 요소</span><span class="sxs-lookup"><span data-stu-id="da465-116">Child Elements</span></span>  
 <span data-ttu-id="da465-117">없음</span><span class="sxs-lookup"><span data-stu-id="da465-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="da465-118">부모 요소</span><span class="sxs-lookup"><span data-stu-id="da465-118">Parent Elements</span></span>  
  
|<span data-ttu-id="da465-119">요소</span><span class="sxs-lookup"><span data-stu-id="da465-119">Element</span></span>|<span data-ttu-id="da465-120">설명</span><span class="sxs-lookup"><span data-stu-id="da465-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="da465-121">\<add></span><span class="sxs-lookup"><span data-stu-id="da465-121">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="da465-122">토큰 처리기 컬렉션에 지정 된 보안 토큰 처리기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="da465-122">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="da465-123">예제</span><span class="sxs-lookup"><span data-stu-id="da465-123">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
