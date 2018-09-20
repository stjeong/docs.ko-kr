---
title: Visual Studio Tools for Docker (Windows의 Visual Studio) 사용
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: af14c92ab27885deec878dc33e7b94035f43e65b
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46488953"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="a6665-103">Visual Studio Tools for Docker (Windows의 Visual Studio) 사용</span><span class="sxs-lookup"><span data-stu-id="a6665-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="a6665-104">개발 워크플로에서 Docker 용 Visual Studio Tools를 사용 하는 경우 Visual Studio Code 및 Docker CLI를 사용 하는 경우 워크플로 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-104">The development workflow when using Visual Studio Tools for Docker is similar to the workflow when using Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="a6665-105">실제로 동일한 Docker CLI는 기반 하지만 시작 하기가, 프로세스를 단순화 하 고 향상 된 생산성을 제공 합니다. 빌드를 실행 하 고 작업을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-105">In fact, it's based on the same Docker CLI, but it's easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="a6665-106">실행 하 고 f5 키 또는 Ctrl + f5를 눌러 Visual Studio에서와 같은 간단한 작업을 통해 컨테이너를 디버그할 수 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-106">It's also able to execute and debug your containers via simple actions like F5 and Ctrl+F5 from Visual Studio.</span></span> <span data-ttu-id="a6665-107">실행 하 고 단일 컨테이너를 디버그할 수 있을 뿐 아니라 선택적 컨테이너 오케스트레이션 지원 기능을 사용 하 여 실행 하 고 동시에 컨테이너 (전체 솔루션)의 그룹을 디버그할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-107">With the optional container orchestration support, in addition to being able to run and debug a single container, you can run and debug a group of containers (a whole solution) at the same time.</span></span> <span data-ttu-id="a6665-108">동일한 컨테이너를 정의할 *docker compose.yml* 솔루션 수준 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-108">Just define the containers in the same *docker-compose.yml* file at the solution level.</span></span>

## <a name="configuring-your-local-environment"></a><span data-ttu-id="a6665-109">로컬 환경 구성</span><span class="sxs-lookup"><span data-stu-id="a6665-109">Configuring your local environment</span></span>

<span data-ttu-id="a6665-110">Docker 지원은 설치 하는.NET 및.NET Core 워크 로드를 사용 하 여 Visual Studio 2017에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-110">Docker support is included in Visual Studio 2017 with any of the .NET and .NET Core workloads installed.</span></span> <span data-ttu-id="a6665-111">Docker에 대 한 Windows를 별도로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-111">Install Docker for Windows separately.</span></span>

<span data-ttu-id="a6665-112">Docker에 대 한 Windows의 최신 버전을 계속 하려면 Docker 응용 프로그램 설치 프로그램은 다음 참조에 설명 된 대로 간단 하기 때문에 개발 보다 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-112">With the latest versions of Docker for Windows, it is easier than ever to develop Docker applications because the setup is straightforward, as explained in the following references.</span></span>

<span data-ttu-id="a6665-113">**자세한 정보:** 이동할 Docker에 대 한 Windows를 설치 하는 방법에 대 한 자세한 내용은 <https://docs.docker.com/docker-for-windows/>합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-113">**More info:** To learn more about installing Docker for Windows, go to <https://docs.docker.com/docker-for-windows/>.</span></span>

<span data-ttu-id="a6665-114">**자세한 정보:** 이동할를 Visual Studio 설치에 대 한 [ https://visualstudio.microsoft.com/downloads/ ](https://visualstudio.microsoft.com/downloads/)합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-114">**More info:** For instructions on installing Visual Studio, go to [https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="a6665-115">Visual Studio Tools for Docker 설치 하는 방법에 대 한 자세한 내용은로 이동 <http://aka.ms/vstoolsfordocker> 고 <https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>입니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-115">To see more about installing Visual Studio Tools for Docker, go to <http://aka.ms/vstoolsfordocker> and <https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>.</span></span>

## <a name="using-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="a6665-116">Docker 도구를 사용 하 여 Visual Studio 2017에서</span><span class="sxs-lookup"><span data-stu-id="a6665-116">Using Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="a6665-117">프로젝트에 Docker 지원을 추가 하는 경우 (그림 4-26 참조) Visual Studio 추가 *Dockerfile* 프로젝트 루트에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-117">When adding Docker support to a project (see Figure 4-26), Visual Studio adds a *Dockerfile* to the project root.</span></span>

![Visual Studio 2017 프로젝트에 Docker 솔루션 지원을 켜기](./media/image32.png)

<span data-ttu-id="a6665-119">그림 4-26: Visual Studio 2017 프로젝트에 Docker 솔루션 지원을 켜기</span><span class="sxs-lookup"><span data-stu-id="a6665-119">Figure 4-26: Turning on Docker Solution support in a Visual Studio 2017 project</span></span>

 <span data-ttu-id="a6665-120">Docker Compose를 통해 컨테이너 오케스트레이션을 지원, Visual Studio 2017 버전 15.7 또는 이전 버전에서 기본적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-120">Container orchestration support, via Docker Compose, is added by default in Visual Studio 2017 versions 15.7 or earlier.</span></span> <span data-ttu-id="a6665-121">컨테이너 오케스트레이션 지원은 Visual Studio 2017 버전 15.8 하는 옵트인 기능 또는 나중에 경우에서 Docker Compose 및 Service Fabric 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-121">Container orchestration support is an opt-in feature in Visual Studio 2017 versions 15.8 or later, in which case Docker Compose and Service Fabric are supported.</span></span>

<span data-ttu-id="a6665-122">15.8 이상 버전의 Visual Studio를 사용 하 여 연결 된 컨테이너를 포함 하는 솔루션의 여러 프로젝트에 대 한 지원을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-122">With Visual Studio version 15.8 and later, you can add support for multiple projects in a solution that each have an associated container.</span></span> <span data-ttu-id="a6665-123">솔루션 또는 프로젝트 노드를 마우스 오른쪽 단추로 클릭 **솔루션 탐색기**, 선택한 **추가** > **컨테이너 오케스트레이션을 지원**합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-123">Right-click on the solution or project node in **Solution Explorer**, and choose **Add** > **Container Orchestration Support**.</span></span>  <span data-ttu-id="a6665-124">선택한 **Docker Compose** 또는 **Service Fabric** 컨테이너를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-124">Then choose **Docker Compose** or **Service Fabric** to manage the containers.</span></span>

<span data-ttu-id="a6665-125">선택 하는 경우 **Docker Compose**, Visual Studio 솔루션에 서비스 섹션을 추가한 *docker compose.yml* 파일 (또는 존재 하지 않는 경우 파일을 만듭니다).</span><span class="sxs-lookup"><span data-stu-id="a6665-125">When you choose **Docker Compose**, Visual Studio adds a service section in your solution's *docker-compose.yml* files (or creates the files if they didn't exist).</span></span> <span data-ttu-id="a6665-126">다중 컨테이너 솔루션을 작성 하려면 하는 쉬운 방법 열 수를 *docker compose.yml* 파일과 추가 기능을 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-126">It's an easy way to begin composing your multi-container solution; you then can open the *docker-compose.yml* files and update them with additional features.</span></span>

