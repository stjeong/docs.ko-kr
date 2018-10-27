---
title: Docker란?
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: 056fb613c078cc407380060dc11890406ac8cffd
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50044732"
---
# <a name="what-is-docker"></a><span data-ttu-id="ce0eb-103">Docker란?</span><span class="sxs-lookup"><span data-stu-id="ce0eb-103">What is Docker?</span></span>

<span data-ttu-id="ce0eb-104">[Docker](https://www.docker.com/) 되는 [오픈 소스 프로젝트](https://github.com/docker/docker) 클라우드 또는 온-프레미스에서 실행할 수 있는 자체 충족 적 이동식 컨테이너를 응용 프로그램 배포를 자동화 하는 것에 대 한 (참조 그림 1-2).</span><span class="sxs-lookup"><span data-stu-id="ce0eb-104">[Docker](https://www.docker.com/) is an [open-source project](https://github.com/docker/docker) for automating the deployment of applications as portable, self-sufficient containers that can run in the cloud or on-premises (see Figure 1-2).</span></span> <span data-ttu-id="ce0eb-105">Docker 이기도 한 [회사](https://www.docker.com/) 장려 하 고이 기술은 클라우드, Linux 및 Windows 공급 업체를 비롯 하 여 Microsoft와 공동 작업에서 작업을 개발 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-105">Docker is also a [company](https://www.docker.com/) that promotes and develops this technology, working in collaboration with cloud, Linux, and Windows vendors, including Microsoft.</span></span>

![](./media/image2.png)

<span data-ttu-id="ce0eb-106">그림 1-2: Docker 하이브리드 클라우드의 모든 계층에서 컨테이너를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-106">Figure 1-2: Docker deploys containers at all layers of the hybrid cloud</span></span>

<span data-ttu-id="ce0eb-107">Docker 이미지 컨테이너는 Linux 및 Windows에서 기본적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-107">Docker image containers can run natively on Linux and Windows.</span></span> <span data-ttu-id="ce0eb-108">그러나 Windows 이미지 Windows 호스트 에서만 실행할 수 있으며 Linux 이미지는 Linux 호스트, 즉 호스트 서버 또는 VM에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-108">However, Windows images can run only on Windows hosts and Linux images can run only on Linux hosts, meaning a host server or a VM.</span></span>

<span data-ttu-id="ce0eb-109">개발자는 Windows, Linux 또는 macOS에서 개발 환경을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-109">Developers can use development environments on Windows, Linux, or macOS.</span></span> <span data-ttu-id="ce0eb-110">개발 컴퓨터의 개발자는 docker 이미지가 배포 된 앱 및 해당 종속성을 포함 하 여 Docker 호스트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-110">On the development computer, the developer runs a Docker host to which Docker images are deployed, including the app and its dependencies.</span></span> <span data-ttu-id="ce0eb-111">Linux 또는 Mac에서 작업하는 개발자는 Linux 기반의 Docker 호스트를 사용하고 Linux 컨테이너용 이미지만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-111">Developers who work on Linux or on the Mac use a Docker host that is Linux based, and they can create images only for Linux containers.</span></span> <span data-ttu-id="ce0eb-112">(Mac에서 작업 하는 개발자 코드를 편집 하거나 Docker 명령줄 인터페이스를 실행할 수 있습니다 \[CLI\] 컨테이너 macOS에서 하지만이 문서의 작성 시점 현재, macOS에서 직접 실행 되지 않습니다.) Windows에서 작업하는 개발자는 Linux 또는 Windows 컨테이너용 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-112">(Developers working on the Mac can edit code or run the Docker command-line interface \[CLI\] from macOS, but, as of this writing, containers do not run directly on macOS.) Developers who work on Windows can create images for either Linux or Windows Containers.</span></span>

<span data-ttu-id="ce0eb-113">개발 환경에서 컨테이너를 호스트하고 추가 개발자 도구를 제공하기 위해 Docker는 Windows 또는 macOS용 [Docker CE(Community Edition)](https://www.docker.com/community-edition)를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-113">To host containers in development environments and provide additional developer tools, Docker ships [Docker Community Edition (CE)](https://www.docker.com/community-edition) for Windows or for macOS.</span></span> <span data-ttu-id="ce0eb-114">이러한 제품은 컨테이너를 호스트하는 데 필요한 VM(Docker 호스트)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-114">These products install the necessary VM (the Docker host) to host the containers.</span></span> <span data-ttu-id="ce0eb-115">Docker는 기업 개발용으로 설계되고 프로덕션 환경에서 대규모의 업무상 중요한 응용 프로그램을 빌드, 제공 및 실행하는 IT 팀에서 사용되는 [Docker EE(Enterprise Edition)](https://www.docker.com/enterprise-edition)도 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-115">Docker also makes available [Docker Enterprise Edition (EE)](https://www.docker.com/enterprise-edition), which is designed for enterprise development and is used by IT teams who build, ship, and run large business-critical applications in production.</span></span>

<span data-ttu-id="ce0eb-116">[Windows 컨테이너](/virtualization/windowscontainers/about/)를 실행하기 위해 다음 두 가지 유형의 런타임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-116">To run [Windows Containers](/virtualization/windowscontainers/about/), there are two types of runtimes:</span></span>

-   <span data-ttu-id="ce0eb-117">**Windows Server 컨테이너** 이 런타임 프로세스 및 네임 스페이스 격리 기술을 통해 응용 프로그램 격리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-117">**Windows Server Container** This runtime provides application isolation through process and namespace isolation technology.</span></span> <span data-ttu-id="ce0eb-118">Windows Server 컨테이너는 컨테이너 호스트와 호스트에서 실행 중인 모든 컨테이너와 커널을 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-118">A Windows Server Container shares a kernel with the container host and with all containers running on the host.</span></span>

-   <span data-ttu-id="ce0eb-119">**Hyper-v 컨테이너** 이 각 컨테이너를 고도로 최적화 된 VM에서 실행 하 여 Windows Server 컨테이너에서 제공 하는 격리를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-119">**Hyper-V Container** This expands on the isolation provided by Windows Server Containers by running each container in a highly optimized VM.</span></span> <span data-ttu-id="ce0eb-120">이 구성에서 컨테이너 호스트의 커널은 Hyper-V 컨테이너와 공유되지 않으므로 격리 기능이 향상됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-120">In this configuration, the kernel of the container host is not shared with the Hyper-V Containers, providing better isolation.</span></span>

<span data-ttu-id="ce0eb-121">이러한 컨테이너 이미지를 동일한 방식으로 생성 되 고 동일 하 게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-121">The images for these containers are created in the same way and function the same.</span></span> <span data-ttu-id="ce0eb-122">차이점은 컨테이너 이미지에서 만들어지는 방법을-Hyper-v 컨테이너를 실행에 추가 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-122">The difference is in how the container is created from the image—running a Hyper-V Container requires an extra parameter.</span></span> <span data-ttu-id="ce0eb-123">자세한 내용은 [Hyper-V 컨테이너](/virtualization/windowscontainers/about/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-123">For details, see [Hyper-V Containers](/virtualization/windowscontainers/about/).</span></span>

## <a name="comparing-docker-containers-with-vms"></a><span data-ttu-id="ce0eb-124">Vm 사용 하 여 Docker 컨테이너 비교</span><span class="sxs-lookup"><span data-stu-id="ce0eb-124">Comparing Docker containers with VMs</span></span>

<span data-ttu-id="ce0eb-125">그림 1-3 Vm과 Docker 비교를 보여 줍니다. 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-125">Figure 1-3 shows a comparison between VMs and Docker containers.</span></span>

<span data-ttu-id="ce0eb-126">컨테이너는 훨씬 더 적은 리소스가 필요 하기 때문에 (예를 들어 필요가 없습니다 전체 OS)를 쉽게 배포할 수 있으며 빠른 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-126">Because containers require far fewer resources (for example, they do not need a full OS), they are easy to deploy and they start fast.</span></span> <span data-ttu-id="ce0eb-127">이렇게 하면 더 높은 밀도 줄여 비용 동일한 하드웨어 단위에서 더 많은 서비스를 실행할 수 있습니다 의미 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-127">This makes it possible for you to have higher density, meaning that you can run more services on the same hardware unit, thereby reducing costs.</span></span>

<span data-ttu-id="ce0eb-128">동일한 커널에서 실행의 부작용을으로 Vm 보다는 격리가 덜 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-128">As a side effect of running on the same kernel, you achieve less isolation than VMs.</span></span>

<span data-ttu-id="ce0eb-129">이미지의 주요 목표는 서로 다른 배포에서 환경(종속성)을 동일하게 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-129">The main goal of an image is that it makes the environment (dependencies) the same across different deployments.</span></span> <span data-ttu-id="ce0eb-130">즉, 컴퓨터에서 이를 디버그한 다음, 동일한 환경의 다른 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-130">This means that you can debug it on your machine and then deploy it to another machine with the same environment guaranteed.</span></span>

<span data-ttu-id="ce0eb-131">컨테이너 이미지는 앱 또는 서비스를 패키지 하 고 안정적이 고 재현 가능한 방식으로 배포 하는 방법을 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-131">A container image is a way to package an app or service and deploy it in a reliable and reproducible manner.</span></span> <span data-ttu-id="ce0eb-132">이러한 점에서 Docker는 기술만 아닙니다, 그리고 그리고 개념 및 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-132">In this respect, Docker is not only a technology, it's also a philosophy and a process.</span></span>

<span data-ttu-id="ce0eb-133">Docker를 사용 하는 경우 예를 들어 개발자를 들에서는 "작동 내 컴퓨터에서 없습니까 프로덕션 환경에서?"</span><span class="sxs-lookup"><span data-stu-id="ce0eb-133">When using Docker, you will not hear developers say, "It works on my machine, why not in production?"</span></span> <span data-ttu-id="ce0eb-134">단순히 말할 수, "Docker에서 실행" 모든 지원 되는 Docker 환경에서 패키지에 포함 된 Docker 응용 프로그램을 실행할 수 있습니다 하 고 모든 배포 대상 (개발, QA, 스테이징, 프로덕션 등.)에서 원래 방식으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce0eb-134">They can simply say, "It runs on Docker," because the packaged Docker application can be run on any supported Docker environment, and it will run the way it was intended to on all deployment destinations (Dev, QA, staging, production, etc.).</span></span>

![](./media/image3.png)

<span data-ttu-id="ce0eb-135">그림 1-3: 기존 Vm Docker 컨테이너 비교</span><span class="sxs-lookup"><span data-stu-id="ce0eb-135">Figure 1-3: Comparison of traditional VMs to Docker containers</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="ce0eb-136">[이전](index.md)
[다음](docker-terminology.md)</span><span class="sxs-lookup"><span data-stu-id="ce0eb-136">[Previous](index.md)
[Next](docker-terminology.md)</span></span>
