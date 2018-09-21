---
title: '방법: 기본 Windows Communication Foundation 서비스 호스트 및 실행'
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: b79c3246b7c12a3a99a5c68586387fc30573dcb6
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562296"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a>방법: 기본 Windows Communication Foundation 서비스 호스트 및 실행

WCF(Windows Communication Foundation) 응용 프로그램을 만드는 데 필요한 6가지 작업 중 세 번째 작업입니다. 6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.

이 항목에서는 콘솔 응용 프로그램에서 WCF(Windows Communication Foundation) 서비스를 호스팅하는 방법에 대해 설명합니다. 이 절차는 다음 단계로 구성됩니다.

- 서비스를 호스팅할 콘솔 응용 프로그램 프로젝트를 만듭니다.

- 서비스에 대한 서비스 호스트를 만듭니다.

- 메타데이터 교환을 사용하도록 설정합니다.

- 서비스 호스트를 엽니다.

이 작업에서 작성된 전체 코드 목록은 이 절차 다음에 나오는 다음 예제에 제공되어 있습니다.

## <a name="create-a-new-console-application-to-host-the-service"></a>서비스를 호스팅할 새 콘솔 응용 프로그램 만들기

1. Getting Started 솔루션을 마우스 오른쪽 단추로 클릭 하 고 선택 하 여 Visual Studio에서 새 콘솔 응용 프로그램 프로젝트를 만듭니다 **추가** > **새 프로젝트**합니다. 에 **새 프로젝트 추가** 대화 상자의 왼쪽에 있는 선택에서 **Windows Desktop** 에서 범주 **Visual C#** 또는 **Visual Basic**합니다. 선택 된 **콘솔 앱 (.NET Framework)** 템플릿을 선택한 후 프로젝트 이름을 **GettingStartedHost**합니다.

2. GettingStartedLib 프로젝트에 대 한 참조를 GettingStartedHost 프로젝트에 추가 합니다. 마우스 오른쪽 단추로 클릭 합니다 **참조** GettingStartedHost 프로젝트의 폴더 **솔루션 탐색기**를 선택한 후 **참조 추가**합니다. 에 **참조 추가** 대화 상자에서 **솔루션** 대화 상자의 왼쪽에서 대화 상자 가운데에서 GettingStartedLib를 선택 하 고 선택한 **추가**합니다. 이제 GettingStartedLib에 정의된 형식을 GettingStartedHost 프로젝트에서 사용할 수 있습니다.

3. System.ServiceModel에 대 한 참조를 GettingStartedHost 프로젝트에 추가 합니다. 마우스 오른쪽 단추로 클릭 합니다 **참조** GettingStartedHost 프로젝트의 폴더 **솔루션 탐색기** 선택한 **참조 추가**합니다. 에 **참조 추가** 대화 상자에서 **프레임 워크** 대화 상자의 왼쪽에서 **어셈블리**합니다. 찾기 및 선택 **System.ServiceModel**를 선택한 후 **확인**합니다. 선택 하 여 솔루션을 저장할 **파일** > **모두 저장**합니다.

## <a name="host-the-service"></a>서비스 호스트

편집할 Program.cs 또는 Module.vb 파일을 열고 다음 코드를 입력합니다.

```csharp
using System;
using System.ServiceModel;
using System.ServiceModel.Description;
using GettingStartedLib;

namespace GettingStartedHost
{
    class Program
    {
        static void Main(string[] args)
        {
            // Step 1 Create a URI to serve as the base address.
            Uri baseAddress = new Uri("http://localhost:8000/GettingStarted/");

            // Step 2 Create a ServiceHost instance
            ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

            try
            {
                // Step 3 Add a service endpoint.
                selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                // Step 4 Enable metadata exchange.
                ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                smb.HttpGetEnabled = true;
                selfHost.Description.Behaviors.Add(smb);

                // Step 5 Start the service.
                selfHost.Open();
                Console.WriteLine("The service is ready.");
                Console.WriteLine("Press <ENTER> to terminate service.");
                Console.WriteLine();
                Console.ReadLine();

                // Close the ServiceHostBase to shutdown the service.
                selfHost.Close();
            }
            catch (CommunicationException ce)
            {
                Console.WriteLine("An exception occurred: {0}", ce.Message);
                selfHost.Abort();
            }
        }
    }
}
```

