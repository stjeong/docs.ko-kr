---
title: '&lt;제거할&gt; 요소에 대 한 &lt;수신기&gt; 에 대 한 &lt;원본&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/remove
helpviewer_keywords:
- remove element for <listeners> for <source>
- <remove> element for <listeners> for <source>
ms.assetid: 3ff6b578-273d-407f-b07f-8251f1f9f5d0
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 8beb3ef041b153535afcb8bd92e1c29787e1f161
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654414"
---
# <a name="ltremovegt-element-for-ltlistenersgt-for-ltsourcegt"></a><span data-ttu-id="d7517-102">&lt;제거할&gt; 요소에 대 한 &lt;수신기&gt; 에 대 한 &lt;원본&gt;</span><span class="sxs-lookup"><span data-stu-id="d7517-102">&lt;remove&gt; Element for &lt;listeners&gt; for &lt;source&gt;</span></span>
<span data-ttu-id="d7517-103">추적 소스의 `Listeners` 컬렉션에서 수신기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-103">Removes a listener from the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="d7517-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d7517-104">\<configuration></span></span>  
<span data-ttu-id="d7517-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="d7517-105">\<system.diagnostics></span></span>  
<span data-ttu-id="d7517-106">\<sources></span><span class="sxs-lookup"><span data-stu-id="d7517-106">\<sources></span></span>  
<span data-ttu-id="d7517-107">\<source></span><span class="sxs-lookup"><span data-stu-id="d7517-107">\<source></span></span>  
<span data-ttu-id="d7517-108">\<listeners></span><span class="sxs-lookup"><span data-stu-id="d7517-108">\<listeners></span></span>  
<span data-ttu-id="d7517-109">\<remove></span><span class="sxs-lookup"><span data-stu-id="d7517-109">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7517-110">구문</span><span class="sxs-lookup"><span data-stu-id="d7517-110">Syntax</span></span>  
  
```xml  
<remove name="listenerName" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d7517-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="d7517-111">Attributes and Elements</span></span>  
 <span data-ttu-id="d7517-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d7517-113">특성</span><span class="sxs-lookup"><span data-stu-id="d7517-113">Attributes</span></span>  
  
|<span data-ttu-id="d7517-114">특성</span><span class="sxs-lookup"><span data-stu-id="d7517-114">Attribute</span></span>|<span data-ttu-id="d7517-115">설명</span><span class="sxs-lookup"><span data-stu-id="d7517-115">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="d7517-116">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="d7517-117">제거할 수신기의 이름을 합니다 `Listeners` 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-117">The name of the listener to remove from the `Listeners` collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d7517-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="d7517-118">Child Elements</span></span>  
 <span data-ttu-id="d7517-119">없음</span><span class="sxs-lookup"><span data-stu-id="d7517-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d7517-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="d7517-120">Parent Elements</span></span>  
  
|<span data-ttu-id="d7517-121">요소</span><span class="sxs-lookup"><span data-stu-id="d7517-121">Element</span></span>|<span data-ttu-id="d7517-122">설명</span><span class="sxs-lookup"><span data-stu-id="d7517-122">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="d7517-123">공용 언어 런타임 및 .NET Framework 애플리케이션에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="d7517-124">메시지를 수집하고 저장하고 라우팅하는 추적 수신기를 지정하며, 추적 스위치가 설정되는 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-124">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="d7517-125">추적 메시지를 시작하는 추적 소스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-125">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="d7517-126">추적 메시지를 시작하는 추적 소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-126">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="d7517-127">수집, 저장 하 고 메시지를 라우팅하는 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-127">Specifies listeners that collect, store, and route messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d7517-128">설명</span><span class="sxs-lookup"><span data-stu-id="d7517-128">Remarks</span></span>  
 <span data-ttu-id="d7517-129">합니다 `<remove>` 요소에서 지정 된 수신기를 제거 합니다 `Listeners` 추적 소스에 대 한 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-129">The `<remove>` element removes a specified listener from the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="d7517-130">요소를 제거할 수 있습니다는 `Listeners` 호출 하 여 프로그래밍 방식으로 추적 소스에 대 한 컬렉션을 <xref:System.Diagnostics.TraceListenerCollection.Remove%2A> 메서드를 <xref:System.Diagnostics.TraceSource.Listeners%2A> 의 속성을 <xref:System.Diagnostics.TraceSource> 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="d7517-130">You can remove an element from the `Listeners` collection for a trace source programmatically by calling the <xref:System.Diagnostics.TraceListenerCollection.Remove%2A> method on the <xref:System.Diagnostics.TraceSource.Listeners%2A> property of the <xref:System.Diagnostics.TraceSource> instance.</span></span>  
  
 <span data-ttu-id="d7517-131">이 요소는 응용 프로그램 구성 파일과 컴퓨터 구성 파일 (Machine.config)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-131">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d7517-132">예제</span><span class="sxs-lookup"><span data-stu-id="d7517-132">Example</span></span>  
 <span data-ttu-id="d7517-133">다음 예제에서는 사용 하는 방법을 보여 줍니다는 `<remove>` 요소를 사용 하기 전에 `<add>` 수신기를 추가 하는 요소 `console` 에 `Listeners` 추적 소스에 대 한 컬렉션 `TraceSourceApp`합니다.</span><span class="sxs-lookup"><span data-stu-id="d7517-133">The following example shows how to use the `<remove>` element before using the `<add>` element to add the listener `console` to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch" >  
         <listeners>  
           <remove name="Default"/>  
           <add name="console"   
             type="System.Diagnostics.ConsoleTraceListener" />  
         </listeners>  
      </source>  
    </sources>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="d7517-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="d7517-134">See also</span></span>
- <xref:System.Diagnostics.TraceSource.Listeners%2A>
- <xref:System.Diagnostics.TraceSource>
- [<span data-ttu-id="d7517-135">추적 및 디버그 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="d7517-135">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [<span data-ttu-id="d7517-136">\<clear></span><span class="sxs-lookup"><span data-stu-id="d7517-136">\<clear></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-source.md)
- [<span data-ttu-id="d7517-137">추적 수신기</span><span class="sxs-lookup"><span data-stu-id="d7517-137">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
