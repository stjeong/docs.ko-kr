---
title: '&lt;추가&gt; 요소에 대 한 &lt;sharedListeners&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add
helpviewer_keywords:
- initializeData attribute
- <add> element for <sharedListeners>
- add element for <sharedListeners>
ms.assetid: 1595e1bc-2492-421f-8384-7f382eb8eb57
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 93fdb548882422634e1d2456b4d37f434b278f8d
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216536"
---
# <a name="ltaddgt-element-for-ltsharedlistenersgt"></a><span data-ttu-id="c1117-102">&lt;추가&gt; 요소에 대 한 &lt;sharedListeners&gt;</span><span class="sxs-lookup"><span data-stu-id="c1117-102">&lt;add&gt; Element for &lt;sharedListeners&gt;</span></span>
<span data-ttu-id="c1117-103">`sharedListeners` 컬렉션에 수신기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-103">Adds a listener to the `sharedListeners` collection.</span></span> <span data-ttu-id="c1117-104">`sharedListeners` 이 수신기의 컬렉션인 모든 [ \<소스 >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) 또는 [ \<추적 >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md) 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-104">`sharedListeners` is a collection of listeners that any [\<source>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) or [\<trace>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md) can reference.</span></span>  <span data-ttu-id="c1117-105">기본적으로 수신기에는 `sharedListeners` 컬렉션에 있지 않은지를 `Listeners` 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-105">By default, listeners in the `sharedListeners` collection are not placed in a `Listeners` collection.</span></span> <span data-ttu-id="c1117-106">이름으로 추가 해야 합니다 [ \<소스 >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) 또는 [ \<추적 >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-106">They must be added by name to the [\<source>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/source-element.md) or [\<trace>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md).</span></span> <span data-ttu-id="c1117-107">수신기에서 가져올 수 없는 `sharedListeners` 런타임 시 코드의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-107">It is not possible to get the listeners in the `sharedListeners` collection in code at run time.</span></span>  
  
 <span data-ttu-id="c1117-108">\<configuration></span><span class="sxs-lookup"><span data-stu-id="c1117-108">\<configuration></span></span>  
<span data-ttu-id="c1117-109">\<system.diagnostics ></span><span class="sxs-lookup"><span data-stu-id="c1117-109">\<system.diagnostics></span></span>  
<span data-ttu-id="c1117-110">\<sharedListeners > 요소</span><span class="sxs-lookup"><span data-stu-id="c1117-110">\<sharedListeners> Element</span></span>  
<span data-ttu-id="c1117-111">\<add></span><span class="sxs-lookup"><span data-stu-id="c1117-111">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1117-112">구문</span><span class="sxs-lookup"><span data-stu-id="c1117-112">Syntax</span></span>  
  
```xml  
<add name="name"   
  type="TraceListenerClassName, Version, Culture, PublicKeyToken"  
  initializeData="data"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c1117-113">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="c1117-113">Attributes and Elements</span></span>  
 <span data-ttu-id="c1117-114">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c1117-115">특성</span><span class="sxs-lookup"><span data-stu-id="c1117-115">Attributes</span></span>  
  
|<span data-ttu-id="c1117-116">특성</span><span class="sxs-lookup"><span data-stu-id="c1117-116">Attribute</span></span>|<span data-ttu-id="c1117-117">설명</span><span class="sxs-lookup"><span data-stu-id="c1117-117">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="c1117-118">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-118">Required attribute.</span></span><br /><br /> <span data-ttu-id="c1117-119">공유 수신기를 추가 하는 데 사용 되는 수신기의 이름을 지정는 `Listeners` 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-119">Specifies the name of the listener that is used to add the shared listener to a `Listeners` collection.</span></span>|  
|`type`|<span data-ttu-id="c1117-120">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-120">Required attribute.</span></span><br /><br /> <span data-ttu-id="c1117-121">수신기의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-121">Specifies the type of the listener.</span></span> <span data-ttu-id="c1117-122">에 지정 된 요구 사항을 충족 하는 문자열을 사용 해야 합니다 [정규화 된 형식 이름 지정](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-122">You must use a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|`initializeData`|<span data-ttu-id="c1117-123">선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="c1117-124">지정된 된 클래스에 대 한 생성자에 전달 된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-124">The string passed to the constructor for the specified class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c1117-125">자식 요소</span><span class="sxs-lookup"><span data-stu-id="c1117-125">Child Elements</span></span>  
  
|<span data-ttu-id="c1117-126">요소</span><span class="sxs-lookup"><span data-stu-id="c1117-126">Element</span></span>|<span data-ttu-id="c1117-127">설명</span><span class="sxs-lookup"><span data-stu-id="c1117-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c1117-128">\<filter></span><span class="sxs-lookup"><span data-stu-id="c1117-128">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-sharedlisteners.md)|<span data-ttu-id="c1117-129">`sharedListeners` 컬렉션에 있는 수신기에 필터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-129">Adds a filter to a listener in the `sharedListeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c1117-130">부모 요소</span><span class="sxs-lookup"><span data-stu-id="c1117-130">Parent Elements</span></span>  
  
