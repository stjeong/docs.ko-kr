---
title: Visual Studio Tools for Windows의 Docker
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: 79e9b5cc9bac317a368583013abbc5124ef2c9ac
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151215"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="39be6-103">Visual Studio Tools for Docker (Windows의 Visual Studio) 사용</span><span class="sxs-lookup"><span data-stu-id="39be6-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="39be6-104">Docker 개발 워크플로에 대 한 Visual Studio Tools-Visual Studio Code 및 Docker CLI를 사용 하는 경우 워크플로가 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-104">The Visual Studio Tools for Docker development workflow is similar to the workflow when using Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="39be6-105">실제로 동일한 Docker CLI는 기반 하지만 시작 하기가, 프로세스를 단순화 하 고 향상 된 생산성을 제공 합니다. 빌드를 실행 하 고 작업을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-105">In fact, it's based on the same Docker CLI, but it's easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="39be6-106">실행 및 디버그와 같은 간단한 작업을 통해 컨테이너 **F5** 하 고 **Ctrl**+**F5**합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-106">Execute and debug your containers via simple actions like **F5** and **Ctrl**+**F5**.</span></span> <span data-ttu-id="39be6-107">실행 하 고 단일 컨테이너를 디버그할 수 있을 뿐 아니라 선택적 컨테이너 오케스트레이션 지원 기능을 사용 하 여 실행 하 고 동시에 컨테이너 (전체 솔루션)의 그룹을 디버그할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-107">With the optional container orchestration support, in addition to being able to run and debug a single container, you can run and debug a group of containers (a whole solution) at the same time.</span></span>

> [!NOTE]
> <span data-ttu-id="39be6-108">이 문서에서는 mac 용, Windows에서 Visual Studio 및 Visual Studio가 아니라에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-108">This article applies to Visual Studio on Windows, and not Visual Studio for Mac.</span></span>

## <a name="configure-your-local-environment"></a><span data-ttu-id="39be6-109">로컬 환경 구성</span><span class="sxs-lookup"><span data-stu-id="39be6-109">Configure your local environment</span></span>

<span data-ttu-id="39be6-110">Docker에 대 한 Windows의 최신 버전을 사용 하 여 ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), 간단 하 게 설치를 사용 하면 쉽게 Docker 응용 프로그램을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-110">With the latest versions of Docker for Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), the straightforward setup makes it easy to develop Docker applications.</span></span>

<span data-ttu-id="39be6-111">Visual Studio 2017에 docker 지원이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-111">Docker support is included in Visual Studio 2017.</span></span> <span data-ttu-id="39be6-112">여기서 Visual Studio 2017을 다운로드 합니다. [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span><span class="sxs-lookup"><span data-stu-id="39be6-112">Download Visual Studio 2017 here: [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span></span>

## <a name="use-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="39be6-113">Visual Studio 2017에서 사용 하 여 Docker 도구</span><span class="sxs-lookup"><span data-stu-id="39be6-113">Use Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="39be6-114">두 가지 수준의 Docker 지원 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-114">There are two levels of Docker support you can add to a project.</span></span> <span data-ttu-id="39be6-115">.NET Core 웹 앱 프로젝트에 추가 하기만 하면를 *Dockerfile* 파일을 프로젝트에 Docker 지원을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-115">In .NET Core web app projects, you can just add a *Dockerfile* file to the project by enabling Docker support.</span></span> <span data-ttu-id="39be6-116">다음 수준이 추가 하는 컨테이너 오케스트레이션 지원 기능을 *Dockerfile* (이미 존재 하지 않는) 하는 경우 프로젝트에 및 *docker compose.yml* 솔루션 수준 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-116">The next level is container orchestration support, which adds a *Dockerfile* to the project (if it doesn't already exist) and a *docker-compose.yml* file at the solution level.</span></span> <span data-ttu-id="39be6-117">Docker Compose를 통해 컨테이너 오케스트레이션을 지원, Visual Studio 2017 버전 15.7 또는 이전 버전에서 기본적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-117">Container orchestration support, via Docker Compose, is added by default in Visual Studio 2017 versions 15.7 or earlier.</span></span> <span data-ttu-id="39be6-118">컨테이너 오케스트레이션 지원은 Visual Studio 2017 버전 15.8 하는 옵트인 기능 또는 나중에 경우에서 Docker Compose 및 Service Fabric 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-118">Container orchestration support is an opt-in feature in Visual Studio 2017 versions 15.8 or later, in which case Docker Compose and Service Fabric are supported.</span></span>

