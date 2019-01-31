---
title: 호스트 및 기본 Windows Communication Foundation 서비스를 실행 하는 방법
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: 3a029ef23ba3e9a0dd62e410739fa8734acc202a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277773"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a><span data-ttu-id="01f72-102">호스트 및 기본 Windows Communication Foundation 서비스를 실행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="01f72-102">How to host and run a basic Windows Communication Foundation service</span></span>

<span data-ttu-id="01f72-103">WCF(Windows Communication Foundation) 애플리케이션을 만드는 데 필요한 6가지 작업 중 세 번째 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-103">This is the third of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="01f72-104">6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](getting-started-tutorial.md) 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01f72-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="01f72-105">이 항목에서는 콘솔 애플리케이션에서 WCF(Windows Communication Foundation) 서비스를 호스팅하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-105">This topic describes how to host a Windows Communication Foundation (WCF) service in a console application.</span></span> <span data-ttu-id="01f72-106">이 절차는 다음 단계로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-106">This procedure consists of the following steps:</span></span>

- <span data-ttu-id="01f72-107">서비스를 호스팅할 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-107">Create a console application project to host the service.</span></span>

- <span data-ttu-id="01f72-108">서비스에 대한 서비스 호스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-108">Create a service host for the service.</span></span>

- <span data-ttu-id="01f72-109">메타데이터 교환을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-109">Enable metadata exchange.</span></span>

- <span data-ttu-id="01f72-110">서비스 호스트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-110">Open the service host.</span></span>

<span data-ttu-id="01f72-111">이 작업에서 작성된 전체 코드 목록은 이 절차 다음에 나오는 다음 예제에 제공되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-111">A complete listing of the code written in this task is provided in the example following the procedure.</span></span>

## <a name="create-a-new-console-application-to-host-the-service"></a><span data-ttu-id="01f72-112">서비스를 호스팅할 새 콘솔 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="01f72-112">Create a new console application to host the service</span></span>

1. <span data-ttu-id="01f72-113">Getting Started 솔루션을 마우스 오른쪽 단추로 클릭 하 고 선택 하 여 Visual Studio에서 새 콘솔 응용 프로그램 프로젝트를 만듭니다 **추가** > **새 프로젝트**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-113">Create a new Console Application project in Visual Studio by right-clicking on the Getting Started solution and selecting **Add** > **New Project**.</span></span> <span data-ttu-id="01f72-114">에 **새 프로젝트 추가** 대화 상자의 왼쪽에 있는 선택에서 **Windows Desktop** 에서 범주 **Visual C#** 또는 **Visual Basic**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-114">In the **Add New Project** dialog, on the left-hand side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> <span data-ttu-id="01f72-115">선택 된 **콘솔 앱 (.NET Framework)** 템플릿을 선택한 후 프로젝트 이름을 **GettingStartedHost**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-115">Select the **Console App (.NET Framework)** template, and then name the project **GettingStartedHost**.</span></span>

2. <span data-ttu-id="01f72-116">GettingStartedLib 프로젝트에 대 한 참조를 GettingStartedHost 프로젝트에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-116">Add a reference to the GettingStartedLib project to the GettingStartedHost project.</span></span> <span data-ttu-id="01f72-117">마우스 오른쪽 단추로 클릭 합니다 **참조** GettingStartedHost 프로젝트의 폴더 **솔루션 탐색기**를 선택한 후 **참조 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-117">Right-click on the **References** folder under the GettingStartedHost project in **Solution Explorer**, and then select **Add Reference**.</span></span> <span data-ttu-id="01f72-118">에 **참조 추가** 대화 상자에서 **솔루션** 대화 상자의 왼쪽에서 대화 상자 가운데에서 GettingStartedLib를 선택 하 고 선택한 **추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-118">In the **Add Reference** dialog, select **Solution** on the left-hand side of the dialog, select GettingStartedLib in the center section of the dialog, and then choose **Add**.</span></span> <span data-ttu-id="01f72-119">이제 GettingStartedLib에 정의된 형식을 GettingStartedHost 프로젝트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-119">This makes the types defined in GettingStartedLib available to the GettingStartedHost project.</span></span>

