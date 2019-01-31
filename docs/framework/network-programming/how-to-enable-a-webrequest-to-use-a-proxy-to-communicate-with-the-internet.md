---
title: '방법: 프록시를 사용하여 인터넷과 통신하도록 WebRequest 설정'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 63c0ef2c-44b5-4c54-9804-ba0b9b001ac7
ms.openlocfilehash: d8bcf20831a806694ab40ed7584365d8109e1460
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689015"
---
# <a name="how-to-enable-a-webrequest-to-use-a-proxy-to-communicate-with-the-internet"></a><span data-ttu-id="0c5c2-102">방법: 프록시를 사용하여 인터넷과 통신하도록 WebRequest 설정</span><span class="sxs-lookup"><span data-stu-id="0c5c2-102">How to: Enable a WebRequest to Use a Proxy to Communicate With the Internet</span></span>
<span data-ttu-id="0c5c2-103">이 예제에서는 인터넷과 통신하는 데 프록시를 사용하기 위해 <xref:System.Net.WebRequest>를 사용하도록 설정할 전역 프록시 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-103">This example creates a global proxy instance that will enable any <xref:System.Net.WebRequest> to use a proxy to communicate with the Internet.</span></span> <span data-ttu-id="0c5c2-104">예제에서는 프록시 서버의 이름이 `webproxy`이고 표준 HTTP 포트인 포트 80에서 통신한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-104">The example assumes that the proxy server is named `webproxy` and that it communicates on port 80, the standard HTTP port.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c5c2-105">예제</span><span class="sxs-lookup"><span data-stu-id="0c5c2-105">Example</span></span>  
  
```csharp  
WebProxy proxyObject = new WebProxy("http://webproxy:80/");  
GlobalProxySelection.Select = proxyObject;  
```  
  
```vb  
Dim proxyObject As WebProxy = New WebProxy("http://webproxy:80/")  
GlobalProxySelection.Select = proxyObject  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0c5c2-106">코드 컴파일</span><span class="sxs-lookup"><span data-stu-id="0c5c2-106">Compiling the Code</span></span>  
 <span data-ttu-id="0c5c2-107">이 예제에는 다음 사항이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-107">This example requires:</span></span>  
  
-   <span data-ttu-id="0c5c2-108">**System.Net** 네임스페이스에 대한 [`using` 지시문](../../csharp/language-reference/keywords/using-directive.md)</span><span class="sxs-lookup"><span data-stu-id="0c5c2-108">A [`using` directive](../../csharp/language-reference/keywords/using-directive.md) for the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c5c2-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0c5c2-109">See also</span></span>
- [<span data-ttu-id="0c5c2-110">애플리케이션 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="0c5c2-110">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)
- [<span data-ttu-id="0c5c2-111">프록시를 통해 인터넷 액세스</span><span class="sxs-lookup"><span data-stu-id="0c5c2-111">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
