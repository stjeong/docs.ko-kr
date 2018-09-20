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
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>Visual Studio Tools for Docker (Windows의 Visual Studio) 사용

개발 워크플로에서 Docker 용 Visual Studio Tools를 사용 하는 경우 Visual Studio Code 및 Docker CLI를 사용 하는 경우 워크플로 비슷합니다. 실제로 동일한 Docker CLI는 기반 하지만 시작 하기가, 프로세스를 단순화 하 고 향상 된 생산성을 제공 합니다. 빌드를 실행 하 고 작업을 구성 합니다. 실행 하 고 f5 키 또는 Ctrl + f5를 눌러 Visual Studio에서와 같은 간단한 작업을 통해 컨테이너를 디버그할 수 이기도 합니다. 실행 하 고 단일 컨테이너를 디버그할 수 있을 뿐 아니라 선택적 컨테이너 오케스트레이션 지원 기능을 사용 하 여 실행 하 고 동시에 컨테이너 (전체 솔루션)의 그룹을 디버그할 수 있습니다. 동일한 컨테이너를 정의할 *docker compose.yml* 솔루션 수준 파일입니다.

## <a name="configuring-your-local-environment"></a>로컬 환경 구성

Docker 지원은 설치 하는.NET 및.NET Core 워크 로드를 사용 하 여 Visual Studio 2017에 포함 됩니다. Docker에 대 한 Windows를 별도로 설치 합니다.

Docker에 대 한 Windows의 최신 버전을 계속 하려면 Docker 응용 프로그램 설치 프로그램은 다음 참조에 설명 된 대로 간단 하기 때문에 개발 보다 쉽습니다.

**자세한 정보:** 이동할 Docker에 대 한 Windows를 설치 하는 방법에 대 한 자세한 내용은 <https://docs.docker.com/docker-for-windows/>합니다.

**자세한 정보:** 이동할를 Visual Studio 설치에 대 한 [ https://visualstudio.microsoft.com/downloads/ ](https://visualstudio.microsoft.com/downloads/)합니다.

Visual Studio Tools for Docker 설치 하는 방법에 대 한 자세한 내용은로 이동 <http://aka.ms/vstoolsfordocker> 고 <https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>입니다.

## <a name="using-docker-tools-in-visual-studio-2017"></a>Docker 도구를 사용 하 여 Visual Studio 2017에서

프로젝트에 Docker 지원을 추가 하는 경우 (그림 4-26 참조) Visual Studio 추가 *Dockerfile* 프로젝트 루트에 있습니다.

![Visual Studio 2017 프로젝트에 Docker 솔루션 지원을 켜기](./media/image32.png)

그림 4-26: Visual Studio 2017 프로젝트에 Docker 솔루션 지원을 켜기

 Docker Compose를 통해 컨테이너 오케스트레이션을 지원, Visual Studio 2017 버전 15.7 또는 이전 버전에서 기본적으로 추가 됩니다. 컨테이너 오케스트레이션 지원은 Visual Studio 2017 버전 15.8 하는 옵트인 기능 또는 나중에 경우에서 Docker Compose 및 Service Fabric 지원 됩니다.

15.8 이상 버전의 Visual Studio를 사용 하 여 연결 된 컨테이너를 포함 하는 솔루션의 여러 프로젝트에 대 한 지원을 추가할 수 있습니다. 솔루션 또는 프로젝트 노드를 마우스 오른쪽 단추로 클릭 **솔루션 탐색기**, 선택한 **추가** > **컨테이너 오케스트레이션을 지원**합니다.  선택한 **Docker Compose** 또는 **Service Fabric** 컨테이너를 관리할 수 있습니다.

선택 하는 경우 **Docker Compose**, Visual Studio 솔루션에 서비스 섹션을 추가한 *docker compose.yml* 파일 (또는 존재 하지 않는 경우 파일을 만듭니다). 다중 컨테이너 솔루션을 작성 하려면 하는 쉬운 방법 열 수를 *docker compose.yml* 파일과 추가 기능을 사용 하 여 업데이트 합니다.

필수 구성 줄의 코드를 추가 하는이 작업을 *docker compose.yml* 솔루션 수준에서 설정 합니다.

또한 켤 수 있습니다 Docker 지원을 Visual Studio 2017에 ASP.NET Core 프로젝트를 만들 때 그림 4-27에서와 같이 합니다.

![프로젝트를 만들 때 Docker 지원 설정](./media/image33.png)

프로젝트를 만들 때 그림 4-27: Docker 지원 켜기

Visual Studio에서 솔루션에 Docker 지원을 추가 하면도 표시 됩니다에 새 노드 트리 **솔루션 탐색기** 추가 된 *docker compose.yml* 그림 4-28에서 보듯이 파일입니다.

![솔루션 탐색기에서 docker compose.yml 파일 표시](./media/image34.PNG)

그림 4-28: docker compose.yml 파일에서 이제 표시 **솔루션 탐색기**

단일을 사용 하 여 다중 컨테이너 앱을 배포할 수 있습니다 *docker compose.yml* 실행 하면 파일 `docker-compose up`소비량이 적어지지만 Visual Studio (개발 또는 환경에 따라 값을 재정의할 수 있도록 그룹을 추가 프로덕션) 및 실행 (릴리스 또는 디버그)을 입력 합니다. 이 기능은 뒷부분에서 더 잘 설명 되어 있습니다.

여러 컨테이너를 관리 하 Service Fabric Docker Compose 대신 사용할 수도 있습니다. 참조 [자습서: Azure Service Fabric에 Windows 컨테이너에서.NET 응용 프로그램을 배포](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container)합니다.

**자세한 정보:** 서비스 구현 및 Visual Studio Tools for Docker 사용에 자세한 내용은 다음 문서를 참조 하세요.

빌드, 디버그, 업데이트 및 로컬 Docker 컨테이너에서 앱을 새로 고칩니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

ASP.NET Core Docker 컨테이너를 컨테이너 레지스트리에 배포 합니다. [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
[이전](docker-apps-inner-loop-workflow.md)
[다음](set-up-windows-containers-with-powershell.md)
