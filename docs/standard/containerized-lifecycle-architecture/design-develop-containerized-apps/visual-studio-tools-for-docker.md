---
title: Visual Studio Tools for Windows의 Docker
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: cd140c12ef4a0187cce096e013937d5c98cd4b39
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47235717"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="51e02-103">Visual Studio Tools for Docker (Windows의 Visual Studio) 사용</span><span class="sxs-lookup"><span data-stu-id="51e02-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="51e02-104">Visual Studio Tools for Docker 개발자 워크플로 Visual Studio Code 및 Docker CLI (기반으로 동일한 Docker CLI)를 사용 하는 것과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-104">The Visual Studio Tools for Docker developer workflow is similar to using Visual Studio Code and Docker CLI (it is based on the same Docker CLI).</span></span> <span data-ttu-id="51e02-105">Visual Studio 도구 실행 Docker 보다 쉽게 시작 하는 프로세스를 간소화 하 고 빌드에 대 한 향상 된 생산성을 제공 및 작업을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-105">Visual Studio Tools for Docker makes it even easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="51e02-106">실행 및 디버그와 같은 간단한 작업을 통해 컨테이너 **F5** 하 고 **Ctrl**+**F5**합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-106">Execute and debug your containers via simple actions like **F5** and **Ctrl**+**F5**.</span></span>

> [!NOTE]
> <span data-ttu-id="51e02-107">이 문서에서는 mac 용, Windows에서 Visual Studio 및 Visual Studio가 아니라에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-107">This article applies to Visual Studio on Windows, and not Visual Studio for Mac.</span></span>

## <a name="configure-your-local-environment"></a><span data-ttu-id="51e02-108">로컬 환경 구성</span><span class="sxs-lookup"><span data-stu-id="51e02-108">Configure your local environment</span></span>

<span data-ttu-id="51e02-109">Docker에 대 한 Windows의 최신 버전을 사용 하 여 ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), 간단 하 게 설치를 사용 하면 쉽게 Docker 응용 프로그램을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-109">With the latest versions of Docker for Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), the straightforward setup makes it easy to develop Docker applications.</span></span>

<span data-ttu-id="51e02-110">Visual Studio 2017에 docker 지원이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-110">Docker support is included in Visual Studio 2017.</span></span> <span data-ttu-id="51e02-111">여기서 Visual Studio 2017을 다운로드 합니다. [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span><span class="sxs-lookup"><span data-stu-id="51e02-111">Download Visual Studio 2017 here: [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span></span>

## <a name="use-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="51e02-112">Visual Studio 2017에서 사용 하 여 Docker 도구</span><span class="sxs-lookup"><span data-stu-id="51e02-112">Use Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="51e02-113">두 가지 수준의 Docker 지원 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-113">There are two levels of Docker support you can add to a project.</span></span> <span data-ttu-id="51e02-114">.NET Core 웹 앱 프로젝트에 추가 하기만 하면를 *Dockerfile* 파일을 프로젝트에 Docker 지원을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-114">In .NET Core web app projects, you can just add a *Dockerfile* file to the project by enabling Docker support.</span></span> <span data-ttu-id="51e02-115">다음 수준은 추가 하는 컨테이너 오 케 스트레이 터 지원 기능을 *Dockerfile* (이미 존재 하지 않는) 하는 경우 프로젝트에 및 *docker compose.yml* 솔루션 수준 파일.</span><span class="sxs-lookup"><span data-stu-id="51e02-115">The next level is container orchestrator support, which adds a *Dockerfile* to the project (if it doesn't already exist) and a *docker-compose.yml* file at the solution level.</span></span>

<span data-ttu-id="51e02-116">합니다 **추가** > **Docker 지원** 하 고 **추가** > **컨테이너 오 케 스트레이 터 지원** 명령은 웹 앱 프로젝트의 프로젝트 노드의 오른쪽 클릭 메뉴 (또는 상황에 맞는 메뉴)에 있는 **솔루션 탐색기**그림 4-26에 표시 된 것 처럼:</span><span class="sxs-lookup"><span data-stu-id="51e02-116">The **Add** > **Docker Support** and **Add** > **Container Orchestrator Support** commands are located on the right-click menu (or context menu) of the project node for a web app project in **Solution Explorer**, as shown in Figure 4-26:</span></span>

![Visual Studio에서 메뉴 옵션을 Docker 지원 추가](media/add-docker-support-menu.png)

<span data-ttu-id="51e02-118">그림 4-26: Visual Studio 2017 프로젝트에 Docker 지원 추가</span><span class="sxs-lookup"><span data-stu-id="51e02-118">Figure 4-26: Adding Docker support to a Visual Studio 2017 project</span></span>

### <a name="add-docker-support"></a><span data-ttu-id="51e02-119">Docker 지원 추가</span><span class="sxs-lookup"><span data-stu-id="51e02-119">Add Docker support</span></span>

