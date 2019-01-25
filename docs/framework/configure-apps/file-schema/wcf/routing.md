---
title: '&lt;routing&gt;'
ms.date: 03/30/2017
ms.assetid: a210c209-3940-4288-9a8e-39b1e62606bc
ms.openlocfilehash: 855faedfd2e9523e939174441b0cfa50e052b375
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565880"
---
# <a name="ltroutinggt"></a><span data-ttu-id="0c259-102">&lt;routing&gt;</span><span class="sxs-lookup"><span data-stu-id="0c259-102">&lt;routing&gt;</span></span>

<span data-ttu-id="0c259-103">Windows Communication Foundation (WCF)의 형식을 결정 하는 라우팅 필터 집합을 정의 하기 위한 구성 섹션을 나타냅니다 <xref:System.ServiceModel.Dispatcher.MessageFilter> 사용할 대상 끝점을 정의 하는 들어오는 메시지를 평가할 수 있을 뿐만 아니라 라우팅 테이블 필터가 일치할 때에 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c259-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>

<span data-ttu-id="0c259-104">[**\<system.serviceModel>**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="0c259-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="0c259-105">&nbsp;&nbsp;**\<routing>**</span><span class="sxs-lookup"><span data-stu-id="0c259-105">&nbsp;&nbsp;**\<routing>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0c259-106">구문</span><span class="sxs-lookup"><span data-stu-id="0c259-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
    <routingTables>
      <table name="String">
        <entries>
          <add endpoint="String"
               filterName="String"
               priority="Integer" />
        </entries>
      </table>
    </routingTables>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c259-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="0c259-107">Attributes and elements</span></span>

<span data-ttu-id="0c259-108">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0c259-108">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="0c259-109">특성</span><span class="sxs-lookup"><span data-stu-id="0c259-109">Attributes</span></span>

<span data-ttu-id="0c259-110">없음</span><span class="sxs-lookup"><span data-stu-id="0c259-110">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="0c259-111">자식 요소</span><span class="sxs-lookup"><span data-stu-id="0c259-111">Child elements</span></span>

|     | <span data-ttu-id="0c259-112">설명</span><span class="sxs-lookup"><span data-stu-id="0c259-112">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="0c259-113">**\<filters>**</span><span class="sxs-lookup"><span data-stu-id="0c259-113">**\<filters>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md) | <span data-ttu-id="0c259-114">들어오는 메시지를 평가할 때 Windows Communication Foundation (WCF) messagefilter 형식을 사용할지를 결정 하는 라우팅 필터 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c259-114">Contains a set of routing filters that determine the type of Windows Communication Foundation (WCF) MessageFilter will be used when evaluating incoming messages.</span></span> |
| [<span data-ttu-id="0c259-115">**\<filterTables>**</span><span class="sxs-lookup"><span data-stu-id="0c259-115">**\<filterTables>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) | <span data-ttu-id="0c259-116">필터가 일치할 때 사용할 엔드포인트를 지정하기 위한 라우팅 필터와 대상 엔드포인트 간의 매핑을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0c259-116">Contains mappings between the routing filters and the target endpoints to specify which endpoint to use when the filter matches.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="0c259-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="0c259-117">Parent elements</span></span>

|     | <span data-ttu-id="0c259-118">설명</span><span class="sxs-lookup"><span data-stu-id="0c259-118">Description</span></span> |
| --- | ----------- |
| <span data-ttu-id="0c259-119">**\<system.ServiceModel>**</span><span class="sxs-lookup"><span data-stu-id="0c259-119">**\<system.ServiceModel>**</span></span> | <span data-ttu-id="0c259-120">모든 WCF 구성 요소의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0c259-120">The root element of all WCF configuration elements.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0c259-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="0c259-121">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
