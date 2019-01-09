---
title: '&lt;callbackTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 85e7b1f0d009e27cbacd9f69b381e4f05984bf56
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149113"
---
# <a name="ltcallbacktimeoutsgt"></a><span data-ttu-id="e0421-102">&lt;callbackTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="e0421-102">&lt;callbackTimeouts&gt;</span></span>
<span data-ttu-id="e0421-103">이중 콜백 계약 시나리오에서 트랜잭션이 서버에서 클라이언트로 이동할 때의 시간 제한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0421-103">Specifies the timeout value when flowing transactions from server to client.in a duplex callback contract scenario.</span></span>  
  
 <span data-ttu-id="e0421-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e0421-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="e0421-105">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="e0421-105">\<behaviors></span></span>  
<span data-ttu-id="e0421-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="e0421-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="e0421-107">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="e0421-107">\<behavior></span></span>  
<span data-ttu-id="e0421-108">\<callbackTimeOuts ></span><span class="sxs-lookup"><span data-stu-id="e0421-108">\<callbackTimeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0421-109">구문</span><span class="sxs-lookup"><span data-stu-id="e0421-109">Syntax</span></span>  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />
```  
  
## <a name="type"></a><span data-ttu-id="e0421-110">형식</span><span class="sxs-lookup"><span data-stu-id="e0421-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e0421-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="e0421-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e0421-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e0421-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e0421-113">특성</span><span class="sxs-lookup"><span data-stu-id="e0421-113">Attributes</span></span>  
  
|<span data-ttu-id="e0421-114">특성</span><span class="sxs-lookup"><span data-stu-id="e0421-114">Attribute</span></span>|<span data-ttu-id="e0421-115">설명</span><span class="sxs-lookup"><span data-stu-id="e0421-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="e0421-116">트랜잭션이 완료되어야 하거나, 완료되지 못할 경우 자동으로 종료되어야 하는 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e0421-116">A <xref:System.TimeSpan> value that specifies the interval of time within which transactions must complete or be automatically terminated.</span></span> <span data-ttu-id="e0421-117">기본값은 "00: 00:00"입니다.</span><span class="sxs-lookup"><span data-stu-id="e0421-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e0421-118">자식 요소</span><span class="sxs-lookup"><span data-stu-id="e0421-118">Child Elements</span></span>  
 <span data-ttu-id="e0421-119">없음</span><span class="sxs-lookup"><span data-stu-id="e0421-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e0421-120">부모 요소</span><span class="sxs-lookup"><span data-stu-id="e0421-120">Parent Elements</span></span>  
  
|<span data-ttu-id="e0421-121">요소</span><span class="sxs-lookup"><span data-stu-id="e0421-121">Element</span></span>|<span data-ttu-id="e0421-122">설명</span><span class="sxs-lookup"><span data-stu-id="e0421-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0421-123">\<동작 ></span><span class="sxs-lookup"><span data-stu-id="e0421-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="e0421-124">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0421-124">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e0421-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e0421-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
