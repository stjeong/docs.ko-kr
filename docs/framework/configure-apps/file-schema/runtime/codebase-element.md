---
title: <codeBase> 요소
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#codeBase
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/codeBase
helpviewer_keywords:
- <codeBase> element
- container tags, <codeBase> element
- codeBase element
ms.assetid: d48a3983-2297-43ff-a14d-1f29d3995822
ms.openlocfilehash: ebf7e2624cc36fb6a758afef38e2054669061dff
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269655"
---
# <a name="codebase-element"></a><span data-ttu-id="ce302-102">\<코드 베이스 > 요소</span><span class="sxs-lookup"><span data-stu-id="ce302-102">\<codeBase> Element</span></span>
<span data-ttu-id="ce302-103">공용 언어 런타임에서 어셈블리를 찾는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-103">Specifies where the common language runtime can find an assembly.</span></span>  
  
 <span data-ttu-id="ce302-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ce302-104">\<configuration></span></span>  
<span data-ttu-id="ce302-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="ce302-105">\<runtime></span></span>  
<span data-ttu-id="ce302-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="ce302-106">\<assemblyBinding></span></span>  
<span data-ttu-id="ce302-107">\<dependentAssembly></span><span class="sxs-lookup"><span data-stu-id="ce302-107">\<dependentAssembly></span></span>  
<span data-ttu-id="ce302-108">\<codeBase></span><span class="sxs-lookup"><span data-stu-id="ce302-108">\<codeBase></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce302-109">구문</span><span class="sxs-lookup"><span data-stu-id="ce302-109">Syntax</span></span>  
  
