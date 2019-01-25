---
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: 437ccc0446e3cc05596ab12b7908177b7f78e431
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670656"
---
# <a name="peertransportbindingelement"></a><span data-ttu-id="72184-102">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="72184-102">PeerTransportBindingElement</span></span>
<span data-ttu-id="72184-103">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="72184-103">PeerTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72184-104">구문</span><span class="sxs-lookup"><span data-stu-id="72184-104">Syntax</span></span>  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="72184-105">메서드</span><span class="sxs-lookup"><span data-stu-id="72184-105">Methods</span></span>  
 <span data-ttu-id="72184-106">PeerTransportBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72184-106">The PeerTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="72184-107">속성</span><span class="sxs-lookup"><span data-stu-id="72184-107">Properties</span></span>  
 <span data-ttu-id="72184-108">PeerTransportBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72184-108">The PeerTransportBindingElement class has the following properties:</span></span>  
  
### <a name="listenipaddress"></a><span data-ttu-id="72184-109">ListenIPAddress</span><span class="sxs-lookup"><span data-stu-id="72184-109">ListenIPAddress</span></span>  
 <span data-ttu-id="72184-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="72184-110">Data type: string</span></span>  
  
 <span data-ttu-id="72184-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="72184-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="72184-112">피어 노드가 메시지를 수신하는 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="72184-112">The IP address on which the peer node listens for messages.</span></span>  
  
### <a name="port"></a><span data-ttu-id="72184-113">포트</span><span class="sxs-lookup"><span data-stu-id="72184-113">Port</span></span>  
 <span data-ttu-id="72184-114">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="72184-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="72184-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="72184-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="72184-116">이 바인딩이 피어 채널 메시지를 처리할 네트워크 인터페이스 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="72184-116">The network interface port on which this binding processes peer channel messages.</span></span>  
  
### <a name="security"></a><span data-ttu-id="72184-117">보안</span><span class="sxs-lookup"><span data-stu-id="72184-117">Security</span></span>  
 <span data-ttu-id="72184-118">데이터 형식: PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="72184-118">Data type: PeerSecuritySettings</span></span>  
  
 <span data-ttu-id="72184-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="72184-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="72184-120">피어 전송 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="72184-120">Peer transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72184-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="72184-121">Requirements</span></span>  
  
|<span data-ttu-id="72184-122">MOF</span><span class="sxs-lookup"><span data-stu-id="72184-122">MOF</span></span>|<span data-ttu-id="72184-123">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72184-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="72184-124">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="72184-124">Namespace</span></span>|<span data-ttu-id="72184-125">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72184-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="72184-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="72184-126">See also</span></span>
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
