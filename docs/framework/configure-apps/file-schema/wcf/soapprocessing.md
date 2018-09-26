---
title: '&lt;soapProcessing&gt;'
ms.date: 03/30/2017
ms.assetid: e8707027-e6b8-4539-893d-3cd7c13fbc18
ms.openlocfilehash: 296993f1a91a6da93f01610357f35dac4cfab9e6
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47210149"
---
# <a name="ltsoapprocessinggt"></a><span data-ttu-id="445c7-102">&lt;soapProcessing&gt;</span><span class="sxs-lookup"><span data-stu-id="445c7-102">&lt;soapProcessing&gt;</span></span>

<span data-ttu-id="445c7-103">서로 다른 바인딩 형식과 메시지 버전 간에 메시지 마샬링을 위해 사용되는 클라이언트 엔드포인트 동작을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-103">Defines the client endpoint behavior used to marshal messages between different binding types and message versions.</span></span>

<span data-ttu-id="445c7-104">**\<시스템입니다. ServiceModel >** </span><span class="sxs-lookup"><span data-stu-id="445c7-104">**\<system.ServiceModel>** </span></span>  
<span data-ttu-id="445c7-105">&nbsp;&nbsp;**\<동작 >** </span><span class="sxs-lookup"><span data-stu-id="445c7-105">&nbsp;&nbsp;**\<behaviors>** </span></span>  
<span data-ttu-id="445c7-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<endpointBehaviors >** </span><span class="sxs-lookup"><span data-stu-id="445c7-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<endpointBehaviors>** </span></span>  
<span data-ttu-id="445c7-107">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<동작 >** </span><span class="sxs-lookup"><span data-stu-id="445c7-107">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<behavior>** </span></span>  
<span data-ttu-id="445c7-108">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<soapProcessing >**</span><span class="sxs-lookup"><span data-stu-id="445c7-108">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<soapProcessing>**</span></span>

## <a name="syntax"></a><span data-ttu-id="445c7-109">구문</span><span class="sxs-lookup"><span data-stu-id="445c7-109">Syntax</span></span>

