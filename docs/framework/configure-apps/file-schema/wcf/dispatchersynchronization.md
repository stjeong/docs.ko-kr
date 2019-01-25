---
title: '&lt;dispatcherSynchronization&gt;'
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 537dee408f1af29a06042de439a2c1e7d7874222
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555390"
---
# <a name="ltdispatchersynchronizationgt"></a><span data-ttu-id="91516-102">&lt;dispatcherSynchronization&gt;</span><span class="sxs-lookup"><span data-stu-id="91516-102">&lt;dispatcherSynchronization&gt;</span></span>
  
<span data-ttu-id="91516-103">서비스에서 응답을 비동기적으로 보낼 수 있도록 하는 엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91516-103">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>  
  
<span data-ttu-id="91516-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="91516-104">\<system.serviceModel></span></span>  
<span data-ttu-id="91516-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="91516-105">\<behaviors></span></span>  
<span data-ttu-id="91516-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="91516-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="91516-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="91516-107">\<behavior></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91516-108">구문</span><span class="sxs-lookup"><span data-stu-id="91516-108">Syntax</span></span>  
  
```xml  
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean"
                                   maxPendingReceives="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="91516-109">형식</span><span class="sxs-lookup"><span data-stu-id="91516-109">Type</span></span>  
  
`Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="91516-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="91516-110">Attributes and elements</span></span>  
  
<span data-ttu-id="91516-111">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="91516-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="91516-112">특성</span><span class="sxs-lookup"><span data-stu-id="91516-112">Attributes</span></span>

| <span data-ttu-id="91516-113">특성</span><span class="sxs-lookup"><span data-stu-id="91516-113">Attribute</span></span>               | <span data-ttu-id="91516-114">설명</span><span class="sxs-lookup"><span data-stu-id="91516-114">Description</span></span>       |
| ----------------------- | ----------------- |
| <span data-ttu-id="91516-115">asynchronousSendEnabled</span><span class="sxs-lookup"><span data-stu-id="91516-115">asynchronousSendEnabled</span></span> | <span data-ttu-id="91516-116">비동기 보내기 동작 사용 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="91516-116">A Boolean that specifies whether asynchronous send behavior is enabled.</span></span> |
| `maxPendingReceives`    | <span data-ttu-id="91516-117">채널에서 발급할 수 있는 동시 수신의 수를 지정하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="91516-117">An integer that specifies the number of concurrent receives that can be issued on the channel.</span></span><br /><br /> <span data-ttu-id="91516-118">이 값은 서비스 스로틀 동작을 제대로 구성한 후에 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91516-118">This value should be configured only after you have properly configured service throttling behavior.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="91516-119">자식 요소</span><span class="sxs-lookup"><span data-stu-id="91516-119">Child elements</span></span>

<span data-ttu-id="91516-120">없음</span><span class="sxs-lookup"><span data-stu-id="91516-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="91516-121">부모 요소</span><span class="sxs-lookup"><span data-stu-id="91516-121">Parent elements</span></span>

| <span data-ttu-id="91516-122">요소</span><span class="sxs-lookup"><span data-stu-id="91516-122">Element</span></span> | <span data-ttu-id="91516-123">설명</span><span class="sxs-lookup"><span data-stu-id="91516-123">Description</span></span> |  
| ------- | ----------- |  
| [<span data-ttu-id="91516-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="91516-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="91516-125">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91516-125">Specifies an endpoint behavior.</span></span> |

## <a name="see-also"></a><span data-ttu-id="91516-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="91516-126">See also</span></span>

- <xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement>
- <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior>
