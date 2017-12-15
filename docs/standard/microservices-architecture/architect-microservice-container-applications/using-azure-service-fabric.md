---
title: "Azure 서비스 패브릭을 사용 하 여"
description: "컨테이너 화 된.NET 응용 프로그램에 대 한.NET Microservices 아키텍처 | Azure 서비스 패브릭을 사용 하 여"
keywords: "Docker, 마이크로 서비스, ASP.NET, 컨테이너"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: aa15f9cf9bc60e9e70607da921f2ce2c75e39ec2
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2017
---
# <a name="using-azure-service-fabric"></a><span data-ttu-id="bf719-104">Azure 서비스 패브릭을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="bf719-104">Using Azure Service Fabric</span></span>

<span data-ttu-id="bf719-105">Azure 서비스 패브릭 서비스 제공를 일반적으로 스타일에서 모놀리식 였던 상자 제품 배달에서 Microsoft의 전환에서 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-105">Azure Service Fabric arose from Microsoft’s transition from delivering box products, which were typically monolithic in style, to delivering services.</span></span> <span data-ttu-id="bf719-106">Azure SQL 데이터베이스, Azure Cosmos DB, Azure 서비스 버스 Cortana의 백 엔드 등 규모에 대규모 서비스 구축 및 운영 하는 환경을 서비스 패브릭 모양이 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-106">The experience of building and operating large services at scale, such as Azure SQL Database, Azure Cosmos DB, Azure Service Bus, or Cortana’s Backend, shaped Service Fabric.</span></span> <span data-ttu-id="bf719-107">플랫폼 발전 함에 따라 시간이 지남에 따라 점점 더 많은 서비스 채택으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-107">The platform evolved over time as more and more services adopted it.</span></span> <span data-ttu-id="bf719-108">중요 서비스 패브릭 Azure에서 뿐만 아니라 독립 실행형 Windows Server 배포에서 실행 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-108">Importantly, Service Fabric had to run not only in Azure but also in standalone Windows Server deployments.</span></span>

<span data-ttu-id="bf719-109">서비스 패브릭의 목적은 팀 microservices 방식을 사용 하 여 비즈니스 문제를 해결할 수 있도록 구축 하 고 서비스를 실행 하 고 인프라 리소스를 효율적으로 활용의 어려운 문제를 해결 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-109">The aim of Service Fabric is to solve the hard problems of building and running a service and utilizing infrastructure resources efficiently, so that teams can solve business problems using a microservices approach.</span></span>

<span data-ttu-id="bf719-110">서비스 패브릭 microservices 접근 방식을 사용 하는 응용 프로그램을 빌드할 수 있도록 두 가지 광범위 한 영역을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-110">Service Fabric provides two broad areas to help you build applications that use a microservices approach:</span></span>

-   <span data-ttu-id="bf719-111">시스템 서비스를 배포, 확장, 업그레이드, 검색 및 실패 한 서비스를 다시 시작, 서비스 위치 검색, 상태를 관리 및 상태 모니터링을 제공 하는 플랫폼입니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-111">A platform that provides system services to deploy, scale, upgrade, detect, and restart failed services, discover service location, manage state, and monitor health.</span></span> <span data-ttu-id="bf719-112">이러한 시스템 서비스를 통해 이전에 설명한 microservices 특징을 많이 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-112">These system services in effect enable many of the characteristics of microservices described previously.</span></span>