|<span data-ttu-id="c1117-131">요소</span><span class="sxs-lookup"><span data-stu-id="c1117-131">Element</span></span>|<span data-ttu-id="c1117-132">설명</span><span class="sxs-lookup"><span data-stu-id="c1117-132">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="c1117-133">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="c1117-134">메시지를 수집하고 저장하고 라우팅하는 추적 수신기를 지정하며, 추적 스위치가 설정되는 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-134">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sharedListeners`|<span data-ttu-id="c1117-135">모든 소스 또는 추적 요소가 참조할 수 있는 수신기의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-135">A collection of listeners that any source or trace element can reference.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c1117-136">설명</span><span class="sxs-lookup"><span data-stu-id="c1117-136">Remarks</span></span>  
 <span data-ttu-id="c1117-137">.NET Framework와 함께 제공 되는 수신기 클래스에서 파생 된 <xref:System.Diagnostics.TraceListener> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-137">The listener classes shipped with the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span> <span data-ttu-id="c1117-138">에 대 한 값을 `name` 특성 공유 수신기를 추가 하는 데 사용 됩니다는 `Listeners` 추적 또는 추적 소스에 대 한 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-138">The value for the `name` attribute is used to add the shared listener to a `Listeners` collection for either a trace or a trace source.</span></span> <span data-ttu-id="c1117-139">에 대 한 값을 `initializeData` 특성 만든 수신기의 형식에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-139">The value for the `initializeData` attribute depends on the type of listener you create.</span></span> <span data-ttu-id="c1117-140">모든 추적 수신기에 지정 해야 `initializeData`합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-140">Not all trace listeners require that you specify `initializeData`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c1117-141">사용 하는 경우는 `initializeData` 특성인 컴파일러 "'initializeData' 특성이 선언 되지 않았습니다." 경고를 발생할 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="c1117-141">When you use the `initializeData` attribute, you may get the compiler warning "The 'initializeData' attribute is not declared."</span></span> <span data-ttu-id="c1117-142">이 경고는 추상 기본 클래스에 대 한 구성 설정이 검증 되었으며 때문에 발생 <xref:System.Diagnostics.TraceListener>를 인식 하지 않습니다는 `initializeData` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-142">This warning occurs because the configuration settings are validated against the abstract base class <xref:System.Diagnostics.TraceListener>, which does not recognize the `initializeData` attribute.</span></span> <span data-ttu-id="c1117-143">일반적으로 매개 변수를 사용 하는 생성자가 하는 추적 수신기 구현에 대 한이 경고를 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-143">Typically, you can ignore this warning for trace listener implementations that have a constructor that takes a parameter.</span></span>  
  
 <span data-ttu-id="c1117-144">다음 표는.NET Framework에 포함 된 추적 수신기를 보여 주고 값을 설명 합니다 해당 `initializeData` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-144">The following table shows the trace listeners that are included with the .NET Framework and describes the value of their `initializeData` attributes.</span></span>  
  
