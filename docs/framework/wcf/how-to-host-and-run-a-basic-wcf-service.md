---
title: '방법: 기본 Windows Communication Foundation 서비스 호스트 및 실행'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF services [WCF]
- WCF services [WCF], running
ms.assetid: 31774d36-923b-4e2d-812e-aa190127266f
ms.openlocfilehash: e2bf16bd07c7ac9d918a4ae95d7f4aa185d436ec
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43741161"
---
# <a name="how-to-host-and-run-a-basic-windows-communication-foundation-service"></a><span data-ttu-id="d3327-102">방법: 기본 Windows Communication Foundation 서비스 호스트 및 실행</span><span class="sxs-lookup"><span data-stu-id="d3327-102">How to: Host and Run a Basic Windows Communication Foundation Service</span></span>
<span data-ttu-id="d3327-103">WCF(Windows Communication Foundation) 응용 프로그램을 만드는 데 필요한 6가지 작업 중 세 번째 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-103">This is the third of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="d3327-104">6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>  
  
 <span data-ttu-id="d3327-105">이 항목에서는 콘솔 응용 프로그램에서 WCF(Windows Communication Foundation) 서비스를 호스팅하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-105">This topic describes how to host a Windows Communication Foundation (WCF) service in a console application.</span></span> <span data-ttu-id="d3327-106">이 절차는 다음 단계로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-106">This procedure consists of the following steps:</span></span>  
  
-   <span data-ttu-id="d3327-107">서비스를 호스팅할 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-107">Create a console application project to host the service.</span></span>  
  
-   <span data-ttu-id="d3327-108">서비스에 대한 서비스 호스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-108">Create a service host for the service.</span></span>  
  
-   <span data-ttu-id="d3327-109">메타데이터 교환을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-109">Enable metadata exchange.</span></span>  
  
-   <span data-ttu-id="d3327-110">서비스 호스트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-110">Open the service host.</span></span>  
  
 <span data-ttu-id="d3327-111">이 작업에서 작성된 전체 코드 목록은 이 절차 다음에 나오는 다음 예제에 제공되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-111">A complete listing of the code written in this task is provided in the example following the procedure.</span></span>  
  
## <a name="to-create-a-new-console-application-to-host-the-service"></a><span data-ttu-id="d3327-112">서비스를 호스팅할 새 콘솔 응용 프로그램을 만들려면</span><span class="sxs-lookup"><span data-stu-id="d3327-112">To create a new console application to host the service</span></span>  
  
1.  <span data-ttu-id="d3327-113">Getting Started 솔루션을 마우스 오른쪽 단추로 클릭하고 **추가**, **새 프로젝트**를 차례로 선택하여 새 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-113">Create a new Console Application project by right-clicking on the Getting Started solution, selecting, **Add**, **New Project**.</span></span> <span data-ttu-id="d3327-114">대화 상자의 왼쪽에 있는 **새 프로젝트 추가** 대화 상자에서 **C#** 또는 **VB** 아래의 **Windows**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-114">In the **Add New Project** dialog on the left hand side of the dialog select **Windows** under **C#** or **VB**.</span></span> <span data-ttu-id="d3327-115">대화 상자 가운데에서 **콘솔 응용 프로그램**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-115">In the center section of the dialog select **Console Application**.</span></span> <span data-ttu-id="d3327-116">프로젝트 이름으로 GettingStartedHost를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-116">Name the project GettingStartedHost.</span></span>  
  
2.  <span data-ttu-id="d3327-117">솔루션 탐색기에서 **GettingStartedHost**를 마우스 오른쪽 단추로 클릭한 다음, **속성**을 선택하여 GettingStartedHost 프로젝트의 대상 프레임워크로 .NET Framework 4.5를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-117">Set the target framework of the GettingStartedHost project to .NET Framework 4.5 by right clicking on **GettingStartedHost** in the Solution Explorer and selecting **Properties**.</span></span> <span data-ttu-id="d3327-118">**대상 프레임워크** 드롭다운 목록에서 **.NET Framework 4.5**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-118">In the dropdown box labeled **Target Framework** select **.NET Framework 4.5**.</span></span> <span data-ttu-id="d3327-119">VB 프로젝트의 대상 프레임워크를 설정하는 방법은 약간 다릅니다. GettingStartedHost 프로젝트 속성 대화 상자에서 화면 왼쪽의 **컴파일** 탭을 클릭한 다음, 대화 상자의 왼쪽 아래 모퉁이에 있는 **고급 컴파일 옵션** 단추를 클릭하십시오.</span><span class="sxs-lookup"><span data-stu-id="d3327-119">Setting the target framework for a VB project is a little different, in the GettingStartedHost project properties dialog, click the **Compile** tab on the left-hand side of the screen, and then click the **Advanced Compile Options** button at the lower left-hand corner of the dialog.</span></span> <span data-ttu-id="d3327-120">그런 다음, **대상 프레임워크** 드롭다운 상자에서 **.NET Framework 4.5**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-120">Then select **.NET Framework 4.5** in the dropdown box labeled **Target Framework**.</span></span>  
  
     <span data-ttu-id="d3327-121">대상 프레임워크를 설정하면 [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)]에서 솔루션을 다시 로드합니다. 메시지가 나타나면 **확인**을 누르세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-121">Setting the target framework will cause [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] to reload the solution, press **OK** when prompted.</span></span>  
  