```xml
<soapProcessing processMessages="true|false" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="445c7-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="445c7-110">Attributes and elements</span></span>

<span data-ttu-id="445c7-111">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-111">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="445c7-112">특성</span><span class="sxs-lookup"><span data-stu-id="445c7-112">Attributes</span></span>

|                   | <span data-ttu-id="445c7-113">설명</span><span class="sxs-lookup"><span data-stu-id="445c7-113">Description</span></span> |
| ----------------- | ----------- |
| `processMessages` | <span data-ttu-id="445c7-114">SOAP 메시지 버전 간에 메시지가 마샬링되어야 하는지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-114">A Boolean value that specifies whether messages should be marshaled between SOAP message versions.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="445c7-115">자식 요소</span><span class="sxs-lookup"><span data-stu-id="445c7-115">Child elements</span></span>

<span data-ttu-id="445c7-116">없음</span><span class="sxs-lookup"><span data-stu-id="445c7-116">None</span></span>

### <a name="parent-elements"></a><span data-ttu-id="445c7-117">부모 요소</span><span class="sxs-lookup"><span data-stu-id="445c7-117">Parent elements</span></span>

|     | <span data-ttu-id="445c7-118">설명</span><span class="sxs-lookup"><span data-stu-id="445c7-118">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="445c7-119">**\<동작 >**</span><span class="sxs-lookup"><span data-stu-id="445c7-119">**\<behavior>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) | <span data-ttu-id="445c7-120">엔드포인트 동작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-120">Specifies an endpoint behavior.</span></span> |

## <a name="remarks"></a><span data-ttu-id="445c7-121">설명</span><span class="sxs-lookup"><span data-stu-id="445c7-121">Remarks</span></span>

<span data-ttu-id="445c7-122">SOAP 처리는 메시지 버전 간에 메시지를 변환하는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-122">SOAP processing is the process where messages are converted between message versions.</span></span>

<span data-ttu-id="445c7-123">Windows Communication Foundation (WCF) 라우팅 서비스는 다른 프로토콜 중에서 메시지를 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-123">The Windows Communication Foundation (WCF) Routing Service can convert messages from one protocol to another.</span></span> <span data-ttu-id="445c7-124">들어오는 메시지 버전과 나가는 메시지 버전이 다른 경우 올바른 버전의 새로운 메시지가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-124">If the incoming and outgoing Message Versions are different, a new message of the correct version is created.</span></span> <span data-ttu-id="445c7-125">한 <xref:System.ServiceModel.Channels.MessageVersion>에서 다른 버전으로 메시지를 처리하는 작업은 들어오는 WCF 메시지의 본문 부분과 관련 헤더를 포함하는 새 WCF 메시지를 생성하는 방법으로 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-125">Processing messages from one <xref:System.ServiceModel.Channels.MessageVersion> to another is accomplished by constructing a new WCF message that contains the body part and relevant headers from the incoming WCF message.</span></span> <span data-ttu-id="445c7-126">주소 지정에만 사용되는 헤더나 라우터 수준에서 인식되는 헤더는 새 WCF 메시지 생성 중에 사용되지 않습니다. 이러한 헤더는 서로 다른 버전(주소 지정 헤더인 경우)이거나 클라이언트와 라우터 간의 통신의 일부로 처리되었기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-126">Headers that are specific to addressing, or that are understood at the router level, are not used during construction of the new WCF message because these headers are either of a different version (in the case of addressing headers) or have been processed as part of the communication between the client and the router.</span></span>

<span data-ttu-id="445c7-127">헤더가 아웃바운드 메시지에 배치되는지 여부는 들어오는 채널 계층을 통해 전달될 때 해당 헤더가 인식된 것으로 표시되었는지 여부에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-127">Whether a header is placed in the outbound message is determined by whether or not it was marked as understood as it passed through the incoming channel layer.</span></span> <span data-ttu-id="445c7-128">사용자 지정 헤더 등과 같이 인식되지 않는 헤더는 제거되지 않고 아웃바운드 메시지에 복사되어 라우팅 서비스를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-128">Headers that are not understood (such as custom headers) are not removed and so pass through the routing service by being copied to the outbound message.</span></span> <span data-ttu-id="445c7-129">메시지의 본문은 아웃바운드 메시지에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-129">The body of the message is copied to the outbound message.</span></span> <span data-ttu-id="445c7-130">그런 다음 메시지가 아웃바운드 채널로 전송되며 이때 해당 통신 프로토콜/전송에 대한 모든 헤더와 기타 봉투 데이터가 만들어지고 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-130">The message is then sent out the outbound channel, at which point all of the headers and other envelope data specific to that communication protocol/transport will be created and added.</span></span>

<span data-ttu-id="445c7-131">이러한 처리 단계는 SOAP 처리 동작이 지정될 때 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-131">Such processing steps take place when the SOAP processing behavior is specified.</span></span> <span data-ttu-id="445c7-132">이렇게 [ \<soapProcessingExtension >](../../../../../docs/framework/configure-apps/file-schema/wcf/soapprocessing.md) 동작은 라우팅 서비스를 시작할 때 모든 클라이언트 (나가는) 끝점에 적용 되는 끝점 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-132">This [\<soapProcessingExtension>](../../../../../docs/framework/configure-apps/file-schema/wcf/soapprocessing.md) behavior is an endpoint behavior that is applied to all client (outgoing) endpoints when the Routing Service starts up.</span></span> <span data-ttu-id="445c7-133">기본적으로는 [ \<라우팅 >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md) 동작을 만들고 새 연결 [ \<soapProcessingExtension >](../../../../../docs/framework/configure-apps/file-schema/wcf/soapprocessing.md) 동작 `processMessages` 로 `true` 각각에 대해 클라이언트 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-133">default, the [\<routing>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md) behavior creates and attaches a new [\<soapProcessingExtension>](../../../../../docs/framework/configure-apps/file-schema/wcf/soapprocessing.md) behavior with `processMessages` set to `true` for each client endpoint.</span></span> <span data-ttu-id="445c7-134">라우팅 서비스에서 인식하지 못하는 프로토콜을 사용하거나 기본 처리 동작을 재지정하려는 경우 전체 라우팅 서비스 또는 특정 엔드포인트에 대해 SOAP 처리를 사용하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-134">If you have a protocol that the Routing Service does not understand, or wish to override the default processing behavior, you can disable SOAP processing either for the entire Routing Service or just for particular endpoints.</span></span>  <span data-ttu-id="445c7-135">모든 끝점에서 전체 라우팅 서비스에 대해 SOAP 처리를 비활성화 하려면 설정 합니다 `soapProcessing` 특성을 [ \<라우팅 >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md) 동작을 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-135">To disable SOAP processing for the entire routing service on all endpoints, set the `soapProcessing` attribute of the [\<routing>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md) behavior to `false`.</span></span> <span data-ttu-id="445c7-136">특정 엔드포인트에 대해 SOAP 처리를 해제하려면 이 동작을 사용하여 `processMessages` 특성을 `false`로 설정한 다음 이 동작을 기본 처리 코드가 실행되지 않도록 할 엔드포인트에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-136">To turn off SOAP processing for a particular endpoint, use this behavior and set its `processMessages` attribute to `false`, then attach this behavior to the endpoint you do not want the default processing code to run at.</span></span>  <span data-ttu-id="445c7-137">경우는 [ \<라우팅 >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md) 동작은 라우팅 서비스를 설정, 이미 하나 있으므로 끝점 동작을 다시 적용 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="445c7-137">When the [\<routing>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md) behavior sets up the Routing Service, it will skip reapplying the endpoint behavior since one already exists.</span></span>
