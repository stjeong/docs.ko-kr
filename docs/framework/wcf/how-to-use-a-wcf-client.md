---
title: '방법: Windows Communication Foundation 클라이언트 사용'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], using
dev_langs:
- CSharp
- VB
ms.assetid: 190349fc-0573-49c7-bb85-8e316df7f31f
ms.openlocfilehash: 12e911fb899cb85121c129b762828cdda01e64f1
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47112668"
---
# <a name="how-to-use-a-windows-communication-foundation-client"></a>방법: Windows Communication Foundation 클라이언트 사용

이 기본 Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 마지막 작업입니다. 6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.

Windows Communication Foundation (WCF) 프록시를 생성 하 고 구성 된 된 클라이언트 인스턴스를 만들 수 있으며 클라이언트 응용 프로그램 컴파일 및 WCF 서비스와 통신할 때 사용할 수 있습니다. 이 항목에서는 인스턴스화하고 WCF 클라이언트를 사용 하는 절차를 설명 합니다. 이 절차에서는 다음과 같은 세 작업을 수행합니다.

1.  WCF 클라이언트를 인스턴스화합니다.

2.  생성된 프록시에서 서비스 작업 호출

3.  작업 호출이 완료되면 클라이언트 닫기

## <a name="use-a-windows-communication-foundation-client"></a>Windows Communication Foundation 클라이언트 사용

GettingStartedClient 프로젝트에서 코드 편집기에서 Program.cs 또는 Program.vb 파일을 열고 기존 코드를 다음 코드로 바꿉니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using GettingStartedClient.ServiceReference1;

namespace GettingStartedClient
{
    class Program
    {
        static void Main(string[] args)
        {
            //Step 1: Create an instance of the WCF proxy.
            CalculatorClient client = new CalculatorClient();

            // Step 2: Call the service operations.
            // Call the Add service operation.
            double value1 = 100.00D;
            double value2 = 15.99D;
            double result = client.Add(value1, value2);
            Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);

            // Call the Subtract service operation.
            value1 = 145.00D;
            value2 = 76.54D;
            result = client.Subtract(value1, value2);
            Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result);

            // Call the Multiply service operation.
            value1 = 9.00D;
            value2 = 81.25D;
            result = client.Multiply(value1, value2);
            Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result);

            // Call the Divide service operation.
            value1 = 22.00D;
            value2 = 7.00D;
            result = client.Divide(value1, value2);
            Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result);

            //Step 3: Closing the client gracefully closes the connection and cleans up resources.
            client.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Collections.Generic
Imports System.Text
Imports System.ServiceModel
Imports GettingStartedClientVB2.ServiceReference1

Module Module1

    Sub Main()
        ' Step 1: Create an instance of the WCF proxy
        Dim Client As New CalculatorClient()

        'Step 2: Call the service operations.
        'Call the Add service operation.
        Dim value1 As Double = 100D
        Dim value2 As Double = 15.99D
        Dim result As Double = Client.Add(value1, value2)
        Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result)

        'Call the Subtract service operation.
        value1 = 145D
        value2 = 76.54D
        result = Client.Subtract(value1, value2)
        Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result)

        'Call the Multiply service operation.
        value1 = 9D
        value2 = 81.25D
        result = Client.Multiply(value1, value2)
        Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result)

        'Call the Divide service operation.
        value1 = 22D
        value2 = 7D
        result = Client.Divide(value1, value2)
        Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result)

        ' Step 3: Closing the client gracefully closes the connection and cleans up resources.
        Client.Close()

        Console.WriteLine()
        Console.WriteLine("Press <ENTER> to terminate client.")
        Console.ReadLine()

    End Sub

End Module
```

알림 합니다 `using` 또는 `Imports` 가져오는 문은 `GettingStartedClient.ServiceReference1`합니다. 생성 한 코드를 가져옵니다 **서비스 참조 추가** Visual Studio에서. 코드는 WCF 프록시를 인스턴스화합니다 및 다음 각 계산기 서비스에 의해 노출 되는 서비스 작업 호출, 프록시를 닫고 종료 합니다.

이것으로 초보자를 위한 자습서를 완료했습니다. 서비스 계약을 정의했고 서비스 계약을 구현했으며 WCF 프록시를 생성했고 WCF 클라이언트 응용 프로그램을 구성한 다음 서비스 작업을 호출하기 위해 프록시를 사용했습니다. 응용 프로그램을 테스트 하려면 먼저 서비스를 시작한 다음 GettingStartedClient를 실행 하는 GettingStartedHost를 실행 합니다.

GettingStartedHost의 출력은 다음과 같아야 합니다.

```text
The service is ready.Press <ENTER> to terminate service.Received Add(100,15.99)Return: 115.99Received Subtract(145,76.54)Return: 68.46Received Multiply(9,81.25)Return: 731.25Received Divide(22,7)Return: 3.14285714285714
```

GettingStartedClient의 출력은 다음과 같아야 합니다.

```text
Add(100,15.99) = 115.99Subtract(145,76.54) = 68.46Multiply(9,81.25) = 731.25Divide(22,7) = 3.14285714285714Press <ENTER> to terminate client.
```

## <a name="see-also"></a>참고자료

- [클라이언트 빌드](../../../docs/framework/wcf/building-clients.md)
- [방법: 클라이언트 만들기](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md)
- [기본 WCF 프로그래밍](../../../docs/framework/wcf/basic-wcf-programming.md)
- [방법: 이중 계약 만들기](../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
- [방법: 이중 계약을 사용하여 서비스 액세스](../../../docs/framework/wcf/feature-details/how-to-access-services-with-a-duplex-contract.md)
- [시작](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [자체 호스팅](../../../docs/framework/wcf/samples/self-host.md)