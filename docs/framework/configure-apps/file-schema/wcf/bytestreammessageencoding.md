---
title: '&lt;byteStreamMessageEncoding&gt;'
ms.date: 03/30/2017
ms.assetid: bbadd8dd-60a2-4007-b959-89373a8a7d60
ms.openlocfilehash: 9d38f16cdeb8b769f4026ccb29f9129e93ef031c
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146461"
---
# <a name="ltbytestreammessageencodinggt"></a><span data-ttu-id="4dc24-102">&lt;byteStreamMessageEncoding&gt;</span><span class="sxs-lookup"><span data-stu-id="4dc24-102">&lt;byteStreamMessageEncoding&gt;</span></span>
<span data-ttu-id="4dc24-103">문자 인코딩을 지정하는 옵션을 사용하여 메시지 인코딩을 바이트 스트림으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-103">Specifies the message encoding as a stream of bytes, with the option to specify the character encoding.</span></span>  
  
 <span data-ttu-id="4dc24-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4dc24-104">\<system.serviceModel></span></span>  
<span data-ttu-id="4dc24-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="4dc24-105">\<bindings></span></span>  
<span data-ttu-id="4dc24-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4dc24-106">\<customBinding></span></span>  
<span data-ttu-id="4dc24-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="4dc24-107">\<binding></span></span>  
<span data-ttu-id="4dc24-108">\<binaryMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="4dc24-108">\<binaryMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4dc24-109">구문</span><span class="sxs-lookup"><span data-stu-id="4dc24-109">Syntax</span></span>  
  
```xml  
<byteStreamMessageEncoding />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4dc24-110">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="4dc24-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4dc24-111">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4dc24-112">특성</span><span class="sxs-lookup"><span data-stu-id="4dc24-112">Attributes</span></span>  
  
|<span data-ttu-id="4dc24-113">특성</span><span class="sxs-lookup"><span data-stu-id="4dc24-113">Attribute</span></span>|<span data-ttu-id="4dc24-114">설명</span><span class="sxs-lookup"><span data-stu-id="4dc24-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4dc24-115">messageVersion</span><span class="sxs-lookup"><span data-stu-id="4dc24-115">messageVersion</span></span>|<span data-ttu-id="4dc24-116">바인딩을 사용하여 보낸 메시지의 SOAP 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-116">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="4dc24-117">이 속성은 <xref:System.ServiceModel.Channels.MessageVersion.None%2A>의 메시지 버전 값으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-117">This property can only be set to the message version value of <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span> <span data-ttu-id="4dc24-118">바이트 스트림 메시지 인코더는 다른 메시지 버전을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-118">The byte stream message encoder does not support any other message versions.</span></span><br /><br /> <span data-ttu-id="4dc24-119">이 특성은 <xref:System.ServiceModel.Channels.MessageVersion> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-119">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4dc24-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="4dc24-120">Child Elements</span></span>  
  
|<span data-ttu-id="4dc24-121">요소</span><span class="sxs-lookup"><span data-stu-id="4dc24-121">Element</span></span>|<span data-ttu-id="4dc24-122">설명</span><span class="sxs-lookup"><span data-stu-id="4dc24-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4dc24-123">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="4dc24-123">\<readerQuotas></span></span>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="4dc24-124">이 바인딩으로 구성된 엔드포인트에서 처리할 수 있는 SOAP 메시지의 복잡성에 대한 제약 조건을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-124">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="4dc24-125">이 요소는 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-125">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4dc24-126">부모 요소</span><span class="sxs-lookup"><span data-stu-id="4dc24-126">Parent Elements</span></span>  
  
|<span data-ttu-id="4dc24-127">요소</span><span class="sxs-lookup"><span data-stu-id="4dc24-127">Element</span></span>|<span data-ttu-id="4dc24-128">설명</span><span class="sxs-lookup"><span data-stu-id="4dc24-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4dc24-129">\<binding></span><span class="sxs-lookup"><span data-stu-id="4dc24-129">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="4dc24-130">사용자 지정 바인딩의 모든 바인딩 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc24-130">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4dc24-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4dc24-131">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ByteStreamMessageEncodingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>  
 <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>  
 [<span data-ttu-id="4dc24-132">메시지 인코딩</span><span class="sxs-lookup"><span data-stu-id="4dc24-132">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)  
 [<span data-ttu-id="4dc24-133">메시지 인코더 선택</span><span class="sxs-lookup"><span data-stu-id="4dc24-133">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)  
 [<span data-ttu-id="4dc24-134">바인딩</span><span class="sxs-lookup"><span data-stu-id="4dc24-134">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="4dc24-135">바인딩 확장</span><span class="sxs-lookup"><span data-stu-id="4dc24-135">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="4dc24-136">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="4dc24-136">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="4dc24-137">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4dc24-137">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
