---
title: '&lt;requiredRuntime&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requiredRuntime
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup/requiredRuntime
helpviewer_keywords:
- requiredRuntime element
- <requiredRuntime> element
- container tags, <requiredRuntime> element
ms.assetid: 9fa1639e-beb8-43be-b7a4-12f7b229c34b
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 7cb5e29f3d7fc1faffdba01a5322f1883fca8af0
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47069707"
---
# <a name="ltrequiredruntimegt-element"></a><span data-ttu-id="34e28-102">&lt;requiredRuntime&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="34e28-102">&lt;requiredRuntime&gt; Element</span></span>
<span data-ttu-id="34e28-103">응용 프로그램에서 1.0 버전의 공용 언어 런타임만 지원하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-103">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="34e28-104">이 요소는 사용 되지 않으며 더 이상 사용 되지 않음을 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-104">This element is deprecated and should no longer be used.</span></span> <span data-ttu-id="34e28-105">합니다 [ `supportedRuntime` ](supportedruntime-element.md) 요소를 대신 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-105">The [`supportedRuntime`](supportedruntime-element.md) element should be used instead.</span></span>
  
 <span data-ttu-id="34e28-106">\<configuration></span><span class="sxs-lookup"><span data-stu-id="34e28-106">\<configuration></span></span>  
<span data-ttu-id="34e28-107">\<startup></span><span class="sxs-lookup"><span data-stu-id="34e28-107">\<startup></span></span>  
<span data-ttu-id="34e28-108">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="34e28-108">\<requiredRuntime></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34e28-109">구문</span><span class="sxs-lookup"><span data-stu-id="34e28-109">Syntax</span></span>  
  