<span data-ttu-id="39be6-119">합니다 **추가** > **Docker 지원** 하 고 **추가** > **컨테이너 오케스트레이션을 지원** 명령은 웹 앱 프로젝트의 프로젝트 노드의 오른쪽 클릭 메뉴 (또는 상황에 맞는 메뉴)에 있는 **솔루션 탐색기**그림 4-26에 표시 된 것 처럼:</span><span class="sxs-lookup"><span data-stu-id="39be6-119">The **Add** > **Docker Support** and **Add** > **Container orchestration Support** commands are located on the right-click menu (or context menu) of the project node for a web app project in **Solution Explorer**, as shown in Figure 4-26:</span></span>

![Visual Studio에서 메뉴 옵션을 Docker 지원 추가](media/add-docker-support-menu.png)

<span data-ttu-id="39be6-121">그림 4-26: Visual Studio 2017 프로젝트에 Docker 지원 추가</span><span class="sxs-lookup"><span data-stu-id="39be6-121">Figure 4-26: Adding Docker support to a Visual Studio 2017 project</span></span>

### <a name="add-docker-support"></a><span data-ttu-id="39be6-122">Docker 지원 추가</span><span class="sxs-lookup"><span data-stu-id="39be6-122">Add Docker support</span></span>

<span data-ttu-id="39be6-123">선택 하 여 기존.NET Core 웹 앱 프로젝트에 Docker 지원을 추가할 수 있습니다 **추가** > **Docker 지원** 에서 **솔루션 탐색기**합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-123">You can add Docker support to an existing .NET Core web app project by selecting **Add** > **Docker Support** in **Solution Explorer**.</span></span> <span data-ttu-id="39be6-124">또한 Docker 지원을 프로젝트를 만드는 동안 선택 하 여 사용할 수 있습니다 **Docker 지원 사용** 에 **새 ASP.NET Core 웹 응용 프로그램** 클릭 하면 열리는 대화 상자 **확인** 에 **새 프로젝트** 그림 4-27에서와 같이 대화 상자.</span><span class="sxs-lookup"><span data-stu-id="39be6-124">You can also enable Docker support during project creation by selecting **Enable Docker Support** in the **New ASP.NET Core Web Application** dialog box that opens after you click **OK** in the **New Project** dialog box, as shown in Figure 4-27.</span></span>

![Visual Studio에서 새 ASP.NET Core 웹 앱에 대 한 Docker 지원 사용](./media/enable-docker-support-visual-studio.png)

<span data-ttu-id="39be6-126">그림 4-27: Visual Studio 2017에서 프로젝트를 만드는 동안 Docker 지원을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="39be6-126">Figure 4-27: Enable Docker support during project creation in Visual Studio 2017</span></span>

<span data-ttu-id="39be6-127">를 추가 하거나 Docker 지원을 사용 하도록 설정 하는 경우 Visual Studio 추가 된 *Dockerfile* 프로젝트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-127">When you add or enable Docker support, Visual Studio adds a *Dockerfile* file to the project.</span></span>

> [!NOTE]
> <span data-ttu-id="39be6-128">그림 4-28에서와 같이.NET Framework 웹 앱 프로젝트는.NET Core 웹 앱 프로젝트가 아닌 프로젝트를 만드는 동안 Docker Compose 지원을 사용 하면 컨테이너 오케스트레이션을 지원도 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-128">When you enable Docker Compose support during project creation for a .NET Framework web app project (not a .NET Core web app project) as shown in Figure 4-28, container orchestration support is also added.</span></span>
>
> ![Docker를 사용 합니다..NET Framework 웹 앱 프로젝트에 대 한 지원 구성](media/enable-docker-compose-support.png)

> <span data-ttu-id="39be6-130">그림 4-28: Visual Studio 2017에서.NET Framework 웹 앱 프로젝트에서 Docker Compose 지원을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="39be6-130">Figure 4-28: Enabling Docker Compose support on a .NET Framework web app project in Visual Studio 2017</span></span>

### <a name="add-container-orchestration-support"></a><span data-ttu-id="39be6-131">컨테이너 오케스트레이션을 지원 추가</span><span class="sxs-lookup"><span data-stu-id="39be6-131">Add container orchestration support</span></span>

<span data-ttu-id="39be6-132">다중 컨테이너 솔루션을 작성 하려는 경우 컨테이너 오케스트레이션을 지원 프로젝트에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-132">When you want to compose a multicontainer solution, add container orchestration support to your projects.</span></span> <span data-ttu-id="39be6-133">이렇게 하면 실행 하 고 같은 정의 하는 경우 컨테이너 (전체 솔루션)의 그룹을 동시에 디버깅할 수 있습니다 *docker compose.yml* 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-133">This lets you run and debug a group of containers (a whole solution) at the same time if they're defined in the same *docker-compose.yml* file.</span></span>