```xml  
   <codeBase    
version="Assembly version"  
href="URL of assembly"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ce302-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ce302-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ce302-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ce302-112">특성</span><span class="sxs-lookup"><span data-stu-id="ce302-112">Attributes</span></span>  
  
|<span data-ttu-id="ce302-113">특성</span><span class="sxs-lookup"><span data-stu-id="ce302-113">Attribute</span></span>|<span data-ttu-id="ce302-114">설명</span><span class="sxs-lookup"><span data-stu-id="ce302-114">Description</span></span>|  
|---------------|-----------------|  
|`href`|<span data-ttu-id="ce302-115">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-115">Required attribute.</span></span><br /><br /> <span data-ttu-id="ce302-116">런타임에서 어셈블리의 지정된 된 버전을 찾을 수 있는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-116">Specifies the URL where the runtime can find the specified version of the assembly.</span></span>|  
|`version`|<span data-ttu-id="ce302-117">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="ce302-118">코드 베이스에 적용 하는 어셈블리의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-118">Specifies the version of the assembly the codebase applies to.</span></span> <span data-ttu-id="ce302-119">어셈블리 버전 번호의 형식은 *major.minor.build.revision*합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-119">The format of an assembly version number is *major.minor.build.revision*.</span></span>|  
  
## <a name="version-attribute"></a><span data-ttu-id="ce302-120">버전 특성</span><span class="sxs-lookup"><span data-stu-id="ce302-120">version Attribute</span></span>  
  
|<span data-ttu-id="ce302-121">값</span><span class="sxs-lookup"><span data-stu-id="ce302-121">Value</span></span>|<span data-ttu-id="ce302-122">설명</span><span class="sxs-lookup"><span data-stu-id="ce302-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ce302-123">버전 번호의 각 부분에 대 한 유효한 값은 0부터 65535 까지입니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-123">Valid values for each part of the version number are 0 to 65535.</span></span>|<span data-ttu-id="ce302-124">해당 사항 없음.</span><span class="sxs-lookup"><span data-stu-id="ce302-124">Not applicable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ce302-125">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ce302-125">Child Elements</span></span>  
 <span data-ttu-id="ce302-126">없음</span><span class="sxs-lookup"><span data-stu-id="ce302-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ce302-127">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ce302-127">Parent Elements</span></span>  
  
|<span data-ttu-id="ce302-128">요소</span><span class="sxs-lookup"><span data-stu-id="ce302-128">Element</span></span>|<span data-ttu-id="ce302-129">설명</span><span class="sxs-lookup"><span data-stu-id="ce302-129">Description</span></span>|  
|-------------|-----------------|  
|`buildproviders`|<span data-ttu-id="ce302-130">사용자 지정 리소스 파일의 컴파일에 사용되는 빌드 공급자의 컬렉션을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-130">Defines a collection of build providers used to compile custom resource files.</span></span> <span data-ttu-id="ce302-131">빌드 공급자 수에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-131">You can have any number of build providers.</span></span>|  
|`compilation`|<span data-ttu-id="ce302-132">ASP.NET을 사용 하는 모든 컴파일 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-132">Configures all the compilation settings that ASP.NET uses.</span></span>|  
|`configuration`|<span data-ttu-id="ce302-133">공용 언어 런타임 및 .NET Framework 애플리케이션에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`System.web`|<span data-ttu-id="ce302-134">ASP.NET 구성 섹션의 루트 요소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-134">Specifies the root element for the ASP.NET configuration section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ce302-135">설명</span><span class="sxs-lookup"><span data-stu-id="ce302-135">Remarks</span></span>  
 <span data-ttu-id="ce302-136">사용에 런타임에 대 한 합니다  **\<codeBase >** 컴퓨터 구성 파일 또는 게시자 정책 파일에서 설정 파일을 리디렉션해야 어셈블리 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-136">For the runtime to use the **\<codeBase>** setting in a machine configuration file or publisher policy file, the file must also redirect the assembly version.</span></span> <span data-ttu-id="ce302-137">응용 프로그램 구성 파일에는 어셈블리 버전 리디렉션 없이 코드 베이스 설정이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-137">Application configuration files can have a codebase setting without redirecting the assembly version.</span></span> <span data-ttu-id="ce302-138">사용 하는 어셈블리 버전을 결정 한 후 런타임 버전을 결정 하는 파일의 코드 베이스 설정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-138">After determining which assembly version to use, the runtime applies the codebase setting from the file that determines the version.</span></span> <span data-ttu-id="ce302-139">없는 코드 베이스를 지정 하는 경우 런타임은 일반적인 방법으로 어셈블리를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-139">If no codebase is indicated, the runtime probes for the assembly in the usual way.</span></span>  
  
 <span data-ttu-id="ce302-140">어셈블리에 강력한 이름을 하는 경우 코드 베이스 설정을 로컬 인트라넷 또는 인터넷에서 아무 곳 이나 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-140">If the assembly has a strong name, the codebase setting can be anywhere on the local intranet or the Internet.</span></span> <span data-ttu-id="ce302-141">전용 어셈블리를 어셈블리가 있는 경우 코드 베이스 설정을 응용 프로그램의 디렉터리에 상대적인 경로 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-141">If the assembly is a private assembly, the codebase setting must be a path relative to the application's directory.</span></span>  
  
 <span data-ttu-id="ce302-142">강력한 이름이 없는 어셈블리의 경우 버전이 무시 되 고 로더는 첫 번째 모양의 \<codebase > 내에서 \<dependentAssembly >.</span><span class="sxs-lookup"><span data-stu-id="ce302-142">For assemblies without a strong name, version is ignored and the loader uses the first appearance of \<codebase> inside \<dependentAssembly>.</span></span> <span data-ttu-id="ce302-143">다른 어셈블리 바인딩을 리디렉션하는 응용 프로그램 구성 파일에 항목이 있으면 리디렉션 어셈블리 버전 바인딩 요청과 일치 하지 않습니다 하는 경우에 우선을 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-143">If there is an entry in the application configuration file that redirects binding to another assembly, the redirection will take precedence even if the assembly version doesnt match the binding request.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ce302-144">예제</span><span class="sxs-lookup"><span data-stu-id="ce302-144">Example</span></span>  
 <span data-ttu-id="ce302-145">다음 예제에서는 런타임에 어셈블리를 찾을 수 있습니다 위치를 지정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce302-145">The following example shows how to specify where the runtime can find an assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <codeBase version="2.0.0.0"  
                      href="http://www.litwareinc.com/myAssembly.dll"/>  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ce302-146">참고자료</span><span class="sxs-lookup"><span data-stu-id="ce302-146">See also</span></span>
- [<span data-ttu-id="ce302-147">런타임 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="ce302-147">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="ce302-148">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="ce302-148">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="ce302-149">어셈블리 위치 지정</span><span class="sxs-lookup"><span data-stu-id="ce302-149">Specifying an Assembly's Location</span></span>](../../../../../docs/framework/configure-apps/specify-assembly-location.md)
- [<span data-ttu-id="ce302-150">런타임에서 어셈블리를 찾는 방법</span><span class="sxs-lookup"><span data-stu-id="ce302-150">How the Runtime Locates Assemblies</span></span>](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