3. <span data-ttu-id="01f72-120">System.ServiceModel에 대 한 참조를 GettingStartedHost 프로젝트에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-120">Add a reference to System.ServiceModel to the GettingStartedHost project.</span></span> <span data-ttu-id="01f72-121">마우스 오른쪽 단추로 클릭 합니다 **참조** GettingStartedHost 프로젝트의 폴더 **솔루션 탐색기** 선택한 **참조 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-121">Right-click the **References** folder under the GettingStartedHost project in **Solution Explorer** and select **Add Reference**.</span></span> <span data-ttu-id="01f72-122">에 **참조 추가** 대화 상자에서 **프레임 워크** 대화 상자의 왼쪽에서 **어셈블리**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-122">In the **Add Reference** dialog, select **Framework** on the left-hand side of the dialog under **Assemblies**.</span></span> <span data-ttu-id="01f72-123">찾기 및 선택 **System.ServiceModel**를 선택한 후 **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-123">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> <span data-ttu-id="01f72-124">선택 하 여 솔루션을 저장할 **파일** > **모두 저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-124">Save the solution by selecting **File** > **Save All**.</span></span>

## <a name="host-the-service"></a><span data-ttu-id="01f72-125">서비스 호스트</span><span class="sxs-lookup"><span data-stu-id="01f72-125">Host the service</span></span>

<span data-ttu-id="01f72-126">편집할 Program.cs 또는 Module.vb 파일을 열고 다음 코드를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-126">Open the Program.cs or Module.vb file and enter the following code:</span></span>

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

<span data-ttu-id="01f72-127">**1 단계** -서비스의 기본 주소를 보유할 Uri 클래스의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-127">**Step 1** - Creates an instance of the Uri class to hold the base address of the service.</span></span> <span data-ttu-id="01f72-128">서비스는 기본 주소와 선택적 URI를 포함하는 URL로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-128">Services are identified by a URL which contains a base address and an optional URI.</span></span> <span data-ttu-id="01f72-129">기본 주소 형식은 다음과 같습니다. [전송]://[시스템 이름 또는 도메인][:선택적 포트 번호]/[선택적 URI 세그먼트]계산기 서비스의 기본 주소는 HTTP 전송, 로컬 호스트, 포트 8000 및 URI 세그먼트 “GettingStarted”를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-129">The base address is formatted as follows:[transport]://[machine-name or domain][:optional port #]/[optional URI segment]The base address for the calculator service uses the HTTP transport, localhost, port 8000, and the URI segment "GettingStarted"</span></span>

<span data-ttu-id="01f72-130">**2 단계** –의 인스턴스를 만듭니다는 <xref:System.ServiceModel.ServiceHost> 서비스를 호스트 하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-130">**Step 2** – Creates an instance of the <xref:System.ServiceModel.ServiceHost> class to host the service.</span></span> <span data-ttu-id="01f72-131">생성자는 서비스 계약을 구현하는 클래스 형식과 서비스의 기본 주소, 두 가지 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-131">The constructor takes two parameters, the type of the class that implements the service contract, and the base address of the service.</span></span>

<span data-ttu-id="01f72-132">**3 단계** – 만듭니다는 <xref:System.ServiceModel.Description.ServiceEndpoint> 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="01f72-132">**Step 3** – Creates a <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span></span> <span data-ttu-id="01f72-133">서비스 엔드포인트는 주소, 바인딩 및 서비스 계약으로 구성되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-133">A service endpoint is composed of an address, a binding, and a service contract.</span></span> <span data-ttu-id="01f72-134">따라서 <xref:System.ServiceModel.Description.ServiceEndpoint> 생성자는 서비스 계약 인터페이스 형식, 바인딩 및 주소를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-134">The <xref:System.ServiceModel.Description.ServiceEndpoint> constructor therefore takes the service contract interface type, a binding, and an address.</span></span> <span data-ttu-id="01f72-135">서비스 계약은 사용자가 정의한 `ICalculator`이며 서비스 형식에 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-135">The service contract is `ICalculator`, which you defined and implement in the service type.</span></span> <span data-ttu-id="01f72-136">이 예제에 사용된 바인딩은 WS-\* 사양을 따르는 엔드포인트에 연결하는 데 사용되는 기본 바인딩인 <xref:System.ServiceModel.WSHttpBinding>입니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-136">The binding used in this sample is <xref:System.ServiceModel.WSHttpBinding> which is a built-in binding that is used for connecting to endpoints that conform to the WS-\* specifications.</span></span> <span data-ttu-id="01f72-137">WCF 바인딩에 대한 자세한 내용은 [WCF 바인딩 개요](bindings-overview.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01f72-137">For more information about WCF bindings, see [WCF Bindings Overview](bindings-overview.md).</span></span> <span data-ttu-id="01f72-138">엔드포인트를 식별하기 위해 주소가 기본 주소에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-138">The address is appended to the base address to identify the endpoint.</span></span> <span data-ttu-id="01f72-139">끝점에 대 한 정규화 된 주소 이므로이 코드에서 지정 된 주소는 "CalculatorService" `"http://localhost:8000/GettingStarted/CalculatorService"`합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-139">The address specified in this code is "CalculatorService" so the fully qualified address for the endpoint is `"http://localhost:8000/GettingStarted/CalculatorService"`.</span></span>

    > [!IMPORTANT]
    > Adding a service endpoint is optional when using .NET Framework 4 or later. In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service. For more information about default endpoints see [Specifying an Endpoint Address](specifying-an-endpoint-address.md). For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](simplified-configuration.md) and [Simplified Configuration for WCF Services](./samples/simplified-configuration-for-wcf-services.md).

