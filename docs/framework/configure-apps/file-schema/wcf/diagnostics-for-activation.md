---
title: 활성화를 위한 &lt;diagnostics&gt;
ms.date: 03/30/2017
ms.assetid: 1486e0eb-fe2a-46c3-b584-c924889477dd
ms.openlocfilehash: 5d8fcce28182dcac945655a52d829945a432a9b3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723916"
---
# <a name="ltdiagnosticsgt-for-activation"></a><span data-ttu-id="0bd9c-102">활성화를 위한 &lt;diagnostics&gt;</span><span class="sxs-lookup"><span data-stu-id="0bd9c-102">&lt;diagnostics&gt; for Activation</span></span>
<span data-ttu-id="0bd9c-103">Windows Communication Foundation (WCF) 수신기의 진단 기능을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd9c-103">Configures Windows Communication Foundation (WCF) listener's diagnostics functionalities.</span></span>  
  
 <span data-ttu-id="0bd9c-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="0bd9c-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="0bd9c-105">\<diagnostics></span><span class="sxs-lookup"><span data-stu-id="0bd9c-105">\<diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bd9c-106">구문</span><span class="sxs-lookup"><span data-stu-id="0bd9c-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <diagnostics performanceCountersEnabled="Boolean" />
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a><span data-ttu-id="0bd9c-107">형식</span><span class="sxs-lookup"><span data-stu-id="0bd9c-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0bd9c-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="0bd9c-108">Attributes and Elements</span></span>  
 <span data-ttu-id="0bd9c-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd9c-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0bd9c-110">특성</span><span class="sxs-lookup"><span data-stu-id="0bd9c-110">Attributes</span></span>  
  
|<span data-ttu-id="0bd9c-111">특성</span><span class="sxs-lookup"><span data-stu-id="0bd9c-111">Attribute</span></span>|<span data-ttu-id="0bd9c-112">설명</span><span class="sxs-lookup"><span data-stu-id="0bd9c-112">Description</span></span>|  
|---------------|-----------------|  
|`performanceCountersEnabled`|<span data-ttu-id="0bd9c-113">진단 용도로 성능 카운터를 사용할지 여부를 나타내는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0bd9c-113">A Boolean value that indicates whether performance counters are enabled for diagnostic purposes.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0bd9c-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="0bd9c-114">Child Elements</span></span>  
 <span data-ttu-id="0bd9c-115">없음</span><span class="sxs-lookup"><span data-stu-id="0bd9c-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0bd9c-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="0bd9c-116">Parent Elements</span></span>  
  
|<span data-ttu-id="0bd9c-117">요소</span><span class="sxs-lookup"><span data-stu-id="0bd9c-117">Element</span></span>|<span data-ttu-id="0bd9c-118">설명</span><span class="sxs-lookup"><span data-stu-id="0bd9c-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0bd9c-119">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="0bd9c-119">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="0bd9c-120">수신기 프로세스 SMSvcHost.exe에 대한 구성 설정을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd9c-120">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0bd9c-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="0bd9c-121">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.DiagnosticSection>
