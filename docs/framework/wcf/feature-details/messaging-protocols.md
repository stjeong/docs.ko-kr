---
title: 메시징 프로토콜
ms.date: 03/30/2017
ms.assetid: 5b20bca7-87b3-4c8f-811b-f215b5987104
ms.openlocfilehash: 7d94b917f3d8d2fd7faed28b9320edc240724e0b
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46703013"
---
# <a name="messaging-protocols"></a><span data-ttu-id="0229b-102">메시징 프로토콜</span><span class="sxs-lookup"><span data-stu-id="0229b-102">Messaging Protocols</span></span>

<span data-ttu-id="0229b-103">Windows Communication Foundation (WCF) 채널 스택에 내부 메시지 표현을 통신 형식으로 변환 하는 특정 전송을 사용 하 여 보내는 인코딩 및 전송 채널을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-103">The Windows Communication Foundation (WCF) channel stack employs encoding and transport channels to transform internal message representation into its wire format and send it by using a particular transport.</span></span> <span data-ttu-id="0229b-104">웹 서비스 상호 운용성을 위해 사용되는 가장 일반적인 전송은 HTTP이고, 웹 서비스에 사용되는 가장 일반적인 인코딩은 XML 기반 SOAP 1.1, SOAP 1.2 및 MTOM(Message Transmission Optimization Mechanism)입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-104">The most common transport used for Web services interoperability is HTTP, and the most common encodings used by Web services are XML-based SOAP 1.1, SOAP 1.2, and Message Transmission Optimization Mechanism (MTOM).</span></span>

<span data-ttu-id="0229b-105">이 항목에서는 WCF 구현 정보에서 사용 하는 다음 프로토콜에 대해 <xref:System.ServiceModel.Channels.HttpTransportBindingElement>합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-105">This topic covers WCF implementation details for the following protocols employed by <xref:System.ServiceModel.Channels.HttpTransportBindingElement>.</span></span>

<span data-ttu-id="0229b-106">사양/문서:</span><span class="sxs-lookup"><span data-stu-id="0229b-106">Specification/document:</span></span>

