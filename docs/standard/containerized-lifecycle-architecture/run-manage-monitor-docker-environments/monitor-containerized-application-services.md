---
title: 컨테이너 화 된 응용 프로그램 서비스를 모니터링 합니다.
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 4bdc4470624ce6e905ab858a2bd8b607c8d3d646
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44064331"
---
# <a name="monitor-containerized-application-services"></a><span data-ttu-id="15349-103">컨테이너 화 된 응용 프로그램 서비스를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-103">Monitor containerized application services</span></span>

<span data-ttu-id="15349-104">이 응용 프로그램 컨테이너 및 마이크로 서비스를 여러 분할을 모니터링 하 고 응용 프로그램의 동작을 분석 하는 방법이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-104">It is critical for applications split into multiple containers and microservices to have a way to monitor and analyze the behavior of the application.</span></span>

## <a name="microsoft-application-insights"></a><span data-ttu-id="15349-105">Microsoft Application Insights</span><span class="sxs-lookup"><span data-stu-id="15349-105">Microsoft Application Insights</span></span>

<span data-ttu-id="15349-106">[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) 라이브 응용 프로그램을 모니터링 하는 확장 가능한 분석 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="15349-106">[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) is an extensible analytics service that monitors your live application.</span></span> <span data-ttu-id="15349-107">성능 문제 감지 및 진단 하는 데 실제로 할 앱을 사용 하 여 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15349-107">It helps you to detect and diagnose performance issues and to understand what users actually do with your app.</span></span> <span data-ttu-id="15349-108">지속적으로 성능을 향상 시킬 수 있도록 의도 및 서비스 또는 응용 프로그램의 사용 편의성을 사용 하 여 개발자를 위해 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="15349-108">It's designed for developers, with the intent of helping you to continuously improve the performance and usability of your services or applications.</span></span> <span data-ttu-id="15349-109">Application Insights에서 다양 한 플랫폼 같은.NET, Java, Node.js 및 기타 여러 플랫폼, 호스팅된 온-프레미스 또는 클라우드에서 앱을 웹/서비스와 독립 실행형을 사용 하 여 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-109">Application Insights works with both web/services and standalone apps on a wide variety of platforms like .NET, Java, Node.js and many other platforms, hosted on-premises or in the cloud.</span></span>

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a><span data-ttu-id="15349-110">Application Insights를 사용 하 여 QA 환경에서 Docker 앱 분석</span><span class="sxs-lookup"><span data-stu-id="15349-110">Analyzing Docker apps in QA environments using Application Insights</span></span>