-   <span data-ttu-id="bf719-113">Microservices로, 응용 프로그램을 빌드할 수 있도록 프로그래밍 Api 또는 프레임 워크: [신뢰할 수 있는 작업자와 신뢰할 수 있는 서비스](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-113">Programming APIs, or frameworks, to help you build applications as microservices: [reliable actors and reliable services](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework).</span></span> <span data-ttu-id="bf719-114">물론, 프로그램 마이크로 서비스를 작성 하기 위해 코드를 선택할 수 있지만 이러한 Api 작업 더 간단한 만들고 더 하위 수준 플랫폼에 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-114">Of course, you can choose any code to build your microservice, but these APIs make the job more straightforward, and they integrate with the platform at a deeper level.</span></span> <span data-ttu-id="bf719-115">상태 및 진단 정보 또는 있습니다를 얻을 수 있습니다 이러한 방식으로 활용할 수 신뢰할 수 있는 상태 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-115">This way you can get health and diagnostics information, or you can take advantage of reliable state management.</span></span>

<span data-ttu-id="bf719-116">서비스 패브릭 서비스를 구축 하는 방법에 대해 알 수 없는 이며 모든 기술을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-116">Service Fabric is agnostic with respect to how you build your service, and you can use any technology.</span></span> <span data-ttu-id="bf719-117">그러나 보다 쉽게 microservices 빌드할 수 있도록 기본 제공 프로그래밍 Api를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-117">However, it provides built-in programming APIs that make it easier to build microservices.</span></span>

<span data-ttu-id="bf719-118">그림 4-26 같이 수 만들고 간단한 프로세스 또는 Docker 컨테이너 microservices 서비스 패브릭에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-118">As shown in Figure 4-26, you can create and run microservices in Service Fabric either as simple processes or as Docker containers.</span></span> <span data-ttu-id="bf719-119">와 동일한 서비스 패브릭 클러스터 내에서 프로세스 기반 microservices microservices 컨테이너 기반을 함께 사용할 수 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-119">It is also possible to mix container-based microservices with process-based microservices within the same Service Fabric cluster.</span></span>

![](./media/image30.png)

<span data-ttu-id="bf719-120">**그림 4-26**합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-120">**Figure 4-26**.</span></span> <span data-ttu-id="bf719-121">프로세스 또는 Azure 서비스 패브릭에서 컨테이너로 microservices 배포</span><span class="sxs-lookup"><span data-stu-id="bf719-121">Deploying microservices as processes or as containers in Azure Service Fabric</span></span>

<span data-ttu-id="bf719-122">Linux 및 Windows 호스트에 따라 서비스 패브릭 클러스터 Linux Docker 컨테이너와 Windows 컨테이너를 각각 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-122">Service Fabric clusters based on Linux and Windows hosts can run Docker Linux containers and Windows Containers, respectively.</span></span>

<span data-ttu-id="bf719-123">Azure 서비스 패브릭에서 컨테이너 지원에 대 한 최신 정보를 참조 하십시오. [서비스 패브릭 및 컨테이너](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-123">For up-to-date information about containers support in Azure Service Fabric, see [Service Fabric and containers](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).</span></span>

<span data-ttu-id="bf719-124">서비스 패브릭은 다른 논리적 아키텍처 (비즈니스 microservices 또는 경계가 지정 된 컨텍스트)에서 소개 된 물리적 구현 보다을 정의할 수 있는 플랫폼의 좋은 예는 [물리적 및 논리적 아키텍처 아키텍처](#logical-architecture-versus-physical-architecture) 섹션.</span><span class="sxs-lookup"><span data-stu-id="bf719-124">Service Fabric is a good example of a platform where you can define a different logical architecture (business microservices or Bounded Contexts) than the physical implementation that were introduced in the [Logical architecture versus physical architecture](#logical-architecture-versus-physical-architecture) section.</span></span> <span data-ttu-id="bf719-125">예를 들어, 구현 하는 경우 [상태 저장 Reliable Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) 에 [Azure 서비스 패브릭](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview), 섹션에 도입 된 있는 [와 상태 저장 microservices Stateless](#stateless-versus-stateful-microservices) 이상 버전에서는 여러 실제 서비스는 비즈니스 마이크로 서비스 개념을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-125">For example, if you implement [Stateful Reliable Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) in [Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview), which are introduced in the section [Stateless versus stateful microservices](#stateless-versus-stateful-microservices) later, you can have a business microservice concept with multiple physical services.</span></span>

<span data-ttu-id="bf719-126">그림 4-27 및 서비스 패브릭 상태 저장 신뢰할 수 있는 서비스를 구현 하는 경우 논리적/비즈니스 마이크로 서비스 관점에서의 생각에서와 같이, 일반적으로 해야 합니다 두 계층의 서비스를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-126">As shown in Figure 4-27, and thinking from a logical/business microservice perspective, when implementing a Service Fabric Stateful Reliable Service, you usually will need to implement two tiers of services.</span></span> <span data-ttu-id="bf719-127">첫 번째는 백 엔드 상태 저장 reliable를 처리 하는 서비스 (각 파티션에 상태 저장 서비스) 다중 파티션을 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-127">The first is the back-end stateful reliable service, which handles multiple partitions (each partition is a stateful service).</span></span> <span data-ttu-id="bf719-128">두 번째 프런트 엔드 서비스 또는 라우팅 및 데이터 집계 여러 파티션 또는 상태 저장 서비스 인스턴스는 일을 담당 게이트웨이 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-128">The second is the front-end service, or Gateway service, in charge of routing and data aggregation across multiple partitions or stateful service instances.</span></span> <span data-ttu-id="bf719-129">또한 해당 게이트웨이 서비스 백 엔드 서비스에 액세스 하는 다시 시도 루프 클라이언트 통신을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-129">That Gateway service also handles client-side communication with retry loops accessing the backend service.</span></span>
<span data-ttu-id="bf719-130">사용자 지정 서비스 또는 alternatevely 기본적으로 서비스 패브릭을 사용할 수도 있습니다를 구현 하는 경우 게이트웨이 서비스 라고 [역방향 프록시 서비스](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-130">It is called a Gateway service if you implement your custom service, or alternatevely you can also use the out-of-the-box Service Fabric [Reverse Proxy service](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy).</span></span>

![](./media/image31.png)

<span data-ttu-id="bf719-131">**그림 4-27**합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-131">**Figure 4-27**.</span></span> <span data-ttu-id="bf719-132">여러 상태 저장 서비스 인스턴스 및 프런트 엔드는 사용자 지정 하는 게이트웨이 비즈니스 마이크로 서비스</span><span class="sxs-lookup"><span data-stu-id="bf719-132">Business microservice with several stateful service instances and a custom gateway front-end</span></span>

<span data-ttu-id="bf719-133">어떤 경우 든, 서비스 패브릭 상태 저장 Reliable Services를 사용 하는 경우는 논리 또는 비즈니스 마이크로 서비스 (경계가 지정 된 컨텍스트) 일반적으로 여러 개의 물리적 서비스의 요소로 구성 된도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-133">In any case, when you use Service Fabric Stateful Reliable Services, you also have a logical or business microservice (Bounded Context) that is usually composed of multiple physical services.</span></span> <span data-ttu-id="bf719-134">중의 게이트웨이 서비스와 파티션 서비스 각각 그림 4-26와 같이 ASP.NET Web API를 서비스로 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-134">Each of them, the Gateway service and Partition service could be implemented as ASP.NET Web API services, as shown in Figure 4-26.</span></span>

<span data-ttu-id="bf719-135">서비스 패브릭에서 그룹화를 그룹으로 서비스를 배포할 수 있습니다는 [서비스 패브릭 응용 프로그램](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model)는 패키징 및 orchestrator 또는 클러스터에 대 한 배포의 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-135">In Service Fabric, you can group and deploy groups of services as a [Service Fabric Application](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model), which is the unit of packaging and deployment for the orchestrator or cluster.</span></span> <span data-ttu-id="bf719-136">따라서 서비스 패브릭 응용 프로그램에 매핑할 수이 자율 영업 및 논리 마이크로 서비스 경계 또는 컨텍스트 제한도 자율적으로 이러한 서비스를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-136">Therefore, the Service Fabric Application could be mapped to this autonomous business and logical microservice boundary or Bounded Context, as well, so you could deploy these services autonomously.</span></span>

## <a name="service-fabric-and-containers"></a><span data-ttu-id="bf719-137">서비스 패브릭 및 컨테이너</span><span class="sxs-lookup"><span data-stu-id="bf719-137">Service Fabric and containers</span></span>

<span data-ttu-id="bf719-138">서비스 패브릭에서 컨테이너와 관련 하 여 서비스 패브릭 클러스터 내에서 컨테이너 이미지에서 서비스를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-138">With regard to containers in Service Fabric, you can also deploy services in container images within a Service Fabric cluster.</span></span> <span data-ttu-id="bf719-139">그림 4-28에서 볼 수 있듯이 대부분의 경우만 됩니다 서비스 당 하나의 컨테이너.</span><span class="sxs-lookup"><span data-stu-id="bf719-139">As Figure 4-28 shows, most of the time there will only be one container per service.</span></span>

![](./media/image32.png)

<span data-ttu-id="bf719-140">**그림 4-28**합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-140">**Figure 4-28**.</span></span> <span data-ttu-id="bf719-141">서비스 패브릭에서 여러 개의 서비스 (컨테이너)를 비즈니스 마이크로 서비스</span><span class="sxs-lookup"><span data-stu-id="bf719-141">Business microservice with several services (containers) in Service Fabric</span></span>

<span data-ttu-id="bf719-142">하지만 이른바 "사이드카" 컨테이너 (함께 논리 서비스의 일부분으로 배포 해야 하는 두 개의 컨테이너)는 서비스 패브릭에서 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-142">However, so-called “sidecar” containers (two containers that must be deployed together as part of a logical service) are also possible in Service Fabric.</span></span> <span data-ttu-id="bf719-143">것이 중요 비즈니스 마이크로 서비스 여러 화합 요소 주위에 논리적 경계 된다는 점입니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-143">The important thing is that a business microservice is the logical boundary around several cohesive elements.</span></span> <span data-ttu-id="bf719-144">대부분의 경우에서 단일 데이터 모델에서는 단일 서비스 않을 수 있지만 다른 경우에 실제 몇 가지 서비스도 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-144">In many cases, it might be a single service with a single data model, but in some other cases you might have physical several services as well.</span></span>

<span data-ttu-id="bf719-145">Mid-2017 년을 기준으로 서비스 패브릭에서 배포할 수 없습니다 SF 신뢰할 수 있는 상태 저장 서비스 컨테이너에-상태 비저장 서비스 및 행위자 서비스 컨테이너에만 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-145">As of mid-2017, in Service Fabric you cannot deploy SF Reliable Stateful Services on containers—you can only deploy stateless services and actor services in containers.</span></span> <span data-ttu-id="bf719-146">그러나 프로세스의 서비스 및 서비스에 동일한 서비스 패브릭 응용 프로그램의 컨테이너를 혼합할 수 그림 4-29와 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-146">But note that you can mix services in processes and services in containers in the same Service Fabric application, as shown in Figure 4-29.</span></span>

![](./media/image33.png)

<span data-ttu-id="bf719-147">**그림 4-29**합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-147">**Figure 4-29**.</span></span> <span data-ttu-id="bf719-148">컨테이너 및 상태 저장 서비스와 함께 서비스 패브릭 응용 프로그램에 매핑된 비즈니스 마이크로 서비스</span><span class="sxs-lookup"><span data-stu-id="bf719-148">Business microservice mapped to a Service Fabric application with containers and stateful services</span></span>

<span data-ttu-id="bf719-149">Azure 서비스 패브릭에서 컨테이너 지원에 대 한 자세한 내용은 참조 [서비스 패브릭 및 컨테이너](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-149">For more information about container support in Azure Service Fabric, see [Service Fabric and containers](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).</span></span>

## <a name="stateless-versus-stateful-microservices"></a><span data-ttu-id="bf719-150">상태 저장 microservices와 상태 비저장</span><span class="sxs-lookup"><span data-stu-id="bf719-150">Stateless versus stateful microservices</span></span>

<span data-ttu-id="bf719-151">에서 설명한 대로 각 마이크로 서비스 (논리적 경계가 지정 된 컨텍스트) 해당 도메인 모델 (데이터와 논리)를 소유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-151">As mentioned earlier, each microservice (logical Bounded Context) must own its domain model (data and logic).</span></span> <span data-ttu-id="bf719-152">상태 비저장 microservices의 경우 데이터베이스 외부 SQL Server와 같은 관계형 옵션 또는 MongoDB 또는 Azure Cosmos DB와 같은 NoSQL 옵션이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-152">In the case of stateless microservices, the databases will be external, employing relational options like SQL Server, or NoSQL options like MongoDB or Azure Cosmos DB.</span></span>

<span data-ttu-id="bf719-153">하지만 서비스 자체는 마이크로 서비스 내에서 멤버의 데이터는 서비스 패브릭에서 상태 저장 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-153">But the services themselves can also be stateful in Service Fabric, which means that the data resides within the microservice.</span></span> <span data-ttu-id="bf719-154">이 데이터는 동일한 서버의 뿐 아니라 그러나 마이크로 서비스 프로세스 메모리에 내에 있을 수 있습니다 및 하드 드라이브에 유지 다른 노드에 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-154">This data might exist not just on the same server, but within the microservice process, in memory and persisted on hard drives and replicated to other nodes.</span></span> <span data-ttu-id="bf719-155">그림 4-30 두 가지 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-155">Figure 4-30 shows the different approaches.</span></span>

![](./media/image34.png)

<span data-ttu-id="bf719-156">**그림 4-30**합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-156">**Figure 4-30**.</span></span> <span data-ttu-id="bf719-157">상태 저장 microservices와 상태 비저장</span><span class="sxs-lookup"><span data-stu-id="bf719-157">Stateless versus stateful microservices</span></span>

<span data-ttu-id="bf719-158">상태 비저장 방법을 완벽 하 게 올바른지와 방법은 전통적인 및 잘 알려진 패턴 유사 하므로 상태 저장 microservices 보다 구현 하기가 더 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-158">A stateless approach is perfectly valid and is easier to implement than stateful microservices, since the approach is similar to traditional and well-known patterns.</span></span> <span data-ttu-id="bf719-159">하지만 상태 비저장 microservices 프로세스 및 데이터 원본 간의 대기 시간을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-159">But stateless microservices impose latency between the process and data sources.</span></span> <span data-ttu-id="bf719-160">추가 캐시 및 큐를 사용 하 여 성능 개선 하려고 시도할 때 더 이동 조각도 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-160">They also involve more moving pieces when you are trying to improve performance with additional cache and queues.</span></span> <span data-ttu-id="bf719-161">결과 너무 많은 계층에 있는 복잡 한 아키텍처를 가진 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-161">The result is that you can end up with complex architectures that have too many tiers.</span></span>

<span data-ttu-id="bf719-162">반면, [상태 저장 microservices](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) 도메인 논리 및 데이터가 간의 대기 시간이 없음이 있기 때문에 고급 시나리오에서 excel 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-162">In contrast, [stateful microservices](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) can excel in advanced scenarios, because there is no latency between the domain logic and data.</span></span> <span data-ttu-id="bf719-163">많은 데이터 처리 다시 게임 엔드 서비스인 데이터베이스 및 모든 다른 대기 시간이 짧은 시나리오에서 로컬 상태에 대 한 빠른 액세스를 사용 하도록 설정 하는 상태 저장 서비스를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-163">Heavy data processing, gaming back ends, databases as a service, and other low-latency scenarios all benefit from stateful services, which enable local state for faster access.</span></span>

<span data-ttu-id="bf719-164">상태 비저장 및 상태 저장 서비스를 보완 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-164">Stateless and stateful services are complementary.</span></span> <span data-ttu-id="bf719-165">예를 들어, 볼 수 있습니다 그림 4-30에 오른쪽 다이어그램에는 상태 저장 서비스의 여러 파티션을으로 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-165">For instance, you can see in Figure 4-30, in the right diagram, that a stateful service could be split into multiple partitions.</span></span> <span data-ttu-id="bf719-166">이러한 파티션을 액세스 하려면 역할을 각 파티션의 파티션 키를 기반으로 주소를 지정 하는 방법을 알고 있는 게이트웨이 서비스 상태 비저장 서비스를 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-166">To access those partitions, you might need a stateless service acting as a gateway service that knows how to address each partition based on partition keys.</span></span>

<span data-ttu-id="bf719-167">상태 저장 서비스 단점이지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-167">Stateful services do have drawbacks.</span></span> <span data-ttu-id="bf719-168">스케일 아웃을 허용 하는 복잡성 수준을 적용 하 합니다. 상태 저장 microservices 및 분할 하는 데이터 간의 데이터 복제와 같은 작업에 대 한 일반적으로 외부 데이터베이스 시스템으로 구현할 수 있는 기능을 보내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-168">They impose a level of complexity that allows to scale out. Functionality that would usually be implemented by external database systems must be addressed for tasks such as data replication across stateful microservices and data partitioning.</span></span> <span data-ttu-id="bf719-169">그러나이 orchestrator와 같은 영역 중 하나는 [Azure 서비스 패브릭](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-platform-architecture) 와 해당 [신뢰할 수 있는 상태 저장 서비스](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) 가장 수-개발 및 상태 저장의 수명 주기를 단순화 하 여 microservices를 사용 하 여 [신뢰할 수 있는 서비스 API](https://docs.microsoft.com/azure/service-fabric/service-fabric-work-with-reliable-collections) 및 [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-169">However, this is one of the areas where an orchestrator like [Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-platform-architecture) with its [stateful reliable services](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) can help the most—by simplifying the development and lifecycle of stateful microservices using the [Reliable Services API](https://docs.microsoft.com/azure/service-fabric/service-fabric-work-with-reliable-collections) and [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).</span></span>

<span data-ttu-id="bf719-170">상태 저장 서비스 Actor 패턴을 지 원하는 및 내결함성 및 비즈니스 논리와 데이터 사이의 대기 시간을 개선 시켜 주는 허용 하는 다른 마이크로 서비스 프레임 워크는 Microsoft [식품](https://github.com/dotnet/orleans): Microsoft Research 를[ Akka.NET](http://getakka.net/)합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-170">Other microservice frameworks that allow stateful services, that support the Actor pattern, and that improve fault tolerance and latency between business logic and data are Microsoft [Orleans](https://github.com/dotnet/orleans), from Microsoft Research, and [Akka.NET](http://getakka.net/).</span></span> <span data-ttu-id="bf719-171">현재 두 프레임 워크 Docker에 대 한 지원을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-171">Both frameworks are currently improving their support for Docker.</span></span>

<span data-ttu-id="bf719-172">Docker 컨테이너는 자체 상태 비저장 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-172">Note that Docker containers are themselves stateless.</span></span> <span data-ttu-id="bf719-173">상태 저장 서비스를 구현 하려는 경우 앞에서 기록한 추가 규정 및 상위 수준 프레임 워크 중 하나가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf719-173">If you want to implement a stateful service, you need one of the additional prescriptive and higher-level frameworks noted earlier.</span></span> 

>[!div class="step-by-step"]
<span data-ttu-id="bf719-174">[이전] [다음]을 (scalable-available-multi-container-microservice-applications.md) (... /docker-application-development-process/index.md)</span><span class="sxs-lookup"><span data-stu-id="bf719-174">[Previous] (scalable-available-multi-container-microservice-applications.md) [Next] (../docker-application-development-process/index.md)</span></span>