<span data-ttu-id="01f72-140">**4 단계** – 메타 데이터 교환을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-140">**Step 4** – Enable metadata exchange.</span></span> <span data-ttu-id="01f72-141">클라이언트는 메타데이터 교환을 사용하여 서비스 작업을 호출하는 데 사용되는 프록시를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-141">Clients will use metadata exchange to generate proxies that will be used to call the service operations.</span></span> <span data-ttu-id="01f72-142">메타데이터 교환을 활성화하려면 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 인스턴스를 만들고 해당 <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> 속성을 `true`로 설정한 다음 동작을 <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> 인스턴스의 <xref:System.ServiceModel.ServiceHost> 컬렉션에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-142">To enable metadata exchange create a <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, set it’s <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> property to `true`, and add the behavior to the <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection of the <xref:System.ServiceModel.ServiceHost> instance.</span></span>

<span data-ttu-id="01f72-143">**5 단계** Open –는 <xref:System.ServiceModel.ServiceHost> 들어오는 메시지를 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-143">**Step 5** – Open the <xref:System.ServiceModel.ServiceHost> to listen for incoming messages.</span></span> <span data-ttu-id="01f72-144">코드는 사용자가 Enter를 누를 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-144">Notice the code waits for the user to hit enter.</span></span> <span data-ttu-id="01f72-145">이를 수행하지 않으면 응용 프로그램이 즉시 닫히고 서비스가 종료합니다. 또한 사용된 try/catch 블록도 주의하십시오.</span><span class="sxs-lookup"><span data-stu-id="01f72-145">If you do not do this, the app will close immediately and the service will shut down.Also notice a  try/catch block used.</span></span> <span data-ttu-id="01f72-146"><xref:System.ServiceModel.ServiceHost>를 인스턴스화한 후에는 나머지 코드가 try/catch 블록에 배치됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-146">After the <xref:System.ServiceModel.ServiceHost> has been instantiated, all other code is placed in a try/catch block.</span></span> <span data-ttu-id="01f72-147">안전 하 게에서 throw 된 예외를 catch 하는 방법에 대 한 자세한 내용은 <xref:System.ServiceModel.ServiceHost>를 참조 하세요 [사용 하 여 닫기 및 중단 WCF 클라이언트 리소스를 해제 하려면](samples/use-close-abort-release-wcf-client-resources.md)</span><span class="sxs-lookup"><span data-stu-id="01f72-147">For more information about safely catching exceptions thrown by <xref:System.ServiceModel.ServiceHost>, see [Use Close and Abort to release WCF client resources](samples/use-close-abort-release-wcf-client-resources.md)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01f72-148">코드에서 변경한 내용을 반영 하도록 GettingStartedLib에서 App.config를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-148">Edit App.config in GettingStartedLib to reflect the changes made in code:</span></span>
> 1. <span data-ttu-id="01f72-149">줄 14를 변경 합니다. `<service name="GettingStartedLib.CalculatorService">`</span><span class="sxs-lookup"><span data-stu-id="01f72-149">Change line 14 to `<service name="GettingStartedLib.CalculatorService">`</span></span>
> 2. <span data-ttu-id="01f72-150">줄 17을 변경 합니다. `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span><span class="sxs-lookup"><span data-stu-id="01f72-150">Change line 17 to `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span></span>
> 3. <span data-ttu-id="01f72-151">22 줄을 변경 합니다. `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span><span class="sxs-lookup"><span data-stu-id="01f72-151">Change line 22 to `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span></span>

## <a name="verify-the-service-is-working"></a><span data-ttu-id="01f72-152">서비스가 작동 확인</span><span class="sxs-lookup"><span data-stu-id="01f72-152">Verify the service is working</span></span>

