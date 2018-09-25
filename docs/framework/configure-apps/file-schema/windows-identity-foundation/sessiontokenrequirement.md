---
title: '&lt;sessionTokenRequirement&gt;'
ms.date: 03/30/2017
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
author: BrucePerlerMS
ms.openlocfilehash: 4d5d2348f04ace7596a3a513c5106ea612dc17b7
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47070094"
---
# <a name="ltsessiontokenrequirementgt"></a><span data-ttu-id="ae483-102">&lt;sessionTokenRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="ae483-102">&lt;sessionTokenRequirement&gt;</span></span>
<span data-ttu-id="ae483-103">에 대 한 구성을 제공 합니다 <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> 클래스나 파생된 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="ae483-103">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="ae483-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="ae483-104">\<system.identityModel></span></span>  
<span data-ttu-id="ae483-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="ae483-105">\<identityConfiguration></span></span>  
<span data-ttu-id="ae483-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="ae483-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="ae483-107">\<add></span><span class="sxs-lookup"><span data-stu-id="ae483-107">\<add></span></span>  
<span data-ttu-id="ae483-108">\<sessionTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="ae483-108">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae483-109">구문</span><span class="sxs-lookup"><span data-stu-id="ae483-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ae483-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ae483-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ae483-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ae483-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ae483-112">특성</span><span class="sxs-lookup"><span data-stu-id="ae483-112">Attributes</span></span>  
  
|<span data-ttu-id="ae483-113">특성</span><span class="sxs-lookup"><span data-stu-id="ae483-113">Attribute</span></span>|<span data-ttu-id="ae483-114">설명</span><span class="sxs-lookup"><span data-stu-id="ae483-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ae483-115">수명(lifetime)</span><span class="sxs-lookup"><span data-stu-id="ae483-115">lifetime</span></span>|<span data-ttu-id="ae483-116">세션 토큰의 수명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae483-116">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ae483-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ae483-117">Child Elements</span></span>  
 <span data-ttu-id="ae483-118">없음</span><span class="sxs-lookup"><span data-stu-id="ae483-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ae483-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ae483-119">Parent Elements</span></span>  
  
|<span data-ttu-id="ae483-120">요소</span><span class="sxs-lookup"><span data-stu-id="ae483-120">Element</span></span>|<span data-ttu-id="ae483-121">설명</span><span class="sxs-lookup"><span data-stu-id="ae483-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ae483-122">\<add></span><span class="sxs-lookup"><span data-stu-id="ae483-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="ae483-123">토큰 처리기 컬렉션에 지정 된 보안 토큰 처리기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ae483-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ae483-124">예제</span><span class="sxs-lookup"><span data-stu-id="ae483-124">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
