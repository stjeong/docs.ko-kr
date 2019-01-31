---
title: <remove>
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: a54957458311e2d5941d1aa1c2486a2f66994d9b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288134"
---
# <a name="remove"></a><span data-ttu-id="2589d-101">\<remove></span><span class="sxs-lookup"><span data-stu-id="2589d-101">\<remove></span></span>
<span data-ttu-id="2589d-102">토큰 처리기 컬렉션에서 지정 된 보안 토큰 처리기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-102">Removes the specified security token handler from the token handler collection.</span></span>  
  
 <span data-ttu-id="2589d-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="2589d-103">\<system.identityModel></span></span>  
<span data-ttu-id="2589d-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="2589d-104">\<identityConfiguration></span></span>  
<span data-ttu-id="2589d-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="2589d-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="2589d-106">\<remove></span><span class="sxs-lookup"><span data-stu-id="2589d-106">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2589d-107">구문</span><span class="sxs-lookup"><span data-stu-id="2589d-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <remove type=xs:string >  
      </remove>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2589d-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="2589d-108">Attributes and Elements</span></span>  
 <span data-ttu-id="2589d-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2589d-110">특성</span><span class="sxs-lookup"><span data-stu-id="2589d-110">Attributes</span></span>  
  
|<span data-ttu-id="2589d-111">특성</span><span class="sxs-lookup"><span data-stu-id="2589d-111">Attribute</span></span>|<span data-ttu-id="2589d-112">설명</span><span class="sxs-lookup"><span data-stu-id="2589d-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2589d-113">형식</span><span class="sxs-lookup"><span data-stu-id="2589d-113">type</span></span>|<span data-ttu-id="2589d-114">제거할 토큰 처리기의 CLR 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-114">The CLR type name of the token handler to be removed.</span></span> <span data-ttu-id="2589d-115">지정 하는 방법에 대 한 자세한 내용은 합니다 `type` 특성을 참조 하십시오 [사용자 지정 형식 참조](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24)합니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-115">For more information about how to specify the `type` attribute, see [Custom Type References](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24).</span></span> <span data-ttu-id="2589d-116">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="2589d-116">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2589d-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="2589d-117">Child Elements</span></span>  
 <span data-ttu-id="2589d-118">없음</span><span class="sxs-lookup"><span data-stu-id="2589d-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2589d-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="2589d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="2589d-120">요소</span><span class="sxs-lookup"><span data-stu-id="2589d-120">Element</span></span>|<span data-ttu-id="2589d-121">설명</span><span class="sxs-lookup"><span data-stu-id="2589d-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2589d-122">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="2589d-122">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="2589d-123">끝점을 사용 하 여 등록 된 보안 토큰 처리기 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-123">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="2589d-124">예제</span><span class="sxs-lookup"><span data-stu-id="2589d-124">Example</span></span>  
 <span data-ttu-id="2589d-125">다음 XML의 사용을 보여 줍니다.는 `<add>` 및 `<remove>` 사용자 지정 세션 토큰 처리기를 사용 하 여 기본 세션 토큰 처리기를 바꿀 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-125">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="2589d-126">XML에서 가져온 것은 `ClaimsAwareWebFarm` 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="2589d-126">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
