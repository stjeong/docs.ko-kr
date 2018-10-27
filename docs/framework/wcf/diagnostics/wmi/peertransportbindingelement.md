---
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: 58bf07b0429ca2435b5aae3683ef69951a10003e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185185"
---
# <a name="peertransportbindingelement"></a><span data-ttu-id="85efc-102">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="85efc-102">PeerTransportBindingElement</span></span>
<span data-ttu-id="85efc-103">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="85efc-103">PeerTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85efc-104">구문</span><span class="sxs-lookup"><span data-stu-id="85efc-104">Syntax</span></span>  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="85efc-105">메서드</span><span class="sxs-lookup"><span data-stu-id="85efc-105">Methods</span></span>  
 <span data-ttu-id="85efc-106">PeerTransportBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-106">The PeerTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="85efc-107">속성</span><span class="sxs-lookup"><span data-stu-id="85efc-107">Properties</span></span>  
 <span data-ttu-id="85efc-108">PeerTransportBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-108">The PeerTransportBindingElement class has the following properties:</span></span>  
  
### <a name="listenipaddress"></a><span data-ttu-id="85efc-109">ListenIPAddress</span><span class="sxs-lookup"><span data-stu-id="85efc-109">ListenIPAddress</span></span>  
 <span data-ttu-id="85efc-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="85efc-110">Data type: string</span></span>  
  
 <span data-ttu-id="85efc-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="85efc-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="85efc-112">피어 노드가 메시지를 수신하는 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-112">The IP address on which the peer node listens for messages.</span></span>  
  
### <a name="port"></a><span data-ttu-id="85efc-113">포트</span><span class="sxs-lookup"><span data-stu-id="85efc-113">Port</span></span>  
 <span data-ttu-id="85efc-114">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="85efc-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="85efc-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="85efc-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="85efc-116">이 바인딩이 피어 채널 메시지를 처리할 네트워크 인터페이스 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-116">The network interface port on which this binding processes peer channel messages.</span></span>  
  
### <a name="security"></a><span data-ttu-id="85efc-117">보안</span><span class="sxs-lookup"><span data-stu-id="85efc-117">Security</span></span>  
 <span data-ttu-id="85efc-118">데이터 형식: PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="85efc-118">Data type: PeerSecuritySettings</span></span>  
  
 <span data-ttu-id="85efc-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="85efc-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="85efc-120">피어 전송 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-120">Peer transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85efc-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="85efc-121">Requirements</span></span>  
  
|<span data-ttu-id="85efc-122">MOF</span><span class="sxs-lookup"><span data-stu-id="85efc-122">MOF</span></span>|<span data-ttu-id="85efc-123">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="85efc-124">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="85efc-124">Namespace</span></span>|<span data-ttu-id="85efc-125">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85efc-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="85efc-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="85efc-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