3.  <span data-ttu-id="d3327-122">솔루션 탐색기에서 GettingStartedHost 프로젝트의 **References** 폴더를 마우스 오른쪽 단추로 클릭하여 GettingStartedLib 프로젝트에 대한 참조를 GettingStartedHost 프로젝트에 추가하고 **참조 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-122">Add a reference to the GettingStartedLib project to the GettingStartedHost project by right clicking on the **References** folder under the GettingStartedHost project in the solution explorer and select **Add Reference**.</span></span> <span data-ttu-id="d3327-123">**참조 추가** 대화 상자에서 대화 상자의 왼쪽에 있는 **솔루션**을 선택하고 대화 상자 가운데에서 GettingStartedLib를 선택하고 **추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-123">In the **Add Reference** dialog, select **Solution** on the left-hand side of the dialog and select GettingStartedLib in the center section of the dialog and click **Add**.</span></span> <span data-ttu-id="d3327-124">이제 GettingStartedLib에 정의된 형식을 GettingStartedHost 프로젝트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-124">This makes the types defined in GettingStartedLib available to the GettingStartedHost project.</span></span>  
  
4.  <span data-ttu-id="d3327-125">솔루션 탐색기에서 GettingStartedHost 프로젝트의 **Reference** 폴더를 마우스 오른쪽 단추로 클릭하여 System.ServiceModel에 대한 참조를 GettingStartedHost에 추가하고 **참조 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-125">Add a reference to System.ServiceModel to the GettingStartedHost project by right-clicking the **Reference** folder under the GettingStartedHost project in Solution Explorer and select **Add** Reference.</span></span> <span data-ttu-id="d3327-126">**참조 추가** 대화 상자에서 대화 상자 왼쪽의 **프레임워크**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-126">In the **Add Reference** dialog select **Framework** on the left-hand side of the dialog.</span></span> <span data-ttu-id="d3327-127">검색 어셈블리 텍스트 상자에 `System.ServiceModel`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-127">In the Search Assemblies textbox, type in `System.ServiceModel`.</span></span> <span data-ttu-id="d3327-128">대화 상자 가운데에서 **System.ServiceModel**을 선택하고 **추가** 단추를 클릭한 다음, **닫기** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-128">In the center section of the dialog select **System.ServiceModel**, click the **Add** button, and click the **Close** button.</span></span> <span data-ttu-id="d3327-129">주 메뉴에서 모두 저장 단추를 클릭하여 솔루션을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-129">Save the solution by clicking the Save All button below the main menu.</span></span>  
  
### <a name="to-host-the-service"></a><span data-ttu-id="d3327-130">서비스를 호스트하려면</span><span class="sxs-lookup"><span data-stu-id="d3327-130">To host the service</span></span>  
  