<span data-ttu-id="a6665-127">필수 구성 줄의 코드를 추가 하는이 작업을 *docker compose.yml* 솔루션 수준에서 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-127">This action adds the required configuration lines of code to a *docker-compose.yml* set at the solution level.</span></span>

<span data-ttu-id="a6665-128">또한 켤 수 있습니다 Docker 지원을 Visual Studio 2017에 ASP.NET Core 프로젝트를 만들 때 그림 4-27에서와 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-128">You also can turn on Docker support when creating an ASP.NET Core project in Visual Studio 2017, as shown in Figure 4-27.</span></span>

![프로젝트를 만들 때 Docker 지원 설정](./media/image33.png)

<span data-ttu-id="a6665-130">프로젝트를 만들 때 그림 4-27: Docker 지원 켜기</span><span class="sxs-lookup"><span data-stu-id="a6665-130">Figure 4-27: Turning on Docker support when creating a project</span></span>

<span data-ttu-id="a6665-131">Visual Studio에서 솔루션에 Docker 지원을 추가 하면도 표시 됩니다에 새 노드 트리 **솔루션 탐색기** 추가 된 *docker compose.yml* 그림 4-28에서 보듯이 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-131">After you add Docker support to your solution in Visual Studio, you also will see a new node tree in **Solution Explorer** with the added *docker-compose.yml* files, as depicted in Figure 4-28.</span></span>

![솔루션 탐색기에서 docker compose.yml 파일 표시](./media/image34.PNG)

<span data-ttu-id="a6665-133">그림 4-28: docker compose.yml 파일에서 이제 표시 **솔루션 탐색기**</span><span class="sxs-lookup"><span data-stu-id="a6665-133">Figure 4-28: docker-compose.yml files now display in **Solution Explorer**</span></span>

<span data-ttu-id="a6665-134">단일을 사용 하 여 다중 컨테이너 앱을 배포할 수 있습니다 *docker compose.yml* 실행 하면 파일 `docker-compose up`소비량이 적어지지만 Visual Studio (개발 또는 환경에 따라 값을 재정의할 수 있도록 그룹을 추가 프로덕션) 및 실행 (릴리스 또는 디버그)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-134">You could deploy a multi-container app by using a single *docker-compose.yml* file when you run `docker-compose up`; however, Visual Studio adds a group of them, so you can override values depending on the environment (development versus production) and the execution type (release versus debug).</span></span> <span data-ttu-id="a6665-135">이 기능은 뒷부분에서 더 잘 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-135">This capability is better explained in later chapters.</span></span>

<span data-ttu-id="a6665-136">여러 컨테이너를 관리 하 Service Fabric Docker Compose 대신 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-136">You can also use Service Fabric instead of Docker Compose to manage multiple containers.</span></span> <span data-ttu-id="a6665-137">참조 [자습서: Azure Service Fabric에 Windows 컨테이너에서.NET 응용 프로그램을 배포](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container)합니다.</span><span class="sxs-lookup"><span data-stu-id="a6665-137">See [Tutorial: Deploy a .NET application in a Windows container to Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container).</span></span>

<span data-ttu-id="a6665-138">**자세한 정보:** 서비스 구현 및 Visual Studio Tools for Docker 사용에 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6665-138">**More info:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="a6665-139">빌드, 디버그, 업데이트 및 로컬 Docker 컨테이너에서 앱을 새로 고칩니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="a6665-139">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="a6665-140">ASP.NET Core Docker 컨테이너를 컨테이너 레지스트리에 배포 합니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="a6665-140">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="a6665-141">[이전](docker-apps-inner-loop-workflow.md)
[다음](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="a6665-141">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>