```vb
Imports System.ServiceModel
Imports System.ServiceModel.Description
Imports GettingStartedLibVB.GettingStartedLib

Module Service

    Class Program
        Shared Sub Main()
            ' Step 1 Create a URI to serve as the base address
            Dim baseAddress As New Uri("http://localhost:8000/ServiceModelSamples/Service")

            ' Step 2 Create a ServiceHost instance
            Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
           Try

                ' Step 3 Add a service endpoint
                ' Add a service endpoint
                selfHost.AddServiceEndpoint( _
                    GetType(ICalculator), _
                    New WSHttpBinding(), _
                    "CalculatorService")

                ' Step 4 Enable metadata exchange.
                Dim smb As New ServiceMetadataBehavior()
                smb.HttpGetEnabled = True
                selfHost.Description.Behaviors.Add(smb)

                ' Step 5 Start the service
                selfHost.Open()
                Console.WriteLine("The service is ready.")
                Console.WriteLine("Press <ENTER> to terminate service.")
                Console.WriteLine()
                Console.ReadLine()

                ' Close the ServiceHostBase to shutdown the service.
                selfHost.Close()
            Catch ce As CommunicationException
                Console.WriteLine("An exception occurred: {0}", ce.Message)
                selfHost.Abort()
            End Try
        End Sub
    End Class

End Module
```

**1 단계** -서비스의 기본 주소를 보유할 Uri 클래스의 인스턴스를 만듭니다. 서비스는 기본 주소와 선택적 URI를 포함하는 URL로 식별됩니다. 기본 주소 형식은 다음과 같습니다. [전송]://[시스템 이름 또는 도메인][:선택적 포트 번호]/[선택적 URI 세그먼트]계산기 서비스의 기본 주소는 HTTP 전송, 로컬 호스트, 포트 8000 및 URI 세그먼트 “GettingStarted”를 사용합니다.

**2 단계** –의 인스턴스를 만듭니다는 <xref:System.ServiceModel.ServiceHost> 서비스를 호스트 하는 클래스입니다. 생성자는 서비스 계약을 구현하는 클래스 형식과 서비스의 기본 주소, 두 가지 매개 변수를 사용합니다.

**3 단계** – 만듭니다는 <xref:System.ServiceModel.Description.ServiceEndpoint> 인스턴스. 서비스 엔드포인트는 주소, 바인딩 및 서비스 계약으로 구성되어 있습니다. 따라서 <xref:System.ServiceModel.Description.ServiceEndpoint> 생성자는 서비스 계약 인터페이스 형식, 바인딩 및 주소를 사용합니다. 서비스 계약은 사용자가 정의한 `ICalculator`이며 서비스 형식에 구현합니다. 이 예제에 사용된 바인딩은 WS-* 사양을 따르는 엔드포인트에 연결하는 데 사용되는 기본 바인딩인 <xref:System.ServiceModel.WSHttpBinding>입니다. WCF 바인딩에 대한 자세한 내용은 [WCF 바인딩 개요](../../../docs/framework/wcf/bindings-overview.md)를 참조하세요. 엔드포인트를 식별하기 위해 주소가 기본 주소에 추가됩니다. 끝점에 대 한 정규화 된 주소 이므로이 코드에서 지정 된 주소는 "CalculatorService" `"http://localhost:8000/GettingStarted/CalculatorService"`합니다.

    > [!IMPORTANT]
    > Adding a service endpoint is optional when using .NET Framework 4 or later. In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service. For more information about default endpoints see [Specifying an Endpoint Address](../../../docs/framework/wcf/specifying-an-endpoint-address.md). For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).

