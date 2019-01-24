---
title: '&lt;routing&gt;의 &lt;filters&gt;'
ms.date: 03/30/2017
ms.assetid: 7993cf90-9afd-4c3c-9608-184d5da1105c
ms.openlocfilehash: 468c10bc06b60f80ce93cf413c02582fe3861f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704435"
---
# <a name="ltfiltersgt-of-ltroutinggt"></a><span data-ttu-id="7f740-102">&lt;routing&gt;의 &lt;filters&gt;</span><span class="sxs-lookup"><span data-stu-id="7f740-102">&lt;filters&gt; of &lt;routing&gt;</span></span>

<span data-ttu-id="7f740-103">Windows Communication Foundation (WCF)의 형식을 결정 하는 라우팅 필터 집합을 정의 하기 위한 구성 섹션을 나타냅니다 <xref:System.ServiceModel.Dispatcher.MessageFilter> 들어오는 메시지를 평가할 때 사용 되는 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f740-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span>

<span data-ttu-id="7f740-104">[**\<system.serviceModel>**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="7f740-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="7f740-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span><span class="sxs-lookup"><span data-stu-id="7f740-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span></span>  
<span data-ttu-id="7f740-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span><span class="sxs-lookup"><span data-stu-id="7f740-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7f740-107">구문</span><span class="sxs-lookup"><span data-stu-id="7f740-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7f740-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="7f740-108">Attributes and elements</span></span>

<span data-ttu-id="7f740-109">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="7f740-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="7f740-110">특성</span><span class="sxs-lookup"><span data-stu-id="7f740-110">Attributes</span></span>

<span data-ttu-id="7f740-111">없음</span><span class="sxs-lookup"><span data-stu-id="7f740-111">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="7f740-112">자식 요소</span><span class="sxs-lookup"><span data-stu-id="7f740-112">Child elements</span></span>

|     | <span data-ttu-id="7f740-113">설명</span><span class="sxs-lookup"><span data-stu-id="7f740-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="7f740-114">**\<filter>**</span><span class="sxs-lookup"><span data-stu-id="7f740-114">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="7f740-115">Windows Communication Foundation (WCF)의 형식을 결정 하는 라우팅 필터를 포함<xref:System.ServiceModel.Dispatcher.MessageFilter> 들어오는 메시지를 평가할 때 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f740-115">Contains a routing filter that determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> will be used when evaluating incoming messages.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="7f740-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="7f740-116">Parent elements</span></span>

|     | <span data-ttu-id="7f740-117">설명</span><span class="sxs-lookup"><span data-stu-id="7f740-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="7f740-118">**\<routing>**</span><span class="sxs-lookup"><span data-stu-id="7f740-118">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="7f740-119">Windows Communication Foundation (WCF)의 형식을 결정 하는 라우팅 필터 집합을 정의 하기 위한 구성 섹션을 나타냅니다<xref:System.ServiceModel.Dispatcher.MessageFilter> 사용할 대상 끝점을 정의 하는 들어오는 메시지를 평가할 수 있을 뿐만 아니라 라우팅 테이블 필터가 일치할 때에 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7f740-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7f740-120">참고자료</span><span class="sxs-lookup"><span data-stu-id="7f740-120">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