-   <span data-ttu-id="d3327-131">편집할 Program.cs 또는 Module.vb 파일을 열고 다음 코드를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-131">Open the Program.cs or Module.vb file and enter the following code:</span></span>  
  
    ```csharp
    // program.cs  
    using System;  
    using System.Collections.Generic;  
    using System.Linq;  
    using System.Text;  
    using System.ServiceModel;  
    using GettingStartedLib;  
    using System.ServiceModel.Description;   
  
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
    'Module1.vb  
    Imports System  
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
  
    1.  <span data-ttu-id="d3327-132">1단계 - 서비스의 기본 주소를 보유할 URI 클래스의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-132">Step 1 - Creates an instance of the Uri class to hold the base address of the service.</span></span> <span data-ttu-id="d3327-133">서비스는 기본 주소와 선택적 URI를 포함하는 URL로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-133">Services are identified by a URL which contains a base address and an optional URI.</span></span> <span data-ttu-id="d3327-134">기본 주소 형식은 다음과 같습니다. [전송]://[시스템 이름 또는 도메인][:선택적 포트 번호]/[선택적 URI 세그먼트]계산기 서비스의 기본 주소는 HTTP 전송, 로컬 호스트, 포트 8000 및 URI 세그먼트 “GettingStarted”를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-134">The base address is formatted as follows:[transport]://[machine-name or domain][:optional port #]/[optional URI segment]The base address for the calculator service uses the HTTP transport, localhost, port 8000, and the URI segment "GettingStarted"</span></span>  
  
    2.  <span data-ttu-id="d3327-135">2단계 - 서비스를 호스팅할 <xref:System.ServiceModel.ServiceHost> 클래스의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-135">Step 2 – Creates an instance of the <xref:System.ServiceModel.ServiceHost> class to host the service.</span></span> <span data-ttu-id="d3327-136">생성자는 서비스 계약을 구현하는 클래스 형식과 서비스의 기본 주소, 두 가지 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-136">The constructor takes two parameters, the type of the class that implements the service contract, and the base address of the service.</span></span>  
  
    3.  <span data-ttu-id="d3327-137">3단계 - 새 <xref:System.ServiceModel.Description.ServiceEndpoint> 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-137">Step 3 – Creates a <xref:System.ServiceModel.Description.ServiceEndpoint> instance.</span></span> <span data-ttu-id="d3327-138">서비스 엔드포인트는 주소, 바인딩 및 서비스 계약으로 구성되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-138">A service endpoint is composed of an address, a binding, and a service contract.</span></span> <span data-ttu-id="d3327-139">따라서 <xref:System.ServiceModel.Description.ServiceEndpoint> 생성자는 서비스 계약 인터페이스 형식, 바인딩 및 주소를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-139">The <xref:System.ServiceModel.Description.ServiceEndpoint> constructor therefore takes the service contract interface type, a binding, and an address.</span></span> <span data-ttu-id="d3327-140">서비스 계약은 사용자가 정의한 `ICalculator`이며 서비스 형식에 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-140">The service contract is `ICalculator`, which you defined and implement in the service type.</span></span> <span data-ttu-id="d3327-141">이 예제에 사용된 바인딩은 WS-\* 사양을 따르는 엔드포인트에 연결하는 데 사용되는 기본 바인딩인 <xref:System.ServiceModel.WSHttpBinding>입니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-141">The binding used in this sample is <xref:System.ServiceModel.WSHttpBinding> which is a built-in binding that is used for connecting to endpoints that conform to the WS-\* specifications.</span></span> <span data-ttu-id="d3327-142">WCF 바인딩에 대한 자세한 내용은 [WCF 바인딩 개요](../../../docs/framework/wcf/bindings-overview.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-142">For more information about WCF bindings, see [WCF Bindings Overview](../../../docs/framework/wcf/bindings-overview.md).</span></span> <span data-ttu-id="d3327-143">엔드포인트를 식별하기 위해 주소가 기본 주소에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-143">The address is appended to the base address to identify the endpoint.</span></span> <span data-ttu-id="d3327-144">끝점에 대 한 정규화 된 주소 이므로이 코드에서 지정 된 주소는 "CalculatorService" `"http://localhost:8000/GettingStarted/CalculatorService"`합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-144">The address specified in this code is "CalculatorService" so the fully qualified address for the endpoint is `"http://localhost:8000/GettingStarted/CalculatorService"`.</span></span>  
  
        > [!IMPORTANT]
        >  <span data-ttu-id="d3327-145">.NET Framework 4 이상을 사용할 때 서비스 엔드포인트 추가는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-145">Adding a service endpoint is optional when using .NET Framework 4 or later.</span></span> <span data-ttu-id="d3327-146">이러한 버전에서 코드 또는 구성에 엔드포인트가 추가되지 않으면 WCF가 기본 주소의 각 결합에 기본 엔드포인트 하나씩을 추가하고 서비스에서 구현한 계약을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-146">In these versions, if no endpoints are added in code or configuration, WCF adds one default endpoint for each combination of base address and contract implemented by the service.</span></span> <span data-ttu-id="d3327-147">기본 엔드포인트에 대한 자세한 내용은 [엔드포인트 주소 지정](../../../docs/framework/wcf/specifying-an-endpoint-address.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-147">For more information about default endpoints see [Specifying an Endpoint Address](../../../docs/framework/wcf/specifying-an-endpoint-address.md).</span></span> <span data-ttu-id="d3327-148">기본 엔드포인트, 바인딩 및 동작에 대한 자세한 내용은 [단순화된 구성](../../../docs/framework/wcf/simplified-configuration.md) 및 [WCF 서비스를 위한 단순화된 구성](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-148">For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
    4.  <span data-ttu-id="d3327-149">4단계 - 메타데이터 교환을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-149">Step 4 – Enable metadata exchange.</span></span> <span data-ttu-id="d3327-150">클라이언트는 메타데이터 교환을 사용하여 서비스 작업을 호출하는 데 사용되는 프록시를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-150">Clients will use metadata exchange to generate proxies that will be used to call the service operations.</span></span> <span data-ttu-id="d3327-151">메타데이터 교환을 활성화하려면 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 인스턴스를 만들고 해당 <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> 속성을 `true`로 설정한 다음, 동작을 <xref:System.ServiceModel.ServiceHost> 인스턴스의 <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` 컬렉션에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-151">To enable metadata exchange create a <xref:System.ServiceModel.Description.ServiceMetadataBehavior> instance, set it’s <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> property to `true`, and add the behavior to the <!--zz <xref:System.ServiceModel.ServiceHost.Behaviors%2A>  -->`System.ServiceModel.ServiceHost.Behaviors%2A` collection of the <xref:System.ServiceModel.ServiceHost> instance.</span></span>  
  
    5.  <span data-ttu-id="d3327-152">5단계 - <xref:System.ServiceModel.ServiceHost>를 열어 들어오는 메시지를 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-152">Step 5 – Open the <xref:System.ServiceModel.ServiceHost> to listen for incoming messages.</span></span> <span data-ttu-id="d3327-153">코드는 사용자가 Enter를 누를 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-153">Notice the code waits for the user to hit enter.</span></span> <span data-ttu-id="d3327-154">이를 수행하지 않으면 응용 프로그램이 즉시 닫히고 서비스가 종료합니다. 또한 사용된 try/catch 블록도 주의하십시오.</span><span class="sxs-lookup"><span data-stu-id="d3327-154">If you do not do this, the app will close immediately and the service will shut down.Also notice a  try/catch block used.</span></span> <span data-ttu-id="d3327-155"><xref:System.ServiceModel.ServiceHost>를 인스턴스화한 후에는 나머지 코드가 try/catch 블록에 배치됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-155">After the <xref:System.ServiceModel.ServiceHost> has been instantiated, all other code is placed in a try/catch block.</span></span> <span data-ttu-id="d3327-156"><xref:System.ServiceModel.ServiceHost>에서 throw된 예외를 안전하게 catch하는 방법에 대한 자세한 내용은 [Using 문 사용 시 문제 회피](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-156">For more information about safely catching exceptions thrown by <xref:System.ServiceModel.ServiceHost>, see [Avoiding Problems with the Using Statement](../../../docs/framework/wcf/samples/avoiding-problems-with-the-using-statement.md)</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="d3327-157">코드에서 변경한 내용을 반영 하도록 GettingStartedLib에서 App.config를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-157">Edit App.config in GettingStartedLib to reflect the changes made in code:</span></span> 
