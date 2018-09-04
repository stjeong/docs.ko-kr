---
title: CustomDiscoveryMetadata
ms.date: 03/30/2017
ms.assetid: c42455fd-3652-4b7e-b698-ab3a2bb52e48
ms.openlocfilehash: 181910db3f1dd6da892f6ae2ddcbf7bd5859ff17
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43525423"
---
# <a name="customdiscoverymetadata"></a><span data-ttu-id="f5d36-102">CustomDiscoveryMetadata</span><span class="sxs-lookup"><span data-stu-id="f5d36-102">CustomDiscoveryMetadata</span></span>
<span data-ttu-id="f5d36-103">이 샘플에서는 서비스에서 노출하는 검색 가능한 엔드포인트의 검색 메타데이터에 사용자 지정 XML 메타데이터를 삽입하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-103">This sample shows how to insert custom XML metadata into the discovery metadata for a discoverable endpoint exposed by a service.</span></span> <span data-ttu-id="f5d36-104">그런 다음 이 샘플에서는 클라이언트가 서비스를 검색하고 이 사용자 지정 데이터를 추출하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-104">The sample then shows how a client can search for the service and extract this custom data.</span></span> <span data-ttu-id="f5d36-105">이 샘플은 서비스와 클라이언트에 해당하는 두 개의 프로젝트로 구성되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-105">This sample consists of two projects, service and client.</span></span>  
  
## <a name="service"></a><span data-ttu-id="f5d36-106">서비스</span><span class="sxs-lookup"><span data-stu-id="f5d36-106">Service</span></span>  
 <span data-ttu-id="f5d36-107">샘플의 `main` 메서드에서는 <xref:System.Xml.Linq.XElement> 형식의 개체를 원하는 필드로 채우고 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>에 추가하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-107">In the `main` method, the sample shows that an object of type <xref:System.Xml.Linq.XElement> is populated with the desired fields and is added to the <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>.</span></span> <span data-ttu-id="f5d36-108">이 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>는 특정 끝점에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-108">This <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior> is added to a particular endpoint.</span></span> <span data-ttu-id="f5d36-109">해당 특정 엔드포인트가 검색될 때 검색 메타데이터에는 여기서 추가한 사용자 지정 데이터가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-109">When that particular endpoint is discovered, the discovery metadata contains the custom data that was added here.</span></span>  
  
## <a name="client"></a><span data-ttu-id="f5d36-110">클라이언트</span><span class="sxs-lookup"><span data-stu-id="f5d36-110">Client</span></span>  
 <span data-ttu-id="f5d36-111">이 샘플에서는 <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A>에서 호출되는 <xref:System.ServiceModel.Discovery.DiscoveryClient> 메서드를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-111">The sample shows the <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A> method being called on a <xref:System.ServiceModel.Discovery.DiscoveryClient>.</span></span> <span data-ttu-id="f5d36-112">그런 다음 결과 <xref:System.ServiceModel.Discovery.FindResponse>에서 적절한 예상 XML 요소를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-112">The resulting <xref:System.ServiceModel.Discovery.FindResponse> is then queried for the appropriate and expected XML elements.</span></span> <span data-ttu-id="f5d36-113">그런 다음 이러한 요소를 콘솔에 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-113">These elements are then printed to the console.</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="f5d36-114">이 샘플을 사용하려면</span><span class="sxs-lookup"><span data-stu-id="f5d36-114">To use this sample</span></span>  
  
1.  <span data-ttu-id="f5d36-115">[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)]에 프로젝트 솔루션을 로드하고 프로젝트를 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-115">Load the project solution in [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] and build the project.</span></span>  
  
2.  <span data-ttu-id="f5d36-116">먼저 [solution base directory]\service\bin\debug에 생성된 Service 응용 프로그램을 실행한 다음 [solution base directory]\Client\bin\debug에 생성된 Client 응용 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-116">First run the Service application, generated in [solution base directory]\service\bin\debug, and then run the Client application, generated in [solution base directory]\Client\bin\debug</span></span>  
  
3.  <span data-ttu-id="f5d36-117">서비스가 온라인 상태로 전환되며 클라이언트에서는 서비스를 찾고 엔드포인트에 게시된 메타데이터를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-117">Note that the service comes online, the client locates the service and prints the metadata published in the endpoint.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="f5d36-118">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-118">The samples may already be installed on your machine.</span></span> <span data-ttu-id="f5d36-119">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="f5d36-119">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="f5d36-120">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="f5d36-120">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="f5d36-121">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d36-121">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Extensibility\DiscoveryExtensibility\CustomDiscoveryMetadata`  
  
## <a name="see-also"></a><span data-ttu-id="f5d36-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f5d36-122">See Also</span></span>
