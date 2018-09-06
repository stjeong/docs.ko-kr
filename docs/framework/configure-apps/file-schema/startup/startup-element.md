---
title: '&lt;시작&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup
- http://schemas.microsoft.com/.NetConfiguration/v2.0#startup
helpviewer_keywords:
- container tags, <startup> element
- <startup> element
- startup element
ms.assetid: 536acfd8-f827-452f-838a-e14fa3b87621
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 4d39dc28082fbed932a60228ac216f2f700c2e9f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734709"
---
# <a name="ltstartupgt-element"></a><span data-ttu-id="62d93-102">&lt;시작&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="62d93-102">&lt;startup&gt; Element</span></span>
<span data-ttu-id="62d93-103">공용 언어 런타임 시작 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-103">Specifies common language runtime startup information.</span></span>  
  
 <span data-ttu-id="62d93-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="62d93-104">\<configuration></span></span>  
<span data-ttu-id="62d93-105">\<startup></span><span class="sxs-lookup"><span data-stu-id="62d93-105">\<startup></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62d93-106">구문</span><span class="sxs-lookup"><span data-stu-id="62d93-106">Syntax</span></span>  
  
```xml  
<startup useLegacyV2RuntimeActivationPolicy="true|false" >   
</startup>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="62d93-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="62d93-107">Attributes and Elements</span></span>  
 <span data-ttu-id="62d93-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="62d93-109">특성</span><span class="sxs-lookup"><span data-stu-id="62d93-109">Attributes</span></span>  
  
|<span data-ttu-id="62d93-110">특성</span><span class="sxs-lookup"><span data-stu-id="62d93-110">Attribute</span></span>|<span data-ttu-id="62d93-111">설명</span><span class="sxs-lookup"><span data-stu-id="62d93-111">Description</span></span>|  
|---------------|-----------------|  
|`useLegacyV2RuntimeActivationPolicy`|<span data-ttu-id="62d93-112">선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-112">Optional attribute.</span></span><br /><br /> <span data-ttu-id="62d93-113">사용 여부를 지정 합니다 [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] 런타임 정품 인증 정책 사용 하는 [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] 정품 인증 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-113">Specifies whether to enable the [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] runtime activation policy or to use the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] activation policy.</span></span>|  
  
## <a name="uselegacyv2runtimeactivationpolicy-attribute"></a><span data-ttu-id="62d93-114">useLegacyV2RuntimeActivationPolicy 특성</span><span class="sxs-lookup"><span data-stu-id="62d93-114">useLegacyV2RuntimeActivationPolicy Attribute</span></span>  
  
|<span data-ttu-id="62d93-115">값</span><span class="sxs-lookup"><span data-stu-id="62d93-115">Value</span></span>|<span data-ttu-id="62d93-116">설명</span><span class="sxs-lookup"><span data-stu-id="62d93-116">Description</span></span>|  
|-----------|-----------------|  
|`true`|<span data-ttu-id="62d93-117">사용 하도록 설정 [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] 레거시 런타임 정품 인증 기술에 바인딩하는 선택한 런타임에 대 한 런타임 정품 인증 정책 (같은 합니다 [CorBindToRuntimeEx 함수](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)) 대신 구성 파일에서 선택한 런타임에 CLR 버전 2.0에서 해당를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-117">Enable [!INCLUDE[dnprdnext](../../../../../includes/dnprdnext-md.md)] runtime activation policy for the chosen runtime, which is to bind legacy runtime activation techniques (such as the [CorBindToRuntimeEx function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)) to the runtime chosen from the configuration file instead of capping them at CLR version 2.0.</span></span> <span data-ttu-id="62d93-118">따라서 CLR 버전 4 이상을 구성 파일에서을 선택 하면 이전 버전의.NET Framework를 사용 하 여 만든 혼합 모드 어셈블리에 있는 선택한 CLR 버전을 사용 하 여 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-118">Thus, if CLR version 4 or later is chosen from the configuration file, mixed-mode assemblies created with earlier versions of the .NET Framework are loaded with the chosen CLR version.</span></span> <span data-ttu-id="62d93-119">CLR 버전 1.1 또는 CLR 버전 2.0-in-process side-by-side-기능을 효과적으로 사용 하지 않도록 설정 하는 동일한 프로세스로 로드 방지이 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-119">Setting this value prevents CLR version 1.1 or CLR version 2.0 from loading into the same process, effectively disabling the in-process side-by-side feature.</span></span>|  
|`false`|<span data-ttu-id="62d93-120">에 대 한 기본 활성화 정책을 사용 하는 [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] 이며 나중에 레거시 런타임 정품 인증 기술을 프로세스에 1.1 또는 2.0 버전 CLR을 로드할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-120">Use the default activation policy for the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] and later, which is to allow legacy runtime activation techniques to load CLR version 1.1 or 2.0 into the process.</span></span> <span data-ttu-id="62d93-121">혼합 모드 어셈블리의.NET Framework 4 이상 빌드된.NET Framework 4 또는 나중에 로드를 방해이 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-121">Setting this value prevents mixed-mode assemblies from loading into the .NET Framework 4 or later unless they were built with the .NET Framework 4 or later.</span></span> <span data-ttu-id="62d93-122">이 값은 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-122">This value is the default.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="62d93-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="62d93-123">Child Elements</span></span>  
  
|<span data-ttu-id="62d93-124">요소</span><span class="sxs-lookup"><span data-stu-id="62d93-124">Element</span></span>|<span data-ttu-id="62d93-125">설명</span><span class="sxs-lookup"><span data-stu-id="62d93-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="62d93-126">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="62d93-126">\<requiredRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md)|<span data-ttu-id="62d93-127">응용 프로그램에서 1.0 버전의 공용 언어 런타임만 지원하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-127">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="62d93-128">런타임 버전 1.1 이상으로 빌드된 응용 프로그램을 사용 해야 합니다  **\<supportedRuntime >** 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-128">Applications built with runtime version 1.1 or later should use the **\<supportedRuntime>** element.</span></span>|  
|[<span data-ttu-id="62d93-129">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="62d93-129">\<supportedRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/supportedruntime-element.md)|<span data-ttu-id="62d93-130">응용 프로그램이 지원하는 공용 언어 런타임 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-130">Specifies which versions of the common language runtime the application supports.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="62d93-131">부모 요소</span><span class="sxs-lookup"><span data-stu-id="62d93-131">Parent Elements</span></span>  
  
|<span data-ttu-id="62d93-132">요소</span><span class="sxs-lookup"><span data-stu-id="62d93-132">Element</span></span>|<span data-ttu-id="62d93-133">설명</span><span class="sxs-lookup"><span data-stu-id="62d93-133">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="62d93-134">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-134">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62d93-135">설명</span><span class="sxs-lookup"><span data-stu-id="62d93-135">Remarks</span></span>  
 <span data-ttu-id="62d93-136">합니다  **\<supportedRuntime >** 런타임의 1.1 이상 버전을 사용 하 여 빌드된 모든 응용 프로그램에서 요소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-136">The **\<supportedRuntime>** element should be used by all applications built using version 1.1 or later of the runtime.</span></span> <span data-ttu-id="62d93-137">런타임이 버전 1.0만을 지원 하도록 빌드된 응용 프로그램을 사용 해야 합니다  **\<requiredRuntime >** 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-137">Applications built to support only version 1.0 of the runtime must use the **\<requiredRuntime>** element.</span></span>  
  
 <span data-ttu-id="62d93-138">Microsoft Internet Explorer에서 호스팅되는 응용 프로그램 시작 코드를 무시 합니다  **\<시작 >** 요소와 해당 자식 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-138">The startup code for an application hosted in Microsoft Internet Explorer ignores the **\<startup>** element and its child elements.</span></span>  
  
## <a name="the-uselegacyv2runtimeactivationpolicy-attribute"></a><span data-ttu-id="62d93-139">UseLegacyV2RuntimeActivationPolicy 특성</span><span class="sxs-lookup"><span data-stu-id="62d93-139">The useLegacyV2RuntimeActivationPolicy Attribute</span></span>  
 <span data-ttu-id="62d93-140">이 특성은 응용 프로그램에서 같은 레거시 활성화 경로 사용 하는 경우에 유용 합니다 [CorBindToRuntimeEx 함수](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), 해당 경로 이전 버전 대신 CLR 버전 4를 활성화 하 고 응용 프로그램이 나 사용 하 여 빌드한는 [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] 하지만 이전 버전의.NET Framework를 사용 하 여 빌드된 혼합 모드 어셈블리에 종속 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-140">This attribute is useful if your application uses legacy activation paths, such as the [CorBindToRuntimeEx function](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), and you want those paths to activate version 4 of the CLR instead of an earlier version, or if your application is built with the [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] but has a dependency on a mixed-mode assembly built with an earlier version of the .NET Framework.</span></span> <span data-ttu-id="62d93-141">이러한 시나리오에서는 특성을 설정할 `true`합니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-141">In those scenarios, set the attribute to `true`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="62d93-142">특성을 설정 `true` CLR 버전 1.1 또는 CLR 버전 2.0-in-process side-by-side-기능을 효과적으로 사용 하지 않도록 설정 하는 동일한 프로세스로 로드 방지 하 고 (참조 [COM Interop에 대 한 Side-by-side-실행](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)).</span><span class="sxs-lookup"><span data-stu-id="62d93-142">Setting the attribute to `true` prevents CLR version 1.1 or CLR version 2.0 from loading into the same process, effectively disabling the in-process side-by-side feature (see [Side-by-Side Execution for COM Interop](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="62d93-143">예제</span><span class="sxs-lookup"><span data-stu-id="62d93-143">Example</span></span>  
 <span data-ttu-id="62d93-144">다음 예제에서는 구성 파일에서 런타임 버전을 지정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62d93-144">The following example shows how to specify the runtime version in a configuration file.</span></span>  
  
```xml  
<!-- When used with version 1.0 of the .NET Framework runtime -->  
<configuration>  
   <startup>  
      <requiredRuntime version="v1.0.3705" safemode="true"/>  
   </startup>  
