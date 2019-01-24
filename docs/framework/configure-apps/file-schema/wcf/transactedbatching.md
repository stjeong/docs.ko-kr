---
title: '&lt;transactedBatching&gt;'
ms.date: 03/30/2017
ms.assetid: 2f790a0d-8f03-4b86-81b5-ce1bc1a6c575
ms.openlocfilehash: 2f89a1a6c2cc110a4695b792c5aa801b516393be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565997"
---
# <a name="lttransactedbatchinggt"></a><span data-ttu-id="4d2b5-102">&lt;transactedBatching&gt;</span><span class="sxs-lookup"><span data-stu-id="4d2b5-102">&lt;transactedBatching&gt;</span></span>
<span data-ttu-id="4d2b5-103">받기 작업에 트랜잭션 일괄 처리가 지원되는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-103">Specifies whether transaction batching is supported for receive operations.</span></span>  
  
 <span data-ttu-id="4d2b5-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="4d2b5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4d2b5-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="4d2b5-105">\<behaviors></span></span>  
<span data-ttu-id="4d2b5-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="4d2b5-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="4d2b5-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4d2b5-107">\<behavior></span></span>  
<span data-ttu-id="4d2b5-108">\<transactedBatching></span><span class="sxs-lookup"><span data-stu-id="4d2b5-108">\<transactedBatching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d2b5-109">구문</span><span class="sxs-lookup"><span data-stu-id="4d2b5-109">Syntax</span></span>  
  
```xml  
<transactedBatching maxBatchSize="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4d2b5-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4d2b5-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4d2b5-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4d2b5-112">특성</span><span class="sxs-lookup"><span data-stu-id="4d2b5-112">Attributes</span></span>  
  
|<span data-ttu-id="4d2b5-113">특성</span><span class="sxs-lookup"><span data-stu-id="4d2b5-113">Attribute</span></span>|<span data-ttu-id="4d2b5-114">설명</span><span class="sxs-lookup"><span data-stu-id="4d2b5-114">Description</span></span>|  
|---------------|-----------------|  
|`maxBatchSize`|<span data-ttu-id="4d2b5-115">트랜잭션 한 번으로 일괄 처리할 수 있는 받기 작업의 최대 수를 지정하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-115">An integer that specifies the maximum number of receive operations that can be batched together in one transaction.</span></span> <span data-ttu-id="4d2b5-116">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-116">The default is 0.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4d2b5-117">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4d2b5-117">Child Elements</span></span>  
 <span data-ttu-id="4d2b5-118">없음</span><span class="sxs-lookup"><span data-stu-id="4d2b5-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4d2b5-119">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4d2b5-119">Parent Elements</span></span>  
  
|<span data-ttu-id="4d2b5-120">요소</span><span class="sxs-lookup"><span data-stu-id="4d2b5-120">Element</span></span>|<span data-ttu-id="4d2b5-121">설명</span><span class="sxs-lookup"><span data-stu-id="4d2b5-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4d2b5-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="4d2b5-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="4d2b5-123">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-123">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4d2b5-124">설명</span><span class="sxs-lookup"><span data-stu-id="4d2b5-124">Remarks</span></span>  
 <span data-ttu-id="4d2b5-125">트랜잭션 일괄 처리로 구성된 전송에서 여러 개의 받기 작업을 한 번의 트랜잭션으로 일괄 처리하도록 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-125">A transport that is configured with transaction batching attempts to batch several receive operations into one transaction.</span></span> <span data-ttu-id="4d2b5-126">이렇게 하면 모든 받기 작업에서 트랜잭션을 만들고 이를 커밋하는 비용을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-126">By doing so, the relatively high cost of creating a transaction and committing it in every receive operation is avoided.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4d2b5-127">예제</span><span class="sxs-lookup"><span data-stu-id="4d2b5-127">Example</span></span>  
 <span data-ttu-id="4d2b5-128">다음 예제에서는 구성 파일에서 트랜잭션된 일괄 처리 동작을 서비스에 추가하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d2b5-128">The following example shows how to add the transacted batching behavior to a service in a configuration file.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <host>
        <baseAddresses>
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service" />
        </baseAddresses>
      </host>
      <!-- Define NetMsmqEndpoint -->
      <endpoint address="net.msmq://localhost/private/ServiceModelSamples"
                binding="netMsmqBinding"
                contract="Microsoft.ServiceModel.Samples.IQueueCalculator" />
      <!-- the mex endpoint is explosed at http://localhost:8000/ServiceModelSamples/service/mex -->
      <endpoint address="mex"
                binding="mexHttpBinding"
                contract="IMetadataExchange" />
    </service>
  </services>
  <behaviors>
    <endpointBehaviors>
      <behavior name="endpointBehavior">
        <transactedBatching maxBatchSize="10" />
      </behavior>
    </endpointBehaviors>
    <serviceBehaviors>
      <behavior name="CalculatorServiceBehavior">
        <serviceMetadata httpGetEnabled="true" />
      </behavior>
    </serviceBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="4d2b5-129">참고자료</span><span class="sxs-lookup"><span data-stu-id="4d2b5-129">See also</span></span>
- <xref:System.ServiceModel.Configuration.TransactedBatchingElement>
- <xref:System.ServiceModel.Description.TransactedBatchingBehavior>
