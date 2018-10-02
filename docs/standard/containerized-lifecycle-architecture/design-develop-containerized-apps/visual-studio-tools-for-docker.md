---
title: Visual Studio Tools for Windows의 Docker
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: 7daac744238feb38358e4cc0ab185e90257aa98d
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48027457"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>Visual Studio Tools for Docker (Windows의 Visual Studio) 사용

Docker 개발 워크플로에 대 한 Visual Studio Tools-Visual Studio Code 및 Docker CLI를 사용 하는 경우 워크플로가 비슷합니다. 실제로 동일한 Docker CLI는 기반 하지만 시작 하기가, 프로세스를 단순화 하 고 향상 된 생산성을 제공 합니다. 빌드를 실행 하 고 작업을 구성 합니다. 실행 및 디버그와 같은 간단한 작업을 통해 컨테이너 **F5** 하 고 **Ctrl**+**F5**합니다. 실행 하 고 단일 컨테이너를 디버그할 수 있을 뿐 아니라 선택적 컨테이너 오케스트레이션 지원 기능을 사용 하 여 실행 하 고 동시에 컨테이너 (전체 솔루션)의 그룹을 디버그할 수 있습니다.

> [!NOTE]
> 이 문서에서는 mac 용, Windows에서 Visual Studio 및 Visual Studio가 아니라에 적용 됩니다.

## <a name="configure-your-local-environment"></a>로컬 환경 구성

Docker에 대 한 Windows의 최신 버전을 사용 하 여 ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), 간단 하 게 설치를 사용 하면 쉽게 Docker 응용 프로그램을 개발할 수 있습니다.

Visual Studio 2017에 docker 지원이 포함 됩니다. 여기서 Visual Studio 2017을 다운로드 합니다. [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

## <a name="use-docker-tools-in-visual-studio-2017"></a>Visual Studio 2017에서 사용 하 여 Docker 도구

두 가지 수준의 Docker 지원 프로젝트에 추가할 수 있습니다. .NET Core 웹 앱 프로젝트에 추가 하기만 하면를 *Dockerfile* 파일을 프로젝트에 Docker 지원을 사용 하도록 설정 합니다. 다음 수준이 추가 하는 컨테이너 오케스트레이션 지원 기능을 *Dockerfile* (이미 존재 하지 않는) 하는 경우 프로젝트에 및 *docker compose.yml* 솔루션 수준 파일입니다. Docker Compose를 통해 컨테이너 오케스트레이션을 지원, Visual Studio 2017 버전 15.7 또는 이전 버전에서 기본적으로 추가 됩니다. 컨테이너 오케스트레이션 지원은 Visual Studio 2017 버전 15.8 하는 옵트인 기능 또는 나중에 경우에서 Docker Compose 및 Service Fabric 지원 됩니다.

합니다 **추가** > **Docker 지원** 하 고 **추가** > **컨테이너 오케스트레이션을 지원** 명령은 웹 앱 프로젝트의 프로젝트 노드의 오른쪽 클릭 메뉴 (또는 상황에 맞는 메뉴)에 있는 **솔루션 탐색기**그림 4-26에 표시 된 것 처럼:

![Visual Studio에서 메뉴 옵션을 Docker 지원 추가](media/add-docker-support-menu.png)

그림 4-26: Visual Studio 2017 프로젝트에 Docker 지원 추가

### <a name="add-docker-support"></a>Docker 지원 추가

선택 하 여 기존.NET Core 웹 앱 프로젝트에 Docker 지원을 추가할 수 있습니다 **추가** > **Docker 지원** 에서 **솔루션 탐색기**합니다. 또한 Docker 지원을 프로젝트를 만드는 동안 선택 하 여 사용할 수 있습니다 **Docker 지원 사용** 에 **새 ASP.NET Core 웹 응용 프로그램** 클릭 하면 열리는 대화 상자 **확인** 에 **새 프로젝트** 그림 4-27에서와 같이 대화 상자.

![Visual Studio에서 새 ASP.NET Core 웹 앱에 대 한 Docker 지원 사용](./media/enable-docker-support-visual-studio.png)

그림 4-27: Visual Studio 2017에서 프로젝트를 만드는 동안 Docker 지원 사용

를 추가 하거나 Docker 지원을 사용 하도록 설정 하는 경우 Visual Studio 추가 된 *Dockerfile* 프로젝트 파일입니다.

> [!NOTE]
> 그림 4-28에서와 같이.NET Framework 웹 앱 프로젝트는.NET Core 웹 앱 프로젝트가 아닌 프로젝트를 만드는 동안 Docker Compose 지원을 사용 하면 컨테이너 오케스트레이션을 지원도 추가 됩니다.
>
> ![Docker를 사용 합니다..NET Framework 웹 앱 프로젝트에 대 한 지원 구성](media/enable-docker-compose-support.png)

> 그림 4-28: Visual Studio 2017에서.NET Framework 웹 앱 프로젝트에서 Docker Compose 지원을 사용 하도록 설정

### <a name="add-container-orchestration-support"></a>컨테이너 오케스트레이션을 지원 추가

다중 컨테이너 솔루션을 작성 하려는 경우 컨테이너 오케스트레이션을 지원 프로젝트에 추가 합니다. 이렇게 하면 실행 하 고 같은 정의 하는 경우 컨테이너 (전체 솔루션)의 그룹을 동시에 디버깅할 수 있습니다 *docker compose.yml* 파일입니다.

컨테이너 오케스트레이션을 지원 기능을 추가 하려면 마우스 오른쪽 단추로 클릭에서 솔루션 또는 프로젝트 노드 **솔루션 탐색기**, 선택한 **추가** > **컨테이너 오케스트레이션지원**. 선택한 **Docker Compose** 또는 **Service Fabric** 컨테이너를 관리할 수 있습니다.

프로젝트에 추가 하는 Dockerfile 컨테이너 오케스트레이션을 지원 프로젝트에 추가한 후 표시와 **docker compose** 솔루션에 추가 하는 폴더 **솔루션 탐색기**그림 4-29에 표시 된 것 처럼:

![Visual Studio의 솔루션 탐색기에서 docker 파일](media/docker-support-solution-explorer.png)

Visual Studio 2017의 솔루션 탐색기에서 그림 4-29: Docker 파일

하는 경우 *docker compose.yml* 이미 하기만 하면 Visual Studio에 필요한 구성 코드 줄을 추가 합니다.

**자세한 정보:** 서비스 구현 및 Visual Studio Tools for Docker 사용에 자세한 내용은 다음 문서를 참조 하세요.

빌드, 디버그, 업데이트 및 로컬 Docker 컨테이너에서 앱을 새로 고칩니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

ASP.NET Core Docker 컨테이너를 컨테이너 레지스트리에 배포 합니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
[이전](docker-apps-inner-loop-workflow.md)
[다음](set-up-windows-containers-with-powershell.md)