**4 단계** – 메타 데이터 교환을 사용 하도록 설정 합니다. 클라이언트는 메타데이터 교환을 사용하여 서비스 작업을 호출하는 데 사용되는 프록시를 생성합니다. 메타데이터 교환을 활성화하려면 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 인스턴스를 만들고 해당 <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> 속성을 `true`로 설정한 다음, 동작을 <xref:System.ServiceModel.ServiceHost> 인스턴스의 <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` 컬렉션에 추가합니다.

**5 단계** Open –는 <xref:System.ServiceModel.ServiceHost> 들어오는 메시지를 수신 대기 합니다. 코드는 사용자가 Enter를 누를 때까지 기다립니다. 이를 수행하지 않으면 응용 프로그램이 즉시 닫히고 서비스가 종료합니다. 또한 사용된 try/catch 블록도 주의하십시오. <xref:System.ServiceModel.ServiceHost>를 인스턴스화한 후에는 나머지 코드가 try/catch 블록에 배치됩니다. <xref:System.ServiceModel.ServiceHost>에서 throw된 예외를 안전하게 catch하는 방법에 대한 자세한 내용은 [Using 문 사용 시 문제 회피](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)를 참조하세요.

> [!IMPORTANT]
> 코드에서 변경한 내용을 반영 하도록 GettingStartedLib에서 App.config를 편집 합니다.
> 1. 줄 14를 변경 합니다. `<service name="GettingStartedLib.CalculatorService">`
> 2. 줄 17을 변경 합니다. `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`
> 3. 22 줄을 변경 합니다. `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`

## <a name="verify-the-service-is-working"></a>서비스가 작동 확인

1. GettingStartedHost 콘솔 실행 Visual Studio 내부에서 응용 프로그램입니다.

   서비스는 관리자 권한으로 실행 되어야 합니다. 관리자 권한으로 Visual Studio를 열었으므로 GettingStartedHost도 관리자 권한으로 실행 됩니다. 사용 하 여 새 명령 프롬프트를 열 수도 있습니다 **관리자 권한으로 실행** 내에서 service.exe를 실행 합니다.

2. 웹 브라우저를 열고 서비스의 디버그 페이지인 `http://localhost:8000/GettingStarted/CalculatorService`합니다.

## <a name="example"></a>예제

다음 예제에는 자습서의 이전 단계의 서비스 계약과 구현이 포함되어 있으며 콘솔 응용 프로그램에서 서비스를 호스팅합니다.

이 명령줄 컴파일러로 컴파일하려면 IService1.cs 및 컴파일합니다 Service1.cs 참조 하는 클래스 라이브러리로 `System.ServiceModel.dll`합니다. Program.cs를 콘솔 응용 프로그램으로 컴파일하십시오.

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
        [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
        public interface ICalculator
        {
            [OperationContract]
            double Add(double n1, double n2);
            [OperationContract]
            double Subtract(double n1, double n2);
            [OperationContract]
            double Multiply(double n1, double n2);
            [OperationContract]
            double Divide(double n1, double n2);
        }
}
```

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
    public class CalculatorService : ICalculator
    {
        public double Add(double n1, double n2)
        {
            double result = n1 + n2;
            Console.WriteLine("Received Add({0},{1})", n1, n2);
            // Code added to write output to the console window.
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Subtract(double n1, double n2)
        {
            double result = n1 - n2;
            Console.WriteLine("Received Subtract({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Multiply(double n1, double n2)
        {
            double result = n1 * n2;
            Console.WriteLine("Received Multiply({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Divide(double n1, double n2)
        {
            double result = n1 / n2;
            Console.WriteLine("Received Divide({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }
    }
}
```