<span data-ttu-id="51e02-120">선택 하 여 기존.NET Core 웹 앱 프로젝트에 Docker 지원을 추가할 수 있습니다 **추가** > **Docker 지원** 에서 **솔루션 탐색기**합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-120">You can add Docker support to an existing .NET Core web app project by selecting **Add** > **Docker Support** in **Solution Explorer**.</span></span> <span data-ttu-id="51e02-121">또한 Docker 지원을 프로젝트를 만드는 동안 선택 하 여 사용할 수 있습니다 **Docker 지원 사용** 에 **새 ASP.NET Core 웹 응용 프로그램** 클릭 하면 열리는 대화 상자 **확인** 에 **새 프로젝트** 그림 4-27에서와 같이 대화 상자.</span><span class="sxs-lookup"><span data-stu-id="51e02-121">You can also enable Docker support during project creation by selecting **Enable Docker Support** in the **New ASP.NET Core Web Application** dialog box that opens after you click **OK** in the **New Project** dialog box, as shown in Figure 4-27.</span></span>

![Visual Studio에서 새 ASP.NET Core 웹 앱에 대 한 Docker 지원 사용](./media/enable-docker-support-visual-studio.png)

<span data-ttu-id="51e02-123">그림 4-27: Visual Studio 2017에서 프로젝트를 만드는 동안 Docker 지원 사용</span><span class="sxs-lookup"><span data-stu-id="51e02-123">Figure 4-27: Enable Docker support during project creation in Visual Studio 2017</span></span>

<span data-ttu-id="51e02-124">를 추가 하거나 Docker 지원을 사용 하도록 설정 하는 경우 Visual Studio 추가 된 *Dockerfile* 프로젝트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-124">When you add or enable Docker support, Visual Studio adds a *Dockerfile* file to the project.</span></span>

> [!NOTE]
> <span data-ttu-id="51e02-125">그림 4-28에서와 같이.NET Framework 웹 앱 프로젝트는.NET Core 웹 앱 프로젝트가 아닌 프로젝트를 만드는 동안 Docker Compose 지원을 사용 하면 컨테이너 오 케 스트레이 터 지원도 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-125">When you enable Docker Compose support during project creation for a .NET Framework web app project (not a .NET Core web app project) as shown in Figure 4-28, container orchestrator support is also added.</span></span>
>
> ![Docker를 사용 합니다..NET Framework 웹 앱 프로젝트에 대 한 지원 구성](media/enable-docker-compose-support.png)

> <span data-ttu-id="51e02-127">그림 4-28: Visual Studio 2017에서.NET Framework 웹 앱 프로젝트에서 Docker Compose 지원을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="51e02-127">Figure 4-28: Enabling Docker Compose support on a .NET Framework web app project in Visual Studio 2017</span></span>

### <a name="add-container-orchestrator-support"></a><span data-ttu-id="51e02-128">컨테이너 orchestrator 지원 추가</span><span class="sxs-lookup"><span data-stu-id="51e02-128">Add container orchestrator support</span></span>

<span data-ttu-id="51e02-129">다중 컨테이너 솔루션을 작성 하려는 경우 프로젝트에 컨테이너 오 케 스트레이 터 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-129">When you want to compose a multicontainer solution, add container orchestrator support to your projects.</span></span> <span data-ttu-id="51e02-130">컨테이너 orchestrator 지원에 추가 하면 Visual Studio 추가 *Dockerfile* (이미 존재 하지 않는) 하는 경우 프로젝트 및 전역 *docker compose.yml* 솔루션 수준 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-130">When you add container orchestrator support, Visual Studio adds a *Dockerfile* to the project (if it doesn't already exist) and a global *docker-compose.yml* file at the solution level.</span></span> <span data-ttu-id="51e02-131">이렇게 하면 실행 하 고 같은 정의 하는 경우 컨테이너 (전체 솔루션)의 그룹을 동시에 디버깅할 수 있습니다 *docker compose.yml* 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-131">This lets you run and debug a group of containers (a whole solution) at the same time if they're defined in the same *docker-compose.yml* file.</span></span> <span data-ttu-id="51e02-132">하는 경우 *docker compose.yml* 이미 하기만 하면 Visual Studio에 필요한 구성 코드 줄을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="51e02-132">If *docker-compose.yml* already exists, Visual Studio just adds the required lines of configuration code to it.</span></span>

<span data-ttu-id="51e02-133">프로젝트에 추가 하는 Dockerfile 컨테이너 오케스트레이션을 지원 프로젝트에 추가한 후 표시와 **docker compose** 솔루션에 추가 하는 폴더 **솔루션 탐색기**그림 4-29에 표시 된 것 처럼:</span><span class="sxs-lookup"><span data-stu-id="51e02-133">After you add container orchestration support to your project, you see a Dockerfile added to the project and a **docker-compose** folder added to the solution in **Solution Explorer**, as shown in Figure 4-29:</span></span>

![Visual Studio의 솔루션 탐색기에서 docker 파일](media/docker-support-solution-explorer.png)

<span data-ttu-id="51e02-135">Visual Studio 2017의 솔루션 탐색기에서 그림 4-29: Docker 파일</span><span class="sxs-lookup"><span data-stu-id="51e02-135">Figure 4-29: Docker files in Solution Explorer in Visual Studio 2017</span></span>

<span data-ttu-id="51e02-136">**자세한 정보:** 서비스 구현 및 Visual Studio Tools for Docker 사용에 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51e02-136">**More information:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="51e02-137">빌드, 디버그, 업데이트 및 로컬 Docker 컨테이너에서 앱을 새로 고칩니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="51e02-137">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="51e02-138">ASP.NET Core Docker 컨테이너를 컨테이너 레지스트리에 배포 합니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="51e02-138">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="51e02-139">[이전](docker-apps-inner-loop-workflow.md)
[다음](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="51e02-139">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>