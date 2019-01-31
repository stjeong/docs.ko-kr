---
title: <diagnostics>
ms.date: 03/30/2017
ms.assetid: 0c2f95c4-cc12-4fb5-a70c-7fc6fa95db58
ms.openlocfilehash: 2041125e5bb538a9b64beb54778219c2a51a18f7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264715"
---
# <a name="diagnostics"></a><span data-ttu-id="ac850-101">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="ac850-101">\<diagnostics></span></span>
<span data-ttu-id="ac850-102">`diagnostics` 요소는 관리자가 런타임 검사 및 제어에 사용할 수 있는 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-102">The `diagnostics` element defines settings that can be used by an administrator for run-time inspection and control.</span></span>  
  
 <span data-ttu-id="ac850-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ac850-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="ac850-104">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="ac850-104">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac850-105">구문</span><span class="sxs-lookup"><span data-stu-id="ac850-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics etwProviderId="String"
               performanceCounters="Off/ServiceOnly/All/Default"
               wmiProviderEnabled="Boolean">
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
    <messageLogging logEntireMessage="Boolean"
                    logMalformedMessages="Boolean"
                    logMessagesAtServiceLevel="Boolean"
                    logMessagesAtTransportLevel="Boolean"
                    maxMessagesToLog="Integer"
                    maxSizeOfMessageToLog="Integer">
      <filters>
        <clear />
      </filters>
    </messageLogging>
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ac850-106">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ac850-106">Attributes and Elements</span></span>  
 <span data-ttu-id="ac850-107">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ac850-108">특성</span><span class="sxs-lookup"><span data-stu-id="ac850-108">Attributes</span></span>  
  
|<span data-ttu-id="ac850-109">특성</span><span class="sxs-lookup"><span data-stu-id="ac850-109">Attribute</span></span>|<span data-ttu-id="ac850-110">설명</span><span class="sxs-lookup"><span data-stu-id="ac850-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ac850-111">etwProviderId</span><span class="sxs-lookup"><span data-stu-id="ac850-111">etwProviderId</span></span>|<span data-ttu-id="ac850-112">ETW 세션에 이벤트를 기록하는 이벤트 추적 공급자에 대한 식별자를 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-112">A string that specifies the identifier for the Event-Tracing provider, which writes events to ETW sessions.</span></span>|  
|<span data-ttu-id="ac850-113">performanceCounters</span><span class="sxs-lookup"><span data-stu-id="ac850-113">performanceCounters</span></span>|<span data-ttu-id="ac850-114">어셈블리에 대해 성능 카운터를 사용할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-114">Specifies whether performance counters for the assembly are enabled.</span></span> <span data-ttu-id="ac850-115">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-115">Valid values are</span></span><br /><br /> <span data-ttu-id="ac850-116">-Off: 성능 카운터를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-116">-   Off: Performance counters are disabled.</span></span><br /><span data-ttu-id="ac850-117">-   ServiceOnly: 이 서비스와 관련된 성능 카운터만 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-117">-   ServiceOnly: Only performance counters relevant to this service is enabled.</span></span><br /><span data-ttu-id="ac850-118">-   All: 성능 카운터를 런타임에 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-118">-   All: Performance counters can be viewed at runtime.</span></span><br /><span data-ttu-id="ac850-119">-기본: 단일 성능 카운터 인스턴스 _WCF_Admin이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-119">-   Default: A single performance counter instance _WCF_Admin is created.</span></span> <span data-ttu-id="ac850-120">이 인스턴스는 인프라에서 사용되는 SQM 데이터 컬렉션을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-120">This instance is used to enable the collection of SQM data for used by the infrastructure.</span></span> <span data-ttu-id="ac850-121">이 인스턴스의 어떤 카운터 값도 업데이트되지 않으므로 0으로 남게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-121">None of the counter values for this instance are updated and therefore will remain at zero.</span></span> <span data-ttu-id="ac850-122">이것은 WCF에 대한 구성이 없을 경우 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-122">This is the default value if no configuration is present for WCF.</span></span>|  
|<span data-ttu-id="ac850-123">wmiProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="ac850-123">wmiProviderEnabled</span></span>|<span data-ttu-id="ac850-124">어셈블리에 대해 WMI 공급자를 사용할 수 있는지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-124">A Boolean value that specifies whether the WMI provider for the assembly is enabled.</span></span> <span data-ttu-id="ac850-125">사용자가 WCF(Windows Communication Foundation)의 검사 및 제어 기능에 대해 런타임 액세스 권한을 얻으려면 WMI 공급자가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-125">The WMI provider is required for user to gain run-time access to the inspection and control features of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="ac850-126">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-126">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ac850-127">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ac850-127">Child Elements</span></span>  
  
