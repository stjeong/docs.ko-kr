---
title: Docker 앱을 위한 개발 환경
description: Docker 개발 수명 주기를 지 원하는 가장 중요 한 개발 도구 옵션 익히기.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 1d22b45a8eee9198d337df9f0b8b4b78371fa31a
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219999"
---
# <a name="development-environment-for-docker-apps"></a><span data-ttu-id="15e05-103">Docker 앱을 위한 개발 환경</span><span class="sxs-lookup"><span data-stu-id="15e05-103">Development environment for Docker apps</span></span>

## <a name="development-tools-choices-ide-or-editor"></a><span data-ttu-id="15e05-104">개발 도구 선택: IDE 또는 편집기</span><span class="sxs-lookup"><span data-stu-id="15e05-104">Development tools choices: IDE or editor</span></span>

<span data-ttu-id="15e05-105">든 관계 없이 완전 하 고 강력한 IDE 또는 가볍고 민첩 한 편집기를 선호 하는 경우 Microsoft는 Docker 응용 프로그램 개발에 있어.</span><span class="sxs-lookup"><span data-stu-id="15e05-105">No matter if you prefer a full and powerful IDE or a lightweight and agile editor, Microsoft has you covered when it comes to developing Docker applications.</span></span>

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a><span data-ttu-id="15e05-106">Visual Studio Code 및 Docker CLI (Mac, Linux 및 Windows 용 플랫폼 간 도구)</span><span class="sxs-lookup"><span data-stu-id="15e05-106">Visual Studio Code and Docker CLI (cross-platform tools for Mac, Linux, and Windows)</span></span>

<span data-ttu-id="15e05-107">모든 개발 언어를 지 원하는 경량, 플랫폼 간 편집기를 원한다 면 Visual Studio Code 및 Docker CLI를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-107">If you prefer a lightweight, cross-platform editor supporting any development language, you can use Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="15e05-108">이러한 제품은 개발자 워크플로 간소화 하는 것에 대 한 중요 한 간단 하지만 강력한 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-108">These products provide a simple yet robust experience, which is critical for streamlining the developer workflow.</span></span> <span data-ttu-id="15e05-109">"Docker에 대 한 Mac" 또는 "Docker에 대 한 Windows" (개발 환경)를 설치 하 여 Docker 개발자 모두 Windows 또는 Linux (런타임 환경)에 대 한 앱을 빌드할 수는 단일 Docker CLI를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-109">By installing "Docker for Mac" or "Docker for Windows" (development environment), Docker developers can use a single Docker CLI to build apps for both Windows or Linux (runtime environment).</span></span> <span data-ttu-id="15e05-110">또한 Visual Studio Code 편집기에서 Docker 명령을 실행 하는 Dockerfile 및 바로 가기 작업에 대 한 IntelliSense 사용 하 여 Docker에 대 한 확장을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-110">Plus, Visual Studio Code supports extensions for Docker with IntelliSense for Dockerfiles and shortcut-tasks to run Docker commands from the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="15e05-111">Visual Studio Code를 다운로드 하려면로 이동 <https://code.visualstudio.com/download>합니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-111">To download Visual Studio Code, go to <https://code.visualstudio.com/download>.</span></span>

<span data-ttu-id="15e05-112">Mac 및 Windows 용 Docker를 다운로드 하려면로 이동 <https://www.docker.com/products/docker>합니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-112">To download Docker for Mac and Windows, go to <https://www.docker.com/products/docker>.</span></span>

### <a name="visual-studio-with-docker-tools"></a><span data-ttu-id="15e05-113">Docker 도구를 사용 하 여 visual Studio</span><span class="sxs-lookup"><span data-stu-id="15e05-113">Visual Studio with Docker Tools</span></span>

<span data-ttu-id="15e05-114">Visual Studio 2015를 사용 하는 경우 "Visual Studio 용 Docker 도구입니다." 추가 기능 도구를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-114">When you're using Visual Studio 2015 you can install the add-on tools "Docker Tools for Visual Studio."</span></span> <span data-ttu-id="15e05-115">Visual Studio 2017 용 Docker 도구 기본적으로 제공 되에 이미 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-115">For Visual Studio 2017, Docker Tools come built in already.</span></span> <span data-ttu-id="15e05-116">두 경우 모두를 개발할 수 있습니다를 실행 하 고 선택한 Docker 환경에서 직접 응용 프로그램을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-116">In both cases you can develop, run, and validate your applications directly in the chosen Docker environment.</span></span> <span data-ttu-id="15e05-117">F5 응용 프로그램 (단일 컨테이너 또는 여러 컨테이너)을 Docker에 직접 디버깅을 사용 하 여 호스트 또는 Ctrl + f5를 눌러 편집 하 고 컨테이너를 다시 빌드하지 않고 앱을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-117">F5 your application (single container or multiple containers) directly into a Docker host with debugging, or press Ctrl+F5 to edit and refresh your app without having to rebuild the container.</span></span> <span data-ttu-id="15e05-118">이 Linux 또는 Windows 용 Docker 컨테이너를 만들고 Windows 개발자를 위한 간단 하 고 더 강력한 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-118">This is the simplest and more powerful choice for Windows developers creating Docker containers for Linux or Windows.</span></span>

> [!NOTE]
> <span data-ttu-id="15e05-119">Visual Studio 용 Docker 도구를 다운로드 하려면로 이동 <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>합니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-119">To download Docker Tools for Visual Studio, go to <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span></span>

## <a name="language-and-framework-choices"></a><span data-ttu-id="15e05-120">언어 및 프레임 워크 선택</span><span class="sxs-lookup"><span data-stu-id="15e05-120">Language and framework choices</span></span>

<span data-ttu-id="15e05-121">Docker 응용 프로그램 및 최신 언어를 사용 하 여 Microsoft 도구를 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-121">You can develop Docker applications and Microsoft tools with most modern languages.</span></span> <span data-ttu-id="15e05-122">다음은 초기 목록을, 하지만에 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-122">The following is an initial list, but you are not limited to it:</span></span>

-   <span data-ttu-id="15e05-123">.NET Core 및 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="15e05-123">.NET Core and ASP.NET Core</span></span>
-   <span data-ttu-id="15e05-124">Node.js</span><span class="sxs-lookup"><span data-stu-id="15e05-124">Node.js</span></span>
-   <span data-ttu-id="15e05-125">Golang</span><span class="sxs-lookup"><span data-stu-id="15e05-125">Golang</span></span>
-   <span data-ttu-id="15e05-126">Java</span><span class="sxs-lookup"><span data-stu-id="15e05-126">Java</span></span>
-   <span data-ttu-id="15e05-127">Ruby</span><span class="sxs-lookup"><span data-stu-id="15e05-127">Ruby</span></span>
-   <span data-ttu-id="15e05-128">Python</span><span class="sxs-lookup"><span data-stu-id="15e05-128">Python</span></span>

<span data-ttu-id="15e05-129">기본적으로, Linux 또는 Windows에서 Docker를 지 원하는 모든 최신 언어를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e05-129">Basically, you can use any modern language supported by Docker in Linux or Windows.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="15e05-130">[이전](deploy-azure-kubernetes-service.md)
>[다음](docker-apps-inner-loop-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="15e05-130">[Previous](deploy-azure-kubernetes-service.md)
[Next](docker-apps-inner-loop-workflow.md)</span></span>