|<span data-ttu-id="c1117-145">추적 수신기 클래스</span><span class="sxs-lookup"><span data-stu-id="c1117-145">Trace listener class</span></span>|<span data-ttu-id="c1117-146">initializeData 특성 값</span><span class="sxs-lookup"><span data-stu-id="c1117-146">initializeData attribute value</span></span>|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener>|<span data-ttu-id="c1117-147">합니다 `useErrorStream` 에 대 한 값을 <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> 생성자입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-147">The `useErrorStream` value for the <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructor.</span></span>  <span data-ttu-id="c1117-148">설정 된 `initializeData` 특성을 "`true`"쓸 추적 및 디버그 출력을 표준 오류 스트림에;로 설정"`false`" 표준 출력 스트림에 쓸입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-148">Set the `initializeData` attribute to "`true`" to write trace and debug output to the standard error stream; set it to "`false`" to write to the standard output stream.</span></span>|  
|<xref:System.Diagnostics.DelimitedListTraceListener>|<span data-ttu-id="c1117-149">파일의 이름을 합니다 <xref:System.Diagnostics.DelimitedListTraceListener> 를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-149">The name of the file the <xref:System.Diagnostics.DelimitedListTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|<span data-ttu-id="c1117-150">기존 이벤트 로그 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-150">The name of an existing event log source.</span></span>|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|<span data-ttu-id="c1117-151">파일의 이름을는 <xref:System.Diagnostics.EventSchemaTraceListener> 를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-151">The name of the file that the <xref:System.Diagnostics.EventSchemaTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|<span data-ttu-id="c1117-152">파일의 이름을는 <xref:System.Diagnostics.TextWriterTraceListener> 를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-152">The name of the file that the <xref:System.Diagnostics.TextWriterTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.XmlWriterTraceListener>|<span data-ttu-id="c1117-153">파일의 이름을는 <xref:System.Diagnostics.XmlWriterTraceListener> 를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-153">The name of the file that the <xref:System.Diagnostics.XmlWriterTraceListener> writes to.</span></span>|  
  
## <a name="configuration-file"></a><span data-ttu-id="c1117-154">구성 파일</span><span class="sxs-lookup"><span data-stu-id="c1117-154">Configuration File</span></span>  
 <span data-ttu-id="c1117-155">이 요소는 응용 프로그램 구성 파일과 컴퓨터 구성 파일 (Machine.config)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-155">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1117-156">예제</span><span class="sxs-lookup"><span data-stu-id="c1117-156">Example</span></span>  
 <span data-ttu-id="c1117-157">다음 예제에서는 사용 하는 방법을 보여 줍니다 `<add>` 요소를 추가 하는 <xref:System.Diagnostics.TextWriterTraceListener> `textListener` 에 `sharedListeners` 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-157">The following example shows how to use `<add>` elements to add the <xref:System.Diagnostics.TextWriterTraceListener>`textListener` to the `sharedListeners` collection.</span></span>   <span data-ttu-id="c1117-158">`textListener` 이름으로 추가 되는 `Listeners` 추적 소스에 대 한 컬렉션 `TraceSourceApp`합니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-158">`textListener` is added by name to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span> <span data-ttu-id="c1117-159">`textListener` 수신기 파일 myListener.log에 추적 출력을 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c1117-159">The `textListener` listener writes trace output to the file myListener.log.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
          <remove name="Default"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"   
        type="System.Diagnostics.TextWriterTraceListener"   
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="c1117-160">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c1117-160">See Also</span></span>  
 <xref:System.Diagnostics.TraceSource>  
 <xref:System.Diagnostics.TraceListener>  
 [<span data-ttu-id="c1117-161">추적 및 디버그 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="c1117-161">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="c1117-162">추적 수신기</span><span class="sxs-lookup"><span data-stu-id="c1117-162">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
