---
title: '방법: Windows Communication Foundation 서비스 계약 정의'
ms.date: 09/14/2018
helpviewer_keywords:
- service contracts [WCF], defining
dev_langs:
- CSharp
- VB
ms.assetid: 67bf05b7-1d08-4911-83b7-a45d0b036fc3
ms.openlocfilehash: 9f7f696b1f5be2e96c50938f4627271d891deb32
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582202"
---
# <a name="how-to-define-a-windows-communication-foundation-service-contract"></a><span data-ttu-id="21140-102">방법: Windows Communication Foundation 서비스 계약 정의</span><span class="sxs-lookup"><span data-stu-id="21140-102">How to: Define a Windows Communication Foundation Service Contract</span></span>
<span data-ttu-id="21140-103">이 기본 Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 첫 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="21140-103">This is the first of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="21140-104">6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21140-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

 <span data-ttu-id="21140-105">WCF 서비스를 만들 때 첫 번째 작업은 서비스 계약 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="21140-105">When creating a WCF service, the first task is to define a service contract.</span></span> <span data-ttu-id="21140-106">서비스 계약은 서비스가 지원하는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-106">The service contract specifies what operations the service supports.</span></span> <span data-ttu-id="21140-107">작업은 웹 서비스 메서드로 간주될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-107">An operation can be thought of as a Web service method.</span></span> <span data-ttu-id="21140-108">C++, C# 또는 VB(Visual Basic) 인터페이스를 정의하여 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21140-108">Contracts are created by defining a C++, C#, or Visual Basic (VB) interface.</span></span> <span data-ttu-id="21140-109">인터페이스의 각 메서드는 특정 서비스 작업에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-109">Each method in the interface corresponds to a specific service operation.</span></span> <span data-ttu-id="21140-110">각 인터페이스에는 <xref:System.ServiceModel.ServiceContractAttribute>가 적용되어야 하고 각 작업에는 <xref:System.ServiceModel.OperationContractAttribute> 특성이 적용되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-110">Each interface must have the <xref:System.ServiceModel.ServiceContractAttribute> applied to it and each operation must have the <xref:System.ServiceModel.OperationContractAttribute> attribute applied to it.</span></span> <span data-ttu-id="21140-111"><xref:System.ServiceModel.ServiceContractAttribute> 특성을 포함하는 인터페이스 내에 있는 메서드에 <xref:System.ServiceModel.OperationContractAttribute> 특성이 없으면 서비스에 의해 해당 메서드가 노출되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-111">If a method within an interface that has the <xref:System.ServiceModel.ServiceContractAttribute> attribute does not have the <xref:System.ServiceModel.OperationContractAttribute> attribute, that method is not exposed by the service.</span></span>

 <span data-ttu-id="21140-112">이 작업에 사용되는 코드는 이 절차 다음에 나오는 예제에 제공되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-112">The code used for this task is provided in the example following the procedure.</span></span>

## <a name="define-a-service-contract"></a><span data-ttu-id="21140-113">서비스 계약 정의</span><span class="sxs-lookup"><span data-stu-id="21140-113">Define a service contract</span></span>

1. <span data-ttu-id="21140-114">프로그램을 마우스 오른쪽 단추로 클릭 하 여 관리자 권한으로 Visual Studio를 엽니다는 **시작** 메뉴에서 **자세한** > **관리자 권한으로 실행**합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-114">Open Visual Studio as an administrator by right-clicking the program in the **Start** menu and selecting **More** > **Run as administrator**.</span></span>