```csharp
using System;
using System.ServiceModel;
using System.ServiceModel.Description;
using GettingStartedLib;

namespace GettingStartedHost
{
    class Program
    {
        static void Main(string[] args)
        {
            // Step 1 of the address configuration procedure: Create a URI to serve as the base address.
            Uri baseAddress = new Uri("http://localhost:8000/ServiceModelSamples/Service");

            // Step 2 of the hosting procedure: Create ServiceHost
            ServiceHost selfHost = new ServiceHost(typeof(CalculatorService), baseAddress);

            try
            {
                // Step 3 of the hosting procedure: Add a service endpoint.
                selfHost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(), "CalculatorService");

                // Step 4 of the hosting procedure: Enable metadata exchange.
                ServiceMetadataBehavior smb = new ServiceMetadataBehavior();
                smb.HttpGetEnabled = true;
                selfHost.Description.Behaviors.Add(smb);

                // Step 5 of the hosting procedure: Start (and then stop) the service.
                selfHost.Open();
                Console.WriteLine("The service is ready.");
                Console.WriteLine("Press <ENTER> to terminate service.");
                Console.WriteLine();
                Console.ReadLine();

                // Close the ServiceHostBase to shutdown the service.
                selfHost.Close();
            }
            catch (CommunicationException ce)
            {
                Console.WriteLine("An exception occurred: {0}", ce.Message);
                selfHost.Abort();
            }
        }
    }
}
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
    Public Interface ICalculator

        <OperationContract()> _
        Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
    End Interface
End Namespace
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    Public Class CalculatorService
        Implements ICalculator

        Public Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Add
            Dim result As Double = n1 + n2
            ' Code added to write output to the console window.
            Console.WriteLine("Received Add({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result
        End Function

        Public Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Subtract
            Dim result As Double = n1 - n2
            Console.WriteLine("Received Subtract({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Multiply
            Dim result As Double = n1 * n2
            Console.WriteLine("Received Multiply({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Divide
            Dim result As Double = n1 / n2
            Console.WriteLine("Received Divide({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function
    End Class
End Namespace
```

```vb
Imports System.ServiceModel
Imports System.ServiceModel.Description
Imports GettingStartedLibVB.GettingStartedLib

Module Service

    Class Program
        Shared Sub Main()
            ' Step 1 of the address configuration procedure: Create a URI to serve as the base address.
            Dim baseAddress As New Uri("http://localhost:8000/ServiceModelSamples/Service")

            ' Step 2 of the hosting procedure: Create ServiceHost
            Dim selfHost As New ServiceHost(GetType(CalculatorService), baseAddress)
            Try

                ' Step 3 of the hosting procedure: Add a service endpoint.
                ' Add a service endpoint
                selfHost.AddServiceEndpoint( _
                    GetType(ICalculator), _
                    New WSHttpBinding(), _
                    "CalculatorService")

                ' Step 4 of the hosting procedure: Enable metadata exchange.
                ' Enable metadata exchange
                Dim smb As New ServiceMetadataBehavior()
                smb.HttpGetEnabled = True
                selfHost.Description.Behaviors.Add(smb)

                ' Step 5 of the hosting procedure: Start (and then stop) the service.
                selfHost.Open()
                Console.WriteLine("The service is ready.")
                Console.WriteLine("Press <ENTER> to terminate service.")
                Console.WriteLine()
                Console.ReadLine()

                ' Close the ServiceHostBase to shutdown the service.
                selfHost.Close()
            Catch ce As CommunicationException
                Console.WriteLine("An exception occurred: {0}", ce.Message)
                selfHost.Abort()
            End Try
        End Sub
    End Class

End Module
```

> [!NOTE]
> 이러한 서비스에는 수신 대기를 위해 시스템에 HTTP 주소를 등록할 권한이 있어야 합니다. 관리자 계정에는 이 권한이 있지만, 관리자 이외의 계정에는 HTTP 네임스페이스에 대한 권한을 부여해야 합니다. 네임스페이스 예약을 구성하는 방법에 대한 자세한 내용은 [HTTP 및 HTTPS 구성](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md)을 참조하세요. Visual Studio에서 실행하는 경우 service.exe는 관리자 권한으로 실행해야 합니다.

## <a name="next-steps"></a>다음 단계

서비스가 실행되고 있습니다. 다음 태스크에서는 WCF 클라이언트를 만듭니다.

> [!div class="nextstepaction"]
> [방법: WCF 클라이언트 만들기](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)

문제 해결 정보는 [초보자를 위한 자습서 문제 해결](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md)을 참조하세요.

## <a name="see-also"></a>참고자료

- [시작](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [자체 호스팅](../../../docs/framework/wcf/samples/self-host.md)