<span data-ttu-id="15349-111">Docker에 관련 된 수명 주기 이벤트 및 Application Insights에서 Docker 컨테이너에서 성능 카운터를 차트로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15349-111">As it pertains to Docker, you can chart life-cycle events and performance counters from Docker containers on Application Insights.</span></span> <span data-ttu-id="15349-112">실행 해야 합니다 [Application Insights Docker 이미지](https://hub.docker.com/r/microsoft/applicationinsights/) 컨테이너 호스트에 다른 Docker 이미지 뿐만 아니라 호스트에 대 한 성능 카운터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-112">You just need to run the [Application Insights Docker image](https://hub.docker.com/r/microsoft/applicationinsights/) as a container in your host, and it will display performance counters for the host as well as for the other Docker images.</span></span> <span data-ttu-id="15349-113">이 Application Insights Docker 이미지 (그림 6-1) 성능 및 Docker 호스트 (즉, Linux Vm), Docker 컨테이너 및 실행 중인 응용 프로그램의 활동에 대 한 원격 분석을 수집 하 여 컨테이너 화 된 응용 프로그램을 모니터링할 수 있습니다 내에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15349-113">This Application Insights Docker image (Figure 6-1) helps you to monitor your containerized applications by collecting telemetry about the performance and activity of your Docker host (that is, your Linux VMs), Docker containers and the applications running within them.</span></span>

![예제](./media/image1.png)

<span data-ttu-id="15349-115">그림 6-1: Application Insights Docker 호스트 및 컨테이너를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-115">Figure 6-1: Application Insights monitoring Docker hosts and containers</span></span>

<span data-ttu-id="15349-116">실행 하는 경우는 [Application Insights Docker 이미지](https://hub.docker.com/r/microsoft/applicationinsights/) Docker 호스트에서 다음 중 하나를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-116">When you run the [Application Insights Docker image](https://hub.docker.com/r/microsoft/applicationinsights/) on your Docker host, you benefit from the following:</span></span>

-   <span data-ttu-id="15349-117">호스트에서 실행 중인 모든 컨테이너에 대 한 원격 분석 수명 주기-시작, 중지 및 등입니다.</span><span class="sxs-lookup"><span data-stu-id="15349-117">Life-cycle telemetry about all the containers running on the host—start, stop, and so on.</span></span>

-   <span data-ttu-id="15349-118">모든 컨테이너에 대 한 성능 카운터: CPU, 메모리, 네트워크 사용량 등.</span><span class="sxs-lookup"><span data-stu-id="15349-118">Performance counters for all the containers: CPU, memory, network usage, and more.</span></span>

-   <span data-ttu-id="15349-119">또한 설치 하는 경우 [Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) 컨테이너에서 실행 중인 앱에서 해당 앱의 모든 원격 분석에는 컨테이너와 호스트 컴퓨터를 식별 하는 추가적인 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15349-119">If you also installed [Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) in the apps running in the containers, all the telemetry of those apps will have additional properties identifying the container and host machine.</span></span> <span data-ttu-id="15349-120">따라서 예를 들어 둘 이상의 호스트에서 실행 되는 앱 인스턴스가 있는 경우 쉽게 수 있습니다 호스트에서 앱 원격 분석을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-120">So, for example, if you have instances of an app running in more than one host, you'll easily be able to filter your app telemetry by host.</span></span>

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a><span data-ttu-id="15349-121">Docker 응용 프로그램 및 Docker 호스트를 모니터링 하도록 Application Insights 설정</span><span class="sxs-lookup"><span data-stu-id="15349-121">Setting up Application Insights to monitor Docker applications and Docker hosts</span></span>

<span data-ttu-id="15349-122">Application Insights 리소스를 만들려면 다음에 나오는 목록에 표시 하는 문서에서 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="15349-122">To create an Application Insights resource, follow the instructions in the articles presented in the list that follows.</span></span> <span data-ttu-id="15349-123">Azure Portal 필요한 스크립트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15349-123">Azure Portal will create the necessary script for you.</span></span>

-   <span data-ttu-id="15349-124">**Application Insights에서 Docker 응용 프로그램을 모니터링 합니다.**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)</span><span class="sxs-lookup"><span data-stu-id="15349-124">**Monitor Docker applications in Application Insights:**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)</span></span>

-   <span data-ttu-id="15349-125">**Docker 허브 및 Github에서 application Insights Docker 이미지:**</span><span class="sxs-lookup"><span data-stu-id="15349-125">**Application Insights Docker image at Docker Hub and Github:**</span></span>  
<span data-ttu-id="15349-126">[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) 및 <https://github.com/Microsoft/ApplicationInsights-Docker></span><span class="sxs-lookup"><span data-stu-id="15349-126">[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) and <https://github.com/Microsoft/ApplicationInsights-Docker></span></span>

