---
title: '&lt;dependentAssembly&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly
- http://schemas.microsoft.com/.NetConfiguration/v2.0#dependentAssembly
helpviewer_keywords:
- container tags, <dependentAssembly> element
- dependentAssembly element
- <dependentAssembly> element
ms.assetid: 14e95627-dd79-4b82-ac85-e682aa3a31d8
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5b0d3bfb7e4db2fec39f37c9fb794731cdf5bbc
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53613299"
---
# <a name="ltdependentassemblygt-element"></a><span data-ttu-id="bad8c-102">&lt;dependentAssembly&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="bad8c-102">&lt;dependentAssembly&gt; Element</span></span>
<span data-ttu-id="bad8c-103">각 어셈블리에 대한 바인딩 정책 및 어셈블리 위치를 캡슐화합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-103">Encapsulates binding policy and assembly location for each assembly.</span></span> <span data-ttu-id="bad8c-104">하나를 사용 하 여 `dependentAssembly` 각 어셈블리에 대 한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-104">Use one `dependentAssembly` element for each assembly.</span></span>  
  
 <span data-ttu-id="bad8c-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="bad8c-105">\<configuration></span></span>  
<span data-ttu-id="bad8c-106">\<runtime></span><span class="sxs-lookup"><span data-stu-id="bad8c-106">\<runtime></span></span>  
<span data-ttu-id="bad8c-107">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="bad8c-107">\<assemblyBinding></span></span>  
<span data-ttu-id="bad8c-108">\<dependentAssembly ></span><span class="sxs-lookup"><span data-stu-id="bad8c-108">\<dependentAssembly></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bad8c-109">구문</span><span class="sxs-lookup"><span data-stu-id="bad8c-109">Syntax</span></span>  
  
```xml  
<dependentAssembly>   
</dependentAssembly>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bad8c-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="bad8c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="bad8c-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bad8c-112">특성</span><span class="sxs-lookup"><span data-stu-id="bad8c-112">Attributes</span></span>  
 <span data-ttu-id="bad8c-113">없음</span><span class="sxs-lookup"><span data-stu-id="bad8c-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="bad8c-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="bad8c-114">Child Elements</span></span>  
  
|<span data-ttu-id="bad8c-115">요소</span><span class="sxs-lookup"><span data-stu-id="bad8c-115">Element</span></span>|<span data-ttu-id="bad8c-116">설명</span><span class="sxs-lookup"><span data-stu-id="bad8c-116">Description</span></span>|  
|-------------|-----------------|  
|`assemblyIdentity`|<span data-ttu-id="bad8c-117">어셈블리에 대 한 식별 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-117">Contains identifying information about the assembly.</span></span> <span data-ttu-id="bad8c-118">이 요소는 각각에 포함 되어야 합니다 `dependentAssembly` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-118">This element must be included in each `dependentAssembly` element.</span></span>|  
|`codeBase`|<span data-ttu-id="bad8c-119">런타임 컴퓨터에 설치 되지 않은 경우 공유 어셈블리를 찾을 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-119">Specifies where the runtime can find a shared assembly if it is not installed on the computer.</span></span>|  
|`bindingRedirect`|<span data-ttu-id="bad8c-120">어셈블리 버전을 다른 버전으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-120">Redirects one assembly version to another.</span></span>|  
|`publisherPolicy`|<span data-ttu-id="bad8c-121">런타임에서이 어셈블리에 대 한 게시자 정책을 적용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-121">Specifies whether the runtime applies publisher policy for this assembly.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bad8c-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="bad8c-122">Parent Elements</span></span>  
  
|<span data-ttu-id="bad8c-123">요소</span><span class="sxs-lookup"><span data-stu-id="bad8c-123">Element</span></span>|<span data-ttu-id="bad8c-124">설명</span><span class="sxs-lookup"><span data-stu-id="bad8c-124">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="bad8c-125">어셈블리 버전 리디렉션 및 어셈블리 위치에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-125">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="bad8c-126">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="bad8c-127">어셈블리 바인딩 및 가비지 컬렉션에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="bad8c-128">예제</span><span class="sxs-lookup"><span data-stu-id="bad8c-128">Example</span></span>  
 <span data-ttu-id="bad8c-129">다음 예제에서는 두 어셈블리에 대 한 어셈블리 정보를 캡슐화 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bad8c-129">The following example shows how to encapsulate assembly information for two assemblies.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <!--Redirection and codeBase policy for myAssembly.-->  
         </dependentAssembly>  
         <dependentAssembly>  
            <assemblyIdentity name="mySecondAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <!--Redirection and codeBase policy for mySecondAssembly.-->  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="bad8c-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bad8c-130">See Also</span></span>  
- [<span data-ttu-id="bad8c-131">런타임 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="bad8c-131">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
- [<span data-ttu-id="bad8c-132">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="bad8c-132">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [<span data-ttu-id="bad8c-133">어셈블리 버전 리디렉션</span><span class="sxs-lookup"><span data-stu-id="bad8c-133">Redirecting Assembly Versions</span></span>](../../../../../docs/framework/configure-apps/redirect-assembly-versions.md)
