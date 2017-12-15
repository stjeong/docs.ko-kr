---
title: "Microservices 및 높은 확장성 및 가용성을 위한 다중 컨테이너 응용 프로그램 오케스트레이션"
description: "컨테이너 화 된.NET 응용 프로그램에 대 한.NET Microservices 아키텍처 | Microservices 및 높은 확장성 및 가용성을 위한 다중 컨테이너 응용 프로그램 오케스트레이션"
keywords: "Docker, 마이크로 서비스, ASP.NET, 컨테이너"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: ec33901a0ddc9e5b58263440b0e4399e687c6904
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2017
---
# <a name="orchestrating-microservices-and-multi-container-applications-for-high-scalability-and-availability"></a><span data-ttu-id="9840e-104">Microservices 및 높은 확장성 및 가용성을 위한 다중 컨테이너 응용 프로그램 오케스트레이션</span><span class="sxs-lookup"><span data-stu-id="9840e-104">Orchestrating microservices and multi-container applications for high scalability and availability</span></span>

<span data-ttu-id="9840e-105">프로덕션에 사용 가능한 응용 프로그램에 대 한 orchestrators를 사용 하 여이 응용 프로그램에 microservices 기반 또는 단순히 여러 컨테이너에서 분할 하는 경우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-105">Using orchestrators for production-ready applications is essential if your application is based on microservices or simply split across multiple containers.</span></span> <span data-ttu-id="9840e-106">마이크로 서비스 기반 접근 방식에서 이전에 도입 된 각 마이크로 서비스 소유 하 고 해당 모델 및 데이터 하는 개발 및 배포 측면 자치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-106">As introduced previously, in a microservice-based approach, each microservice owns its model and data so that it will be autonomous from a development and deployment point of view.</span></span> <span data-ttu-id="9840e-107">그러나는 보다 일반적인 응용 프로그램으로 구성 된 여러 서비스 (예: SOA)의 경우에는 또한 여러 컨테이너 또는 분산된 시스템으로 배포 되어야 하는 단일 비즈니스 응용 프로그램을 구성 하는 서비스.</span><span class="sxs-lookup"><span data-stu-id="9840e-107">But even if you have a more traditional application that is composed of multiple services (like SOA), you will also have multiple containers or services comprising a single business application that need to be deployed as a distributed system.</span></span> <span data-ttu-id="9840e-108">이러한 종류의 시스템은 확장성 및 관리; 복잡 따라서 있습니다 반드시 사용할 필요는 orchestrator 프로덕션 지원 하 고 확장 가능한 다중 컨테이너 응용 프로그램을 포함 하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="9840e-108">These kinds of systems are complex to scale out and manage; therefore, you absolutely need an orchestrator if you want to have a production-ready and scalable multi-container application.</span></span>

<span data-ttu-id="9840e-109">그림 4-23 여러 microservices (컨테이너)의 구성 된 응용 프로그램의 클러스터로 배포를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-109">Figure 4-23 illustrates deployment into a cluster of an application composed of multiple microservices (containers).</span></span>

![](./media/image23.PNG)

<span data-ttu-id="9840e-110">**그림 4-23**합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-110">**Figure 4-23**.</span></span> <span data-ttu-id="9840e-111">컨테이너의 클러스터</span><span class="sxs-lookup"><span data-stu-id="9840e-111">A cluster of containers</span></span>

<span data-ttu-id="9840e-112">논리적인 접근법 모양입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-112">It looks like a logical approach.</span></span> <span data-ttu-id="9840e-113">하지만 응용 프로그램 구성 어떻게 처리 부하 분산, 라우팅 및 이러한 조정 입니까?</span><span class="sxs-lookup"><span data-stu-id="9840e-113">But how are you handling load-balancing, routing, and orchestrating these composed applications?</span></span>