<span data-ttu-id="39be6-134">컨테이너 오케스트레이션을 지원 기능을 추가 하려면 마우스 오른쪽 단추로 클릭에서 솔루션 또는 프로젝트 노드 **솔루션 탐색기**, 선택한 **추가** > **컨테이너 오케스트레이션지원**.</span><span class="sxs-lookup"><span data-stu-id="39be6-134">To add container orchestration support, right-click on the solution or project node in **Solution Explorer**, and choose **Add** > **Container Orchestration Support**.</span></span> <span data-ttu-id="39be6-135">선택한 **Docker Compose** 또는 **Service Fabric** 컨테이너를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-135">Then choose **Docker Compose** or **Service Fabric** to manage the containers.</span></span>

<span data-ttu-id="39be6-136">프로젝트에 추가 하는 Dockerfile 컨테이너 오케스트레이션을 지원 프로젝트에 추가한 후 표시와 **docker compose** 솔루션에 추가 하는 폴더 **솔루션 탐색기**그림 4-29에 표시 된 것 처럼:</span><span class="sxs-lookup"><span data-stu-id="39be6-136">After you add container orchestration support to your project, you see a Dockerfile added to the project and a **docker-compose** folder added to the solution in **Solution Explorer**, as shown in Figure 4-29:</span></span>

![Visual Studio의 솔루션 탐색기에서 docker 파일](media/docker-support-solution-explorer.png)

<span data-ttu-id="39be6-138">그림 4-29: Visual Studio 2017의 솔루션 탐색기에서 docker 파일</span><span class="sxs-lookup"><span data-stu-id="39be6-138">Figure 4-29: Docker files in Solution Explorer in Visual Studio 2017</span></span>

<span data-ttu-id="39be6-139">하는 경우 *docker compose.yml* 이미 하기만 하면 Visual Studio에 필요한 구성 코드 줄을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-139">If *docker-compose.yml* already exists, Visual Studio just adds the required lines of configuration code to it.</span></span>

## <a name="configure-docker-tools"></a><span data-ttu-id="39be6-140">Docker 도구를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-140">Configure Docker tools</span></span>

<span data-ttu-id="39be6-141">주 메뉴에서 선택 **도구** > **옵션**을 확장 하 고 **컨테이너 도구** > **설정**합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-141">From the main menu, choose **Tools** > **Options**, and expand **Container Tools** > **Settings**.</span></span> <span data-ttu-id="39be6-142">컨테이너 도구 설정이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-142">The container tools settings appear.</span></span>

![](./media/visual-studio-docker-tools-options.png)

<span data-ttu-id="39be6-143">그림 4-30: Docker 도구 옵션</span><span class="sxs-lookup"><span data-stu-id="39be6-143">Figure 4-30: Docker Tools Options</span></span>

<span data-ttu-id="39be6-144">다음 표에서 이러한 옵션을 설정 하는 방법을 결정 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-144">The following table might help you decide how to set these options.</span></span>