> 1. <span data-ttu-id="d3327-158">줄 14를 변경 합니다. `<service name="GettingStartedLib.CalculatorService">`</span><span class="sxs-lookup"><span data-stu-id="d3327-158">Change line 14 to `<service name="GettingStartedLib.CalculatorService">`</span></span>
> 2. <span data-ttu-id="d3327-159">줄 17을 변경 합니다. `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span><span class="sxs-lookup"><span data-stu-id="d3327-159">Change line 17 to `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span></span>
> 3. <span data-ttu-id="d3327-160">22 줄을 변경 합니다. `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span><span class="sxs-lookup"><span data-stu-id="d3327-160">Change line 22 to `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span></span>
        
### <a name="to-verify-the-service-is-working"></a><span data-ttu-id="d3327-161">서비스가 작동하는지 확인하려면</span><span class="sxs-lookup"><span data-stu-id="d3327-161">To verify the service is working</span></span>  
  
1.  <span data-ttu-id="d3327-162">[!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)]에서 GettingStartedHost 콘솔 응용 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-162">Run the GettingStartedHost console application from inside [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)].</span></span> <span data-ttu-id="d3327-163">[!INCLUDE[wv](../../../includes/wv-md.md)]에서 실행하면서 나중에 운영 체제에서 실행하는 경우 서비스를 관리자 권한으로 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-163">When running on [!INCLUDE[wv](../../../includes/wv-md.md)] and later operating systems, the service must be run with administrator privileges.</span></span> <span data-ttu-id="d3327-164">Visual Studio가 관리자 권한으로 실행되었기 때문에 GettingStartedHost도 관리자 권한으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-164">Because Visual Studio was run with Administrator privileges, GettingStartedHost is also run with Administrator privileges.</span></span> <span data-ttu-id="d3327-165">또한 관리자 권한으로 서비스를 실행하는 새 명령 프롬프트를 시작하고 해당 명령 프롬프트 내에서 service.exe를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-165">You can also start a new command prompt running it with Administrator privileges and run service.exe within it.</span></span>  
  