- [<span data-ttu-id="0229b-107">HTTP 1.1</span><span class="sxs-lookup"><span data-stu-id="0229b-107">HTTP 1.1</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
- <span data-ttu-id="0229b-108">[SOAP 1.1 HTTP 바인딩](https://www.w3.org/TR/2000/NOTE-SOAP-20000508), 섹션 7</span><span class="sxs-lookup"><span data-stu-id="0229b-108">[SOAP 1.1 HTTP Binding](https://www.w3.org/TR/2000/NOTE-SOAP-20000508), Section 7</span></span>
- <span data-ttu-id="0229b-109">[SOAP 1.2 HTTP 바인딩](https://www.w3.org/TR/soap12-part2) 섹션 7</span><span class="sxs-lookup"><span data-stu-id="0229b-109">[SOAP 1.2 HTTP Binding](https://www.w3.org/TR/soap12-part2) Section 7</span></span>

<span data-ttu-id="0229b-110">이 항목에서는 다음 프로토콜에 대 한 WCF 구현 세부 정보를 다룹니다 <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement> 고 <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement> 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-110">This topic covers WCF implementation details for the following protocols  that <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement> and <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement> employ.</span></span>

<span data-ttu-id="0229b-111">사양/문서:</span><span class="sxs-lookup"><span data-stu-id="0229b-111">Specification/Document:</span></span>

- [<span data-ttu-id="0229b-112">XML</span><span class="sxs-lookup"><span data-stu-id="0229b-112">XML</span></span>](https://www.w3.org/TR/REC-xml)
- [<span data-ttu-id="0229b-113">SOAP 1.1</span><span class="sxs-lookup"><span data-stu-id="0229b-113">SOAP 1.1</span></span>](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/)
- [<span data-ttu-id="0229b-114">SOAP 1.2 코어</span><span class="sxs-lookup"><span data-stu-id="0229b-114">SOAP 1.2 Core</span></span>](https://www.w3.org/TR/soap12-part1/)
- [<span data-ttu-id="0229b-115">Ws-addressing 2004/08</span><span class="sxs-lookup"><span data-stu-id="0229b-115">WS-Addressing 2004/08</span></span>](https://www.w3.org/Submission/2004/SUBM-ws-addressing-20040810/)
- [<span data-ttu-id="0229b-116">W3C Web Services 주소 지정 1.0-Core</span><span class="sxs-lookup"><span data-stu-id="0229b-116">W3C Web Services Addressing 1.0 - Core</span></span>](https://www.w3.org/TR/2006/REC-ws-addr-core-20060509)
- [<span data-ttu-id="0229b-117">W3C Web Services Addressing 1.0-SOAP 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-117">W3C Web Services Addressing 1.0 - SOAP Binding</span></span>](https://www.w3.org/TR/2006/REC-ws-addr-soap-20060509)
- [<span data-ttu-id="0229b-118">W3C Web Services Addressing 1.0-WSDL 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-118">W3C Web Services Addressing 1.0 - WSDL Binding</span></span>](https://www.w3.org/TR/2006/CR-ws-addr-wsdl-20060529/)
- [<span data-ttu-id="0229b-119">W3C Web Services 주소 지정 1.0-메타 데이터</span><span class="sxs-lookup"><span data-stu-id="0229b-119">W3C Web Services Addressing 1.0 - Metadata</span></span>](https://www.w3.org/TR/ws-addr-metadata/)
- [<span data-ttu-id="0229b-120">WSDL SOAP1.1 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-120">WSDL SOAP1.1 Binding</span></span>](https://www.w3.org/TR/wsdl/)
- [<span data-ttu-id="0229b-121">WSDL SOAP1.2 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-121">WSDL SOAP1.2 Binding</span></span>](https://www.w3.org/Submission/wsdl11soap12/)

<span data-ttu-id="0229b-122">이 항목에서는 다음 프로토콜에 대 한 WCF 구현 세부 정보를 다룹니다 <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement> 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-122">This topic covers WCF implementation details for the following protocols that <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement> employs.</span></span>

<span data-ttu-id="0229b-123">사양/문서:</span><span class="sxs-lookup"><span data-stu-id="0229b-123">Specification/document:</span></span>

- [<span data-ttu-id="0229b-124">XOP</span><span class="sxs-lookup"><span data-stu-id="0229b-124">XOP</span></span>](https://www.w3.org/TR/xop10/)
- [<span data-ttu-id="0229b-125">MTOM + SOAP 1.2 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-125">MTOM + SOAP 1.2 Binding</span></span>](https://www.w3.org/TR/soap12-mtom/)
- [<span data-ttu-id="0229b-126">MTOM SOAP 1.1 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-126">MTOM SOAP 1.1 Binding</span></span>](https://www.w3.org/Submission/soap11mtom10/)
- [<span data-ttu-id="0229b-127">MTOM Ws-policy Assertion</span><span class="sxs-lookup"><span data-stu-id="0229b-127">MTOM WS-Policy Assertion</span></span>](https://www.w3.org/Submission/2006/SUBM-WS-MTOMPolicy-20061101/)

<span data-ttu-id="0229b-128">다음 XML 네임 스페이스 및 관련된 접두사는이 항목 전체에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-128">The following XML namespaces and associated prefixes are used throughout this topic:</span></span>

<span data-ttu-id="0229b-129">| 접두사 | Namespace Uniform Resource Identifier (URI) | [---|---| | s11 | `http://schemas.xmlsoap.org/soap/envelope`| | s12 | `http://www.w3.org/2003/05/soap-envelope`| | wsa | `http://www.w3.org/2004/08/addressing`| | wsam | `http://www.w3.org/2007/05/addressing/metadata`| | wsap | `http://schemas.xmlsoap.org/ws/2004/09/policy/addressing`| | wsa10 | `http://www.w3.org/2005/08/addressing`| | wsaw10 | `http://www.w3.org/2006/05/addressing/wsdl`| | xop | `http://www.w3.org/2004/08/xop/include`| | xmime |`http://www.w3.org/2004/06/xmlmime`</span><span class="sxs-lookup"><span data-stu-id="0229b-129">|Prefix|Namespace Uniform Resource Identifier (URI)| [------------|---------------------------------------------------| |s11|`http://schemas.xmlsoap.org/soap/envelope`| |s12|`http://www.w3.org/2003/05/soap-envelope`| |wsa|`http://www.w3.org/2004/08/addressing`| |wsam|`http://www.w3.org/2007/05/addressing/metadata`| |wsap|`http://schemas.xmlsoap.org/ws/2004/09/policy/addressing`| |wsa10|`http://www.w3.org/2005/08/addressing`| |wsaw10|`http://www.w3.org/2006/05/addressing/wsdl`| |xop|`http://www.w3.org/2004/08/xop/include`| |xmime|`http://www.w3.org/2004/06/xmlmime`</span></span><br /><br /> <span data-ttu-id="0229b-130">`http://www.w3.org/2005/05/xmlmime`| | dp |`http://schemas.microsoft.com/net/2006/06/duplex`|</span><span class="sxs-lookup"><span data-stu-id="0229b-130">`http://www.w3.org/2005/05/xmlmime`| |dp|`http://schemas.microsoft.com/net/2006/06/duplex`|</span></span>

## <a name="soap-11-and-soap-12"></a><span data-ttu-id="0229b-131">SOAP 1.1 및 SOAP 1.2</span><span class="sxs-lookup"><span data-stu-id="0229b-131">SOAP 1.1 and SOAP 1.2</span></span>

### <a name="envelope-and-processing-model"></a><span data-ttu-id="0229b-132">봉투 및 처리 모델</span><span class="sxs-lookup"><span data-stu-id="0229b-132">Envelope and Processing Model</span></span>
<span data-ttu-id="0229b-133">WCF는 SOAP 1.1 봉투 처리 (BP11) Basic Profile 1.1 및 Basic Profile 1.0 (SSBP10)를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-133">WCF implements SOAP 1.1 envelope processing following Basic Profile 1.1 (BP11) and Basic Profile 1.0 (SSBP10).</span></span> <span data-ttu-id="0229b-134">SOAP 1.2 봉투 처리는 SOAP12-Part1에 따라 구현됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-134">SOAP 1.2 Envelope processing is implemented following SOAP12-Part1.</span></span>

<span data-ttu-id="0229b-135">이 섹션에서는 BP11 및 SOAP12-Part1 관련 하 여 WCF에 의해 특정 구현 선택 항목을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-135">This section explains certain implementation choices taken by WCF with regard to BP11 and SOAP12-Part1.</span></span>

#### <a name="mandatory-header-processing"></a><span data-ttu-id="0229b-136">필수 헤더 처리</span><span class="sxs-lookup"><span data-stu-id="0229b-136">Mandatory Header Processing</span></span>
<span data-ttu-id="0229b-137">WCF 헤더 처리에 대 한 규칙을 따릅니다 `mustUnderstand` 다음과 같은 형태로 사용 하 여 SOAP 1.1과 SOAP 1.2 사양에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-137">WCF follows rules for processing headers marked `mustUnderstand` described in the SOAP 1.1 and SOAP 1.2 specifications, with the following variations.</span></span>

<span data-ttu-id="0229b-138">메시지가 WCF 채널 스택은 입력 하는 예를 들어 관련된 바인딩 요소로 구성 된 개별 채널, 텍스트 메시지 인코딩, 보안, 안정적인 메시징 및 트랜잭션에 의해 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-138">A message that enters the WCF channel stack is processed by individual channels configured by associated binding elements, for example, Text Message Encoding, Security, Reliable Messaging, and Transactions.</span></span> <span data-ttu-id="0229b-139">각 채널은 연결된 네임스페이스에서 헤더를 인식한 후 인식된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-139">Each channel recognizes headers from the associated namespace and marks them as understood.</span></span> <span data-ttu-id="0229b-140">메시지가 디스패처에 전달되면 작업 포맷터는 해당 메시지/작업 계약에 필요한 헤더를 읽고 인식된 것으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-140">Once a message enters the dispatcher, the operation formatter reads headers expected by the corresponding message/operation contract and marks them understood.</span></span> <span data-ttu-id="0229b-141">그런 다음 디스패처는 나머지 헤더가 인식되지 않았지만 `mustUnderstand`로 표시되지 않았는지 확인하고 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-141">Then the dispatcher verifies whether any remaining headers are not understood but marked as `mustUnderstand` and throws an exception.</span></span> <span data-ttu-id="0229b-142">받는 사람을 대상으로 하는 `mustUnderstand` 헤더가 포함된 메시지는 받는 사람 응용 프로그램 코드로 처리되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-142">Messages that contain `mustUnderstand` headers that are targeted at the recipient are not processed by recipient application code.</span></span>

<span data-ttu-id="0229b-143">이러한 계층화된 처리를 사용하면 SOAP 노드의 응용 프로그램 계층과 인프라 계층을 분리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-143">Such layered processing allows for separation between infrastructure layers and application layers of the SOAP node:</span></span>

- <span data-ttu-id="0229b-144">B1111: 인식 되지 않는 헤더 메시지는 WCF 인프라 채널 스택에서 처리 된 후 하지만 응용 프로그램에서 처리 되기 전에 검색 된</span><span class="sxs-lookup"><span data-stu-id="0229b-144">B1111: Headers that are not understood are detected after the message is processed by the WCF infrastructure channel stack, but before it is processed by application</span></span>

     <span data-ttu-id="0229b-145">SOAP 1.1과 SOAP 1.2의 `mustUnderstand` 헤더 값은 서로 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-145">The `mustUnderstand` header value differs between SOAP 1.1 and SOAP 1.2.</span></span> <span data-ttu-id="0229b-146">Basic Profile 1.1에서 SOAP 1.1 메시지의 `mustUnderstand` 값은 0 또는 1이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-146">Basic Profile 1.1 requires that the `mustUnderstand` value be 0 or 1 for SOAP 1.1 messages.</span></span> <span data-ttu-id="0229b-147">SOAP 1.2에서는 0, 1, `false` 및 `true`를 값으로 사용할 수 있지만 정식으로 표현된 `xs:boolean` 값(`false`, `true`)을 내보내는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-147">SOAP 1.2 allows 0, 1, `false`, and `true` as values, but recommends emitting a canonical representation of `xs:boolean` values (`false`, `true`).</span></span>

- <span data-ttu-id="0229b-148">B1112: WCF 내보냅니다 `mustUnderstand` 값 0과 1 SOAP 1.1 및 SOAP 1.2 버전 SOAP 봉투의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-148">B1112: WCF emits `mustUnderstand` values 0 and 1 for both SOAP 1.1 and SOAP 1.2 versions of the SOAP envelope.</span></span> <span data-ttu-id="0229b-149">전체 값 공간을 허용 하는 WCF `xs:boolean` 에 대 한 합니다 `mustUnderstand` 머리글 (0, 1, `false`, `true`)</span><span class="sxs-lookup"><span data-stu-id="0229b-149">WCF accepts the entire value space of `xs:boolean` for the `mustUnderstand` header (0, 1, `false`, `true`)</span></span>

#### <a name="soap-faults"></a><span data-ttu-id="0229b-150">SOAP 오류</span><span class="sxs-lookup"><span data-stu-id="0229b-150">SOAP Faults</span></span>
<span data-ttu-id="0229b-151">다음은 WCF 관련 SOAP 오류 구현 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-151">The following is a list of WCF-specific SOAP fault implementations.</span></span>

- <span data-ttu-id="0229b-152">B2121: WCF에는 다음 SOAP 1.1 오류 코드를 반환 합니다. `s11:mustUnderstand`, `s11:Client`, 및 `s11:Server`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-152">B2121: WCF returns the following SOAP 1.1 Fault Codes: `s11:mustUnderstand`, `s11:Client`, and `s11:Server`.</span></span>

- <span data-ttu-id="0229b-153">B2122: WCF에는 다음 SOAP 1.2 오류 코드를 반환 합니다. `s12:MustUnderstand`, `s12:Sender`, 및 `s12:Receiver`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-153">B2122: WCF returns the following SOAP 1.2 Fault Codes: `s12:MustUnderstand`, `s12:Sender`, and `s12:Receiver`.</span></span>

### <a name="http-binding"></a><span data-ttu-id="0229b-154">HTTP 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-154">HTTP Binding</span></span>

#### <a name="soap-11-http-binding"></a><span data-ttu-id="0229b-155">SOAP 1.1 HTTP 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-155">SOAP 1.1 HTTP Binding</span></span>
<span data-ttu-id="0229b-156">WCF는 Basic Profile 1.1 사양 단원 3.4에 따라 SOAP1.1 HTTP 바인딩을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-156">WCF implements SOAP1.1 HTTP binding following the Basic Profile 1.1 specification section 3.4 with the following clarifications:</span></span>

- <span data-ttu-id="0229b-157">B2211: WCF 서비스 HTTP POST 요청의 리디렉션을 구현 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-157">B2211: WCF service does not implement redirection of HTTP POST requests.</span></span>

- <span data-ttu-id="0229b-158">B2212: WCF 클라이언트 3.4.8에 따라 HTTP 쿠키를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-158">B2212: WCF clients support HTTP Cookies in accordance with 3.4.8.</span></span>

#### <a name="soap-12-http-binding"></a><span data-ttu-id="0229b-159">SOAP 1.2 HTTP 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-159">SOAP 1.2 HTTP Binding</span></span>
<span data-ttu-id="0229b-160">WCF에 SOAP 1.2-part 2 (SOAP12Part2) 사양에 설명 된 대로 SOAP 1.2 HTTP 바인딩을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-160">WCF implements SOAP 1.2 HTTP binding as described in the SOAP 1.2-part 2 (SOAP12Part2) specification with the following clarifications.</span></span>

<span data-ttu-id="0229b-161">SOAP 1.2에는 `application/soap+xml` 미디어 유형에 대한 선택적 작업 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-161">SOAP 1.2 introduced an optional action parameter for the `application/soap+xml` media type.</span></span> <span data-ttu-id="0229b-162">이 매개 변수는 WS-Addressing을 사용하지 않을 때 SOAP 메시지 본문을 구문 분석할 필요 없이 메시지 디스패치를 최적화하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-162">This parameter is useful to optimize message dispatch without requiring that the body of the SOAP message be parsed when WS-Addressing is not used.</span></span>

- <span data-ttu-id="0229b-163">R2221: `application/soap+xml` 작업 매개 변수(SOAP 1.2 요청에 있는 경우)는 해당 WSDL 바인딩 내 `soapAction` 요소의 `wsoap12:operation` 특성과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-163">R2221: The `application/soap+xml` action parameter, when present on a SOAP 1.2 request, must match the `soapAction` attribute on the `wsoap12:operation` element inside the corresponding WSDL binding.</span></span>

- <span data-ttu-id="0229b-164">R2222: WS-Addressing 2004/08 또는 WS-Addressing 1.0을 사용할 경우 `application/soap+xml` 작업 매개 변수(SOAP 1.2 메시지에 있는 경우)가 `wsa:Action`과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-164">R2222: The `application/soap+xml` action parameter, when present on a SOAP 1.2 message, must match `wsa:Action` when WS-Addressing 2004/08 or WS-Addressing 1.0 are used.</span></span>

<span data-ttu-id="0229b-165">WS-Addressing을 사용하지 않고 들어오는 요청에 작업 매개 변수가 없는 경우 메시지 `Action`이 지정되지 않은 것으로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-165">When WS-Addressing is disabled and an incoming request does not contain an action parameter, message `Action` is considered not specified.</span></span>

## <a name="ws-addressing"></a><span data-ttu-id="0229b-166">WS-Addressing</span><span class="sxs-lookup"><span data-stu-id="0229b-166">WS-Addressing</span></span>
<span data-ttu-id="0229b-167">WCF는 세 가지 버전의 Ws-addressing을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-167">WCF implements 3 versions of WS-Addressing:</span></span>

- <span data-ttu-id="0229b-168">WS-Addressing 2004/08</span><span class="sxs-lookup"><span data-stu-id="0229b-168">WS-Addressing 2004/08</span></span>

- <span data-ttu-id="0229b-169">W3C Web Services Addressing 1.0 Core(ADDR10-CORE) 및 SOAP 바인딩(ADDR10-SOAP)</span><span class="sxs-lookup"><span data-stu-id="0229b-169">W3C Web Services Addressing 1.0 Core  (ADDR10-CORE) and SOAP Binding (ADDR10-SOAP)</span></span>

- <span data-ttu-id="0229b-170">WS-Addressing 1.0 - Metadata</span><span class="sxs-lookup"><span data-stu-id="0229b-170">WS-Addressing 1.0 - Metadata</span></span>

### <a name="endpoint-references"></a><span data-ttu-id="0229b-171">엔드포인트 참조</span><span class="sxs-lookup"><span data-stu-id="0229b-171">Endpoint References</span></span>
<span data-ttu-id="0229b-172">모든 버전의 Ws-addressing WCF 구현 하는 끝점 참조를 사용 하 여 끝점을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-172">All versions of WS-Addressing that WCF implements use endpoint references to describe endpoints.</span></span>

#### <a name="endpoint-references-and-ws-addressing-versions"></a><span data-ttu-id="0229b-173">엔드포인트 참조 및 WS-Addressing 버전</span><span class="sxs-lookup"><span data-stu-id="0229b-173">Endpoint References and WS-Addressing Versions</span></span>
<span data-ttu-id="0229b-174">WCF 숫자로 특정 및 Ws-addressing을 사용 하는 인프라 프로토콜을 구현 합니다 `EndpointReference` 요소 및 `W3C.WsAddressing.EndpointReferenceType` 클래스 (예를 들어, WS-ReliableMessaging, Ws-secureconversation, Ws-trust).</span><span class="sxs-lookup"><span data-stu-id="0229b-174">WCF implements a number of the infrastructure protocols that use WS-Addressing and in particular the `EndpointReference` element and `W3C.WsAddressing.EndpointReferenceType` class (for example, WS-ReliableMessaging, WS-SecureConversation, and WS-Trust).</span></span> <span data-ttu-id="0229b-175">WCF의 다른 인프라 프로토콜과 함께 Ws-addressing 버전 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-175">WCF supports the use of either version of WS-Addressing with other infrastructure protocols.</span></span> <span data-ttu-id="0229b-176">WCF 끝점 끝점당 하나의 버전의 Ws-addressing을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-176">WCF endpoints support one version of WS-Addressing per endpoint.</span></span>

<span data-ttu-id="0229b-177">R3111에서 네임 스페이스는 `EndpointReference` 요소나 WCF 끝점 교환 된 메시지에 사용 되는 형식은 ws-addressing이 끝점에서 구현 된 버전과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-177">For R3111, the namespace for the `EndpointReference` element or type used in messages exchanged with a WCF endpoint must match the version of WS-Addressing implemented by this endpoint.</span></span>

<span data-ttu-id="0229b-178">예를 들어 WCF 종단점 WS-ReliableMessaging 구현 하는 경우는 `AcksTo` 에서 이러한 끝점에 의해 반환 되는 헤더 `CreateSequenceResponse` Ws-addressing 버전을 사용 하는 `EncodingBinding` 이 끝점에 대 한 요소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-178">For example, if a WCF endpoint implements WS-ReliableMessaging, the `AcksTo` header returned by such an endpoint inside `CreateSequenceResponse` uses the WS-Addressing version that the `EncodingBinding` element specifies for this endpoint.</span></span>

#### <a name="endpoint-references-and-metadata"></a><span data-ttu-id="0229b-179">엔드포인트 참조 및 메타데이터</span><span class="sxs-lookup"><span data-stu-id="0229b-179">Endpoint References and Metadata</span></span>
<span data-ttu-id="0229b-180">대부분의 시나리오에서는 지정된 엔드포인트에 대해 메타데이터 또는 메타데이터 참조를 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-180">A number of scenarios require communicating metadata or a reference to metadata for a given endpoint.</span></span>

<span data-ttu-id="0229b-181">B3121: WCF에서 Ws-metadataexchange (MEX) 사양 단원 6 값별 또는 참조별 끝점 참조에 대 한 메타 데이터를 포함 하는에 설명 된 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-181">B3121: WCF employs mechanisms described in the WS-MetadataExchange (MEX) specification Section 6 to include metadata for endpoint references by value or by reference.</span></span>

<span data-ttu-id="0229b-182">WCF 서비스에서 토큰 발급자가 발급 한 보안 Assertions Markup Language (SAML) 토큰을 사용 하 여 인증이 필요로 하는 경우를 고려해 보십시오 `http://sts.fabrikam123.com`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-182">Consider a scenario where a WCF service requires authentication using a Security Assertions Markup Language (SAML) token issued by the token issuer at `http://sts.fabrikam123.com`.</span></span> <span data-ttu-id="0229b-183">WCF 끝점을 사용 하 여이 인증 요구 사항을 설명 `sp:IssuedToken` 중첩 된 어설션 `sp:Issuer` 토큰 발급자를 가리키는 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-183">The WCF endpoint describes this authentication requirement by using `sp:IssuedToken` assertion with a nested `sp:Issuer` assertion pointing to the token issuer.</span></span> <span data-ttu-id="0229b-184">`sp:Issuer` 어설션에 액세스하는 클라이언트 응용 프로그램은 토큰 발급자 엔드포인트와 통신하는 방법을 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-184">Client applications that access the `sp:Issuer` assertion need to know how to communicate with the token issuer endpoint.</span></span> <span data-ttu-id="0229b-185">클라이언트는 토큰 발급자에 대한 메타데이터를 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-185">The client needs to know metadata about the token issuer.</span></span> <span data-ttu-id="0229b-186">MEX에 정의 된 끝점 참조 메타 데이터 확장을 사용 하 여을 WCF 토큰 발급자 메타 데이터에 대 한 참조를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-186">Using the endpoint reference metadata extensions defined in MEX, WCF provides a reference to the token issuer metadata.</span></span>

```xml
<sp:IssuedToken>
  <sp:Issuer>
    <wsa10:Address>
      http://sts.fabrikam123.com
    </wsa10:Address>
    <wsa10:Metadata>
      <mex:Metadata>
        <mex:MetadataSection>
          <mex:MetadataReference>
            <wsa10:Address>
              http://sts.fabrikam123.com/mex
            </wsa10:Address>
          </mex:MetadataReference>
        </mex:MetadataSection>
      </mex:Metadata>
    </wsa10:Metadata>
  </sp:Issuer>
</sp:IssuedToken>
```

### <a name="message-addressing-headers"></a><span data-ttu-id="0229b-187">메시지 주소 지정 헤더</span><span class="sxs-lookup"><span data-stu-id="0229b-187">Message Addressing Headers</span></span>

#### <a name="message-headers"></a><span data-ttu-id="0229b-188">메시지 헤더</span><span class="sxs-lookup"><span data-stu-id="0229b-188">Message Headers</span></span>
<span data-ttu-id="0229b-189">두 Ws-addressing 버전에 대해 WCF 사용 하 여 같은 메시지 헤더 사양에서 설명 했 듯이 `wsa:To`, `wsa:ReplyTo`를 `wsa:Action`를 `wsa:MessageID`, 및 `wsa:RelatesTo`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-189">For both WS-Addressing versions, WCF uses the following message headers as prescribed by the specifications `wsa:To`, `wsa:ReplyTo`, `wsa:Action`, `wsa:MessageID`,and `wsa:RelatesTo`.</span></span>

<span data-ttu-id="0229b-190">B3211: 모든 Ws-addressing 버전에 대해 WCF 하지만 기본적으로 Ws-addressing 메시지 헤더를 생성 하지 않습니다 `wsa:FaultTo` 고 `wsa:From`입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-190">B3211: For all WS-Addressing versions, WCF honors, but does not produce out of the box, WS-Addressing message headers `wsa:FaultTo` and `wsa:From`.</span></span>

<span data-ttu-id="0229b-191">WCF 응용 프로그램을 사용 하 여 응용 프로그램 상호 작용 하는 이러한 메시지 헤더 및 WCF에서 처리 적절 하 게 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-191">Applications that interact with WCF applications can add these message headers and WCF will process them accordingly.</span></span>

#### <a name="reference-parameters-and-properties"></a><span data-ttu-id="0229b-192">참조 매개 변수 및 속성</span><span class="sxs-lookup"><span data-stu-id="0229b-192">Reference Parameters and Properties</span></span>

<span data-ttu-id="0229b-193">WCF 끝점 참조 매개 변수 및 해당 사양에 따라 참조 속성의 처리를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-193">WCF implements processing of endpoint reference parameters and reference properties in accordance with respective specifications.</span></span>

<span data-ttu-id="0229b-194">B3221: Ws-addressing 2004/08을 사용 하도록 구성 되 면 WCF 끝점 구분 하지 않습니다 참조 속성과 참조 매개 변수를 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-194">B3221: When configured to use WS-Addressing 2004/08, WCF endpoints do not differentiate between processing Reference Properties and Reference Parameters.</span></span>

### <a name="message-exchange-patterns"></a><span data-ttu-id="0229b-195">메시지 교환 패턴</span><span class="sxs-lookup"><span data-stu-id="0229b-195">Message Exchange Patterns</span></span>
<span data-ttu-id="0229b-196">웹 서비스 작업 호출에 관련 된 메시지의 시퀀스 라고 합니다 *메시지 교환 패턴*합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-196">The sequence of messages involved in the Web service operation invocation is referred to as the *message exchange pattern*.</span></span> <span data-ttu-id="0229b-197">지 원하는 WCF 단방향, 요청-회신 및 이중 메시지 교환 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-197">WCF supports one-way, request-reply, and duplex message exchange patterns.</span></span> <span data-ttu-id="0229b-198">이 단원에서는 사용 중인 메시지 교환 패턴에 따른 메시지 처리에 대한 WS-Addressing 요구 사항에 대해 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-198">This section clarifies WS-Addressing requirements on message processing depending on the message exchange pattern being used.</span></span>

<span data-ttu-id="0229b-199">이 단원에서 요청자는 첫 번째 메시지를 보내고 응답자는 첫 번째 메시지를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-199">Throughout this section, the requester sends the first message and the responder receives the first message.</span></span>

#### <a name="one-way-message"></a><span data-ttu-id="0229b-200">단방향 메시지</span><span class="sxs-lookup"><span data-stu-id="0229b-200">One-Way Message</span></span>
<span data-ttu-id="0229b-201">WCF 끝점을 사용 하 여 메시지를 지원 하도록 구성 된 경우는 지정 된 `Action` 단방향 패턴에 따라 WCF 끝점 동작 및 요구 사항을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-201">When a WCF endpoint is configured to support messages with a given `Action` to follow a one-way pattern, the WCF endpoint follows the following behaviors and requirements.</span></span> <span data-ttu-id="0229b-202">달리 지정 하지 않는 한 동작과 규칙의 두 버전의 Ws-addressing WCF에서 지원 되는 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-202">Unless otherwise specified, behaviors and rules apply for both versions of WS-Addressing supported in WCF:</span></span>

- <span data-ttu-id="0229b-203">R3311: 요청자는 `wsa:To`, `wsa:Action` 및 엔드포인트 참조에 지정된 모든 참조 매개 변수에 대한 헤더를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-203">R3311: The requester must include `wsa:To`, `wsa:Action`, and headers for all reference parameters specified by the endpoint reference.</span></span> <span data-ttu-id="0229b-204">WS-Addressing 2004/08을 사용하고 [reference properties]이 엔드포인트 참조에 지정된 경우에도 해당 헤더를 메시지에 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-204">When WS-Addressing 2004/08 is used and [reference properties] are specified by the endpoint reference, the corresponding headers must be added to the message too.</span></span>

- <span data-ttu-id="0229b-205">B3312: 요청자가 `MessageID`, `ReplyTo` 및 `FaultTo` 헤더를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-205">B3312: The requester may include `MessageID`, `ReplyTo`, and `FaultTo` headers.</span></span> <span data-ttu-id="0229b-206">이러한 헤더는 수신자 인프라에서 무시되고 응용 프로그램으로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-206">The receiver infrastructure will ignore them, and they will be passed to the application.</span></span>

- <span data-ttu-id="0229b-207">R3313: HTTP를 사용하고 HTTP 응답 레그에 전송 중인 메시지가 없을 때 응답자는 HTTP 202 상태 코드와 함께 본문이 빈 HTTP 응답을 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-207">R3313: When HTTP is used and no message is being sent on the HTTP response leg, the responder must send an HTTP response with an empty body and an HTTP 202 status code.</span></span>

     <span data-ttu-id="0229b-208">HTTP 전송을 사용 중이고 작업 계약에 메시지가 단방향으로 선언되어 있는 경우에도 인프라 메시지를 보내는 데 HTTP 응답을 사용할 수 있습니다. 예를 들어, 신뢰할 수 있는 메시징을 사용하여 HTTP 응답에서 `SequenceAcknowledgement` 메시지를 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-208">When the HTTP transport is in use and the operation contract declares a message one-way, the HTTP response can still be used for sending infrastructure messages—for example, reliable messaging can send a `SequenceAcknowledgement` message on an HTTP response.</span></span>

- <span data-ttu-id="0229b-209">B3314: WCF 응답자 오류 메시지를 단방향 메시지에 대 한 응답에서에 보내지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-209">B3314: The WCF responder does not send a fault message in response to a one-way message.</span></span>

#### <a name="request-reply"></a><span data-ttu-id="0229b-210">요청-회신</span><span class="sxs-lookup"><span data-stu-id="0229b-210">Request-Reply</span></span>
<span data-ttu-id="0229b-211">WCF 끝점을 사용 하 여 메시지에 대해 구성 된 경우는 지정 된 `Action` 요청-회신 패턴에 따라, WCF 끝점 동작 및 요구 사항 아래에 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-211">When a WCF endpoint is configured for a message with a given `Action` to follow the request-reply pattern, the WCF endpoint follows the behaviors and requirements below.</span></span> <span data-ttu-id="0229b-212">지정 하지 않는 한 동작과 규칙의 두 버전의 Ws-addressing WCF에서 지원에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-212">Unless specified otherwise, behaviors and rules apply for both versions of WS-Addressing supported in WCF:</span></span>

- <span data-ttu-id="0229b-213">R3321: 요청자는 요청에 포함 해야 `wsa:To`, `wsa:Action`, `wsa:MessageID`, 및 모든 참조 매개 변수 또는 참조 속성 (또는 둘 다) 끝점 참조에 의해 지정 된 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-213">R3321: The requester must include in the request `wsa:To`, `wsa:Action`, `wsa:MessageID`, and headers for all reference parameters or reference properties (or both) specified by the endpoint reference.</span></span>

- <span data-ttu-id="0229b-214">R3322: WS-Addressing 2004/08을 사용하는 경우 `ReplyTo`도 요청에 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-214">R3322: When WS-Addressing 2004/08 is used, `ReplyTo` must also be included in the request.</span></span>

- <span data-ttu-id="0229b-215">R3323: Ws-addressing 1.0을 사용 하는 경우 및 `ReplyTo` 요청에서는 같음 [address] 속성을 사용 하 여 기본 끝점 참조가 없는 `http://www.w3.org/2005/08/addressing/anonymous` 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-215">R3323: When WS-Addressing 1.0 is used and `ReplyTo` is not present in the request, a default endpoint reference with the [address] property equal to `http://www.w3.org/2005/08/addressing/anonymous` is used.</span></span>

- <span data-ttu-id="0229b-216">R3324: 요청자 있어야 `wsa:To`, `wsa:Action`, 및 `wsa:RelatesTo` 회신 메시지의 헤더 뿐만 아니라 모든 참조 매개 변수 또는 참조 속성 (또는 둘 다)로 지정 된 헤더를 `ReplyTo` 끝점 참조에는 요청입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-216">R3324: The requester must include `wsa:To`, `wsa:Action`, and `wsa:RelatesTo` headers in the reply message, as well as headers for all reference parameters or reference properties (or both) specified by the `ReplyTo` endpoint reference in the request.</span></span>

### <a name="web-services-addressing-faults"></a><span data-ttu-id="0229b-217">Web Services Addressing 오류</span><span class="sxs-lookup"><span data-stu-id="0229b-217">Web Services Addressing Faults</span></span>
<span data-ttu-id="0229b-218">R3411: WCF Ws-addressing 2004/08을 정의한 다음 오류를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-218">R3411: WCF produces the following faults defined by WS-Addressing 2004/08.</span></span>

|<span data-ttu-id="0229b-219">코드</span><span class="sxs-lookup"><span data-stu-id="0229b-219">Code</span></span>|<span data-ttu-id="0229b-220">원인</span><span class="sxs-lookup"><span data-stu-id="0229b-220">Cause</span></span>|
|----------|-----------|
|`wsa:DestinationUnreachable`|<span data-ttu-id="0229b-221">이 채널에 대해 설정된 회신 주소와 다른 `ReplyTo`를 사용하여 메시지가 도착했습니다. 받는 사람 헤더에 지정된 주소에서 수신 대기하는 엔드포인트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-221">The message arrived with a `ReplyTo` that is different from the reply address established for this channel; there is no endpoint listening at the address specified in the To header.</span></span>|
|`wsa:ActionNotSupported`|<span data-ttu-id="0229b-222">엔드포인트와 연결된 인프라 채널 또는 디스패처가 `Action` 헤더에 지정된 동작을 인식하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-222">the infrastructure channels or dispatcher associated with the endpoint do not recognize the action specified in the `Action` header.</span></span>|

<span data-ttu-id="0229b-223">R3412: WCF Ws-addressing 1.0을 정의한 다음 오류를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-223">R3412: WCF produces the following faults defined by WS-Addressing 1.0.</span></span>

|<span data-ttu-id="0229b-224">코드</span><span class="sxs-lookup"><span data-stu-id="0229b-224">Code</span></span>|<span data-ttu-id="0229b-225">원인</span><span class="sxs-lookup"><span data-stu-id="0229b-225">Cause</span></span>|
|----------|-----------|
|`wsa10:InvalidAddressingHeader`|<span data-ttu-id="0229b-226">중복 `wsa:To`, `wsa:ReplyTo`하십시오 `wsa:From` 또는 `wsa:MessageID`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-226">Duplicate `wsa:To`, `wsa:ReplyTo`, `wsa:From` or `wsa:MessageID`.</span></span> <span data-ttu-id="0229b-227">중복 `wsa:RelatesTo` 동일한 `RelationshipType`입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-227">Duplicate `wsa:RelatesTo` with the same `RelationshipType`.</span></span>|
|`wsa10:MessageAddressingHeaderRequired`|<span data-ttu-id="0229b-228">필수 주소 지정 헤더가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-228">The required Addressing header is missing.</span></span>|
|`wsa10:DestinationUnreachable`|<span data-ttu-id="0229b-229">이 채널에 대해 설정된 회신 주소와 다른 `ReplyTo`를 사용하여 메시지가 도착했습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-229">The message arrived with a `ReplyTo` that is different from the reply address established for this channel.</span></span> <span data-ttu-id="0229b-230">받는 사람 헤더에 지정된 주소에서 수신 대기하는 엔드포인트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-230">There is no endpoint listening at the address specified in the To header.</span></span>|
|`wsa10:ActionNotSupported`|<span data-ttu-id="0229b-231">`Action` 헤더에 지정된 동작이 엔드포인트와 연결된 디스패처 또는 인프라 채널에서 인식되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-231">An action specified in the `Action` header is not recognized by the infrastructure channels or dispatcher associated with the endpoint.</span></span>|
|`wsa10:EndpointUnavailable`|<span data-ttu-id="0229b-232">RM 채널에서 이 오류를 다시 보냅니다. 이는 엔드포인트에서 `CreateSequence` 메시지의 주소 지정 헤더를 검사하여 시퀀스를 처리하지 않는다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-232">The RM channel sends this fault back, indicating the endpoint will not process the sequence based upon examination of the `CreateSequence` message’s addressing headers.</span></span>|

<span data-ttu-id="0229b-233">위 표의 코드가 SOAP 1.1의 경우 `FaultCode`에 매핑되고 SOAP 1.2의 경우 `SubCode`(Code=Sender)에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-233">Code in the preceding tables maps to `FaultCode` in SOAP 1.1 and `SubCode` (with Code=Sender) in SOAP 1.2.</span></span>

### <a name="wsdl-11-binding-and-ws-policy-assertions"></a><span data-ttu-id="0229b-234">WSDL 1.1 바인딩 및 WS-Policy Assertion</span><span class="sxs-lookup"><span data-stu-id="0229b-234">WSDL 1.1 Binding and WS-Policy Assertions</span></span>

#### <a name="indicating-use-of-ws-addressing"></a><span data-ttu-id="0229b-235">WS-Addressing 사용 지정</span><span class="sxs-lookup"><span data-stu-id="0229b-235">Indicating Use of WS-Addressing</span></span>
<span data-ttu-id="0229b-236">WCF 정책 어설션을 사용 하 여 특정 Ws-addressing 버전에 대 한 끝점 지원을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-236">WCF uses policy assertions to indicate endpoint support for a particular WS-Addressing version.</span></span>

<span data-ttu-id="0229b-237">다음 정책 어설션은 엔드포인트 정책 주체가 [WS-PA]이고 엔드포인트에서 보내거나 받은 메시지가 WS-Addressing 2004/08을 사용해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-237">The following policy assertion has Endpoint Policy Subject [WS-PA] and indicates messages sent and received from the endpoint must use WS-Addressing 2004/08.</span></span>

```xml
<wsap:UsingAddressing />
```

<span data-ttu-id="0229b-238">이 정책 어설션은 WS-Addressing 2004/08 사양을 보완합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-238">This policy assertion augments the WS-Addressing 2004/08 specification.</span></span>

<span data-ttu-id="0229b-239">다음 정책 어설션은 보내거나 받은 메시지가 WS-Addressing 1.0을 사용해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-239">The following policy assertion this indicates that messages sent/received must use WS-Addressing 1.0.</span></span>

```xml
<wsam:Addressing/>
```

<span data-ttu-id="0229b-240">다음 정책 어설션은 엔드포인트 정책 주체가 [WS-PA]이고 엔드포인트에서 보내거나 받은 메시지가 WS-Addressing 2004/08을 사용해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-240">The following policy assertion has an Endpoint Policy Subject [WS-PA] and indicates that messages sent and received from the endpoint must use WS-Addressing 2004/08.</span></span>

```xml
<wsaw10:UsingAddressing />
```

<span data-ttu-id="0229b-241">`wsaw10:UsingAddressing` 요소는 [WS-Addressing-WSDL]에서 가져온 것이며 해당 사양 단원 3.1.2에 따라 WS-Policy 컨텍스트에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-241">The `wsaw10:UsingAddressing` element is borrowed from [WS-Addressing-WSDL] and is used in the context of WS-Policy in compliance with that specification, section 3.1.2.</span></span>

<span data-ttu-id="0229b-242">주소 지정을 사용해도 WSDL 1.1, SOAP 1.1 및 SOAP 1.2 HTTP 바인딩의 의미 체계가 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-242">Use of Addressing does not alter the semantics of WSDL 1.1, SOAP 1.1, and SOAP 1.2 HTTP Bindings.</span></span> <span data-ttu-id="0229b-243">예를 들어, 주소 지정 및 WSDL SOAP 1.x HTTP 바인딩을 사용하는 엔드포인트에 보낸 요청에 대한 회신이 필요한 경우 HTTP 응답을 사용하여 회신을 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-243">For example, if a reply is expected to a request that is sent to an endpoint that uses Addressing and WSDL SOAP 1.x HTTP binding, the reply must be sent by using the HTTP response.</span></span>

<span data-ttu-id="0229b-244">http 응답을 통해 전송되는 회신의 경우 WS-AM 어설션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-244">For replies sent over the http response, the WS-AM assertion is:</span></span>

```xml
<wsam:AnonymousResponses/>
```

<span data-ttu-id="0229b-245">완성된 정책 어설션은 다음과 같을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-245">The complete policy assertion might look like this:</span></span>

```xml
<wsam:Addressing>
    <wsp:Policy>
        <wsam:AnonymousResponses />
    </wsp:Policy>
</wsam:Addressing>
```

<span data-ttu-id="0229b-246">그러나 요청자와 응답자 간에 설정된 두 개의 독립적인 역방향 HTTP 연결을 활용하는 메시지 교환 패턴이 있습니다(예: 응답자가 보낸 원하지 않은 단방향 메시지).</span><span class="sxs-lookup"><span data-stu-id="0229b-246">However, there are message exchange patterns that benefit from having two independent converse HTTP connections established between the requester and the responder, for example, unsolicited one-way messages sent by the responder.</span></span>

<span data-ttu-id="0229b-247">WCF는 두 기본 전송 채널에는 여기서 하나의 채널은 입력된 메시지에 사용 하 고 출력 메시지에 사용 되는 다른 복합 이중 채널을 구성할 수 있습니다 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-247">WCF offers a feature by which two underlying transport channels can form a Composite Duplex channel, where one channel is used for input messages and the other is used for output messages.</span></span> <span data-ttu-id="0229b-248">HTTP 전송의 경우 복합 이중 채널은 두 개의 역방향 HTTP 연결을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-248">In the case of the HTTP Transport, Composite Duplex provides two converse HTTP connections.</span></span> <span data-ttu-id="0229b-249">요청자가 한 연결을 사용하여 메시지를 응답자에게 보내고, 응답자는 다른 연결을 사용하여 메시지를 요청자에게 다시 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-249">The requester uses one connection to send messages to the responder, and the responder uses the other to send messages back to the requester.</span></span>

<span data-ttu-id="0229b-250">별도의 http 요청을 통해 전송되는 회신의 경우 WS-AM 어설션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-250">For replies sent over separate http requests, the ws-am assertion is</span></span>

```xml
<wsam:NonAnonymousResponses/>
```

<span data-ttu-id="0229b-251">완성된 정책 어설션은 다음과 같을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-251">The complete policy assertion might look like this:</span></span>

```xml
<wsam:Addressing>
    <wsp:Policy>
        <wsam:NonAnonymousResponses />
    </wsp:Policy>
</wsam:Addressing>
```

<span data-ttu-id="0229b-252">WSDL 1.1 SOAP 1.x HTTP 바인딩을 사용하는 엔드포인트에서 엔드포인트 정책 주체가 [WS-PA]인 다음 어설션을 사용하려면 요청자와 응답자 간에 주고 받는 메시지 흐름에 각각 사용할 두 개의 개별적인 역방향 HTTP 연결이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-252">Use of the following assertion that has Endpoint Policy Subject [WS-PA] on endpoints that use WSDL 1.1 SOAP 1.x HTTP bindings requires two separate converse HTTP connections to be used for messages flowing from requester to responder and responder to requester, respectively.</span></span>

```xml
<cdp:CompositeDuplex/>
```

<span data-ttu-id="0229b-253">앞의 문에 따라 요청 메시지의 `wsa:ReplyTo` 헤더에 대해 다음 요구 사항이 충족되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-253">The previous statement leads to the following requirements on the `wsa:ReplyTo` header for request messages:</span></span>

- <span data-ttu-id="0229b-254">R3514: 끝점에 보낸 메시지 요청을 `ReplyTo` 헤더를 `[address]` 같지 않음 속성 `http://www.w3.org/2005/08/addressing/anonymous` 끝점이 WSDL 1.1 SOAP 1.x HTTP 바인딩을 사용 하 고 않은 정책 대안이 있는 경우는 `wsap10:UsingAddressing` 또는 `wsap:UsingAddressing` 어설션을 함께 `cdp:CompositeDuplex` 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-254">R3514: Request messages sent to an endpoint must have a `ReplyTo` header with the `[address]` property not equal to `http://www.w3.org/2005/08/addressing/anonymous` if the endpoint uses a WSDL 1.1 SOAP 1.x HTTP binding and has a policy alternative with a `wsap10:UsingAddressing` or `wsap:UsingAddressing` assertion coupled with `cdp:CompositeDuplex` attached.</span></span>

- <span data-ttu-id="0229b-255">R3515: 끝점에 보낸 메시지 요청을 `ReplyTo` 헤더를 `[address]` 속성이 `http://www.w3.org/2005/08/addressing/anonymous`, 수도 있고는 `ReplyTo` 끝점이 WSDL 1.1 SOAP 1.x HTTP 바인딩을 사용 하 고 않은 정책 대안이 있는 경우 모든 헤더 `wsap10:UsingAddressing` 어설션 및 no `cdp:CompositeDuplex` 어설션은 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-255">R3515: Request messages sent to an endpoint must have a `ReplyTo` header with the `[address]` property equal to `http://www.w3.org/2005/08/addressing/anonymous`, or not have a `ReplyTo` header at all, if the endpoint uses a WSDL 1.1 SOAP 1.x HTTP binding and has a policy alternative with `wsap10:UsingAddressing` assertion and no `cdp:CompositeDuplex` assertion attached.</span></span>

- <span data-ttu-id="0229b-256">R3516: 끝점에 보낸 메시지 요청을 `ReplyTo` 헤더를 `[address]` 속성이 `http://www.w3.org/2005/08/addressing/anonymous` 끝점이 WSDL 1.1 SOAP 1.x HTTP 바인딩을 사용 하 고 않은 정책 대안이 있는 경우 `wsap:UsingAddressing` 어설션 및 없음 `cdp:CompositeDuplex`어설션은 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-256">R3516: Request messages sent to an endpoint must have a `ReplyTo` header with an `[address]` property equal to `http://www.w3.org/2005/08/addressing/anonymous` if the endpoint uses a WSDL 1.1 SOAP 1.x HTTP binding and has a policy alternative with `wsap:UsingAddressing` assertion and no `cdp:CompositeDuplex` assertion attached.</span></span>

<span data-ttu-id="0229b-257">WS-addressing WSDL 사양에서는 세 개의 텍스트 값(required, optional, prohibited)을 가진 `<wsaw:Anonymous/>`wsa:ReplyTo 요소를 추가하여`wsa:ReplyTo` 헤더(단원 3.2)에 대한 요구 사항을 나타냄으로써 비슷한 프로토콜 바인딩을 설명하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-257">The WS-addressing WSDL specification attempts to describe similar protocol bindings by introducing an element `<wsaw:Anonymous/>` with three textual values (required, optional, and prohibited) to indicate requirements on the `wsa:ReplyTo` header (section 3.2).</span></span> <span data-ttu-id="0229b-258">그러나 해당 요소를 어설션으로 사용하여 대안 교차를 지원하려면 도메인별 확장이 필요하므로, 이러한 요소 정의는 WS-Policy 컨텍스트에서 어설션으로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-258">Unfortunately, such element definition is not particularly usable as an assertion in the context of WS-Policy, because it requires domain-specific extensions to support the intersection of alternatives using such an element as an assertion.</span></span> <span data-ttu-id="0229b-259">또한 이러한 요소 정의는 통신 중인 엔드포인트 동작과 반대로 `ReplyTo` 헤더 값을 나타내므로 HTTP 전송에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-259">Such element definition also indicates the value of the `ReplyTo` header as opposed to the endpoint behavior on the wire, which makes it specific to HTTP transport.</span></span>

#### <a name="action-definition"></a><span data-ttu-id="0229b-260">동작 정의</span><span class="sxs-lookup"><span data-stu-id="0229b-260">Action Definition</span></span>
<span data-ttu-id="0229b-261">WS-Addressing 2004/08에서는 `wsa:Action` 요소에 대한 `wsdl:portType/wsdl:operation/[wsdl:input | wsdl:output | wsdl:fault]` 특성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-261">WS-Addressing 2004/08 defines a `wsa:Action` attribute for the `wsdl:portType/wsdl:operation/[wsdl:input | wsdl:output | wsdl:fault]` elements.</span></span> <span data-ttu-id="0229b-262">WS-ADDR10-WSDL(WS-Addressing 1.0 WSDL 바인딩)에서는 비슷한 특성인 `wsaw10:Action`을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-262">WS-Addressing 1.0 WSDL Binding (WS-ADDR10-WSDL) defines a similar attribute, `wsaw10:Action`.</span></span>

<span data-ttu-id="0229b-263">둘 간에는 WS-ADDR의 단원 3.3.2와 WS-ADDR10-WSDL의 단원 4.4.4에 각각 설명된 기본 동작 패턴의 의미 체계만 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-263">The only difference between the two is the default Action pattern semantics described in section 3.3.2 of WS-ADDR and section 4.4.4 of WS-ADDR10-WSDL, respectively.</span></span>

<span data-ttu-id="0229b-264">동일한 공유는 두 개의 끝점에이 합리적입니다. `portType` (또는 계약 WCF 용어로) 하지만 서로 다른 버전의 Ws-addressing을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-264">It is a reasonable to have two endpoints that share the same `portType` (or contract, in WCF terminology) but using different versions of WS-Addressing.</span></span> <span data-ttu-id="0229b-265">그러나 동작이 `portType`에 정의되어 있고 `portType`을 구현하는 엔드포인트를 통해 변경되지 않아야 할 경우 두 기본 동작 패턴을 모두 지원할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-265">But given that Action is defined by the `portType` and should not change across the endpoints that implement the `portType`, it becomes impossible to support both default action patterns.</span></span>

<span data-ttu-id="0229b-266">이 문제를 해결 하려면 WCF의 단일 버전을 지원 합니다 `Action` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-266">To resolve this controversy, WCF supports a single version of the `Action` attribute.</span></span>

<span data-ttu-id="0229b-267">B3521: WCF를 사용 합니다 `wsaw10:Action` 특성을 `wsdl:portType/wsdl:operation/[wsdl:input | wsdl:output | wsdl:fault]` 결정할 WS-ADDR10-WSDL에 정의 된 대로 요소는 `Action` 끝점에서 사용 되는 Ws-addressing 버전에 관계 없이 해당 메시지에 대 한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-267">B3521: WCF uses the `wsaw10:Action` attribute on `wsdl:portType/wsdl:operation/[wsdl:input | wsdl:output | wsdl:fault]` elements as defined in WS-ADDR10-WSDL to determine the `Action` URI for the corresponding messages irrespective of the WS-Addressing version used by the endpoint.</span></span>

#### <a name="use-endpoint-reference-inside-wsdl-port"></a><span data-ttu-id="0229b-268">WSDL 포트에서 엔드포인트 참조 사용</span><span class="sxs-lookup"><span data-stu-id="0229b-268">Use Endpoint Reference Inside WSDL Port</span></span>
<span data-ttu-id="0229b-269">WS-ADDR10-WSDL 단원 4.1에서는 `wsdl:port` 자식 요소를 포함하도록 `<wsa10:EndpointReference…/>` 요소를 확장하여 WS-Addressing 용어로 엔드포인트를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-269">WS-ADDR10-WSDL section 4.1 extends the `wsdl:port` element to include the `<wsa10:EndpointReference…/>` child element to describe the endpoint in WS-Addressing terms.</span></span> <span data-ttu-id="0229b-270">Ws-addressing 2004/08에서이 유틸리티를 확장 하는 WCF 허용 `<wsa:EndpointReference…/>` 의 자식 요소로 표시할 `wsdl:port`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-270">WCF expands this utility on WS-Addressing 2004/08, allowing `<wsa:EndpointReference…/>` to appear as a child element of `wsdl:port`.</span></span>

- <span data-ttu-id="0229b-271">R3531: 끝점에 `<wsaw10:UsingAddressing/>` 정책 어설션과 연결된 정책 대안이 있는 경우 해당`wsdl:port` 요소는`<wsa10:EndpointReference …/>` 자식 요소를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-271">R3531: If an endpoint has an attached policy alternative with a `<wsaw10:UsingAddressing/>` policy assertion, the corresponding `wsdl:port` element can contain a child element `<wsa10:EndpointReference …/>`.</span></span>

- <span data-ttu-id="0229b-272">R3532: 경우는 `wsdl:port` 요소에 자식 요소가 `<wsa10:EndpointReference …/>`의 `wsa10:EndpointReference/wsa10:Address` 자식 요소 값의 값과 일치 해야 합니다는 `@address` 형제의 특성 `wsdl:port` / `wsdl:location` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-272">R3532: If a `wsdl:port` contains a child element `<wsa10:EndpointReference …/>`, the `wsa10:EndpointReference/wsa10:Address` child element value must match the value of the `@address` attribute of the sibling `wsdl:port`/`wsdl:location` element.</span></span>

- <span data-ttu-id="0229b-273">R3533: 엔드포인트에 `<wsap:UsingAddressing/>``wsdl:port` 정책 어설션과 연결된 정책 대안이 있는 경우 해당 `<wsa:EndpointReference …/>` 요소는 자식 요소를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-273">R3533: If an endpoint has an attached policy alternative with `<wsap:UsingAddressing/>` policy assertion, the corresponding `wsdl:port` element can contain a child element `<wsa:EndpointReference …/>`.</span></span>

- <span data-ttu-id="0229b-274">R3534: 경우는 `wsdl:port` 요소에 자식 요소가 `<wsa:EndpointReference …/>`의 `wsa:EndpointReference/wsa:Address` 자식 요소 값의 값과 일치 해야 합니다는 `@address` 형제의 특성 `wsdl:port` / `wsdl:location` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-274">R3534: If a `wsdl:port` contains a child element `<wsa:EndpointReference …/>`, the `wsa:EndpointReference/wsa:Address` child element value must match the value of the `@address` attribute of the sibling `wsdl:port`/`wsdl:location` element.</span></span>

### <a name="composition-with-ws-security"></a><span data-ttu-id="0229b-275">WS-Security를 사용하여 구성</span><span class="sxs-lookup"><span data-stu-id="0229b-275">Composition with WS-Security</span></span>
<span data-ttu-id="0229b-276">WS-ADDR 및 WS-ADDR10의 보안 고려 사항 단원에 따르면 모든 주소 지정 메시지 헤더를 메시지 본문과 함께 서명하여 바인딩하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-276">According to security consideration sections in WS-ADDR and WS-ADDR10, all addressing message headers are recommended to be signed together with the message body to bind them together.</span></span>

<span data-ttu-id="0229b-277">WS-Security가 메시지 무결성 보호를 위해 사용될 경우 WS-Addressing 메시지 헤더뿐 아니라 참조 매개 변수 또는 속성(또는 둘 모두)에서 생성된 헤더를 메시지 본문과 함께 서명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-277">When WS-Security is used for message integrity protection, WS-Addressing message headers as well as headers resulted from reference parameters or properties (or both) must be signed together with the body of the message.</span></span>

### <a name="examples"></a><span data-ttu-id="0229b-278">예제</span><span class="sxs-lookup"><span data-stu-id="0229b-278">Examples</span></span>

#### <a name="one-way-message"></a><span data-ttu-id="0229b-279">단방향 메시지</span><span class="sxs-lookup"><span data-stu-id="0229b-279">One-Way Message</span></span>
<span data-ttu-id="0229b-280">이 시나리오에서 발신자는 수신자에게 단방향 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-280">In this scenario, the sender sends a one-way message to the receiver.</span></span> <span data-ttu-id="0229b-281">SOAP 1.2, HTTP 1.1 및 W3C WS-Addressing 1.0이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-281">SOAP 1.2, HTTP 1.1, and W3C WS-Addressing 1.0 are used.</span></span>

<span data-ttu-id="0229b-282">요청 메시지 구조: 메시지 헤더는 `wsa10:To` 및 `wsa10:Action` 요소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-282">The Request Message Structure: The message headers include `wsa10:To` and `wsa10:Action` elements.</span></span> <span data-ttu-id="0229b-283">메시지 본문은 응용 프로그램 네임스페이스의 특정 `<app:Ping>` 요소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-283">The message body includes a specific `<app:Ping>` element from the application namespace.</span></span>

<span data-ttu-id="0229b-284">HTTP 헤더: POST의 대상이의 URI와 일치 하는 `wsa10:To` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-284">HTTP Headers: The destination in POST matches the URI in the `wsa10:To` element.</span></span>

<span data-ttu-id="0229b-285">Content-Type 헤더에는 SOAP 1.2에 필요한 `application/soap+xml` 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-285">The Content-Type header has the value of `application/soap+xml` as required by SOAP 1.2.</span></span> <span data-ttu-id="0229b-286">`charset` 및 `action` 매개 변수가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-286">Parameters `charset` and `action` are included.</span></span> <span data-ttu-id="0229b-287">Content-Type 헤더의 `action` 매개 변수가 `wsa10:Action` 메시지 헤더의 값과 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-287">The `action` parameter of the Content-Type header matches the value of the `wsa10:Action` message header.</span></span>

```
POST http://fabrikam123.com/Service HTTP/1.1
Content-Type: application/soap+xml; charset=utf-8;  
              action="http://fabrikam123.com/Service/OneWay"
Host: 131.107.72.15
Content-Length: 1501
Expect: 100-continue
Proxy-Connection: Keep-Alive
<s12:Envelope>
  <s12:Header>
    <wsa10:To s12:mustUnderstand="1">
        http://fabrikam123.com/Service
    </wsa10:To>
    <wsa10:Action s12:mustUnderstand="1">
        http://fabrikam123.com/Service/OneWay 
    </wsa10:Action>
  </s12:Header>
  <s12:Body>
    <Ping xmlns="http://fabrikam123.com/Service/">
      <Text>Hello World</Text>
    </Ping>
  </s12:Body>
</s12:Envelope>
```

<span data-ttu-id="0229b-288">수신자는 빈 HTTP 응답 및 상태 202를 사용하여 응답합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-288">The receiver responds with an empty HTTP response and status 202.</span></span> <span data-ttu-id="0229b-289">HTTP 응답의 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-289">An example of the HTTP response:</span></span>

```
HTTP/1.1 202 Accepted
Date: Fri, 15 Jul 2005 08:56:07 GMT
Server: Microsoft-IIS/6.0
MicrosoftOfficeWebServer: 5.0_Pub
X-Powered-By: ASP.NET
X-AspNet-Version: 2.0.50215
Cache-Control: private
Content-Length: 0
```

## <a name="soap-message-transmission-optimization-mechanism"></a><span data-ttu-id="0229b-290">SOAP MTOM(Message Transmission Optimization Mechanism)</span><span class="sxs-lookup"><span data-stu-id="0229b-290">SOAP Message Transmission Optimization Mechanism</span></span>
<span data-ttu-id="0229b-291">이 섹션에서는 HTTP SOAP MTOM에 대 한 WCF 구현 세부 정보를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-291">This section describes the WCF implementation details for the HTTP SOAP MTOM.</span></span> <span data-ttu-id="0229b-292">MTOM 기술은 기존 텍스트/x m L 인코딩 또는 WCF 이진 인코딩과 동일한 클래스의 SOAP 메시지 인코딩 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-292">MTOM technology is SOAP message encoding mechanism of the same class as traditional text/XML encoding or WCF Binary encoding.</span></span> <span data-ttu-id="0229b-293">MTOM에는 다음과 같은 내용이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-293">MTOM includes the following:</span></span>

- <span data-ttu-id="0229b-294">base64 인코딩된 이진 데이터를 개별 이진 부분으로 포함하는 XML 정보 항목을 최적화하는 [XOP]에 설명된 XML 인코딩 및 패키징 메커니즘</span><span class="sxs-lookup"><span data-stu-id="0229b-294">An XML encoding and packaging mechanism described by [XOP] that optimizes XML information items containing base64-encoded binary data into separate binary parts.</span></span>

- <span data-ttu-id="0229b-295">XOP 패키지의 각 이진 부분 및 XML Infoset을 개별 MIME 부분으로 serialize하는 XOP 패키지의 MIME 캡슐화</span><span class="sxs-lookup"><span data-stu-id="0229b-295">A MIME encapsulation of the XOP package that serializes the XML Infoset and each binary part of the XOP package into a separate MIME part.</span></span>

- <span data-ttu-id="0229b-296">SOAP 1.x 봉투에 적용되는 MIME XOP 인코딩</span><span class="sxs-lookup"><span data-stu-id="0229b-296">A MIME XOP encoding applied to SOAP 1.x Envelope.</span></span>

- <span data-ttu-id="0229b-297">HTTP 전송 바인딩</span><span class="sxs-lookup"><span data-stu-id="0229b-297">An HTTP transport binding.</span></span>

<span data-ttu-id="0229b-298">MTOM을 사용 하 여 WCF 사용 하 여 HTTP가 아닌 전송을 사용 하는 것이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-298">It is possible to use MTOM with non-HTTP transports with WCF.</span></span> <span data-ttu-id="0229b-299">그러나 이 항목에서는 HTTP에 중점을 두어 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-299">However, in this topic we will focus on HTTP.</span></span>

<span data-ttu-id="0229b-300">MTOM 형식에서는 MTOM 자체와 XOP 및 MIME을 포함한 다양한 사양을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-300">The MTOM format leverages a large set of specifications covering MTOM itself, XOP, and MIME.</span></span> <span data-ttu-id="0229b-301">이 사양의 모듈성으로 인해 형식 및 처리 의미 체계에 대한 정확한 요구 사항을 재구성하기가 다소 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-301">Modularity of this specification set makes it somewhat difficult to reconstruct exact requirements on the format and processing semantics.</span></span> <span data-ttu-id="0229b-302">이 단원에서는 MTOM HTTP 바인딩의 형식 및 처리 요구 사항에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-302">This section describes the format and processing requirements for MTOM HTTP binding.</span></span>

### <a name="mtom-message-encoding"></a><span data-ttu-id="0229b-303">MTOM 메시지 인코딩</span><span class="sxs-lookup"><span data-stu-id="0229b-303">MTOM Message Encoding</span></span>

#### <a name="generating-mtom-messages"></a><span data-ttu-id="0229b-304">MTOM 메시지 생성</span><span class="sxs-lookup"><span data-stu-id="0229b-304">Generating MTOM messages</span></span>
<span data-ttu-id="0229b-305">[XOP] 단원 3.1에서는 base64 값을 추상적으로 정의된 XOP 패키지에 포함하는 요소 정보 항목을 사용하여 XML을 인코딩하는 프로세스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-305">The [XOP] section 3.1 describes the process of encoding XML with element information items that contain base64 values into an abstractly defined XOP package.</span></span>

<span data-ttu-id="0229b-306">다음 단계에서는 MTOM 관련 인코딩 프로세스에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-306">The following sequence of steps describes the MTOM-specific encoding process:</span></span>

1. <span data-ttu-id="0229b-307">인코딩할 SOAP 봉투를 사용 하 여 요소 정보 항목이 포함 되어 있는지 확인 한 `[namespace name]` 의 `http://www.w3.org/2004/08/xop/include` 와 `[local name]` 의 `Include`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-307">Ensure that the SOAP Envelope to be encoded contains no element information item with a `[namespace name]` of `http://www.w3.org/2004/08/xop/include` and a `[local name]` of `Include`.</span></span>

2. <span data-ttu-id="0229b-308">빈 MIME 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-308">Create an empty MIME package.</span></span>

3. <span data-ttu-id="0229b-309">원본 XML Infoset에서 최적화할 요소 정보 항목을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-309">Identify within the Original XML Infoset the element information items to be optimized.</span></span> <span data-ttu-id="0229b-310">최적화 되도록 항목에 대 한 문자를 구성 하는 합니다 `[children]` 요소 정보 항목의 정규 형식이에 있어야 `xs:base64Binary` (xsd-2, 3.2.16 base64Binary) 앞에, 인라인 공백 문자를 사용할 수 없습니다 및 또는 공백이 아닌 콘텐츠를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-310">For the items to be optimized, the characters that make up the `[children]` of the element information item must be in the canonical form of `xs:base64Binary` (see XSD-2, 3.2.16 base64Binary) and must not contain any white-space characters preceding, inline with, or following the non-white-space content.</span></span>

4. <span data-ttu-id="0229b-311">원본 SOAP 봉투의 복사본인 XOP SOAP 봉투를 만듭니다. 단, 이전 단계에서 식별된 각 요소 정보 항목의 자식을 다음과 같이 구성된 `xop:Include` 요소 정보 항목으로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-311">Create an XOP SOAP Envelope that is a copy of the Original SOAP Envelope, but with the children of each element information item identified in the previous step replaced by an `xop:Include` element information item constructed as follows:</span></span>

    1. <span data-ttu-id="0229b-312">대체된 문자를 base64 인코딩된 데이터로 처리하여 이진 데이터로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-312">Transform the replaced characters into binary data by processing them as base64-encoded data.</span></span>

    2. <span data-ttu-id="0229b-313">R3133 및 R3134 요구 사항을 충족하는 고유한 Content-ID 헤더 값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-313">Generate a unique Content-ID header value that satisfies requirements R3133 and R3134.</span></span>

    3. <span data-ttu-id="0229b-314">이진 값을 사용하여 Content-Transfer-Encoding MIME 헤더를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-314">Generate a Content-Transfer-Encoding MIME header with the value binary.</span></span>

    4. <span data-ttu-id="0229b-315">최적화할 요소 정보 항목(새로 삽입된 `xop:Include` 요소 정보 항목의 [parent])에 `xmime:contentType` 특성 정보 항목이 있는 경우 `xmime:contentType` 특성 값을 사용하여 Content-Type MIME 헤더를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-315">If the element information item being optimized (the [parent] of the newly inserted `xop:Include` element information item) has an `xmime:contentType` attribute information item, generate a Content-Type MIME header with the value of the `xmime:contentType` attribute.</span></span>

    5. <span data-ttu-id="0229b-316">base64, 4b의 Content-ID 헤더, 4c의 Content- Transfer-Encoding 헤더, Content-Type 헤더(4d 단계에서 생성된 경우)로 처리된 대체 문자에서 디코딩된 이진 데이터로 형성된 콘텐츠를 사용하여 새 이진 MIME 부분을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-316">Generate a new binary MIME part with content formed by binary data decoded from the replaced characters processed as base64, Content-ID header from 4b, Content- Transfer-Encoding header from 4c, Content-Type header if generated in step 4d.</span></span>

    6. <span data-ttu-id="0229b-317">4b 단계에서 생성된 Content-ID 헤더 값에서 파생된 cid: uri 값을 사용하여 `href` 특성을 `xop:Include` 요소에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-317">Add an `href` attribute to the `xop:Include` element with the value cid: uri derived from Content-ID header value generated in step 4b.</span></span> <span data-ttu-id="0229b-318">바깥쪽 제거 "\<" 및 ">" 문자를 URL-이스케이프 문자열 및 접두사를 추가 합니다. 나머지 `cid:`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-318">Remove the enclosing "\<" and ">" characters, URL-escape the remaining string, and add the prefix `cid:`.</span></span> <span data-ttu-id="0229b-319">RFC1738 및 RFC2396으로 이스케이프하려면 다음과 같은 최소 문자 집합이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-319">The following minimum character set is required to be escaped by RFC1738 and RFC2396.</span></span> <span data-ttu-id="0229b-320">다른 문자를 이스케이프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-320">Other characters can be escaped.</span></span>

        ```
        Hexadecimal 00-1F , 7F, 20, "<" | ">" | "#" | "%" | <">
        "{" | "}" | "|" | "\" | "^" | "[" | "]" | "`" | "~" | "^"
        ```

5. <span data-ttu-id="0229b-321">4단계의 XOP SOAP 봉투를 사용하여 루트 MIME 부분을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-321">Create a root MIME part with the XOP SOAP Envelope from step 4.</span></span>

6. <span data-ttu-id="0229b-322">HTTP Content-Type 헤더를 포함하여 HTTP 헤더를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-322">Write the HTTP headers, including the HTTP Content-Type header.</span></span>

7. <span data-ttu-id="0229b-323">MIME 패키지를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-323">Write the MIME package.</span></span>

#### <a name="processing-mtom-messages"></a><span data-ttu-id="0229b-324">MTOM 메시지 처리</span><span class="sxs-lookup"><span data-stu-id="0229b-324">Processing MTOM messages</span></span>
<span data-ttu-id="0229b-325">MTOM 메시지 처리 과정은 이전 "MTOM 메시지 생성" 단원에서 설명한 프로세스와 정확히 반대입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-325">Processing of an MTOM message is the exact reverse of the process described in the preceding "Generating MTOM messages" section:</span></span>

1. <span data-ttu-id="0229b-326">루트 MIME 부분에 Content-Type `application/xop+xml`이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-326">Ensure the root MIME part has the Content-Type `application/xop+xml`.</span></span>

2. <span data-ttu-id="0229b-327">패키지의 루트 MIME 부분을 구문 분석하여 SOAP 봉투를 XML 문서로 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-327">Construct a SOAP Envelope by parsing the root MIME part of the package as an XML document.</span></span> <span data-ttu-id="0229b-328">문자 인코딩은 루트 MIME 부분 Content-Type의 `charset` 매개 변수에 의해 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-328">Character encoding is determined by the `charset` parameter of the Content-Type of the root MIME part.</span></span>

3. <span data-ttu-id="0229b-329">`xop:Include` 요소 정보 항목을 [children] 속성의 단독 멤버로 가진 구성된 SOAP 봉투의 각 요소 정보 항목의 경우 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-329">For each element information item in the constructed SOAP Envelope, which has, as the sole member of its [children] property, an `xop:Include` element information item:</span></span>

    1. <span data-ttu-id="0229b-330">`cid:` 접두사를 제거하고 `@href` 요소의 `xop:Include` 특성 값에서 모든 URI 이스케이프 시퀀스(RFC 2396)를 이스케이프 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-330">Remove the `cid:` prefix and unescape all URI-escape sequences (RFC 2396) in the value of the `@href` attribute of the `xop:Include` element.</span></span> <span data-ttu-id="0229b-331">결과 문자열을 묶습니다 "\<", ">"입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-331">Enclose the result string in "\<", ">".</span></span>

    2. <span data-ttu-id="0229b-332">3a 단계에서 파생된 문자열과 일치하는 Content-ID 헤더 값을 가진 MIME 부분을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-332">Locate the MIME part with the Content-ID header value that matches the string derived in step 3a.</span></span>

    3. <span data-ttu-id="0229b-333">각 항목의 `xop:Include` 속성에 나타나는 `children` 요소 정보 항목을 3b 단계에서 식별된 MIME 부분의 엔터티 본문의 정규 base64 인코딩(XSD-2, 3.2.16 base64Binary 참조)을 나타내는 문자 정보 항목으로 대체합니다. 즉, `xop:Include` 요소 정보 항목을 패키지 부분에서 재구성된 데이터로 효과적으로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-333">Replace the `xop:Include` element information item that appears in the `children` property of each item with the character information items that represent the canonical base64 encoding (see XSD-2, 3.2.16 base64Binary) of the entity body of the MIME part identified in step 3b (effectively replace the `xop:Include` element information item with the data reconstructed from the package part).</span></span>

#### <a name="http-content-type-header"></a><span data-ttu-id="0229b-334">HTTP Content-Type 헤더</span><span class="sxs-lookup"><span data-stu-id="0229b-334">HTTP Content-Type Header</span></span>
<span data-ttu-id="0229b-335">다음은 SOAP 1.x MTOM 인코딩된 메시지 MTOM 사양 자체에 명시 된 요구 사항에서 파생 된의 HTTP Content-type 헤더의 형식에 대 한 WCF 설명의 목록 및 MTOM 및 RFC 2387에서 파생 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-335">The following is a list of WCF clarifications for the format of the HTTP Content-Type header of a SOAP 1.x MTOM-encoded message derived from requirements stated in the MTOM specification itself and are derived from MTOM and RFC 2387.</span></span>

- <span data-ttu-id="0229b-336">R4131: HTTP Content-Type 헤더에는 multipart/related(대/소문자 구분 안 함) 값 및 해당 매개 변수가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-336">R4131: An HTTP Content-Type header must have the value of multipart/related (case-insensitive) and its parameters.</span></span> <span data-ttu-id="0229b-337">매개 변수 이름은 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-337">Parameter names are case-insensitive.</span></span> <span data-ttu-id="0229b-338">매개 변수의 순서는 중요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-338">Parameter order is not significant.</span></span>

- <span data-ttu-id="0229b-339">MIME 메시지에 대한 Content-Type 헤더의 전체 BNF(Backus-Naur Form)는 RFC 2045, 단원 5.1에 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-339">The full Backus-Naur Form (BNF) of the Content-Type header for MIME messages is listed in RFC 2045, section 5.1.</span></span>

- <span data-ttu-id="0229b-340">R4132: HTTP Content-Type 헤더에는 큰따옴표로 묶은 `application/xop+xml` 값을 가진 형식 매개 변수가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-340">R4132: An HTTP Content-Type header must have a type parameter with the value `application/xop+xml` enclosed in double quotation marks.</span></span>

<span data-ttu-id="0229b-341">텍스트 같은 예약 된 문자를 대부분 포함 모든 multipart/related 미디어 형식 매개 변수에서 큰따옴표를 사용 하는 요구 사항을 RFC 2387에에서 명시적 상태일 "\@" 또는 "/" 큰따옴표 필요 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-341">While the requirement to use double quotation marks is not explicit in RFC 2387, the text observes that all of the multipart/related media type parameters most likely contain reserved characters like "\@" or "/" and therefore need double quotation marks.</span></span>

- <span data-ttu-id="0229b-342">R4133: HTTP Content-Type 헤더에는 SOAP 1.x 봉투를 포함하는 MIMI 부분의 Content-ID 헤더 값이 큰따옴표로 묶인 시작 매개 변수가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-342">R4133: An HTTP Content-Type header should have a start parameter with the value of the Content-ID header of the MIME part that contains the SOAP 1.x Envelope, enclosed in double quotation marks.</span></span> <span data-ttu-id="0229b-343">시작 매개 변수가 생략된 경우 첫 번째 MIME 부분에 SOAP 1.x 봉투가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-343">If the start parameter is omitted, the first MIME part must contain the SOAP 1.x Envelope.</span></span>

- <span data-ttu-id="0229b-344">R4134: SOAP 1.1 MTOM 인코딩된 메시지의 HTTP Content-Type 헤더는 큰따옴표로 묶인 text/xml 값을 가진 start-info 매개 변수를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-344">R4134: An HTTP Content-Type header for a SOAP 1.1 MTOM encoded message must include the start-info parameter with the value of text/xml, enclosed in double quotation marks.</span></span>

- <span data-ttu-id="0229b-345">R4135: SOAP 1.2 MTOM 인코딩된 메시지의 HTTP Content-Type 헤더는 큰따옴표로 묶인 `application/soap+xml` 값을 가진 start-info 매개 변수를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-345">R4135: An HTTP Content-Type header for a SOAP 1.2 MTOM-encoded message must include the start-info parameter with the value of `application/soap+xml`, enclosed in double quotation marks.</span></span>

- <span data-ttu-id="0229b-346">R4136: SOAP 1.x MTOM 인코딩된 메시지의 HTTP Content-Type 헤더에는 RFC 2046, 단원 5.1.1에 정의된 MIME 경계 BNF와 일치하는 큰따옴표로 묶인 값을 가진 boundary 매개 변수가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-346">R4136: HTTP Content-Type header for a SOAP 1.x MTOM-encoded message must have the boundary parameter with the value (enclosed in double quotation marks) that matches the MIME boundary BNF defined in RFC 2046, section 5.1.1</span></span>

    ```
    boundary := 0*69<bchars> bcharsnospace 
    bchars := bcharsnospace / " " 
    bcharsnospace :=    DIGIT / ALPHA / "'" / "(" / ")" / "+" 
                        / "_" / "," / "-" / "." / "/" / ":" / "=" / "?"
    ```

     <span data-ttu-id="0229b-347">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-347">Examples:</span></span>

     <span data-ttu-id="0229b-348">올바른 예</span><span class="sxs-lookup"><span data-stu-id="0229b-348">CORRECT</span></span>

    ```
    Content-Type: multipart/related; type="application/xop+xml";start=" <part0@tempuri.org>";boundary="uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1";start-info="text/xml"
    ```

     <span data-ttu-id="0229b-349">올바른 예</span><span class="sxs-lookup"><span data-stu-id="0229b-349">CORRECT</span></span>

    ```
    Content-Type: Multipart/Related; type="application/xop+xml";start-info="text/xml";boundary="uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1"
    ```

     <span data-ttu-id="0229b-350">잘못된 예</span><span class="sxs-lookup"><span data-stu-id="0229b-350">INCORRECT</span></span>

    ```
    Content-Type: Multipart/Related; type=application/xop+xml;start=" <part0@tempuri.org>";start-info="text/xml";boundary="uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1" 
    ```

#### <a name="infoset-mime-part"></a><span data-ttu-id="0229b-351">Infoset MIME 부분</span><span class="sxs-lookup"><span data-stu-id="0229b-351">Infoset MIME Part</span></span>
<span data-ttu-id="0229b-352">SOAP 1.x 봉투는 XOP MIME 패키지의 루트 부분으로 캡슐화되며 `infoset` 부분이라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-352">The SOAP 1.x Envelope is encapsulated as a root part of the XOP MIME package and is often called the `infoset` part.</span></span>

- <span data-ttu-id="0229b-353">R4141: SOAP 1.x 봉투는 XOP MIME 패키지의 루트 부분으로 캡슐화되어야 하고, `infoset` 부분이라고도 하며, HTTP Content-Type에서 참조되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-353">R4141: The SOAP 1.x Envelope must be encapsulated as a root part of the XOP MIME package, called the `infoset` part and referenced from the HTTP Content-Type.</span></span>

- <span data-ttu-id="0229b-354">R4142: SOAP `Infoset` 부분은 `Content-ID`, `Content-Transfer-Encoding` 및 `Content-Type` MIME 헤더를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-354">R4142: The SOAP `Infoset` part must include the following MIME headers: `Content-ID`, `Content-Transfer-Encoding`, and `Content-Type`.</span></span>

<span data-ttu-id="0229b-355">Content-ID 헤더의 형식은 RFC 2045에 다음과 같이 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-355">The format of the Content-ID header is defined by RFC 2045 as</span></span>

```
"Content-ID" ":" msg-id
```

<span data-ttu-id="0229b-356">`msg-id`는 RFC 2822(RFC 822보다 우선하며, RFC 2045에서 참조됨)에 다음과 같이 정의되어 있으며</span><span class="sxs-lookup"><span data-stu-id="0229b-356">where `msg-id` is defined in RFC 2822 (that supersedes RFC 822, referenced in RFC 2045) as:</span></span>

```
msg-id    =       [CFWS] "<" id-left "@" id-right ">" [CFWS]
```

<span data-ttu-id="0229b-357">효과적으로 전자 메일 주소 내에 포함 하 고 "\<" 및 ">"입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-357">and is effectively an email address enclosed within "\<" and  ">".</span></span> <span data-ttu-id="0229b-358">`[CFWS]` 접두사와 접미사는 설명을 전달하기 위해 RFC 2822에 추가되었지만 상호 운용성을 유지하려면 사용하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-358">The `[CFWS]` prefix and suffix were added in RFC 2822 to carry comments and should not be used to preserve interoperability.</span></span>

<span data-ttu-id="0229b-359">R4143: Infoset MIME 부분의 Content-ID 헤더 값은 `msg-id` 접두사 및 접미사 부분을 생략한 상태의 RFC 2822의 `[CFWS]` 생성을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-359">R4143: The value of the Content-ID header for the Infoset MIME part must follow `msg-id` production from RFC 2822 with the `[CFWS]` prefix and suffix parts omitted.</span></span>

<span data-ttu-id="0229b-360">많은 MIME 구현 내에 포함 된 값에 대 한 요구 사항 완화 "\<" 및 ">" 전자 메일 주소를 사용 `absoluteURI` 묶인 "\<", ">" 전자 메일 주소 외에도 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-360">A number of MIME implementations relaxed requirements for the value enclosed within "\<" and ">" to be an email address and used `absoluteURI` enclosed in "\<" , ">" in addition to the email address.</span></span> <span data-ttu-id="0229b-361">이 WCF 버전은 형식의 CONTENT-ID MIME 헤더의 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-361">This version of WCF uses values of the Content-ID MIME header of the form:</span></span>

```
Content-ID: <http://tempuri.org/0> 
```

<span data-ttu-id="0229b-362">R4144: MTOM 프로세서는 다음과 같은 완화된 `msg-id`와 일치하는 Content-ID 헤더 값을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-362">R4144: MTOM processors should accept Content-ID header values that match the following relaxed `msg-id`.</span></span>

```
msg-id-relaxed =     [CFWS] "<" (absoluteURI | mail-address) ">" [CFWS]
mail-address   =     id-left "@" id-right
```

<span data-ttu-id="0229b-363">MIME(RFC 2045)은 MIME 부분의 콘텐츠 인코딩을 전달하기 위해 Content-Transfer-Encoding 헤더를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-363">MIME (RFC 2045) provides the Content-Transfer-Encoding header to communicate encoding of the content of the MIME part.</span></span> <span data-ttu-id="0229b-364">Content-Transfer-Encoding에 대해 정의된 기본값은 7비트로 대부분의 SOAP 메시지에 적합하지 않으므로 상호 운용성 향상을 위해 Content-Transfer-Encoding 헤더가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-364">The default defined for Content-Transfer-Encoding is 7-bit, which is not suitable for most SOAP messages, so the Content-Transfer-Encoding header is needed for greater interoperability:</span></span>

- <span data-ttu-id="0229b-365">R4145: SOAP Infoset 부분은 Content-Transfer-Encoding 헤더를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-365">R4145: The SOAP Infoset part must contain the Content-Transfer-Encoding header.</span></span>

- <span data-ttu-id="0229b-366">R4146: SOAP 봉투 문자 인코딩이 UTF-8이면 Content-Transfer-Encoding 헤더 값이 8비트여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-366">R4146: If the SOAP Envelope character encoding is UTF-8, the value of the Content-Transfer-Encoding header must be 8-bit.</span></span>

- <span data-ttu-id="0229b-367">R4147: SOAP 봉투 문자 인코딩이 UTF-16이면 Content-Transfer-Encoding 헤더 값이 이진이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-367">R4147: If the SOAP Envelope character encoding is UTF-16, the value of the Content-Transfer-Encoding header must be binary.</span></span>

- <span data-ttu-id="0229b-368">[XOP] 단원 5에 따르면</span><span class="sxs-lookup"><span data-stu-id="0229b-368">According to [XOP] section 5,</span></span>

- <span data-ttu-id="0229b-369">R4148: SOAP1.1 Infoset 부분은 미디어 형식이 application/xop + xml을 사용 하 여 Content-type 헤더를 포함 해야 하 고 매개 변수가 type = "text/xml" 및 charset</span><span class="sxs-lookup"><span data-stu-id="0229b-369">R4148: SOAP1.1 Infoset part must contain Content-Type header with media type application/xop+xml and parameters type="text/xml" and charset</span></span>

    ```
    Content-Type: application/xop+xml;
                  charset=utf-8;type="text/xml"
    ```

- <span data-ttu-id="0229b-370">R4149: SOAP 1.2 Infoset 부분은 미디어 형식 사용 하 여 콘텐츠 형식 헤더를 포함 해야 합니다 `application/xop+xml` 고 매개 변수가 type = "`application/soap+xml`" 및 `charset`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-370">R4149: The SOAP 1.2 Infoset part must contain the Content-Type header with media type `application/xop+xml` and parameters type="`application/soap+xml`" and `charset`.</span></span>

    ```
    Content-Type: application/xop+xml;
                  charset=utf-8;type="application/soap+xml"
    ```

     <span data-ttu-id="0229b-371">XOP에서는 `charset`의 `application/xop+xml` 매개 변수를 선택적 요소로 정의하고 있지만, `charset` 미디어 형식의 `text/xml` 매개 변수에 대한 BP 1.1 요구 사항과 마찬가지로 상호 운용성을 위해 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-371">While XOP defines the `charset` parameter for `application/xop+xml` to be optional, it is needed for interoperability similar to the BP 1.1 requirement on the `charset` parameter for the `text/xml` media type.</span></span>

- <span data-ttu-id="0229b-372">R41410: `type` 및 `charset` 매개 변수가 SOAP 1.x Infoset 부분의 Content-Type 헤더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-372">R41410: The `type` and `charset` parameters must be present on the Content-Type header of the SOAP 1.x Infoset part.</span></span>

#### <a name="wcf-endpoint-support-for-mtom"></a><span data-ttu-id="0229b-373">MTOM에 대한 WCF 엔드포인트 지원</span><span class="sxs-lookup"><span data-stu-id="0229b-373">WCF Endpoint Support for MTOM</span></span>
<span data-ttu-id="0229b-374">MTOM의 목적은 SOAP 메시지를 인코딩하여 base64 인코딩된 데이터를 최적화하는 데 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-374">The purpose of MTOM is to encode a SOAP message to optimize base64-encoded data.</span></span> <span data-ttu-id="0229b-375">다음은 제약 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-375">The following is a list of constraints:</span></span>

- <span data-ttu-id="0229b-376">R4151: base64 인코딩된 데이터를 포함하는 모든 요소 정보 항목이 최적화될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-376">R4151: Any element information item that contains base64-encoded data may be optimized.</span></span>

- <span data-ttu-id="0229b-377">B4152: WCF는 base64로 인코딩된 데이터를 포함 하 고 길이가 1024 바이트를 초과 하는 요소 정보 항목을 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-377">B4152: WCF optimizes element information items that contain base64-encoded data and exceed 1024 bytes in length.</span></span>

<span data-ttu-id="0229b-378">MTOM을 사용 하도록 WCF 종단점은 MTOM 인코딩된 메시지를 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-378">A WCF endpoint configured to use MTOM will always send MTOM-encoded messages.</span></span> <span data-ttu-id="0229b-379">필수 조건을 충족하는 부분이 없더라도 MTOM 인코딩된 메시지를 보냅니다. 이 메시지는 단일 MIME 부분에서 SOAP 봉투를 포함하는 MIME 패키지로 serialize됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-379">Even if no parts meet the required criteria, the message is still MTOM-encoded (serialized as a MIME package with a single MIME part containing the SOAP envelope).</span></span>

### <a name="ws-policy-assertion-for-mtom"></a><span data-ttu-id="0229b-380">MTOM WS-Policy Assertion</span><span class="sxs-lookup"><span data-stu-id="0229b-380">WS-Policy Assertion for MTOM</span></span>
<span data-ttu-id="0229b-381">WCF는 다음 정책 어설션은 사용 하 여 끝점에서 MTOM 사용을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-381">WCF uses the following policy assertion to indicate MTOM usage by endpoint:</span></span>

```xml
<wsoma:OptimizedMimeSerialization ... />
```

- <span data-ttu-id="0229b-382">R4211: 이전 정책 어설션은 엔드포인트 정책 주체를 포함하고 MTOM을 사용하여 엔드포인트에서 보내거나 받은 모든 메시지를 최적화하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-382">R4211: The preceding policy assertion has an Endpoint Policy Subject and specifies that all messages sent to and received from the endpoint must be optimized using MTOM.</span></span>

- <span data-ttu-id="0229b-383">B4212: MTOM 최적화를 사용 하도록 구성 되 면 WCF 끝점 추가 MTOM 정책 어설션을 해당 연결 된 정책 `wsdl:binding`합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-383">B4212: When configured to use MTOM optimization, an WCF endpoint adds an MTOM Policy assertion to the policy attached to the corresponding `wsdl:binding`.</span></span>

### <a name="composition-with-ws-security"></a><span data-ttu-id="0229b-384">WS-Security를 사용하여 구성</span><span class="sxs-lookup"><span data-stu-id="0229b-384">Composition with WS-Security</span></span>
<span data-ttu-id="0229b-385">MTOM은 비슷한 인코딩 메커니즘 `text/xml` 및 WCF 이진 XML입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-385">MTOM is an encoding mechanism that is similar to `text/xml` and WCF Binary XML.</span></span> <span data-ttu-id="0229b-386">MTOM은 WS-Security 및 기타 WS-\* 프로토콜을 사용하여 자연스러운 구성을 제공합니다. WS-Security를 사용하여 보안된 메시지는 MTOM을 사용하여 최적화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-386">MTOM offers natural composition with WS-Security and other WS-\* protocols: a message secured using WS-Security can be optimized using MTOM.</span></span>

### <a name="examples"></a><span data-ttu-id="0229b-387">예제</span><span class="sxs-lookup"><span data-stu-id="0229b-387">Examples</span></span>

#### <a name="wcf-soap-11-message-encoded-using-mtom"></a><span data-ttu-id="0229b-388">MTOM을 사용하여 인코딩한 WCF SOAP 1.1 메시지</span><span class="sxs-lookup"><span data-stu-id="0229b-388">WCF SOAP 1.1 Message Encoded Using MTOM</span></span>

```
POST http://131.107.72.15/Mtom/svc/service.svc/Soap11MtomUTF8 HTTP/1.1
SOAPAction: "http://xmlsoap.org/echoBinaryAsString"
Content-Type: multipart/related;type="application/xop+xml";
              start="<http://tempuri.org/0>";start-info="text/xml";
       boundary="uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1"
Host: 131.107.72.15
Content-Length: 1501
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1
Content-ID: <http://tempuri.org/0>
Content-Transfer-Encoding: 8bit
Content-Type: application/xop+xml;charset=utf-8;type="text/xml"
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body>
    <EchoBinaryAsString xmlns="http://xmlsoap.org/Ping">
      <array>
        <xop:Include
         href="cid:http%3A%2F%2Ftempuri.org%2F1%2F632618206521093670"
         xmlns:xop="http://www.w3.org/2004/08/xop/include"/>
      </array>
    </EchoBinaryAsString>
  </s:Body>
</s:Envelope>
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1
Content-ID: <http://tempuri.org/1/632618206521093670>
Content-Transfer-Encoding: binary
Content-Type: application/octet-stream
…Binary Content..
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=1
```

#### <a name="wcf-secure-soap-12-message-encoded-using-mtom"></a><span data-ttu-id="0229b-389">MTOM을 사용하여 인코딩한 WCF Secure SOAP 1.2 메시지</span><span class="sxs-lookup"><span data-stu-id="0229b-389">WCF Secure SOAP 1.2 Message Encoded Using MTOM</span></span>
<span data-ttu-id="0229b-390">이 예제에서 메시지는 WS-Security를 사용하여 보호된 SOAP 1.2 및 MTOM을 사용하여 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-390">In this example, a message is encoded using MTOM and SOAP 1.2 that is protected using WS-Security.</span></span> <span data-ttu-id="0229b-391">인코딩을 위해 식별되는 이진 부분은 `BinarySecurityToken`의 콘텐츠로서, 암호화된 서명 및 암호화된 본문에 해당하는 `CipherValue`의 `EncryptedData`입니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-391">The binary parts identified for encoding are the contents of the `BinarySecurityToken`, `CipherValue` of the `EncryptedData` corresponding to the encrypted signature and encrypted body.</span></span> <span data-ttu-id="0229b-392">합니다 `CipherValue` 의 `EncryptedKey` 없습니다 최적화 하 여 식별 된 WCF, 길이가 1024 바이트 미만 이므로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0229b-392">Note that the `CipherValue` of the `EncryptedKey` was not identified for optimization by WCF, because its length is less then 1024 bytes.</span></span>

```
POST http://131.107.72.15/Mtom/service.svc/Soap12MtomSecureSignEncrypt HTTP/1.1
Content-Type: multipart/related; type="application/xop+xml";
              start="<http://tempuri.org/0>";
            boundary="uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=3";
              start-info="application/soap+xml"; 
              action="http://xmlsoap.org/echoBinaryAsString"
Host: 131.107.72.15
Content-Length: 1941
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=3
Content-ID: <http://tempuri.org/0>
Content-Transfer-Encoding: 8bit
Content-Type: application/xop+xml;charset=utf-8;type="application/soap+xml"
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:u="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">
  <s:Header>
    <o:Security s:mustUnderstand="1" xmlns:o="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
      <u:Timestamp u:Id="uuid-4d4ee765-5717-4d53-9ac9-99bddc07df6c-5">
        <u:Created>2005-09-09T06:57:32.488Z</u:Created>
        <u:Expires>2005-09-09T07:02:32.488Z</u:Expires>
      </u:Timestamp>
      <o:BinarySecurityToken u:Id="uuid-4d4ee765-5717-4d53-9ac9-99bddc07df6c-2" ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509v3" EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary">
        <xop:Include href="cid:http%3A%2F%2Ftempuri.org%2F1%2F632618206525089430" xmlns:xop="http://www.w3.org/2004/08/xop/include"/>
      </o:BinarySecurityToken>
      <e:EncryptedKey Id="_1" xmlns:e="http://www.w3.org/2001/04/xmlenc#">
        <e:EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#rsa-oaep-mgf1p"/>
        <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
          <o:SecurityTokenReference>
            <o:KeyIdentifier ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509SubjectKeyIdentifier">Xeg55vRyK3ZhAEhEf+YT0z986L0=</o:KeyIdentifier>
          </o:SecurityTokenReference>
        </KeyInfo>
        <e:CipherData>          <e:CipherValue>oQfpxwT8/SAGyZQzKE2b4yO6dXuQj7pwJ+5CGL3Rf7C06bQ5ttMoQ9GLJcQYkXTzin+WwHEgs5bj5ml9HKTW9QAU5JJ6lksdymmQvWP5ZtGPBVchO4sofEGoCKmBiZL/DYS/cnbzgnc/3a6NYnc10y2fWGaGLiqa00zijAw7o0Y=</e:CipherValue>
        </e:CipherData>
      </e:EncryptedKey>
      <c:DerivedKeyToken u:Id="_2" xmlns:c="http://schemas.xmlsoap.org/ws/2005/02/sc">
        <o:SecurityTokenReference>
          <o:Reference URI="#_1"/>
        </o:SecurityTokenReference>
        <c:Nonce>OrEPRX7fISIS4sXYWPMv3g==</c:Nonce>
      </c:DerivedKeyToken>
      <e:ReferenceList xmlns:e="http://www.w3.org/2001/04/xmlenc#">
        <e:DataReference URI="#_3"/>
        <e:DataReference URI="#_4"/>
      </e:ReferenceList>
      <e:EncryptedData Id="_4" Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns:e="http://www.w3.org/2001/04/xmlenc#">
        <e:EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#aes256-cbc"/>
        <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
          <o:SecurityTokenReference>
            <o:Reference URI="#_2"/>
          </o:SecurityTokenReference>
        </KeyInfo>
        <e:CipherData>
          <e:CipherValue>
            <xop:Include href="cid:http%3A%2F%2Ftempuri.org%2F2%2F632618206525089430" xmlns:xop="http://www.w3.org/2004/08/xop/include"/>
          </e:CipherValue>
        </e:CipherData>
      </e:EncryptedData>
    </o:Security>
  </s:Header>
  <s:Body u:Id="_0">
    <e:EncryptedData Id="_3" Type="http://www.w3.org/2001/04/xmlenc#Content" xmlns:e="http://www.w3.org/2001/04/xmlenc#">
      <e:EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#aes256-cbc"/>
      <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
        <o:SecurityTokenReference xmlns:o="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
          <o:Reference URI="#_2"/>
        </o:SecurityTokenReference>
      </KeyInfo>
      <e:CipherData>
        <e:CipherValue>
          <xop:Include href="cid:http%3A%2F%2Ftempuri.org%2F3%2F632618206525089430" xmlns:xop="http://www.w3.org/2004/08/xop/include"/>
        </e:CipherValue>
      </e:CipherData>
    </e:EncryptedData>
  </s:Body>
</s:Envelope>
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=3
Content-ID: <http://tempuri.org/1/632618206525089430>
Content-Transfer-Encoding: binary
Content-Type: application/octet-stream
...Binary content of BinarySecurityToken - X509 Certificate...
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=3
Content-ID: <http://tempuri.org/2/632618206525089430>
Content-Transfer-Encoding: binary
Content-Type: application/octet-stream
...Binary serialization of the encrypted primary signature...
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=3
Content-ID: <http://tempuri.org/3/632618206525089430>
Content-Transfer-Encoding: binary
Content-Type: application/octet-stream
...Binary serialization of the encrypted Body...
--uuid:0ca0e16e-feb1-426c-97d8-c4508ada5e82+id=3--
```