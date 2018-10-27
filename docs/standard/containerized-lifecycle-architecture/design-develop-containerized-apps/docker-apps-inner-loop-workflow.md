---
title: Docker 앱에 대 한 내부 루프 개발 워크플로
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: be9c3fe165be32df43073919904b85120c52d595
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50034463"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a>Docker 앱에 대 한 내부 루프 개발 워크플로

전체 DevOps에 걸쳐 루프 외부 워크플로 트리거하기 전에 주기, 각 개발자의 컴퓨터에서 해당 앱을 코딩, 해당 기본 설정된 언어 또는 플랫폼을 사용 하 여 및 로컬로 테스트 하 고 (그림 4-14) 시작 하는 것입니다. 하지만 모든 경우에서 수는 매우 중요 한 점을 공통적으로 선택 하는 언어, 프레임 워크 또는 플랫폼에 관계 없이 합니다. 이 특정 워크플로에서 항상 개발 하 고 Docker 컨테이너를 로컬로 테스트 합니다.

![](./media/image18.png)

그림 4-14: 내부 루프 개발 컨텍스트

Docker 이미지의 인스턴스를 컨테이너에 이러한 구성 요소를 포함 됩니다.

-   운영 체제 선택 (예: Linux 배포 또는 Windows)

-   개발자 (예: 응용 프로그램 이진 파일)가 추가 된 파일

-   구성 (예: 환경 설정 및 종속성)

-   Docker에서 실행을 처리 하는 것에 대 한 지침

(다음 섹션에서 설명) 프로세스와 Docker를 활용 하는 내부 루프 개발 워크플로를 설정할 수 있습니다. 계정 환경을 설정 하는 초기 단계는 포함 하는 한 번만 수행 해야 하기 때문에 야 합니다.

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a>Visual Studio Code 및 Docker CLI를 사용 하 여 Docker 컨테이너 내에서 단일 앱 빌드

앱은 사용자 고유의 서비스와 추가 라이브러리 (종속성)에서 구성 됩니다.

그림 4-15 일반적으로 각 단계에 자세히 설명 뒤에 Docker 앱을 빌드할 때 수행 해야 하는 기본 단계를 보여 줍니다.

![](./media/image19.png)

Docker CLI를 사용 하 여 컨테이너 화 된 Docker 응용 프로그램 수명 주기에 대 한 개략적인 워크플로 그림 4-15:

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a>1 단계: Visual Studio Code에서 코딩을 시작 하 고 초기 앱/서비스 기준 만들기

응용 프로그램을 개발 하는 방법은 Docker 없이 이렇게 하는 방법은 매우 비슷합니다. 개발 중에만 배포 및 테스트 중인 응용 프로그램 또는 서비스 (예: Linux VM 또는 Windows) 로컬 환경에 배치 하는 Docker 컨테이너 내에서 실행 되는 점이 다릅니다.

**로컬 환경 설정**

최신 버전의 Mac 및 Windows 용 Docker 사용 하 여 Docker 응용 프로그램 개발 그 어느 때 보다 훨씬 더 쉽게 하 고 설치는 간단 합니다.

