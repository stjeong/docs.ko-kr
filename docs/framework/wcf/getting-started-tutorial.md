---
title: Tutorial1 시작
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], getting started
- Windows Communication Foundation [WCF], getting started
- getting started [WCF]
ms.assetid: df939177-73cb-4440-bd95-092a421516a1
ms.openlocfilehash: b7ba25795dd69e5bd978c77928f9b9797f4d4e19
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57200886"
---
# <a name="getting-started-tutorial"></a><span data-ttu-id="bb087-102">초보자를 위한 자습서</span><span class="sxs-lookup"><span data-stu-id="bb087-102">Getting Started Tutorial</span></span>
<span data-ttu-id="bb087-103">이 단원의 항목에서는 프로그래밍 환경을 Windows Communication Foundation (WCF)에 대해 간략하게 위해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-103">The topics contained in this section are intended to give you quick exposure to the Windows Communication Foundation (WCF) programming experience.</span></span> <span data-ttu-id="bb087-104">이 항목 아래쪽에 나열된 순서대로 진행하세요.</span><span class="sxs-lookup"><span data-stu-id="bb087-104">They are designed to be completed in the order of the list at the bottom of this topic.</span></span> <span data-ttu-id="bb087-105">이 자습서를 통해 WCF 서비스 및 클라이언트 응용 프로그램을 만드는 데 필요한 단계를 대략적으로 이해할을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-105">Working through this tutorial gives you an introductory understanding of the steps required to create WCF service and client applications.</span></span> <span data-ttu-id="bb087-106">서비스는 하나 이상의 엔드포인트를 노출하며 각 엔드포인트는 하나 이상의 서비스 작업을 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-106">A service exposes one or more endpoints, each of which exposes one or more service operations.</span></span> <span data-ttu-id="bb087-107">합니다 *끝점* 서비스의 서비스를 찾을 수 있는, 서비스 및 기능을 정의 하는 계약을 사용 하 여 통신 해야 하는 방법을 설명 하는 정보를 포함 하는 바인딩 주소를 지정 합니다. 클라이언트가 서비스에서 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-107">The *endpoint* of a service specifies an address where the service can be found, a binding that contains the information that describes how a client must communicate with the service, and a contract that defines the functionality provided by the service to its clients.</span></span>

 <span data-ttu-id="bb087-108">이 자습서의 항목을 순서대로 수행하면 서비스를 실행하고 클라이언트에서 서비스를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-108">After you work through the sequence of topics in this tutorial, you will have a running service, and a client that calls the service.</span></span> <span data-ttu-id="bb087-109">첫 번째 세 개 항목에서는 서비스 계약을 정의하는 방법, 서비스 계약을 구현하는 방법 및 서비스를 호스트하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-109">The first three topics describe how to define a service contract, how to implement the service contract, and how to host the service.</span></span> <span data-ttu-id="bb087-110">만들어진 서비스는 콘솔 응용 프로그램 내에서 자체 호스트됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-110">The service that is created is self-hosted within a console application.</span></span> <span data-ttu-id="bb087-111">IIS(인터넷 정보 서비스)에서 서비스를 호스트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-111">Services can also be hosted under Internet Information Services (IIS).</span></span> <span data-ttu-id="bb087-112">이 작업을 수행하는 방법에 대한 자세한 내용은 [방법: IIS에서 WCF 서비스 호스팅](../../../docs/framework/wcf/feature-details/how-to-host-a-wcf-service-in-iis.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-112">For more information about how to do this, see [How to: Host a WCF Service in IIS](../../../docs/framework/wcf/feature-details/how-to-host-a-wcf-service-in-iis.md).</span></span> <span data-ttu-id="bb087-113">서비스는 코드로 구성하지만 구성 파일 내에 서비스를 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-113">The service is configured in code; however, services can also be configured within a configuration file.</span></span> <span data-ttu-id="bb087-114">구성 파일을 사용 하는 방법에 대 한 자세한 내용은 참조 하세요. [구성 파일을 사용 하 여 서비스 구성](../../../docs/framework/wcf/configuring-services-using-configuration-files.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-114">For more information about using a configuration file see [Configuring Services Using Configuration Files](../../../docs/framework/wcf/configuring-services-using-configuration-files.md).</span></span>

 <span data-ttu-id="bb087-115">다음 세 개 항목에서는 클라이언트 프록시를 만드는 방법, 클라이언트 응용 프로그램을 구성하는 방법 및 클라이언트 프록시를 사용하여 서비스에서 노출하는 서비스 작업을 호출하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-115">The next three topics describe how to create a client proxy, configure the client application, and use the client proxy to call service operation exposed by the service.</span></span> <span data-ttu-id="bb087-116">서비스는 클라이언트 응용 프로그램이 서비스와 통신하는 데 필요한 정보를 정의하는 메타데이터를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-116">Services publish metadata that define the information a client application needs to communicate with the service.</span></span> <span data-ttu-id="bb087-117">Visual Studio 2012이 메타이 데이터에 액세스 하는 프로세스를 자동화 및 생성 하 고 서비스에 대 한 클라이언트 응용 프로그램을 구성 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-117">Visual Studio 2012 automates the process of accessing this metadata and uses it to construct and configure the client application for the service.</span></span> <span data-ttu-id="bb087-118">Visual Studio 2012를 사용 하지 않는 경우 사용할 수 있습니다 합니다 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 을 생성 및 서비스용 클라이언트 응용 프로그램을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-118">If you are not using Visual Studio 2012, you can use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to construct and configure the client application for the service.</span></span>

<span data-ttu-id="bb087-119">이 섹션의에서 항목에서는 개발 환경으로 Visual Studio를 사용 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-119">The topics in this section assume you are using Visual Studio as the development environment.</span></span> <span data-ttu-id="bb087-120">다른 개발 환경을 사용 하는 경우 Visual Studio 관련 지침을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-120">If you are using another development environment, ignore the Visual Studio-specific instructions.</span></span>

<span data-ttu-id="bb087-121">하드 디스크를 다운로드할 수 있습니다 및 실행의 항목을 참조 하는 샘플 응용 프로그램에 대 한 [Windows Communication Foundation (WCF) 샘플](./samples/index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-121">For sample applications that can be downloaded to your hard disk and run, see the topics in [Windows Communication Foundation (WCF) samples](./samples/index.md).</span></span> <span data-ttu-id="bb087-122">이 항목의 경우 특히 참조를 [Getting Started](../../../docs/framework/wcf/samples/getting-started-sample.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-122">For this topic, see, in particular, the [Getting Started](../../../docs/framework/wcf/samples/getting-started-sample.md).</span></span>

<span data-ttu-id="bb087-123">자세한 내용은 서비스 및 클라이언트 만들기에 대 한 참조 [기본 WCF 프로그래밍](../../../docs/framework/wcf/basic-wcf-programming.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-123">For more in-depth information about creating services and clients, see [Basic WCF Programming](../../../docs/framework/wcf/basic-wcf-programming.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb087-124">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="bb087-124">In This Section</span></span>
 [<span data-ttu-id="bb087-125">방법: 서비스 계약 정의</span><span class="sxs-lookup"><span data-stu-id="bb087-125">How to: Define a Service Contract</span></span>](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md)

 <span data-ttu-id="bb087-126">사용자 정의 인터페이스를 사용 하 여 WCF 계약을 만드는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-126">Describes how to create a WCF contract using a user-defined interface.</span></span> <span data-ttu-id="bb087-127">계약은 서비스에서 노출하는 기능을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-127">The contract defines the functionality exposed by the service.</span></span>

 [<span data-ttu-id="bb087-128">방법: 서비스 계약 구현</span><span class="sxs-lookup"><span data-stu-id="bb087-128">How to: Implement a Service Contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

 <span data-ttu-id="bb087-129">서비스 계약을 구현하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-129">Describes how to implement a service contract.</span></span> <span data-ttu-id="bb087-130">계약을 정의한 후에 서비스 클래스를 사용 하 여 구현 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-130">Once a contract is defined, it must be implemented with a service class.</span></span>

 [<span data-ttu-id="bb087-131">방법: 기본 서비스 호스트 및 실행</span><span class="sxs-lookup"><span data-stu-id="bb087-131">How to: Host and Run a Basic Service</span></span>](../../../docs/framework/wcf/how-to-host-and-run-a-basic-wcf-service.md)

 <span data-ttu-id="bb087-132">코드에서 서비스의 엔드포인트를 구성하는 방법 및 콘솔 응용 프로그램에서 서비스를 호스트하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-132">Describes how to configure an endpoint for the service in code and how to host the service in a console application.</span></span> <span data-ttu-id="bb087-133">서비스를 활성화하려면 런타임 환경에 구성하고 호스트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-133">To become active, a service must be configured and hosted within a run-time environment.</span></span> <span data-ttu-id="bb087-134">이 환경에서 서비스를 만들고 서비스의 컨텍스트 및 수명을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-134">This environment creates the service and controls its context and lifetime.</span></span>

 [<span data-ttu-id="bb087-135">방법: 클라이언트 만들기</span><span class="sxs-lookup"><span data-stu-id="bb087-135">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)

 <span data-ttu-id="bb087-136">WCF 서비스에서 WCF 클라이언트 프록시를 만드는 데 사용 하는 메타 데이터를 검색 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-136">Describes how to retrieve metadata used to create a WCF client proxy from a WCF service.</span></span> <span data-ttu-id="bb087-137">이 프로세스는 Visual Studio 내에서 서비스 참조 추가 기능을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-137">This process uses the Add Service Reference functionality within Visual Studio.</span></span>

 [<span data-ttu-id="bb087-138">방법: 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="bb087-138">How to: Configure a Client</span></span>](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

 <span data-ttu-id="bb087-139">WCF 클라이언트를 구성하는 방법을 설명합니다. 클라이언트를 구성하려면 클라이언트에서 서비스에 액세스하는 데 사용하는 엔드포인트를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-139">Describes how to configure a WCF client Configuring the client requires specifying the endpoint that the client uses to access the service.</span></span>

 [<span data-ttu-id="bb087-140">방법: 클라이언트 사용</span><span class="sxs-lookup"><span data-stu-id="bb087-140">How to: Use a Client</span></span>](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

 <span data-ttu-id="bb087-141">WCF 클라이언트 프록시를 사용 하 여 서비스 작업을 호출 하는 방법에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb087-141">Describes how to use the WCF client proxy to invoke service operations.</span></span>

## <a name="reference"></a><span data-ttu-id="bb087-142">참조</span><span class="sxs-lookup"><span data-stu-id="bb087-142">Reference</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>

## <a name="related-sections"></a><span data-ttu-id="bb087-143">관련 단원</span><span class="sxs-lookup"><span data-stu-id="bb087-143">Related Sections</span></span>

- [<span data-ttu-id="bb087-144">Windows Communication Foundation (WCF) 샘플</span><span class="sxs-lookup"><span data-stu-id="bb087-144">Windows Communication Foundation (WCF) samples</span></span>](./samples/index.md)
- [<span data-ttu-id="bb087-145">기본 프로그래밍 수명 주기</span><span class="sxs-lookup"><span data-stu-id="bb087-145">Basic Programming Lifecycle</span></span>](../../../docs/framework/wcf/basic-programming-lifecycle.md)

## <a name="see-also"></a><span data-ttu-id="bb087-146">참고자료</span><span class="sxs-lookup"><span data-stu-id="bb087-146">See also</span></span>

- [<span data-ttu-id="bb087-147">개념적 개요</span><span class="sxs-lookup"><span data-stu-id="bb087-147">Conceptual Overview</span></span>](../../../docs/framework/wcf/conceptual-overview.md)
- [<span data-ttu-id="bb087-148">설명서에 대한 안내</span><span class="sxs-lookup"><span data-stu-id="bb087-148">Guide to the Documentation</span></span>](../../../docs/framework/wcf/guide-to-the-documentation.md)
- [<span data-ttu-id="bb087-149">Windows Communication Foundation 정의</span><span class="sxs-lookup"><span data-stu-id="bb087-149">What Is Windows Communication Foundation</span></span>](../../../docs/framework/wcf/whats-wcf.md)
- [<span data-ttu-id="bb087-150">WCF 기능 정보</span><span class="sxs-lookup"><span data-stu-id="bb087-150">WCF Feature Details</span></span>](../../../docs/framework/wcf/feature-details/index.md)