2.  <span data-ttu-id="d3327-166">Internet Explorer를 열고 서비스의 디버그 페이지인 `http://localhost:8000/GettingStarted/CalculatorService`를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-166">Open Internet Explorer and browse to the service's debug page at `http://localhost:8000/GettingStarted/CalculatorService`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3327-167">예제</span><span class="sxs-lookup"><span data-stu-id="d3327-167">Example</span></span>  
 <span data-ttu-id="d3327-168">다음 예제에는 자습서의 이전 단계의 서비스 계약과 구현이 포함되어 있으며 콘솔 응용 프로그램에서 서비스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-168">The following example includes the service contract and implementation from previous steps in the tutorial and hosts the service in a console application.</span></span>  
  
 <span data-ttu-id="d3327-169">이를 명령줄 컴파일러로 컴파일하려면 IService1.cs 및 Service1.cs를 `System.ServiceModel.dll`을 참조하는 클래스 라이브러리로 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-169">To compile this with a command-line compiler, compile IService1.cs and Service1.cs into a class library referencing `System.ServiceModel.dll`.</span></span> <span data-ttu-id="d3327-170">그리고 Program.cs를 콘솔 응용 프로그램으로 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-170">And compile Program.cs to a console application.</span></span>  
  
```csharp
// IService1.cs  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Runtime.Serialization;  
using System.ServiceModel;  
using System.Text;  
  
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
// Service1.cs  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Runtime.Serialization;  
using System.ServiceModel;  
using System.Text;  
  
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
//Program.cs  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.ServiceModel;  
using GettingStartedLib;  
using System.ServiceModel.Description;   
  
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
'IService1.vb  
Imports System  
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
'Service1.vb  
Imports System  
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
'Module1.vb  
Imports System  
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
>  <span data-ttu-id="d3327-171">이러한 서비스에는 수신 대기를 위해 시스템에 HTTP 주소를 등록할 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-171">Services such as this one require permission to register HTTP addresses on the machine for listening.</span></span> <span data-ttu-id="d3327-172">관리자 계정에는 이 권한이 있지만, 관리자 이외의 계정에는 HTTP 네임스페이스에 대한 권한을 부여해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-172">Administrator accounts have this permission, but non-administrator accounts must be granted permission for HTTP namespaces.</span></span> <span data-ttu-id="d3327-173">네임스페이스 예약을 구성하는 방법에 대한 자세한 내용은 [HTTP 및 HTTPS 구성](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-173">For more information about how to configure namespace reservations, see [Configuring HTTP and HTTPS](../../../docs/framework/wcf/feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="d3327-174">Visual Studio에서 실행하는 경우 service.exe는 관리자 권한으로 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-174">When running under Visual Studio, the service.exe must be run with administrator privileges.</span></span>  
  
 <span data-ttu-id="d3327-175">서비스가 실행되고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-175">Now the service is running.</span></span> <span data-ttu-id="d3327-176">[방법: 클라이언트 만들기](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)를 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="d3327-176">Proceed to [How to: Create a Client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span></span> <span data-ttu-id="d3327-177">문제 해결 정보는 [초보자를 위한 자습서 문제 해결](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d3327-177">For troubleshooting information, see [Troubleshooting the Getting Started Tutorial](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3327-178">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d3327-178">See Also</span></span>  
 [<span data-ttu-id="d3327-179">시작</span><span class="sxs-lookup"><span data-stu-id="d3327-179">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)  
 [<span data-ttu-id="d3327-180">자체 호스팅</span><span class="sxs-lookup"><span data-stu-id="d3327-180">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)