**자세한 내용은** 이동할를 Docker에 대 한 Windows 설정에 대 한 [ https://docs.docker.com/docker-for-windows/ ](https://docs.docker.com/docker-for-windows/)합니다.

Mac 용 Docker 설정 지침에 대 한 <https://docs.docker.com/docker-for-mac/>합니다.

또한 해야 코드 편집기는 실제로 Docker CLI를 사용 하는 동안 응용 프로그램을 개발할 수 있습니다.

Microsoft 제공 Mac, Windows, 및 Linux에서 지원 되 고 사용 하 여 IntelliSense를 제공 하는 경량 코드 편집기 인 Visual Studio Code [다양 한 언어에 대 한 지원](https://code.visualstudio.com/docs/languages/overview) (JavaScript,.NET, Go, Java, Ruby, Python 및 가장 최신 언어의 경우) [디버깅](https://code.visualstudio.com/Docs/editor/debugging)를 [Git와 통합](https://code.visualstudio.com/Docs/editor/versioncontrol) 하 고 [확장](https://code.visualstudio.com/docs/extensions/overview)합니다. 이 편집기는 Linux 및 Mac 개발자를 위한 최적의 선택입니다. Windows에도 사용할 수 있습니다 전체 Visual Studio 응용 프로그램입니다.

**자세한 내용은** 으로 이동에 대 한 지침은 Visual Studio에 대 한 Windows, Mac 또는 Linux를 설치, <https://code.visualstudio.com/docs/setup/setup-overview/>합니다.

Docker CLI를 사용 하 여 작업 하 고 어떤 코드 편집기를 사용 하 여 코드를 작성할 수 있지만 쉽게 작성 Dockerfile 및 docker-compose.yml 파일 작업 영역에는 Visual Studio Code를 사용 하는 경우. 또한 아래에 있는 Docker CLI를 사용 하 여 상세 작업 실행 될 수 있는 스크립트를 일으키는 IDE에서 Visual Studio Code 작업을 실행할 수 있습니다.

Visual Studio Code는 설치 해야 하는 확장에 의해 제공 됩니다. 이렇게 하려면 키를 눌러 Ctrl + Shift + P를 입력 **ext 설치**, 그런 다음 확장을 실행 하 고: Marketplace 확장 목록을 표시 하려면 확장 설치 명령입니다. 그런 다음 입력 **docker** 결과 필터링 하 여 다음 그림 4-16에 표시 된 대로 Dockerfile 및 Docker Compose 파일 (yml) 지원 확장을 선택 합니다.

![](./media/image20.png)

그림 4-16: Visual Studio Code의 Docker 확장 설치

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a>2 단계: 기존 이미지 (일반 OS 또는.NET Core, Node.js 및 Ruby와 같은 개발 환경)와 관련 된 DockerFile 만들기

만들려는 사용자 지정 이미지 및 컨테이너 배포 당 DockerFile 해야, 따라서 단일 사용자 지정 서비스의 앱 옵션을 구성 된 경우 단일 DockerFile 해야 합니다. 하지만 서비스 당 하나의 Dockerfile 경우 앱은 여러 서비스 (예: 마이크로 서비스 아키텍처)으로 구성 해야 합니다.

DockerFile는 앱 또는 서비스의 루트 폴더 내에서 일반적으로 배치 및 Docker에서 설정 하 고 해당 앱 또는 서비스를 실행 하는 방법을 알 수 있도록 필요한 명령을 포함 합니다. DockerFile을 만들고 코드와 함께 프로젝트에 추가할 수 있습니다 (.NET Core, node.js 등), 또는 환경에 새로운 인 경우 다음 팁을 살펴봅니다.

> [!TIP]
> 라는 명령줄 도구를 사용할 수 있습니다 [yo docker](https://github.com/Microsoft/generator-docker), 파일을 선택 하 고 필요한 Docker 구성 파일을 추가 하는 언어의 프로젝트에서 스 캐 폴딩입니다. 기본적으로, 적절 한 DockerFile 생성을 지원 하기 위해 시작 하는 개발자가 docker compose.yml 및 기타 관련된 스크립트를 빌드하고 Docker 컨테이너를 실행 합니다. 이 yeoman 생성기를 묻는 선택한 개발 언어와 대상 컨테이너 호스트를 요청 하는 몇 가지 질문을 합니다.

![yo docker](./media/image21.png)

예를 들어, 그림 4-17 두 스크린샷에서 터미널에서 실행 하는 Mac, 두 경우 모두 yo 샘플 코드 프로젝트 (현재.NET Core, Golang, 및 지원 되는 언어로 Node.js)에서 작동 하도록 이미 구성 되어 생성 하는 docker 및 Windows에서 Docker의 맨 위에 있습니다.

![](./media/image22.PNG)  ![](./media/image23.png)

그림 4-17: yo docker 명령 도구 (왼쪽) Windows 및 Mac

그림 4-18를 사용 하 여 yo docker 스 캐 폴드 된 수에 기존.NET Core 프로젝트를 만든 후 예제를 제공 합니다.

![](./media/image24.PNG)

그림 4-18: yo는 기존.NET Core를 사용 하 여 docker 프로젝트 준비

DockerFile에서 기본 Docker 이미지를 사용 하기 (예: "에서 microsoft/dotnet:1.0.0-core" 사용) 지정할 수 있습니다. 일반적으로 사용자 지정 이미지에서 공식 리포지토리에서 얻을 수 있는 기본 이미지를 기반으로 빌드됩니다 합니다 [Docker Hub 레지스트리에서](https://hub.docker.com/) (같은 [.NET Core에 대 한 이미지](https://hub.docker.com/r/microsoft/dotnet/) 이상의 [Node.js용](https://hub.docker.com/_/node/)).

***옵션 a: 사용 하 여 기존 공식 Docker 이미지***

버전 번호를 사용 하 여 언어 스택의 공식 리포지토리를 사용 하 여 동일한 언어 기능 (개발, 테스트 및 프로덕션 포함)는 모든 컴퓨터에서 사용할 수 있는지 확인 합니다.

다음은.NET Core 컨테이너에 대 한 샘플 DockerFile을입니다.

```
# Base Docker image to use
FROM microsoft/aspnetcore:1.0.1\

# Set the Working Directory and files to be copied to the image
ARG source
WORKDIR /app
COPY ${source:-bin/Release/PublishOutput} .

# Configure the listening port to 80 (Internal/Secured port within Docker host)
EXPOSE 80

# Application entry point
ENTRYPOINT ["dotnet", "MyCustomMicroservice.dll"]
```

이 경우 microsoft/aspnetcore:1.0.1 이라는 Linux에 대 한 공식 ASP.NET Core Docker 이미지의 버전 1.0.1를 사용 하는 고 합니다. 자세한 내용은 참조는 [ASP.NET Core Docker 이미지 페이지](https://hub.docker.com/r/microsoft/aspnetcore/) 하며 [.NET Core Docker 이미지 페이지](https://hub.docker.com/r/microsoft/dotnet/). 또한 없습니다 사용할 노드: 4와 같은 다른 비교 가능한 이미지-Node.js 또는에서 제공 되는 개발 언어에 대 한 다른 많은 미리 구성 된 이미지에 대 한 onbuild [Docker 허브](https://hub.docker.com/explore/)합니다.

DockerFile에서 Docker (예: 포트 80) 런타임에 사용할 TCP 포트를 수신 대기 하도록 지시 해야 합니다.

Docker에서 앱을 실행 하는 방법을 알 수 있도록 언어/프레임 워크를 사용 하는 따라 DockerFile에 추가할 수 있는 구성의 다른 줄 있습니다. 예를 들어 포함 된 ENTRYPOINT 줄 해야 \["dotnet", "MyCustomMicroservice.dll"\] 빌드하고 서비스를 실행 하는 방법에 따라 여러 변형을 포함할 수는 있지만.NET Core 앱을 실행 합니다. SDK 및 dotnet CLI 사용 하 여.NET 앱 빌드 및 실행 하는, 경우에 약간 다른 것입니다. 결론은 ENTRYPOINT 줄 및 줄 추가 되도록 응용 프로그램에 대해 선택한 언어/플랫폼에 따라 다릅니다.

**자세한 내용은** 로.NET Core 응용 프로그램에 대 한 Docker 이미지 작성에 대 한 내용은 <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>합니다.

사용자 고유의 이미지를 작성 하는 방법에 대 한 자세한 내용은로 이동 [ https://docs.docker.com/engine/\ 자습서/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/)합니다.

**다중 플랫폼 이미지 리포지토리**

Windows 컨테이너 널리 퍼져 있을 경우 단일 리포지토리는 Linux 및 Windows 이미지 같은 플랫폼 변형을 포함할 수 있습니다. 이 공급 업체와 같은 여러 플랫폼에 맞게 단일 리포지토리를 사용할 수 있도록 하는 Docker에서 새로운 기능인 [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) DockerHub 레지스트리에서 사용할 수 있는 저장소입니다. 기능 상태가 유지 되 면으로 Windows 호스트에서이 이미지를 끌어오려면 끌어오면 Windows 변형을 Linux 호스트에서 동일한 이미지 이름을 가져오는 끌어오면 Linux 변형을 반면 합니다.

***부터 기본 이미지 b: 만들기 옵션***

이 항목에 설명 된 대로 처음부터 사용자 고유의 Docker 기본 이미지를 만들 수 있습니다 [문서](https://docs.docker.com/engine/userguide/eng-image/baseimages/) Docker에서. Docker로 시작 하는 경우에 가장 적합 한 않을 하는 시나리오 이지만 고유한 기본 이미지의 특정 비트를 설정 하려는 경우 수행할 수 있습니다.

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a>3 단계: 서비스를 포함 하 여 사용자 지정 Docker 이미지 만들기

앱을 구성 하는 각 사용자 지정 서비스에 대 한 관련된 이미지를 만드는 해야 합니다. 단일 서비스 또는 웹 앱의 앱 옵션을 구성 된 경우에 단일 이미지를 방금 해야 합니다.

> [!NOTE]
> "외부 루프 DevOps 워크플로의" 계정을 고려 하는 경우 이미지는 자동화 된 빌드 프로세스에서 전역 환경에서 이미지를 만들 수는 소스 코드 (연속 통합) Git 리포지토리에 푸시할 때마다에서 만들어집니다 프로그램 소스 코드입니다.

그러나 Docker 응용 프로그램은 실제로 제대로 작동 하는지 확인 (Git 등). 소스 제어 시스템에 제대로 작동 하지 않을 수도 코드를 푸시 하지는 않도록 해야 것으로 간주 해당 외부 반복 경로를 이동 합니다.

따라서 각 개발자는 먼저 로컬에서 테스트 및 개발 하는 완전 한 기능을 푸시하거나 원본 제어 시스템에 변경 하려는 될 때까지 계속 전체 내부 루프 프로세스를 수행 해야 합니다.

이미지를 만드는에서 DockerFile을 사용 하 여 로컬 환경에서 사용할 수 그림 4-19에 설명한 것 처럼 docker build 명령을 (실행할 수도 있습니다 docker compose up--여러 컨테이너/서비스에서 구성 된 응용 프로그램에 대 한 빌드).

![](./media/image25.png)

그림 4-19: docker 빌드를 실행합니다.

필요에 따라 직접 docker를 실행 하는 대신 프로젝트의 폴더에서 빌드를 처음 실행된 dotnet을 사용 하 여 명령을 게시 하 고 docker 빌드를 실행 하 여.NET 라이브러리를 사용 하 여 배포 가능 폴더를 생성할 수 있습니다.

이 예제에서는 이름 cesardl/netcore-webapi-마이크로 서비스를 사용 하 여 Docker 이미지를 만들어집니다-docker: 첫 번째 (: 첫 번째는 특정 버전 태그). 여러 컨테이너를 사용 하 여 구성 된 Docker 응용 프로그램에 대해 만들어야 하는 각 사용자 지정 이미지에 대해이 단계를 수행할 수 있습니다.

찾을 수 있습니다 기존 이미지 로컬 리포지토리 (개발 컴퓨터)에서 docker를 사용 하 여 이미지 명령인 그림 4-20에 설명 된 대로.

![](./media/image26.png)

그림 4-20: docker 이미지를 사용 하 여 기존 이미지 보기

### <a name="step-4-optional-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a>4 단계: (선택 사항) 정의 여러 서비스를 사용 하 여 구성 된 Docker 앱을 빌드할 때 docker-compose.yml에서 서비스

Docker compose.yml 파일을 사용 하 여 다음 단계 섹션에서 설명한 배포 명령을 사용 하 여 구성된 된 응용 프로그램으로 배포할 관련된 서비스 집합을 정의할 수 있습니다.

해당 파일에서 기본 또는 루트 솔루션 폴더를 만들어야 합니다. 다음 docker compose.yml 파일에는 비슷한 내용이 있어야 합니다.

```yml
version: '2'
services:
  web:
    build: .
    ports:
     - "81:80"
    volumes:
     - .:/code
    depends_on:
     - redis
  redis:
    image: redis
```

이 경우에이 파일은 두 서비스를 정의 합니다. (사용자 지정 서비스) 웹 서비스 및 redis 서비스 (인기 있는 캐시 서비스). 각각에 대 한 구체적인 Docker 이미지를 사용 해야 하므로 각 서비스는 컨테이너로 배포 됩니다. 이 특정 웹 서비스에 대 한 이미지는 다음을 수행 해야 합니다.

-   현재 디렉터리에서 DockerFile에서 빌드

-   노출된 된 포트 80 포트 81 호스트 컴퓨터에서 컨테이너에 전달 합니다.

-   이미지를 다시 빌드하지 않고 코드를 수정할 수 있도록 컨테이너 내의 모든 코드를 삽입 하려면 호스트에서 프로젝트 디렉터리 탑재

-   웹 서비스는 redis 서비스에 연결

Redis 서비스에서 사용 하는 [최신 공개 redis 이미지](https://hub.docker.com/_/redis/) Docker Hub 레지스트리에서 끌어옵니다. [redis](https://redis.io/) 는 서버 쪽 응용 프로그램에 대 한 매우 인기 있는 캐시 시스템입니다.

### <a name="step-5-build-and-run-your-docker-app"></a>5 단계: 빌드 및 Docker 앱 실행

앱에 단일 컨테이너만 경우 Docker 호스트 (VM 또는 물리적 서버)에 배포 하 여 실행 하기만 하면 됩니다. 그러나 경우 앱은 여러 서비스로 구성 된, 해야 *구성*도 합니다. 다양 한 옵션을 확인해 보겠습니다.

***옵션 a: 실행 단일 컨테이너 또는 서비스***

여기에 나와 있는 것 처럼 docker run 명령을 사용 하 여 Docker 이미지를 실행할 수 있습니다.

```
docker run -t -d -p 80:5000
cesardl/netcore-webapi-microservice-docker:first
```

이 특정 배포에서는 됩니다 수 리디렉션 내부 포트 5000에 포트 80에 전송 된 요청 note 합니다. 이제 응용 프로그램 호스트 수준에서 80 외부 포트에서 수신 대기 합니다.

***옵션 b: Compose 및 다중 컨테이너 응용 프로그램을 실행***

대부분의 엔터프라이즈 시나리오에서 Docker 응용 프로그램을 여러 서비스로 구성 됩니다. 이러한 경우 명령을 실행할 수 있습니다 docker compose 설치 (그림 4-21), 이전에 만든 수 docker compose.yml 파일을 사용 하는 합니다. 이 명령을 실행의 모든 해당 관련된 컨테이너를 사용 하 여 구성 된 응용 프로그램을 배포 합니다.

![](./media/image27.png)

그림 4-21: "docker compose 구성" 명령을 실행 결과

Docker를 실행 한 후-등록 구성, VM 표현에서 그림 4-22에서와 같이 응용 프로그램 및 해당 관련된 컨테이너에 Docker 호스트에 배포 합니다.

![](./media/image28.png)

배포 된 Docker 컨테이너를 사용 하 여 그림 4-22: VM

참고 docker compose 구성 및 실행 하는 docker 컨테이너 개발 환경에서 테스트를 위해 충분할 수 있습니다 하지 않지만 하지 사용 해당 전혀 Docker 클러스터 작업을 위해 예상 되 고 Docker Swarm, Mesosphere DC/OS 또는 Kubernetes 오 케 스트레이 터와 같은 경우 하기 위해 확장할 수 있습니다. 같은 클러스터를 사용 하는 경우 [Docker Swarm mode](https://docs.docker.com/engine/swarm/) 배포 하 고 있다면 또는 단일 서비스에 대 한 docker 서비스 만들기와 같은 추가 명령을 사용 하 여 테스트 해야 (사용 가능 Docker에 대 한 Windows 및 Mac 버전 1.12부터), 번들 작성 docker를 사용 하 여 여러 컨테이너로 구성 된 앱을 배포 하 고 docker 문서에 설명 된 대로 스택으로 구성 된 앱을 배포 하 여 myBundleFile를 배포 [분산 응용 프로그램 번들](https://blog.docker.com/2016/06/docker-app-bundle/) Docker에서.

에 대 한 [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) 하 고 [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) 다양 한 배포 명령 및 스크립트를 사용 합니다.

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a>6 단계: (로컬 CD VM)에서 로컬로 Docker 응용 프로그램 테스트

이 단계는 고 앱이 수행 되는 내용에 따라 달라 집니다.

매우 간단한.NET Core Web API에 "Hello World" 단일 컨테이너 또는 서비스로 배포를 DockerFile에서 지정 된 TCP 포트를 제공 하 여 서비스에 액세스 해야만 합니다.

서비스를 이동 하려면 localhost에 설정 되지 않은 경우는이 명령을 사용 하 여 컴퓨터에 대 한 IP 주소를 찾으려면:

docker-컴퓨터 ip *사용자 컨테이너 이름*

Docker 호스트에서 브라우저를 열고 해당 사이트로; 이동 그림 4-23에 설명 된 대로 앱/서비스를 실행 하 여 표시 됩니다.

![](./media/image29.png)

그림 4-23: localhost를 사용 하 여 로컬로 Docker 응용 프로그램 테스트

방법으로 배포 되었기를 실행 하는 docker를 사용 하 여 앞에서 설명한 대로 이기 때문에 포트 80을 사용 하지만 내부적으로 포트 5000에 리디렉션되지 된 note 합니다.

터미널에서 CURL을 사용 하 여이 테스트할 수 있습니다. Windows에서 Docker 설치에서 기본 IP 그림 4-24에서 언급 했 듯이 10.0.75.1, 됩니다.

![](./media/image30.png)

그림 4-24: CURL을 사용 하 여 로컬로 Docker 응용 프로그램 테스트

**Docker에서 실행 되는 컨테이너 디버깅**

Visual Studio Code는 Node.js 및.NET Core 컨테이너 등의 다른 플랫폼을 사용 하는 경우 디버깅 Docker를 지원 합니다.

또한 디버깅할 수 있습니다 Docker에서.NET Core 컨테이너 Visual Studio를 사용 하는 경우 다음 섹션에 설명 된 대로.

**자세한 정보:** 로 Node.js Docker 컨테이너를 디버깅 하는 방법에 대 한 자세한 내용은 <https://blog.docker.com/2016/07/live-debugging-docker/> 하 고 [ https://blogs.msdn.microsoft.com/\ 사용자\_ed/2016/02/27 / visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/)합니다.


>[!div class="step-by-step"]
[이전](docker-apps-development-environment.md)
[다음](visual-studio-tools-for-docker.md)