<span data-ttu-id="9840e-114">하나의 호스트에서 단일 이미지 인스턴스를 관리 요구를 충족 하는 단일 Docker 호스트의 일반 Docker 엔진 하 하지만 더 복잡 한 분산된 응용 프로그램에 대 한 여러 호스트에 배포 된 여러 컨테이너를 관리 하는 데 있어 짧은 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-114">The plain Docker Engine in single Docker hosts meets the needs of managing single image instances on one host, but it falls short when it comes to managing multiple containers deployed on multiple hosts for more complex distributed applications.</span></span> <span data-ttu-id="9840e-115">대부분의 경우에서 자동으로 시작 컨테이너 이미지에 여러 개의 인스턴스를 사용 하 여 확장 컨테이너, 일시 중단 하거나 필요한 경우를 종료 되며 이상적으로 네트워크 및 데이터와 같은 리소스에 액세스 하는 방식 또한 제어 하는 관리 플랫폼 필요 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-115">In most cases, you need a management platform that will automatically start containers, scale-out containers with multiple instances per image, suspend them or shut them down when needed, and ideally also control how they access resources like the network and data storage.</span></span>

<span data-ttu-id="9840e-116">개별 컨테이너 또는 매우 간단한 구성 된 앱 및 microservices 있는 대규모 엔터프라이즈 응용 프로그램의 이동 관리 외에 오케스트레이션 및 플랫폼 클러스터링을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-116">To go beyond the management of individual containers or very simple composed apps and move toward larger enterprise applications with microservices, you must turn to orchestration and clustering platforms.</span></span>

<span data-ttu-id="9840e-117">아키텍처 및 개발 관점에서 대기업 microservices 기반 응용 프로그램을 구성을 작성 하는 경우 이기 플랫폼 आ स ा 고급 시나리오를 지 원하는 제품을 이해 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-117">From an architecture and development point of view, if you are building large enterprise composed of microservices-based applications, it is important to understand the following platforms and products that support advanced scenarios:</span></span>

<span data-ttu-id="9840e-118">**클러스터 및 orchestrators**합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-118">**Clusters and orchestrators**.</span></span> <span data-ttu-id="9840e-119">중지 해야 많은 Docker 호스트에 응용 프로그램 확장은를 기본 플랫폼의 복잡성을 추상화 하 여 모든 호스트를 단일 클러스터로 관리할 수 있도록에 중요 한 경우 큰 마이크로 서비스 기반 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-119">When you need to scale out applications across many Docker hosts, as when a large microservice-based application, it is critical to be able to manage all those hosts as a single cluster by abstracting the complexity of the underlying platform.</span></span> <span data-ttu-id="9840e-120">컨테이너 클러스터와 orchestrators 제공 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-120">That is what the container clusters and orchestrators provide.</span></span> <span data-ttu-id="9840e-121">Orchestrators에는 Azure 서비스 패브릭, Kubernetes, docker는 Docker Swarm 및 Mesosphere DC/OS이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-121">Examples of orchestrators are Azure Service Fabric, Kubernetes, Docker Swarm and Mesosphere DC/OS.</span></span> <span data-ttu-id="9840e-122">마지막 세 오픈 소스 orchestrators Azure 컨테이너 서비스를 통해 Azure에서 사용할 수 있는 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-122">The last three open-source orchestrators are available in Azure through Azure Container Service.</span></span>

<span data-ttu-id="9840e-123">**스케줄러**합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-123">**Schedulers**.</span></span> <span data-ttu-id="9840e-124">*예약* 게도 UI를 제공 하는 클러스터의 컨테이너를 시작 하려면 관리자에 대 한 기능을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-124">*Scheduling* means to have the capability for an administrator to launch containers in a cluster so they also provide a UI.</span></span> <span data-ttu-id="9840e-125">클러스터 스케줄러는 여러 가지 역할: 클러스터의 리소스를 효율적으로 사용 하려면, 노드 또는 호스트 간에 부하를 분산 컨테이너와 효율적으로 사용자가 제공한 제약 조건을 설정 및 높음 제공 하는 동안 오류에 대해 강력한 수 가용성입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-125">A cluster scheduler has several responsibilities: to use the cluster’s resources efficiently, to set the constraints provided by the user, to efficiently load-balance containers across nodes or hosts, and to be robust against errors while providing high availability.</span></span>

<span data-ttu-id="9840e-126">클러스터 및 스케줄러의 개념 없으므로 두 가지 기능을 제공 하는 종종 다른 공급 업체에서 제공 하는 제품 관련 밀접 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-126">The concepts of a cluster and a scheduler are closely related, so the products provided by different vendors often provide both sets of capabilities.</span></span> <span data-ttu-id="9840e-127">다음 목록에는 가장 중요 한 플랫폼 및 클러스터 및 스케줄러에 대 한 소프트웨어 선택 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-127">The following list shows the most important platform and software choices you have for clusters and schedulers.</span></span> <span data-ttu-id="9840e-128">이러한 orchestrators Azure와 같은 공용 클라우드에 일반적으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-128">These orchestrators are generally offered in public clouds like Azure.</span></span>

