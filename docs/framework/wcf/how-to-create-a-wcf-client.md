---
title: '방법: Windows Communication Foundation 클라이언트 만들기'
ms.date: 09/14/2018
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 1eadb5008575a1a53d685db14d68e42d0dce1360
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47197528"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a><span data-ttu-id="e57ab-102">방법: Windows Communication Foundation 클라이언트 만들기</span><span class="sxs-lookup"><span data-stu-id="e57ab-102">How to: Create a Windows Communication Foundation Client</span></span>

<span data-ttu-id="e57ab-103">Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 네 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-103">This is the fourth of six tasks required to create a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="e57ab-104">6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e57ab-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="e57ab-105">이 항목에서는 WCF 서비스에서 메타 데이터를 검색 하 고 서비스에 액세스할 수 있는 WCF 프록시를 만드는 데 사용 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-105">This topic describes how to retrieve metadata from a WCF service and use it to create a WCF proxy that can access the service.</span></span> <span data-ttu-id="e57ab-106">사용 하 여이 작업을 완료 합니다 **서비스 참조 추가** Visual Studio에서 제공 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-106">This task is completed by using the **Add Service Reference** functionality provided by Visual Studio.</span></span> <span data-ttu-id="e57ab-107">이 도구는 서비스의 MEX 엔드포인트에서 메타데이터를 가져와 사용자가 선택한 언어를 사용하여 클라이언트 프록시에 대한 관리되는 소스 코드 파일을 생성합니다(기본적으로 C#).</span><span class="sxs-lookup"><span data-stu-id="e57ab-107">This tool obtains the metadata from the service’s MEX endpoint and generates a managed source code file for a client proxy in the language you have chosen (C# by default).</span></span> <span data-ttu-id="e57ab-108">클라이언트 프록시를 만드는 것 이외에 해당 도구는 클라이언트에 대한 구성 파일도 만들거나 업데이트합니다. 이 구성 파일을 사용하여 클라이언트 응용 프로그램에서 해당 엔드포인트 중 하나의 서비스에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-108">In addition to creating the client proxy, the tool also creates or updates the client configuration file which enables the client application to connect to the service at one of its endpoints.</span></span>

> [!NOTE]
> <span data-ttu-id="e57ab-109">사용할 수도 있습니다는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 도구를 사용 하는 대신 구성과 프록시 클래스 생성 **서비스 참조 추가** Visual Studio에서.</span><span class="sxs-lookup"><span data-stu-id="e57ab-109">You can also use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool to generate the proxy class and configuration instead of using **Add Service Reference** in Visual Studio.</span></span>

> [!NOTE]
> <span data-ttu-id="e57ab-110">Visual Studio에서 클래스 라이브러리 프로젝트에서 WCF 서비스를 호출할 때 사용할 수는 **서비스 참조 추가** 프록시 및 관련된 구성 파일을 자동으로 생성 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-110">When calling a WCF service from a class library project in Visual Studio, you can use the **Add Service Reference** feature to automatically generate a proxy and associated configuration file.</span></span> <span data-ttu-id="e57ab-111">이 구성 파일은 클래스 라이브러리 프로젝트에서는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-111">The configuration file will not be used by the class library project.</span></span> <span data-ttu-id="e57ab-112">클래스 라이브러리를 호출 하는 실행 파일에 대 한 app.config 파일에 생성된 된 구성 파일에 설정을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-112">You need to add the settings in the generated configuration file to the app.config file for the executable that calls the class library.</span></span>

