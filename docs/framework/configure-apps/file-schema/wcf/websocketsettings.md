---
title: '&lt;webSocketSettings&gt;'
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: 00c6bc45f06d97d4f95bd6be1515d16141be4e1d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565919"
---
# <a name="ltwebsocketsettingsgt"></a><span data-ttu-id="a67c9-102">&lt;webSocketSettings&gt;</span><span class="sxs-lookup"><span data-stu-id="a67c9-102">&lt;webSocketSettings&gt;</span></span>
<span data-ttu-id="a67c9-103">WebSocket 설정을 지정하는 데 사용되는 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-103">A configuration element used to specify Web Socket settings.</span></span>  
  
<span data-ttu-id="a67c9-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a67c9-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a67c9-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="a67c9-105">\<bindings></span></span>  
<span data-ttu-id="a67c9-106">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="a67c9-106">\<netHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a67c9-107">구문</span><span class="sxs-lookup"><span data-stu-id="a67c9-107">Syntax</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="Boolean"
                       disablePayloadMasking="Boolean"
                       keepAliveInterval="TimeSpan"
                       maxPendingConnections="Integer"
                       receiveBufferSize="Integer"
                       sendBufferSize="Integer"
                       subProtocol="String"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a67c9-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="a67c9-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a67c9-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a67c9-110">특성</span><span class="sxs-lookup"><span data-stu-id="a67c9-110">Attributes</span></span>  
  
|<span data-ttu-id="a67c9-111">특성</span><span class="sxs-lookup"><span data-stu-id="a67c9-111">Attribute</span></span>|<span data-ttu-id="a67c9-112">설명</span><span class="sxs-lookup"><span data-stu-id="a67c9-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a67c9-113">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="a67c9-113">createNotificationOnConnection</span></span>|<span data-ttu-id="a67c9-114">연결 시 알림이 보내지는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-114">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="a67c9-115">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="a67c9-115">disablePayloadMasking</span></span>|<span data-ttu-id="a67c9-116">WebSocket 마스킹을 사용하지 않도록 설정할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-116">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="a67c9-117">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="a67c9-117">keepAliveInterval</span></span>|<span data-ttu-id="a67c9-118">상태 유지 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-118">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="a67c9-119">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="a67c9-119">maxPendingConnections</span></span>|<span data-ttu-id="a67c9-120">서비스에서 디스패치를 대기하는 최대 연결 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-120">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="a67c9-121">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="a67c9-121">receiveBufferSize</span></span>|<span data-ttu-id="a67c9-122">수신 버퍼의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-122">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="a67c9-123">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="a67c9-123">sendBufferSize</span></span>|<span data-ttu-id="a67c9-124">전송 버퍼의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-124">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="a67c9-125">subProtocol</span><span class="sxs-lookup"><span data-stu-id="a67c9-125">subProtocol</span></span>|<span data-ttu-id="a67c9-126">WebSocket 하위 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-126">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="a67c9-127">transportUsage</span><span class="sxs-lookup"><span data-stu-id="a67c9-127">transportUsage</span></span>|<span data-ttu-id="a67c9-128">WebSocket을 사용할 시기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-128">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="a67c9-129">transportUsage 특성</span><span class="sxs-lookup"><span data-stu-id="a67c9-129">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="a67c9-130">값</span><span class="sxs-lookup"><span data-stu-id="a67c9-130">Value</span></span>|<span data-ttu-id="a67c9-131">설명</span><span class="sxs-lookup"><span data-stu-id="a67c9-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="a67c9-132">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="a67c9-132">WhenDuplex</span></span>|<span data-ttu-id="a67c9-133">이중 계약인 경우 WebSocket 프로토콜을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-133">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="a67c9-134">Always</span><span class="sxs-lookup"><span data-stu-id="a67c9-134">Always</span></span>|<span data-ttu-id="a67c9-135">계약과 관계없이 항상 WebSocket 프로토콜을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-135">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="a67c9-136">Never</span><span class="sxs-lookup"><span data-stu-id="a67c9-136">Never</span></span>|<span data-ttu-id="a67c9-137">WebSocket 프로토콜을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-137">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a67c9-138">자식 요소</span><span class="sxs-lookup"><span data-stu-id="a67c9-138">Child Elements</span></span>  
 <span data-ttu-id="a67c9-139">없음</span><span class="sxs-lookup"><span data-stu-id="a67c9-139">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a67c9-140">부모 요소</span><span class="sxs-lookup"><span data-stu-id="a67c9-140">Parent Elements</span></span>  
  
|<span data-ttu-id="a67c9-141">요소</span><span class="sxs-lookup"><span data-stu-id="a67c9-141">Element</span></span>|<span data-ttu-id="a67c9-142">설명</span><span class="sxs-lookup"><span data-stu-id="a67c9-142">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a67c9-143">\<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="a67c9-143">\<netHttpBinding></span></span>|<span data-ttu-id="a67c9-144">NetHttpBinding을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-144">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a67c9-145">예제</span><span class="sxs-lookup"><span data-stu-id="a67c9-145">Example</span></span>  
 <span data-ttu-id="a67c9-146">다음 예제에서는 사용 하는 방법의 \<webSocketSettings > 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c9-146">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="true"
                       disablePayloadMasking="false"
                       keepAliveInterval="00:10:00"
                       maxPendingConnections="100"
                       receiveBufferSize="1000"
                       sendBufferSize="1000"
                       subProtocol="Soap"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="see-also"></a><span data-ttu-id="a67c9-147">참고자료</span><span class="sxs-lookup"><span data-stu-id="a67c9-147">See also</span></span>
- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- <xref:System.ServiceModel.BasicHttpBinding>
- <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>
- [<span data-ttu-id="a67c9-148">바인딩</span><span class="sxs-lookup"><span data-stu-id="a67c9-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="a67c9-149">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="a67c9-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="a67c9-150">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="a67c9-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="a67c9-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="a67c9-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