| <span data-ttu-id="39be6-145">이름</span><span class="sxs-lookup"><span data-stu-id="39be6-145">Name</span></span> | <span data-ttu-id="39be6-146">기본 설정</span><span class="sxs-lookup"><span data-stu-id="39be6-146">Default Setting</span></span> | <span data-ttu-id="39be6-147">적용 대상</span><span class="sxs-lookup"><span data-stu-id="39be6-147">Applies To</span></span> | <span data-ttu-id="39be6-148">설명</span><span class="sxs-lookup"><span data-stu-id="39be6-148">Description</span></span> |
| -----|:---------------:|:----------:| ----------- |
| <span data-ttu-id="39be6-149">프로젝트 로드 시 필요한 Docker 이미지를 자동으로 풀</span><span class="sxs-lookup"><span data-stu-id="39be6-149">Automatically pull required Docker images on project load</span></span> | <span data-ttu-id="39be6-150">켜기</span><span class="sxs-lookup"><span data-stu-id="39be6-150">On</span></span> | <span data-ttu-id="39be6-151">Docker Compose</span><span class="sxs-lookup"><span data-stu-id="39be6-151">Docker Compose</span></span> | <span data-ttu-id="39be6-152">성능 향상된을 위해 프로젝트를 로드 하는 경우, Visual Studio는 Docker 가져오기 작업을 백그라운드에서 이미지가 이미 다운로드 될 때 코드를 실행할 준비가 되도록 또는 시작 다운로드 중입니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-152">For increased performance, when loading projects, Visual Studio will start a Docker pull operation in the background so that when you are ready to run your code, the image is already downloaded or in the process of downloading.</span></span> <span data-ttu-id="39be6-153">방금 프로젝트를 로드 하 고 코드를 검색, 경우 해제할 수 있습니다이 필요 하지 않습니다 하는 컨테이너 이미지 다운로드를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-153">If you're just loading projects and browsing code, you can turn this off to avoid downloading container images you don't need.</span></span> |
| <span data-ttu-id="39be6-154">백그라운드에서 컨테이너를 자동으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-154">Automatically start containers in background</span></span> | <span data-ttu-id="39be6-155">켜기</span><span class="sxs-lookup"><span data-stu-id="39be6-155">On</span></span> | <span data-ttu-id="39be6-156">Docker Compose</span><span class="sxs-lookup"><span data-stu-id="39be6-156">Docker Compose</span></span> | <span data-ttu-id="39be6-157">다시 성능 향상된을 위해 Visual Studio 컨테이너를 만듭니다 볼륨 탑재를 사용 하 여 빌드하고 컨테이너를 실행 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-157">Again for increased performance, Visual Studio creates a container with volume mounts ready for when you build and run your container.</span></span> <span data-ttu-id="39be6-158">컨테이너를 만들 때 제어 하려는 경우이 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-158">If you want to control when your container is created, turn this off.</span></span> |
| <span data-ttu-id="39be6-159">Kill 컨테이너 솔루션에 자동으로 닫기</span><span class="sxs-lookup"><span data-stu-id="39be6-159">Automatically kill containers on solution close</span></span> | <span data-ttu-id="39be6-160">켜기</span><span class="sxs-lookup"><span data-stu-id="39be6-160">On</span></span> | <span data-ttu-id="39be6-161">Docker Compose</span><span class="sxs-lookup"><span data-stu-id="39be6-161">Docker Compose</span></span> | <span data-ttu-id="39be6-162">이 기능을 끌 솔루션을 닫기 또는 Visual Studio를 닫은 후에 계속 실행 하기 위해 솔루션에 대 한 컨테이너를 하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="39be6-162">Turn this off if you would like containers for your solution to continue to run after closing the solution or closing Visual Studio.</span></span> |
| <span data-ttu-id="39be6-163">Localhost SSL 인증서 신뢰에 대 한 확인 안 함</span><span class="sxs-lookup"><span data-stu-id="39be6-163">Do not prompt for trusting localhost SSL certificate</span></span> | <span data-ttu-id="39be6-164">끄기</span><span class="sxs-lookup"><span data-stu-id="39be6-164">Off</span></span> | <span data-ttu-id="39be6-165">ASP.NET Core 2.1 프로젝트</span><span class="sxs-lookup"><span data-stu-id="39be6-165">ASP.NET Core 2.1 projects</span></span> | <span data-ttu-id="39be6-166">Localhost SSL 인증서를 신뢰할 수 없는 경우 Visual Studio 묻는 프로젝트를 실행할 때마다이 확인란을 선택 하지 않으면.</span><span class="sxs-lookup"><span data-stu-id="39be6-166">If the localhost SSL certificate is not trusted, Visual Studio will prompt every time you run your project, unless this checkbox is checked.</span></span> |

> [!WARNING]
> <span data-ttu-id="39be6-167">Localhost SSL 인증서가 신뢰할 수 있는 메시지를 표시 하지 않으려면 확인란을 HTTPS 요청을 웹 앱 또는 서비스에서 런타임에 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-167">If the localhost SSL certificate is not trusted, and you check the box to suppress prompting, then HTTPS web requests might fail at runtime in your app or service.</span></span> <span data-ttu-id="39be6-168">이런 경우의 선택을 취소 합니다 **표시 안 함** 확인란 프로젝트를 실행 하 고 신뢰 프롬프트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39be6-168">In that case, uncheck the **Do not prompt** checkbox, run your project, and indicate trust at the prompt.</span></span>

<span data-ttu-id="39be6-169">**자세한 정보:** 서비스 구현 및 Visual Studio Tools for Docker 사용에 자세한 내용은 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39be6-169">**More information:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="39be6-170">빌드, 디버그, 업데이트 및 로컬 Docker 컨테이너에서 앱을 새로 고칩니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="39be6-170">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="39be6-171">ASP.NET Core Docker 컨테이너를 컨테이너 레지스트리에 배포 합니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="39be6-171">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="39be6-172">[이전](docker-apps-inner-loop-workflow.md)
>[다음](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="39be6-172">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>