## <a name="software-platforms-for-container-clustering-orchestration-and-scheduling"></a><span data-ttu-id="9840e-129">클러스터링 컨테이너, 오케스트레이션 및 예약에 대 한 소프트웨어 플랫폼</span><span class="sxs-lookup"><span data-stu-id="9840e-129">Software platforms for container clustering, orchestration, and scheduling</span></span>

<span data-ttu-id="9840e-130">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="9840e-130">Kubernetes</span></span>

![https://pbs.twimg.com/media/Bt\_pEfqCAAAiVyz.png](./media/image24.png)

> <span data-ttu-id="9840e-132">Kubernetes는 클러스터 인프라 및 컨테이너 조정 기능을 예약 하는 기능을 제공 하는 오픈 소스 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-132">Kubernetes is an open-source product that provides functionality that ranges from cluster infrastructure and container scheduling to orchestrating capabilities.</span></span> <span data-ttu-id="9840e-133">호스트 클러스터 간에 배포, 배율 및 응용 프로그램 컨테이너의 작업을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-133">It lets you automate deployment, scaling, and operations of application containers across clusters of hosts.</span></span>
>
> <span data-ttu-id="9840e-134">Kubernetes는 컨테이너 응용 프로그램을 쉽게 관리 및 검색에 대 한 논리 단위로 그룹화 하는 컨테이너 중심 인프라를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-134">Kubernetes provides a container-centric infrastructure that groups application containers into logical units for easy management and discovery.</span></span>
>
> <span data-ttu-id="9840e-135">Kubernetes linux, Windows에서 덜 완성도 높은 완성도 높은입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-135">Kubernetes is mature in Linux, less mature in Windows.</span></span>

<span data-ttu-id="9840e-136">Docker 웜</span><span class="sxs-lookup"><span data-stu-id="9840e-136">Docker Swarm</span></span>

![http://rancher.com/wp-content/themes/rancher-2016/assets/images/swarm.png?v=2016-07-10-am](./media/image25.png)

> <span data-ttu-id="9840e-138">Docker 웜을 사용 하 여 클러스터 및 Docker 컨테이너를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-138">Docker Swarm lets you cluster and schedule Docker containers.</span></span> <span data-ttu-id="9840e-139">웜을 사용 하 여 단일, 가상 Docker 호스트에 Docker 호스트의 풀을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-139">By using Swarm, you can turn a pool of Docker hosts into a single, virtual Docker host.</span></span> <span data-ttu-id="9840e-140">클라이언트는 호스트는 웜 쉽게 여러 호스트 조정을 응용 프로그램에 대 한 의미를 위한 것 같은 방식으로 Swarm을 API 요청을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-140">Clients can make API requests to Swarm the same way they do to hosts, meaning that Swarm makes it easy for applications to scale to multiple hosts.</span></span>
>
> <span data-ttu-id="9840e-141">Docker 웜은 동시에 회사에서 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-141">Docker Swarm is a product from Docker, the company.</span></span>
>
> <span data-ttu-id="9840e-142">Docker v1.12 하거나 네이티브 및 기본 제공 Swarm 모드 나중에 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-142">Docker v1.12 or later can run native and built-in Swarm Mode.</span></span>

<span data-ttu-id="9840e-143">Mesosphere DC/OS</span><span class="sxs-lookup"><span data-stu-id="9840e-143">Mesosphere DC/OS</span></span>

![https://mesosphere.com/wp-content/uploads/2016/04/logo-horizontal-styled.png](./media/image26.png)

> <span data-ttu-id="9840e-145">Mesosphere 엔터프라이즈 DC/OS (Apache Mesos에 기반)는 컨테이너 및 분산된 응용 프로그램을 실행 하기 위한 프로덕션에 사용 가능한 플랫폼입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-145">Mesosphere Enterprise DC/OS (based on Apache Mesos) is a production-ready platform for running containers and distributed applications.</span></span>
>
> <span data-ttu-id="9840e-146">DC/OS 클러스터에서 사용할 수 있는 리소스의 컬렉션을 추상화 하 고 해당 리소스를 기반으로 하는 구성 요소를 사용할 수 있도록 하 여 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-146">DC/OS works by abstracting a collection of the resources available in the cluster and making those resources available to components built on top of it.</span></span> <span data-ttu-id="9840e-147">풀 마라톤 DC/운영 체제와 통합 하는 스케줄러로 일반적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-147">Marathon is usually used as a scheduler integrated with DC/OS.</span></span>
>
> <span data-ttu-id="9840e-148">DC/OS는 linux, Windows에서 덜 완성도 높은 완성도 높은입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-148">DC/OS is mature in Linux, less mature in Windows.</span></span>

<span data-ttu-id="9840e-149">Azure 서비스 패브릭</span><span class="sxs-lookup"><span data-stu-id="9840e-149">Azure Service Fabric</span></span>

![https://azure.microsoft.com/svghandler/service-fabric?width=600&height=315](./media/image27.png)

> <span data-ttu-id="9840e-151">[서비스 패브릭](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview) 는 응용 프로그램을 빌드하기 위한 Microsoft microservices 플랫폼입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-151">[Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview) is a Microsoft microservices platform for building applications.</span></span> <span data-ttu-id="9840e-152">한 [orchestrator](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction) 의 서비스를 컴퓨터의 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-152">It is an [orchestrator](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction) of services and creates clusters of machines.</span></span> <span data-ttu-id="9840e-153">서비스 패브릭 컨테이너로 또는 일반 프로세스로 서비스를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-153">Service Fabric can deploy services as containers or as plain processes.</span></span> <span data-ttu-id="9840e-154">도 혼합 프로세스의 서비스를 컨테이너 내에서 동일한 응용 프로그램 및 클러스터의에서 서비스와 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-154">It can even mix services in processes with services in containers within the same application and cluster.</span></span>
>
> <span data-ttu-id="9840e-155">서비스 패브릭 추가 및 선택적 제공 규범적인 [프로그래밍 모델 서비스 패브릭 ](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework) 같은 [상태 저장 서비스](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) 및 [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction)합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-155">Service Fabric provides additional and optional prescriptive [Service Fabric programming models ](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework) like [stateful services](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) and [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).</span></span>
>
> <span data-ttu-id="9840e-156">Windows (Windows에서 진화 years)에서 완성 된 덜 Linux에서 서비스 패브릭은 성숙한입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-156">Service Fabric is mature in Windows (years evolving in Windows), less mature in Linux.</span></span> 
> <span data-ttu-id="9840e-157">Linux 및 Windows 컨테이너는 2017 이후 서비스 패브릭에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-157">Both Linux and Windows containers are supported in Service Fabric since 2017.</span></span>

## <a name="using-container-based-orchestrators-in-microsoft-azure"></a><span data-ttu-id="9840e-158">Microsoft Azure에서 컨테이너 기반 orchestrators를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="9840e-158">Using container-based orchestrators in Microsoft Azure</span></span>

<span data-ttu-id="9840e-159">여러 클라우드 공급 업체는 Docker 컨테이너 지원 함께 Docker 클러스터 및 Microsoft Azure, Amazon EC2 컨테이너 서비스 및 Google 컨테이너 엔진 등의 오케스트레이션 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-159">Several cloud vendors offer Docker containers support plus Docker clusters and orchestration support, including Microsoft Azure, Amazon EC2 Container Service, and Google Container Engine.</span></span> <span data-ttu-id="9840e-160">Microsoft Azure는 다음 섹션에 설명 된 대로 클러스터 및 orchestrator 지원을 통해 Azure 컨테이너 서비스 (ACS), Docker를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-160">Microsoft Azure provides Docker cluster and orchestrator support through Azure Container Service (ACS), as explained in the next section.</span></span>

<span data-ttu-id="9840e-161">다른 선택 Microsoft Azure 서비스 패브릭 (microservices 플랫폼)도 Docker를 기반으로 Linux 및 Windows 컨테이너를 지원 하를 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-161">Another choice is to use Microsoft Azure Service Fabric (a microservices platform), which also supports Docker based on Linux and Windows Containers.</span></span> <span data-ttu-id="9840e-162">서비스 패브릭 다른 클라우드 또는 Azure에서 실행 되 고도 실행 [온-프레미스](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere)합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-162">Service Fabric runs on Azure or any other cloud, and also runs [on-premises](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere).</span></span>

## <a name="using-azure-container-service"></a><span data-ttu-id="9840e-163">Azure 컨테이너 서비스를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="9840e-163">Using Azure Container Service</span></span>

<span data-ttu-id="9840e-164">Docker 클러스터 여러 Docker 호스트를 풀링 하 고는 단일 가상 Docker 호스트에 노출 하는 클러스터에 여러 컨테이너를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-164">A Docker cluster pools multiple Docker hosts and exposes them as a single virtual Docker host, so you can deploy multiple containers into the cluster.</span></span> <span data-ttu-id="9840e-165">클러스터는 확장성, 상태, 등과 같은 모든 복잡 한 관리 작업으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-165">The cluster will handle all the complex management plumbing, like scalability, health, and so forth.</span></span> <span data-ttu-id="9840e-166">그림 4-24 구성 된 응용 프로그램에 대 한 Docker 클러스터에 Azure 컨테이너 서비스 (ACS)를 매핑하는 방식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-166">Figure 4-24 represents how a Docker cluster for composed applications maps to Azure Container Service (ACS).</span></span>

<span data-ttu-id="9840e-167">ACS를 생성, 구성 및 클러스터 화 된 응용 프로그램을 실행 하는 미리 구성 된 가상 컴퓨터의 관리를 단순화 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-167">ACS provides a way to simplify the creation, configuration, and management of a cluster of virtual machines that are preconfigured to run containerized applications.</span></span> <span data-ttu-id="9840e-168">인기 있는 오픈 소스 일정 예약 및 오케스트레이션 도구는 최적화 된 구성을 사용 하 여, ACS 하면 사용자의 기존 기술을 사용 하거나 커뮤니티 전문성을 배포 하 고 Microsoft Azure에서 컨테이너 기반 응용 프로그램 관리의 크기가 크고 점점 본문에 그리기 .</span><span class="sxs-lookup"><span data-stu-id="9840e-168">Using an optimized configuration of popular open-source scheduling and orchestration tools, ACS enables you to use your existing skills or draw on a large and growing body of community expertise to deploy and manage container-based applications on Microsoft Azure.</span></span>

<span data-ttu-id="9840e-169">Azure 컨테이너 서비스를 Azure에 맞게 인기 있는 오픈 소스 도구를 클러스터링 하는 Docker 및 기술 구성을 최적화합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-169">Azure Container Service optimizes the configuration of popular Docker clustering open source tools and technologies specifically for Azure.</span></span> <span data-ttu-id="9840e-170">사용자 컨테이너와 응용 프로그램 구성에 대 한 이식성을 제공 하는 열린 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="9840e-170">You get an open solution that offers portability for both your containers and your application configuration.</span></span> <span data-ttu-id="9840e-171">Orchestrator 도구, 호스트, 수 및 크기를 선택 하 고 다른 모든 항목을 처리 하는 컨테이너 서비스 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-171">You select the size, the number of hosts, and the orchestrator tools, and Container Service handles everything else.</span></span>

![](./media/image28.png)

<span data-ttu-id="9840e-172">**그림 4-24**합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-172">**Figure 4-24**.</span></span> <span data-ttu-id="9840e-173">Azure 컨테이너 서비스에서 선택할 수 있는 클러스터링</span><span class="sxs-lookup"><span data-stu-id="9840e-173">Clustering choices in Azure Container Service</span></span>

<span data-ttu-id="9840e-174">ACS 응용 프로그램 컨테이너가 완전히 이식 가능 인지 확인 하는 Docker 이미지를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-174">ACS leverages Docker images to ensure that your application containers are fully portable.</span></span> <span data-ttu-id="9840e-175">선택 하는 DC/OS (Apache Mesos 기반의), (처음 만든 Google에서) Kubernetes 및 docker는 Docker Swarm와 같은 오픈 소스 오케스트레이션 플랫폼 이러한 응용 프로그램 아니면 수천 또는 심지어 수만 컨테이너의 배율을 조정할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-175">It supports your choice of open-source orchestration platforms like DC/OS (powered by Apache Mesos), Kubernetes (originally created by Google), and Docker Swarm, to ensure that these applications can be scaled to thousands or even tens of thousands of containers.</span></span>

<span data-ttu-id="9840e-176">Azure 컨테이너 서비스를 사용 하면 오케스트레이션 계층에 포함 하 여 응용 프로그램 이식성을 유지 하면서 Azure의 엔터프라이즈급 기능을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-176">The Azure Container service enables you to take advantage of the enterprise-grade features of Azure while still maintaining application portability, including at the orchestration layers.</span></span>

![](./media/image29.png)

<span data-ttu-id="9840e-177">**그림 4-25**합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-177">**Figure 4-25**.</span></span> <span data-ttu-id="9840e-178">ACS에서 orchestrators</span><span class="sxs-lookup"><span data-stu-id="9840e-178">Orchestrators in ACS</span></span>

<span data-ttu-id="9840e-179">그림 4-25와 같이 Azure 컨테이너 서비스는 Azure에서 DC/OS, Kubernetes 또는 docker는 Docker Swarm을 배포 하기 위해 제공 하는 인프라 단순히 하지만 ACS 모든 추가 orchestrator를 구현 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-179">As shown in Figure 4-25, Azure Container Service is simply the infrastructure provided by Azure in order to deploy DC/OS, Kubernetes or Docker Swarm, but ACS does not implement any additional orchestrator.</span></span> <span data-ttu-id="9840e-180">따라서 ACS는 orchestrator 마찬가지로 컨테이너에 대 한 기존 오픈 소스 orchestrators를 활용 하는 인프라 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-180">Therefore, ACS is not an orchestrator as such, only an infrastructure that leverages existing open-source orchestrators for containers.</span></span>

<span data-ttu-id="9840e-181">사용 관점에서 Azure 컨테이너 서비스의 목표는 인기 있는 오픈 소스 도구와 기술을 사용 하 여 컨테이너 호스팅 환경을 제공 하는입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-181">From a usage perspective, the goal of Azure Container Service is to provide a container hosting environment by using popular open-source tools and technologies.</span></span> <span data-ttu-id="9840e-182">이 위해 선택한 여 orchestrator에 대 한 표준 API 끝점을 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-182">To this end, it exposes the standard API endpoints for your chosen orchestrator.</span></span> <span data-ttu-id="9840e-183">이러한 끝점을 사용 하 여 해당 끝점에 서로 연결할 수 있는 모든 소프트웨어를 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-183">By using these endpoints, you can leverage any software that can talk to those endpoints.</span></span> <span data-ttu-id="9840e-184">예를 들어 docker는 Docker Swarm 끝점의 경우 Docker 명령줄 인터페이스 (CLI)를 사용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-184">For example, in the case of the Docker Swarm endpoint, you might choose to use the Docker command-line interface (CLI).</span></span> <span data-ttu-id="9840e-185">DC/OS 용 DC/OS CLI를 사용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-185">For DC/OS, you might choose to use the DC/OS CLI.</span></span>

### <a name="getting-started-with-azure-container-service"></a><span data-ttu-id="9840e-186">Azure 컨테이너 서비스를 시작 하기</span><span class="sxs-lookup"><span data-stu-id="9840e-186">Getting started with Azure Container Service</span></span> 

<span data-ttu-id="9840e-187">Azure 컨테이너 서비스를 사용 하 여을 시작 하려면 클러스터를 배포할 있습니다 Azure 컨테이너 서비스는 Azure 포털에서 Azure 리소스 관리자 템플릿을 사용 하 여 또는 [CLI](https://docs.microsoft.com/cli/azure/install-azure-cli)합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-187">To begin using Azure Container Service, you deploy an Azure Container Service cluster from the Azure portal by using an Azure Resource Manager template or the [CLI](https://docs.microsoft.com/cli/azure/install-azure-cli).</span></span> <span data-ttu-id="9840e-188">사용 가능한 템플릿에 포함 [docker는 Docker Swarm](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-swarm), [Kubernetes](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-kubernetes), 및 [DC/OS](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-dcos)합니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-188">Available templates include [Docker Swarm](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-swarm), [Kubernetes](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-kubernetes), and [DC/OS](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-dcos).</span></span> <span data-ttu-id="9840e-189">퀵 스타트 서식 파일을 추가 또는 고급 Azure 구성을 포함 하도록 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-189">The quickstart templates can be modified to include additional or advanced Azure configuration.</span></span> <span data-ttu-id="9840e-190">Azure 컨테이너 서비스 클러스터를 배포 하는 방법에 대 한 자세한 내용은 참조 하십시오. [Azure 컨테이너 서비스 클러스터를 배포할](https://docs.microsoft.com/azure/container-service/container-service-deployment) Azure 웹 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-190">For more information on deploying an Azure Container Service cluster, see [Deploy an Azure Container Service cluster](https://docs.microsoft.com/azure/container-service/container-service-deployment) on the Azure website.</span></span>

<span data-ttu-id="9840e-191">ACS의 일부로 기본적으로 설치 된 소프트웨어의 모든 가격 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-191">There are no fees for any of the software installed by default as part of ACS.</span></span> <span data-ttu-id="9840e-192">모든 기본 옵션은 오픈 소스 소프트웨어로 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-192">All default options are implemented with open-source software.</span></span>

<span data-ttu-id="9840e-193">ACS는 표준 A "," D "," DS "," G "및" GS 시리즈 Azure에서 Linux 가상 컴퓨터를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-193">ACS is currently available for Standard A, D, DS, G, and GS series Linux virtual machines in Azure.</span></span> <span data-ttu-id="9840e-194">다른 기본 인프라 리소스 저장소 및 네트워킹 등 사용 뿐만 아니라 계산 인스턴스를 선택 하면에 대해서만 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-194">You are charged only for the compute instances you choose, as well as the other underlying infrastructure resources consumed, such as storage and networking.</span></span> <span data-ttu-id="9840e-195">자체 ACS에 대 한 증분 요금이 없습니다 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9840e-195">There are no incremental charges for ACS itself.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9840e-196">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="9840e-196">Additional resources</span></span>

-   <span data-ttu-id="9840e-197">**Azure 컨테이너 서비스를 사용 하 여 솔루션을 호스팅하는 Docker 컨테이너 소개**
    [*https://docs.microsoft.com/azure/container-service/container-service-intro*](https://docs.microsoft.com/azure/container-service/container-service-intro)</span><span class="sxs-lookup"><span data-stu-id="9840e-197">**Introduction to Docker container hosting solutions with Azure Container Service**
[*https://docs.microsoft.com/azure/container-service/container-service-intro*](https://docs.microsoft.com/azure/container-service/container-service-intro)</span></span>

-   <span data-ttu-id="9840e-198">**Docker 웜 개요**
    [*https://docs.docker.com/swarm/overview/*](https://docs.docker.com/swarm/overview/)</span><span class="sxs-lookup"><span data-stu-id="9840e-198">**Docker Swarm overview**
[*https://docs.docker.com/swarm/overview/*](https://docs.docker.com/swarm/overview/)</span></span>

-   <span data-ttu-id="9840e-199">**모드 개요 swarm**
    [*https://docs.docker.com/engine/swarm/*](https://docs.docker.com/engine/swarm/)</span><span class="sxs-lookup"><span data-stu-id="9840e-199">**Swarm mode overview**
[*https://docs.docker.com/engine/swarm/*](https://docs.docker.com/engine/swarm/)</span></span>

-   <span data-ttu-id="9840e-200">**DC/OS 개요 mesosphere**
    [*https://docs.mesosphere.com/1.7/overview/*](https://docs.mesosphere.com/1.7/overview/)</span><span class="sxs-lookup"><span data-stu-id="9840e-200">**Mesosphere DC/OS Overview**
[*https://docs.mesosphere.com/1.7/overview/*](https://docs.mesosphere.com/1.7/overview/)</span></span>

-   <span data-ttu-id="9840e-201">**Kubernetes 합니다.**</span><span class="sxs-lookup"><span data-stu-id="9840e-201">**Kubernetes.**</span></span> <span data-ttu-id="9840e-202">공식 사이트입니다. \ \\</span><span class="sxs-lookup"><span data-stu-id="9840e-202">The official site.\\</span></span>
    [<span data-ttu-id="9840e-203">*http://kubernetes.io/*</span><span class="sxs-lookup"><span data-stu-id="9840e-203">*http://kubernetes.io/*</span></span>](http://kubernetes.io/)


>[!div class="step-by-step"]
<span data-ttu-id="9840e-204">[이전] (탄력적인-높은-가용성-microservices.md) [다음] (사용 하 여-azure-서비스-fabric.md)</span><span class="sxs-lookup"><span data-stu-id="9840e-204">[Previous] (resilient-high-availability-microservices.md) [Next] (using-azure-service-fabric.md)</span></span>