2. <span data-ttu-id="21140-115">WCF 서비스 라이브러리 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21140-115">Create a WCF Service Library project.</span></span>

   1. <span data-ttu-id="21140-116">**파일** 메뉴에서 **새로 만들기** > **프로젝트**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-116">From the **File** menu, select **New** > **Project**.</span></span>

   2. <span data-ttu-id="21140-117">에 **새 프로젝트** 대화 상자의 왼쪽에서 확장 **Visual C#** 또는 **Visual Basic**를 선택한 후는 **WCF** 범주입니다.</span><span class="sxs-lookup"><span data-stu-id="21140-117">In the **New Project** dialog, on the left-hand side, expand **Visual C#** or **Visual Basic**, and then select the **WCF** category.</span></span> <span data-ttu-id="21140-118">프로젝트 템플릿의 목록 대화 상자 가운데에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21140-118">A list of project templates is displayed in the center section of the dialog.</span></span> <span data-ttu-id="21140-119">선택 **WCF 서비스 라이브러리**합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-119">Select **WCF Service Library**.</span></span>

   3. <span data-ttu-id="21140-120">입력 `GettingStartedLib` 에 **이름** 텍스트 상자 및 `GettingStarted` 에서 **솔루션 이름** 대화 상자의 맨 아래에 있는 텍스트 상자에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-120">Enter `GettingStartedLib` in the **Name** textbox and `GettingStarted` in the **Solution name** textbox at the bottom of the dialog.</span></span>

   > [!NOTE]
   > <span data-ttu-id="21140-121">표시 되지 않는 경우는 **WCF** 프로젝트 템플릿 범주를 설치 해야 할 수 있습니다 합니다 **Windows Communication Foundation** Visual Studio의 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="21140-121">If you don't see the **WCF** project template category, you may need to install the **Windows Communication Foundation** component of Visual Studio.</span></span> <span data-ttu-id="21140-122">에 **새 프로젝트** 대화 상자에서 링크를 클릭 **Visual Studio 설치 관리자 열기**합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-122">In the **New Project** dialog box, click the link that says **Open Visual Studio Installer**.</span></span> <span data-ttu-id="21140-123">선택 합니다 **개별 구성 요소** 탭 한 다음 찾아서 선택 **Windows Communication Foundation** 아래 합니다 **개발 작업** 범주입니다.</span><span class="sxs-lookup"><span data-stu-id="21140-123">Select the **Individual Components** tab, and then find and select **Windows Communication Foundation** under the **Development activities** category.</span></span> <span data-ttu-id="21140-124">선택할 **수정** 구성 요소 설치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-124">Choose **Modify** to begin installing the component.</span></span>

   <span data-ttu-id="21140-125">Visual Studio는 3 개의 파일이 포함 된 프로젝트를 만듭니다: IService1.cs (또는 IService1.vb), Service1.cs (또는 Service1.vb) 및 App.config입니다. IService1 파일에는 기본 서비스 계약이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-125">Visual Studio creates the project, which contains 3 files: IService1.cs (or IService1.vb), Service1.cs (or Service1.vb), and App.config. The IService1 file contains a default service contract.</span></span> <span data-ttu-id="21140-126">Service1 파일에는 서비스 계약의 기본 구현이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-126">The Service1 file contains a default implementation of the service contract.</span></span> <span data-ttu-id="21140-127">App.config 파일에는 Visual Studio WCF 서비스 호스트가 포함된 기본 서비스를 로드하는 데 필요한 구성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-127">The App.config file contains configuration needed to load the default service with the Visual Studio WCF Service Host.</span></span> <span data-ttu-id="21140-128">WCF 서비스 호스트 도구에 대 한 자세한 내용은 참조 하세요. [WCF 서비스 호스트 (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)</span><span class="sxs-lookup"><span data-stu-id="21140-128">For more information about the WCF Service Host tool, see [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)</span></span>

3. <span data-ttu-id="21140-129">IService1.cs 또는 IService1.vb 파일을 열고 네임 스페이스 선언을 유지 하는 네임 스페이스 선언 안의 코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-129">Open the IService1.cs or IService1.vb file and delete the code within the namespace declaration, leaving the namespace declaration.</span></span> <span data-ttu-id="21140-130">다음 코드와 같이 네임스페이스 선언 내에 `ICalculator`라는 새 인터페이스를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-130">Inside the namespace declaration define a new interface called `ICalculator` as shown in the code below.</span></span>

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

     <span data-ttu-id="21140-131">이 계약은 온라인 계약을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-131">This contract defines an online calculator.</span></span> <span data-ttu-id="21140-132">`ICalculator` 인터페이스에는 <xref:System.ServiceModel.ServiceContractAttribute> 특성이 표시되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-132">Notice the `ICalculator` interface is marked with the <xref:System.ServiceModel.ServiceContractAttribute> attribute.</span></span> <span data-ttu-id="21140-133">이 특성은 계약 이름을 명확히 나타내는 데 사용하는 네임스페이스를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="21140-133">This attribute defines a namespace that is used to disambiguate the contract name.</span></span> <span data-ttu-id="21140-134">각 계산기 연산에는 <xref:System.ServiceModel.OperationContractAttribute> 특성이 표시되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21140-134">Each calculator operation is marked with the <xref:System.ServiceModel.OperationContractAttribute> attribute.</span></span>

## <a name="next-steps"></a><span data-ttu-id="21140-135">다음 단계</span><span class="sxs-lookup"><span data-stu-id="21140-135">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="21140-136">방법: 서비스 계약 구현</span><span class="sxs-lookup"><span data-stu-id="21140-136">How to: Implement a service contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

## <a name="see-also"></a><span data-ttu-id="21140-137">참고자료</span><span class="sxs-lookup"><span data-stu-id="21140-137">See also</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [<span data-ttu-id="21140-138">방법: 서비스 계약 구현</span><span class="sxs-lookup"><span data-stu-id="21140-138">How to: Implement a Service Contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [<span data-ttu-id="21140-139">시작</span><span class="sxs-lookup"><span data-stu-id="21140-139">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="21140-140">자체 호스팅</span><span class="sxs-lookup"><span data-stu-id="21140-140">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)