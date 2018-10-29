---
title: 소켓 코드 예제
ms.date: 03/30/2017
helpviewer_keywords:
- application protocols, sockets
- sending data, sockets
- Socket class, asynchronous server sockets
- data requests, sockets
- requesting data from Internet, sockets
- server sockets
- sockets, code examples
- receiving data, sockets
- protocols, sockets
- Internet, sockets
- client sockets
ms.assetid: f3fc7533-6956-42c6-bbc3-73e5a221027d
ms.openlocfilehash: f709c2e0780b89e072c43e9acaf722e6851d4cbe
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50199957"
---
# <a name="socket-code-examples"></a><span data-ttu-id="32ecc-102">소켓 코드 예제</span><span class="sxs-lookup"><span data-stu-id="32ecc-102">Socket Code Examples</span></span>
<span data-ttu-id="32ecc-103">다음 코드 예제에서는 <xref:System.Net.Sockets.Socket> 클래스를 원격 네트워크 서비스에 연결할 클라이언트 및 원격 클라이언트의 연결을 수신 대기할 서버로 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-103">The following code examples demonstrate how to use the <xref:System.Net.Sockets.Socket> class as a client to connect to remote network services and as a server to listen for connections from remote clients.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="32ecc-104">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="32ecc-104">In This Section</span></span>  
 [<span data-ttu-id="32ecc-105">동기 클라이언트 소켓 예제</span><span class="sxs-lookup"><span data-stu-id="32ecc-105">Synchronous Client Socket Example</span></span>](../../../docs/framework/network-programming/synchronous-client-socket-example.md)  
 <span data-ttu-id="32ecc-106">서버에 연결하고 서버에서 반환된 데이터를 표시하는 동기 <xref:System.Net.Sockets.Socket> 클라이언트를 구현하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-106">Shows how to implement a synchronous <xref:System.Net.Sockets.Socket> client that connects to a server and displays the data returned from the server.</span></span>  
  
 [<span data-ttu-id="32ecc-107">동기 서버 소켓 예제</span><span class="sxs-lookup"><span data-stu-id="32ecc-107">Synchronous Server Socket Example</span></span>](../../../docs/framework/network-programming/synchronous-server-socket-example.md)  
 <span data-ttu-id="32ecc-108">클라이언트의 연결을 수락하고 클라이언트에서 받은 데이터를 다시 에코하는 동기 <xref:System.Net.Sockets.Socket> 서버를 구현하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-108">Shows how to implement a synchronous <xref:System.Net.Sockets.Socket> server that accepts connections from a client and echoes back the data received from the client.</span></span>  
  
 [<span data-ttu-id="32ecc-109">비동기 클라이언트 소켓 예제</span><span class="sxs-lookup"><span data-stu-id="32ecc-109">Asynchronous Client Socket Example</span></span>](../../../docs/framework/network-programming/asynchronous-client-socket-example.md)  
 <span data-ttu-id="32ecc-110">서버에 연결하고 서버에서 반환된 데이터를 표시하는 비동기 <xref:System.Net.Sockets.Socket> 클라이언트를 구현하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-110">Shows how to implement an asynchronous <xref:System.Net.Sockets.Socket> client that connects to a server and displays the data returned from the server.</span></span>  
  
 [<span data-ttu-id="32ecc-111">비동기 서버 소켓 예제</span><span class="sxs-lookup"><span data-stu-id="32ecc-111">Asynchronous Server Socket Example</span></span>](../../../docs/framework/network-programming/asynchronous-server-socket-example.md)  
 <span data-ttu-id="32ecc-112">클라이언트의 연결을 수락하고 클라이언트에서 받은 데이터를 다시 에코하는 비동기 <xref:System.Net.Sockets.Socket> 서버를 구현하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-112">Shows how to implement an asynchronous <xref:System.Net.Sockets.Socket> server that accepts connections from a client and echoes back the data received from the client.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="32ecc-113">관련 단원</span><span class="sxs-lookup"><span data-stu-id="32ecc-113">Related Sections</span></span>  
 [<span data-ttu-id="32ecc-114">소켓</span><span class="sxs-lookup"><span data-stu-id="32ecc-114">Sockets</span></span>](../../../docs/framework/network-programming/sockets.md)  
 <span data-ttu-id="32ecc-115"><xref:System.Net.Sockets> 네임스페이스 및 <xref:System.Net.Sockets.Socket> 클래스에 대한 기본 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-115">Provides basic information about the <xref:System.Net.Sockets> namespace and the <xref:System.Net.Sockets.Socket> class.</span></span>  
  
 [<span data-ttu-id="32ecc-116">네트워크 프로그래밍의 보안</span><span class="sxs-lookup"><span data-stu-id="32ecc-116">Security in Network Programming</span></span>](../../../docs/framework/network-programming/security-in-network-programming.md)  
 <span data-ttu-id="32ecc-117">표준 인터넷 보안 및 인증 기술을 사용하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="32ecc-117">Describes how to use standard Internet security and authentication techniques.</span></span>