<span data-ttu-id="e57ab-113">클라이언트 응용 프로그램은 생성된 프록시 클래스를 사용하여 서비스와 통신합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-113">The client application uses the generated proxy class to communicate with the service.</span></span> <span data-ttu-id="e57ab-114">이 절차에 설명 되어 [방법: 클라이언트를 사용 하 여](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-114">This procedure is described in [How to: Use a Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span></span>

## <a name="to-create-a-windows-communication-foundation-client"></a><span data-ttu-id="e57ab-115">Windows Communication Foundation 클라이언트를 만들려면</span><span class="sxs-lookup"><span data-stu-id="e57ab-115">To create a Windows Communication Foundation client</span></span>

1. <span data-ttu-id="e57ab-116">Visual Studio에서 새 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-116">Create a new console application project in Visual Studio.</span></span> <span data-ttu-id="e57ab-117">Getting Started 솔루션을 마우스 오른쪽 단추로 클릭 **솔루션 탐색기** 선택한 **추가** > **새 프로젝트**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-117">Right-click on the Getting Started solution in **Solution Explorer** and select **Add** > **New Project**.</span></span> <span data-ttu-id="e57ab-118">에 **새 프로젝트 추가** 대화 상자의 왼쪽에 있는 선택에서 **Windows Desktop** 에서 범주 **Visual C#** 또는 **Visual Basic**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-118">In the **Add New Project** dialog, on the left-hand side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> <span data-ttu-id="e57ab-119">선택 된 **콘솔 앱 (.NET Framework)** 템플릿을 선택한 후 프로젝트 이름을 **GettingStartedClient**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-119">Select the **Console App (.NET Framework)** template, and then name the project **GettingStartedClient**.</span></span>

2. <span data-ttu-id="e57ab-120">GettingStartedClient 프로젝트에 System.ServiceModel에 대 한 참조를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-120">Add a reference to System.ServiceModel to the GettingStartedClient project.</span></span> <span data-ttu-id="e57ab-121">마우스 오른쪽 단추로 클릭 합니다 **참조** GettingStartedClient 프로젝트에서 폴더 **솔루션 탐색기**를 선택한 후 **참조 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-121">Right-click on the **References** folder under the GettingStartedClient project in **Solution Explorer**, and then select **Add Reference**.</span></span> <span data-ttu-id="e57ab-122">에 **참조 추가** 대화 상자에서 **프레임 워크** 대화 상자의 왼쪽에서 **어셈블리**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-122">In the **Add Reference** dialog, select **Framework** on the left-hand side of the dialog under **Assemblies**.</span></span> <span data-ttu-id="e57ab-123">찾기 및 선택 **System.ServiceModel**를 선택한 후 **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-123">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> <span data-ttu-id="e57ab-124">선택 하 여 솔루션을 저장할 **파일** > **모두 저장**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-124">Save the solution by selecting **File** > **Save All**.</span></span>

3. <span data-ttu-id="e57ab-125">계산기 서비스에 대 한 서비스 참조를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-125">Add a service reference to the Calculator Service.</span></span>

   1. <span data-ttu-id="e57ab-126">먼저 GettingStartedHost 콘솔 응용 프로그램을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-126">First, start up the GettingStartedHost console application.</span></span>

   2. <span data-ttu-id="e57ab-127">호스트가 실행 되 면 마우스 오른쪽 단추로 클릭 합니다 **참조** 폴더에서 GettingStartedClient 프로젝트 아래의 **솔루션 탐색기** 선택한 **추가**  >   **서비스 참조**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-127">Once the host is running, right-click the **References** folder under the GettingStartedClient project in **Solution Explorer** and select **Add** > **Service Reference**.</span></span>

   3. <span data-ttu-id="e57ab-128">주소 상자에 다음 URL을 입력 합니다 **서비스 참조 추가** 대화 상자: [http://localhost:8000/GettingStartedClient/Service](http://localhost:8000/GettingStartedClient/Service)</span><span class="sxs-lookup"><span data-stu-id="e57ab-128">Enter the following URL in the address box of the **Add Service Reference** dialog: [http://localhost:8000/GettingStartedClient/Service](http://localhost:8000/GettingStartedClient/Service)</span></span>

   4. <span data-ttu-id="e57ab-129">선택할 **이동**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-129">Choose **Go**.</span></span>

   <span data-ttu-id="e57ab-130">CalculatorService에 표시 되는 **Services** 목록 상자입니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-130">The CalculatorService is displayed in the **Services** list box.</span></span> <span data-ttu-id="e57ab-131">확장 하 고 서비스에서 구현 되는 서비스 계약을 표시 하는 CalculatorService를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-131">Double-click CalculatorService to expand it and show the service contracts implemented by the service.</span></span> <span data-ttu-id="e57ab-132">기본 네임 스페이스를 그대로-선택할 **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-132">Leave the default namespace as-is and choose **OK**.</span></span>

    <span data-ttu-id="e57ab-133">새 항목이 나타나는 Visual Studio를 사용 하는 서비스에 대 한 참조를 추가 하면 **솔루션 탐색기** 아래의 합니다 **서비스 참조** GettingStartedClient 프로젝트 아래의 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-133">When you add a reference to a service using Visual Studio, a new item appears in **Solution Explorer** under the **Service References** folder under the GettingStartedClient project.</span></span> <span data-ttu-id="e57ab-134">사용 하는 경우는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 도구, 소스 코드 파일 및 app.config 파일이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-134">If you use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool, a source code file and app.config file are generated.</span></span>

    <span data-ttu-id="e57ab-135">명령줄 도구를 사용할 수도 있습니다 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 클라이언트 코드를 만들려면 적절 한 스위치를 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-135">You can also use the command-line tool [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) with the appropriate switches to create the client code.</span></span> <span data-ttu-id="e57ab-136">다음 예제에서는 서비스에 대해 코드 파일 및 구성 파일을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-136">The following example generates a code file and a configuration file for the service.</span></span> <span data-ttu-id="e57ab-137">첫 번째 예와 VB에서 프록시를 생성 하는 방법 및 두 번째 C#에서 프록시를 생성 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-137">The first example shows how to generate the proxy in VB, and the second shows how to generate the proxy in C#:</span></span>

    ```shell
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

    ```shell
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

## <a name="next-steps"></a><span data-ttu-id="e57ab-138">다음 단계</span><span class="sxs-lookup"><span data-stu-id="e57ab-138">Next steps</span></span>

<span data-ttu-id="e57ab-139">클라이언트 응용 프로그램은 계산기 서비스를 호출 하는 데 사용할 수 있는 프록시를 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-139">You've created the proxy that the client application will use to call the calculator service.</span></span> <span data-ttu-id="e57ab-140">시리즈의 다음 항목으로 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e57ab-140">Proceed to the next topic in the series.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e57ab-141">방법: 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="e57ab-141">How to: Configure a Client</span></span>](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a><span data-ttu-id="e57ab-142">참고자료</span><span class="sxs-lookup"><span data-stu-id="e57ab-142">See also</span></span>

- [<span data-ttu-id="e57ab-143">ServiceModel Metadata 유틸리티 도구(Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="e57ab-143">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="e57ab-144">시작</span><span class="sxs-lookup"><span data-stu-id="e57ab-144">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="e57ab-145">자체 호스팅</span><span class="sxs-lookup"><span data-stu-id="e57ab-145">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)
- [<span data-ttu-id="e57ab-146">방법: 구성 파일을 사용하여 서비스의 메타데이터 게시</span><span class="sxs-lookup"><span data-stu-id="e57ab-146">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="e57ab-147">방법: Svcutil.exe를 사용하여 메타데이터 문서 다운로드</span><span class="sxs-lookup"><span data-stu-id="e57ab-147">How to: Use Svcutil.exe to Download Metadata Documents</span></span>](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