-   <span data-ttu-id="15349-127">**ASP.NET 용 Application Insights를 설정 합니다.**</span><span class="sxs-lookup"><span data-stu-id="15349-127">**Set up Application Insights for ASP.NET:**</span></span>  
[https://docs.microsoft.com/azure/application-insights/app-insights-asp-net](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)

-   <span data-ttu-id="15349-128">**웹 페이지 용 application Insights:**</span><span class="sxs-lookup"><span data-stu-id="15349-128">**Application Insights for web pages:**</span></span>  
<https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="microsoft-operations-management-suite"></a><span data-ttu-id="15349-129">Microsoft 작업 관리 도구 모음</span><span class="sxs-lookup"><span data-stu-id="15349-129">Microsoft Operations Management Suite</span></span>

<span data-ttu-id="15349-130">[Operations Management Suite](https://microsoft.com/oms) 는 log analytics, automation, backup, 사이트 복구를 제공 하는 간소화 된 IT 관리 솔루션입니다.</span><span class="sxs-lookup"><span data-stu-id="15349-130">[Operations Management Suite](https://microsoft.com/oms) is a simplified IT management solution that provides log analytics, automation, backup, and site recovery.</span></span> <span data-ttu-id="15349-131">에 따라 [쿼리](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/) Operations Management Suite에 올리면 [경고](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts) 재구성을 통해 설정 [Azure Automation](https://docs.microsoft.com/azure/automation/)합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-131">Based on [queries](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/) in Operations Management Suite, you can raise [alerts](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts) and set remediation via [Azure Automation](https://docs.microsoft.com/azure/automation/).</span></span> <span data-ttu-id="15349-132">단일 투명 효과 창의 보기를 제공 하 여 기존 관리 솔루션과 원활 하 게 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15349-132">It also seamlessly integrates with your existing management solutions to provide a single pane-of-glass view.</span></span> <span data-ttu-id="15349-133">Operations Management Suite를 사용 하면 온-프레미스 보호 및 클라우드 인프라 및 관리 하도록 도와줍니다.</span><span class="sxs-lookup"><span data-stu-id="15349-133">Operations Management Suite helps you to manage and protect your on-premises and cloud infrastructure.</span></span>

### <a name="operations-management-suitehttpsmicrosoftcomoms-container-solution-for-docker"></a><span data-ttu-id="15349-134">[Operations Management Suite](https://microsoft.com/oms) Docker 용 컨테이너 솔루션</span><span class="sxs-lookup"><span data-stu-id="15349-134">[Operations Management Suite](https://microsoft.com/oms) Container Solution for Docker</span></span>

<span data-ttu-id="15349-135">자체적으로 중요 한 서비스를 제공 하는 것 외에도 Operations Management Suite 컨테이너 솔루션 관리 및 모니터링할 수 Docker 호스트 및 컨테이너에 대 한 정보는 사용자 컨테이너 및 컨테이너 호스트를 표시 하 여 실행 중인 컨테이너는 실패 또는 Docker 디먼 및 컨테이너 로그를 전송 하 고 *stdout* 하 고 *stderr*합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-135">In addition to providing valuable services on its own, the Operations Management Suite Container Solution can manage and monitor Docker hosts and containers by showing information about where your containers and container hosts are, which containers are running or failed, and Docker daemon and container logs sent to *stdout* and *stderr*.</span></span> <span data-ttu-id="15349-136">또한 CPU, 메모리, 네트워크 및 저장소 등 컨테이너 및 호스트에 대한 성능 메트릭을 표시하여 문제를 해결하고, 노이지 네이버(noisy neighbor) 컨테이너를 찾을 수 있게 해줍니다.</span><span class="sxs-lookup"><span data-stu-id="15349-136">It also shows performance metrics such as CPU, memory, network, and storage for the container and hosts to help you troubleshoot and find noisy neighbor containers.</span></span>

![](./media/image2.png)

<span data-ttu-id="15349-137">Operations Management Suite에서 표시 하는 Docker 컨테이너에 대 한 그림 6-2: 정보</span><span class="sxs-lookup"><span data-stu-id="15349-137">Figure 6-2: Information about Docker containers shown by Operations Management Suite</span></span>

<span data-ttu-id="15349-138">Application Insights 및 Operations Management Suite 작업;를 모니터링에 중점 그러나 Application Insights는 앱 내에서 실행 되는 SDK 통해 앱 모니터링에 더 집중 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-138">Application Insights and Operations Management Suite both focus on monitoring activities; however, Application Insights focuses more on monitoring the apps themselves thanks to its SDK running within the app.</span></span> <span data-ttu-id="15349-139">그러나 Operations Management Suite에 중점을 둡니다 훨씬 호스트 관련 인프라와 매우 유연한 데이터 기반 검색/쿼리 시스템을 제공 하는 동안 로그 규모에 대 한 심층 분석을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-139">However, Operations Management Suite focuses much more on the infrastructure around the hosts, plus it offers deep analysis on logs at scale while providing a very flexible data-driven search/query system.</span></span>

<span data-ttu-id="15349-140">Operations Management Suite를 클라우드 기반 서비스로 구현 되므로 있습니다 해당 실행 신속 하 게 인프라 서비스에 대 한 최소한의 투자로.</span><span class="sxs-lookup"><span data-stu-id="15349-140">Because Operations Management Suite is implemented as a cloud-based service, you can have it up and running quickly with minimal investment in infrastructure services.</span></span> <span data-ttu-id="15349-141">새로운 기능이 자동적으로 전달 되므로 지속적인 유지 관리에서 절약할 및 비용을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-141">New features are delivered automatically, saving you from ongoing maintenance and upgrade costs.</span></span>

<span data-ttu-id="15349-142">Operations Management Suite 컨테이너 솔루션을 사용 하 여, 있습니다 다음을 수행할 수 있습니다.:</span><span class="sxs-lookup"><span data-stu-id="15349-142">Using Operations Management Suite Container Solution, you can do the following:</span></span>

-   <span data-ttu-id="15349-143">중앙 집중화 하 고 수백만 개의 대규모 Docker 컨테이너에서 로그를 상호 연결</span><span class="sxs-lookup"><span data-stu-id="15349-143">Centralize and correlate millions of logs from Docker containers at scale</span></span>

-   <span data-ttu-id="15349-144">단일 위치에서 모든 컨테이너 호스트에 대 한 정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15349-144">See information about all container hosts in a single location</span></span>

-   <span data-ttu-id="15349-145">알고 있는 컨테이너를 실행 하는 어떤 이미지를 실행 및 실행 하는 위치</span><span class="sxs-lookup"><span data-stu-id="15349-145">Know which containers are running, what image they're running, and where they're running</span></span>

-   <span data-ttu-id="15349-146">컨테이너 호스트에서 문제가 발생할 수 있는 "시끄러운 이웃" 컨테이너를 빠르게 진단</span><span class="sxs-lookup"><span data-stu-id="15349-146">Quickly diagnose "noisy neighbor" containers that can cause problems on container hosts</span></span>

-   <span data-ttu-id="15349-147">컨테이너에 대 한 작업에 대 한 감사 내역을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15349-147">See an audit trail for actions on containers</span></span>

-   <span data-ttu-id="15349-148">원격 Docker 호스트에 없이 중앙 집중식된 로그를 검색 하 여 문제 해결</span><span class="sxs-lookup"><span data-stu-id="15349-148">Troubleshoot by viewing and searching centralized logs without remoting to the Docker hosts</span></span>

-   <span data-ttu-id="15349-149">"시끄러운 이웃" 및 호스트에 과도 한 리소스 소비 될 수 있는 컨테이너를 찾을</span><span class="sxs-lookup"><span data-stu-id="15349-149">Find containers that might be "noisy neighbors" and consuming excess resources on a host</span></span>

-   <span data-ttu-id="15349-150">중앙화 된 CPU, 메모리, 저장소 및 컨테이너에 대 한 네트워크 사용량 및 성능 정보를 보려면</span><span class="sxs-lookup"><span data-stu-id="15349-150">View centralized CPU, memory, storage, and network usage and performance information for containers</span></span>

-   <span data-ttu-id="15349-151">생성 Azure Automation을 사용 하 여 Docker 컨테이너를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-151">Generate test Docker containers with Azure Automation</span></span>

<span data-ttu-id="15349-152">형식이 같은 쿼리를 실행 하 여 성능 정보를 볼 수 = Perf 그림 6-3에 나와 있는 것 처럼 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-152">You can see performance information by running queries like Type=Perf, as shown in Figure 6-3.</span></span>

![DockerPerfMetricsView](./media/image3.png)<span data-ttu-id="15349-154">{width="5.78625in" height="3.25in"}</span><span class="sxs-lookup"><span data-stu-id="15349-154">{width="5.78625in" height="3.25in"}</span></span>

<span data-ttu-id="15349-155">Operations Management Suite에서 표시 하는 Docker 호스트의 그림 6-3: 성능 메트릭</span><span class="sxs-lookup"><span data-stu-id="15349-155">Figure 6-3: Performance metrics of Docker hosts shown by Operations Management Suite</span></span>

<span data-ttu-id="15349-156">Operations Management Suite의 표준 기능은 또한 쿼리를 저장 및 도움이 될 수 있습니다 유용한 및 시스템의 추세를 검색 하는 쿼리를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="15349-156">Saving queries is also a standard feature in Operations Management Suite and can help you keep queries you've found useful and discover trends in your system.</span></span>

<span data-ttu-id="15349-157">**자세한 내용은** 의 컨테이너 솔루션 설치 및 Docker를 구성에 대 한 정보를 찾으려면 [Operations Management Suite](https://microsoft.com/oms)으로 이동 하 여 <https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>입니다.</span><span class="sxs-lookup"><span data-stu-id="15349-157">**More info** To find information on installing and configuring the Docker container solution in [Operations Management Suite](https://microsoft.com/oms), go to <https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="15349-158">[이전](manage-production-docker-environments.md)
[다음](../key-takeaways/index.md)</span><span class="sxs-lookup"><span data-stu-id="15349-158">[Previous](manage-production-docker-environments.md)
[Next](../key-takeaways/index.md)</span></span>