</configuration>  
<!-- When used with version 1.1 (or later) of the runtime -->  
<configuration>  
   <startup>  
      <supportedRuntime version="v1.1.4322"/>  
      <supportedRuntime version="v1.0.3705"/>  
   </startup>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="62d93-145">참고 항목</span><span class="sxs-lookup"><span data-stu-id="62d93-145">See Also</span></span>  
 [<span data-ttu-id="62d93-146">시작 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="62d93-146">Startup Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)  
 [<span data-ttu-id="62d93-147">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="62d93-147">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="62d93-148">\<PaveOver> 사용할 런타임 버전 지정</span><span class="sxs-lookup"><span data-stu-id="62d93-148">\<PaveOver> Specifying Which Runtime Version to Use</span></span>](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)  
 [<span data-ttu-id="62d93-149">COM Interop에 대 한 Side-by-side-실행</span><span class="sxs-lookup"><span data-stu-id="62d93-149">Side-by-Side Execution for COM Interop</span></span>](https://msdn.microsoft.com/library/4302318c-3586-49bf-8620-b9a39cdf4a32)  
 [<span data-ttu-id="62d93-150">In-Process Side-by-Side 실행</span><span class="sxs-lookup"><span data-stu-id="62d93-150">In-Process Side-by-Side Execution</span></span>](../../../../../docs/framework/deployment/in-process-side-by-side-execution.md)
