---
title: '방법: 기본 Windows Communication Foundation 클라이언트 구성'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 3f267edf87711de8a5969e3e0b577648008c5a75
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46323641"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a><span data-ttu-id="93b08-102">방법: 기본 Windows Communication Foundation 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="93b08-102">How to: Configure a Basic Windows Communication Foundation Client</span></span>

<span data-ttu-id="93b08-103">기본 Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 다섯 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-103">This is the fifth of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="93b08-104">6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93b08-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="93b08-105">이 항목에서는 사용 하 여 생성 된 클라이언트 구성 파일에 설명 합니다 **서비스 참조 추가** Visual Studio의 기능 또는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-105">This topic discusses the client configuration file that was generated using the **Add Service Reference** functionality of Visual Studio or the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="93b08-106">클라이언트를 구성하려면 클라이언트에서 서비스에 액세스하는 데 사용하는 엔드포인트를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-106">Configuring the client consists of specifying the endpoint that the client uses to access the service.</span></span> <span data-ttu-id="93b08-107">끝점 주소, 바인딩 및 계약에 있고 이러한 각 클라이언트를 구성 하는 동안 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-107">An endpoint has an address, a binding, and a contract, and each of these must be specified in the process of configuring the client.</span></span>

## <a name="configure-a-windows-communication-foundation-client"></a><span data-ttu-id="93b08-108">Windows Communication Foundation 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="93b08-108">Configure a Windows Communication Foundation client</span></span>

<span data-ttu-id="93b08-109">GettingStartedClient 프로젝트에서 생성된 구성 파일(App.config)을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-109">Open the generated configuration file (App.config) from the GettingStartedClient project.</span></span> <span data-ttu-id="93b08-110">다음 예제에서는 생성된 구성 파일을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-110">The following example is a view of the generated configuration file.</span></span> <span data-ttu-id="93b08-111">아래는 [ \<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) 섹션에서 찾을 합니다 [ \<끝점 >](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-111">Under the [\<system.serviceModel>](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, find the [\<endpoint>](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) element.</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
          <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5,Profile=Client" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/ServiceModelSamples/Service/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <userPrincipalName value="migree@redmond.corp.microsoft.com" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

<span data-ttu-id="93b08-112">이 예제에서는 다음 주소에 위치한 서비스에 액세스 하는 클라이언트 끝점 구성: `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-112">This example configures the endpoint that the client uses to access the service that is located at the following address: `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.</span></span>

<span data-ttu-id="93b08-113">엔드포인트 요소는 WCF 클라이언트와 서비스 사이의 통신에 `ServiceReference1.ICalculator` 서비스 계약을 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-113">The endpoint element specifies that the `ServiceReference1.ICalculator` service contract is used for communication between the WCF client and service.</span></span> <span data-ttu-id="93b08-114">WCF 채널은 시스템에서 제공한 <xref:System.ServiceModel.WSHttpBinding>을 사용하여 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-114">The WCF channel is configured with the system-provided <xref:System.ServiceModel.WSHttpBinding>.</span></span> <span data-ttu-id="93b08-115">사용 하 여 생성 된이 계약은 **서비스 참조 추가** Visual Studio에서.</span><span class="sxs-lookup"><span data-stu-id="93b08-115">This contract was generated by using **Add Service Reference** in Visual Studio.</span></span> <span data-ttu-id="93b08-116">실질적으로 GettingStartedLib 프로젝트에 정의된 계약의 사본입니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-116">It is essentially a copy of the contract that was defined in the GettingStartedLib project.</span></span> <span data-ttu-id="93b08-117"><xref:System.ServiceModel.WSHttpBinding> 바인딩은 HTTP를 전송, 상호 운용 가능한 보안 및 기타 구성 세부 사항으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-117">The <xref:System.ServiceModel.WSHttpBinding> binding specifies HTTP as the transport, interoperable security, and other configuration details.</span></span>

<span data-ttu-id="93b08-118">이 구성을 사용 하 여 생성된 된 클라이언트를 사용 하는 방법에 대 한 자세한 내용은 참조 하세요. [방법: 클라이언트를 사용 하 여](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-118">For more information about how to use the generated client with this configuration, see [How to: Use a Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="93b08-119">다음 단계</span><span class="sxs-lookup"><span data-stu-id="93b08-119">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="93b08-120">방법: WCF 클라이언트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b08-120">How to: Use a WCF client</span></span>](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

## <a name="see-also"></a><span data-ttu-id="93b08-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="93b08-121">See also</span></span>

- [<span data-ttu-id="93b08-122">바인딩을 사용하여 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="93b08-122">Using Bindings to Configure Services and Clients</span></span>](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="93b08-123">ServiceModel Metadata 유틸리티 도구(Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="93b08-123">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="93b08-124">방법: 클라이언트 만들기</span><span class="sxs-lookup"><span data-stu-id="93b08-124">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [<span data-ttu-id="93b08-125">시작</span><span class="sxs-lookup"><span data-stu-id="93b08-125">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="93b08-126">자체 호스팅</span><span class="sxs-lookup"><span data-stu-id="93b08-126">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)