```xml  
   <requiredRuntime    
version="runtime version"  
safemode="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="34e28-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="34e28-110">Attributes and Elements</span></span>  
 <span data-ttu-id="34e28-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="34e28-112">특성</span><span class="sxs-lookup"><span data-stu-id="34e28-112">Attributes</span></span>  
  
|<span data-ttu-id="34e28-113">특성</span><span class="sxs-lookup"><span data-stu-id="34e28-113">Attribute</span></span>|<span data-ttu-id="34e28-114">설명</span><span class="sxs-lookup"><span data-stu-id="34e28-114">Description</span></span>|  
|---------------|-----------------|  
|`version`|<span data-ttu-id="34e28-115">선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-115">Optional attribute.</span></span><br /><br /> <span data-ttu-id="34e28-116">이 응용 프로그램이 지 원하는.NET Framework의 버전을 지정 하는 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-116">A string value that specifies the version of the .NET Framework that this application supports.</span></span> <span data-ttu-id="34e28-117">문자열 값에는.NET Framework 설치 루트 아래의 있는 디렉터리 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-117">The string value must match the directory name found under the .NET Framework installation root.</span></span> <span data-ttu-id="34e28-118">문자열 값의 내용은 구문 분석 되지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-118">The contents of the string value are not parsed.</span></span>|  
|`safemode`|<span data-ttu-id="34e28-119">선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-119">Optional attribute.</span></span><br /><br /> <span data-ttu-id="34e28-120">런타임 시작 코드가 런타임 버전을 확인 하려면 레지스트리를 검색 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-120">Specifies whether the runtime startup code searches the registry to determine the runtime version.</span></span>|  
  
## <a name="safemode-attribute"></a><span data-ttu-id="34e28-121">안전 모드 특성</span><span class="sxs-lookup"><span data-stu-id="34e28-121">safemode Attribute</span></span>  
  
|<span data-ttu-id="34e28-122">값</span><span class="sxs-lookup"><span data-stu-id="34e28-122">Value</span></span>|<span data-ttu-id="34e28-123">설명</span><span class="sxs-lookup"><span data-stu-id="34e28-123">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="34e28-124">레지스트리는 런타임 시작 코드를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-124">The runtime startup code looks in the registry.</span></span> <span data-ttu-id="34e28-125">기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-125">This is the default value.</span></span>|  
|`true`|<span data-ttu-id="34e28-126">레지스트리에서 런타임 시작 코드를 검사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-126">The runtime startup code does not look in the registry.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="34e28-127">자식 요소</span><span class="sxs-lookup"><span data-stu-id="34e28-127">Child Elements</span></span>  
 <span data-ttu-id="34e28-128">없음</span><span class="sxs-lookup"><span data-stu-id="34e28-128">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="34e28-129">부모 요소</span><span class="sxs-lookup"><span data-stu-id="34e28-129">Parent Elements</span></span>  
  
|<span data-ttu-id="34e28-130">요소</span><span class="sxs-lookup"><span data-stu-id="34e28-130">Element</span></span>|<span data-ttu-id="34e28-131">설명</span><span class="sxs-lookup"><span data-stu-id="34e28-131">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="34e28-132">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-132">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`startup`|<span data-ttu-id="34e28-133">포함 된 `<requiredRuntime>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-133">Contains the `<requiredRuntime>` element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="34e28-134">설명</span><span class="sxs-lookup"><span data-stu-id="34e28-134">Remarks</span></span>  
 <span data-ttu-id="34e28-135">런타임이 버전 1.0만을 지원 하도록 빌드된 응용 프로그램을 사용 해야 합니다는 `<requiredRuntime>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-135">Applications built to support only version 1.0 of the runtime must use the `<requiredRuntime>` element.</span></span> <span data-ttu-id="34e28-136">런타임의 1.1 이상 버전을 사용 하 여 빌드된 응용 프로그램을 사용 해야 합니다는 `<supportedRuntime>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-136">Applications built using version 1.1 or later of the runtime must use the `<supportedRuntime>` element.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="34e28-137">사용 하는 경우는 [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) 구성 파일을 지정 하려면 함수를 사용 해야 합니다는 `<requiredRuntime>` 런타임의 모든 버전에 대 한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-137">If you use the [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) function to specify the configuration file, you must use the `<requiredRuntime>` element for all versions of the runtime.</span></span> <span data-ttu-id="34e28-138">합니다 `<supportedRuntime>` 사용 하는 경우 요소는 무시 됩니다 [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-138">The `<supportedRuntime>` element is ignored when you use [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md).</span></span>  
  
 <span data-ttu-id="34e28-139">`version` 특성 문자열에 지정된 된 버전의.NET Framework에 대 한 설치 폴더 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-139">The `version` attribute string must match the installation folder name for the specified version of the .NET Framework.</span></span> <span data-ttu-id="34e28-140">이 문자열 해석 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-140">This string is not interpreted.</span></span> <span data-ttu-id="34e28-141">런타임 시작 코드에서 일치 하는 폴더를 찾지 못하면 런타임이 로드 되지 않습니다. 시작 코드는 오류 메시지를 표시 하 고 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-141">If the runtime startup code does not find a matching folder, the runtime is not loaded; the startup code shows an error message and quits.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="34e28-142">Microsoft Internet Explorer에서 호스팅되는 응용 프로그램 시작 코드를 무시 합니다 `<requiredRuntime>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-142">The startup code for an application that is hosted in Microsoft Internet Explorer ignores the `<requiredRuntime>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="34e28-143">예제</span><span class="sxs-lookup"><span data-stu-id="34e28-143">Example</span></span>  
 <span data-ttu-id="34e28-144">다음 예제에서는 구성 파일에서 런타임 버전을 지정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34e28-144">The following example shows how to specify the runtime version in a configuration file.</span></span>  
  
```xml  
<configuration>  
   <startup>  
      <requiredRuntime version="v1.0.3705" safemode="true"/>  
   </startup>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="34e28-145">참고 항목</span><span class="sxs-lookup"><span data-stu-id="34e28-145">See Also</span></span>  
 [<span data-ttu-id="34e28-146">시작 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="34e28-146">Startup Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)  
 [<span data-ttu-id="34e28-147">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="34e28-147">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="34e28-148">\<PaveOver> 사용할 런타임 버전 지정</span><span class="sxs-lookup"><span data-stu-id="34e28-148">\<PaveOver> Specifying Which Runtime Version to Use</span></span>](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)