|<span data-ttu-id="ac850-128">요소</span><span class="sxs-lookup"><span data-stu-id="ac850-128">Element</span></span>|<span data-ttu-id="ac850-129">설명</span><span class="sxs-lookup"><span data-stu-id="ac850-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ac850-130">\<endToEndTracing></span><span class="sxs-lookup"><span data-stu-id="ac850-130">\<endToEndTracing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endtoendtracing.md)|<span data-ttu-id="ac850-131">서비스 응용 프로그램 실행 중에 종단 간 추적의 다양한 측면을 사용하거나 사용하지 않도록 설정할 수 있는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-131">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>|  
|[<span data-ttu-id="ac850-132">\<messageLogging></span><span class="sxs-lookup"><span data-stu-id="ac850-132">\<messageLogging></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagelogging.md)|<span data-ttu-id="ac850-133">WCF 메시지 로깅의 설정을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-133">Describes the settings for WCF message logging.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ac850-134">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ac850-134">Parent Elements</span></span>  
  
|<span data-ttu-id="ac850-135">요소</span><span class="sxs-lookup"><span data-stu-id="ac850-135">Element</span></span>|<span data-ttu-id="ac850-136">설명</span><span class="sxs-lookup"><span data-stu-id="ac850-136">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ac850-137">serviceModel</span><span class="sxs-lookup"><span data-stu-id="ac850-137">serviceModel</span></span>|<span data-ttu-id="ac850-138">모든 WCF 구성 요소의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-138">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac850-139">설명</span><span class="sxs-lookup"><span data-stu-id="ac850-139">Remarks</span></span>  
 <span data-ttu-id="ac850-140">`diagnostics` 섹션에서는 어셈블리에 있는 모든 서비스의 진단 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-140">The `diagnostics` section defines the diagnostics settings for all services located in an assembly.</span></span> <span data-ttu-id="ac850-141">어셈블리에 서비스가 하나만 있는 경우가 아니라면 서비스 수준에서 별도의 진단 설정을 정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-141">It is not possible to define separate diagnostics settings at the service level unless there is only one service in the assembly.</span></span> <span data-ttu-id="ac850-142">해당 섹션의 요구 사항에 따라 특성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-142">Attributes are set according to the requirements of the section.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ac850-143">예제</span><span class="sxs-lookup"><span data-stu-id="ac850-143">Example</span></span>  
  
```xml  
<diagnostics wmiProviderEnabled="false"
             performanceCounters="all">
  <messageLogging logEntireMessage="true"
                  logMalformedMessages="true"
                  logMessagesAtServiceLevel="true"
                  logMessagesAtTransportLevel="true"
                  maxMessagesToLog="42"
                  maxSizeOfMessageToLog="42">
    <filters>
      <clear />
    </filters>
  </messageLogging>
</diagnostics>
```  
  
## <a name="see-also"></a><span data-ttu-id="ac850-144">참고자료</span><span class="sxs-lookup"><span data-stu-id="ac850-144">See also</span></span>
- <xref:System.ServiceModel.Configuration.DiagnosticSection>
- <xref:System.ServiceModel.Diagnostics>