1. <span data-ttu-id="01f72-153">GettingStartedHost 콘솔 실행 Visual Studio 내부에서 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-153">Run the GettingStartedHost console application from inside Visual Studio.</span></span>

   <span data-ttu-id="01f72-154">서비스는 관리자 권한으로 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-154">The service must be run with administrator privileges.</span></span> <span data-ttu-id="01f72-155">관리자 권한으로 Visual Studio를 열었으므로 GettingStartedHost도 관리자 권한으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-155">Because Visual Studio was opened with administrator privileges, GettingStartedHost is also run with administrator privileges.</span></span> <span data-ttu-id="01f72-156">사용 하 여 새 명령 프롬프트를 열 수도 있습니다 **관리자 권한으로 실행** 내에서 service.exe를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-156">You can also open a new command prompt using **Run as administrator** and run service.exe within it.</span></span>

2. <span data-ttu-id="01f72-157">웹 브라우저를 열고 서비스의 디버그 페이지인 `http://localhost:8000/GettingStarted/CalculatorService`합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-157">Open a web browser and browse to the service's debug page at `http://localhost:8000/GettingStarted/CalculatorService`.</span></span>

## <a name="example"></a><span data-ttu-id="01f72-158">예제</span><span class="sxs-lookup"><span data-stu-id="01f72-158">Example</span></span>

<span data-ttu-id="01f72-159">다음 예제에는 자습서의 이전 단계의 서비스 계약과 구현이 포함되어 있으며 콘솔 응용 프로그램에서 서비스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-159">The following example includes the service contract and implementation from previous steps in the tutorial and hosts the service in a console application.</span></span>

<span data-ttu-id="01f72-160">이 명령줄 컴파일러로 컴파일하려면 IService1.cs 및 컴파일합니다 Service1.cs 참조 하는 클래스 라이브러리로 `System.ServiceModel.dll`합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-160">To compile this with a command-line compiler, compile IService1.cs and Service1.cs into a class library that references `System.ServiceModel.dll`.</span></span> <span data-ttu-id="01f72-161">Program.cs를 콘솔 응용 프로그램으로 컴파일하십시오.</span><span class="sxs-lookup"><span data-stu-id="01f72-161">Compile Program.cs as a console application.</span></span>

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
> <span data-ttu-id="01f72-162">이러한 서비스에는 수신 대기를 위해 시스템에 HTTP 주소를 등록할 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-162">Services such as this one require permission to register HTTP addresses on the machine for listening.</span></span> <span data-ttu-id="01f72-163">관리자 계정에는 이 권한이 있지만, 관리자 이외의 계정에는 HTTP 네임스페이스에 대한 권한을 부여해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-163">Administrator accounts have this permission, but non-administrator accounts must be granted permission for HTTP namespaces.</span></span> <span data-ttu-id="01f72-164">네임스페이스 예약을 구성하는 방법에 대한 자세한 내용은 [HTTP 및 HTTPS 구성](feature-details/configuring-http-and-https.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01f72-164">For more information about how to configure namespace reservations, see [Configuring HTTP and HTTPS](feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="01f72-165">Visual Studio에서 실행하는 경우 service.exe는 관리자 권한으로 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-165">When running under Visual Studio, the service.exe must be run with administrator privileges.</span></span>

## <a name="next-steps"></a><span data-ttu-id="01f72-166">다음 단계</span><span class="sxs-lookup"><span data-stu-id="01f72-166">Next steps</span></span>

<span data-ttu-id="01f72-167">서비스가 실행되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-167">Now the service is running.</span></span> <span data-ttu-id="01f72-168">다음 태스크에서는 WCF 클라이언트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f72-168">In the next task, you create a WCF client.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="01f72-169">방법: WCF 클라이언트 만들기</span><span class="sxs-lookup"><span data-stu-id="01f72-169">How to: Create a WCF client</span></span>](how-to-create-a-wcf-client.md)

<span data-ttu-id="01f72-170">문제 해결 정보는 [초보자를 위한 자습서 문제 해결](troubleshooting-the-getting-started-tutorial.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01f72-170">For troubleshooting information, see [Troubleshooting the Getting Started Tutorial](troubleshooting-the-getting-started-tutorial.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="01f72-171">참고 항목</span><span class="sxs-lookup"><span data-stu-id="01f72-171">See also</span></span>

- [<span data-ttu-id="01f72-172">시작</span><span class="sxs-lookup"><span data-stu-id="01f72-172">Getting Started</span></span>](samples/getting-started-sample.md)
- [<span data-ttu-id="01f72-173">자체 호스팅</span><span class="sxs-lookup"><span data-stu-id="01f72-173">Self-Host</span></span>](samples/self-host.md)