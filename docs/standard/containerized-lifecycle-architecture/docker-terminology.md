---
title: Docker 용어
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: 1efb2fa567bd452f0a0a5ee5afb6f759511e4145
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151315"
---
# <a name="docker-terminology"></a>Docker 용어

이 섹션에서는 용어 및 정의는 잘 알고 있어야 사용 하 여 Docker에 자세히 살펴보기 전에 (추가 정의 대 한 참조는 광범위 한 [용어집](https://docs.docker.com/glossary/) Docker에서 제공한 <https://docs.docker.com/glossary/>:

-   **컨테이너 이미지** 모든 종속성 및 컨테이너를 만드는 데 필요한 정보를 사용 하 여 패키지 있습니다. 이미지에는 모든 종속성 (예: 프레임 워크)와 배포 및 컨테이너 런타임에서 사용할 구성을 포함 합니다. 일반적으로 이미지에서에서 파생 됩니다 여러 기본 이미지 계층으로 쌓이는 지 컨테이너의 파일 시스템을 구성 하기 위해 다른 위에 하나. 이미지 만든 후 변경할 수 없는 합니다.

-   **컨테이너** Docker 이미지의 인스턴스. 컨테이너는 단일 응용 프로그램, 프로세스 또는 서비스 런타임을 나타냅니다. Docker 이미지를, 런타임 환경 및 명령의 표준 집합의 내용을 구성 됩니다. 서비스의 크기를 조정하는 경우 동일한 이미지에서 컨테이너의 여러 인스턴스를 만듭니다. 또는 일괄 처리 작업을 각 인스턴스에 다른 매개 변수를 전달 동일한 이미지에서 여러 컨테이너를 만들 수 있습니다.

-   **태그** 표시 또는 레이블은 다른 이미지 또는 (버전 번호 또는 대상 환경)에 따라 동일한 이미지의 버전을 식별할 수 있도록 이미지에 적용할 수 있습니다.

-   **Dockerfile** Docker 이미지를 빌드하는 방법에 대 한 지침을 포함 하는 텍스트 파일입니다.

-   **빌드할** 정보 및 이미지 빌드되는 폴더의 추가 파일 뿐만 아니라 해당 Dockerfile에서 제공 된 컨텍스트를 기반으로 컨테이너 이미지를 빌드하는 작업입니다. Docker docker build 명령을 사용 하 여 이미지를 빌드할 수 있습니다.

-   **리포지토리 (repo)** 이미지 버전을 나타내는 태그를 사용 하 여 레이블이 지정 된 관련된 Docker 이미지의 컬렉션입니다. 일부 저장소 Sdk (가벼움)만 런타임, 포함 된 이미지가 포함 된 이미지와 같이 특정 이미지의 여러 변형이 포함 등입니다. 이러한 변형은 태그로 표시할 수 있습니다. 단일 리포지토리는 Linux 이미지 및 Windows 이미지 같은 플랫폼 변형을 포함할 수 있습니다.

-   **레지스트리** 저장소에 대 한 액세스를 제공 하는 서비스입니다. 대부분의 공용 이미지에 대한 기본 레지스트리는 [Docker 허브](https://hub.docker.com/)(조직인 Docker에서 소유함)입니다. 레지스트리는 일반적으로 여러 팀의 리포지토리를 포함합니다. 회사 저장 하 고 만든 이미지를 관리 하는 개인 레지스트리가 있습니다. *Azure Container Registry* 는 또 다른 예입니다.

-   **Docker 허브** 이미지를 업로드 하 고 작업을 하려면 공개 레지스트리입니다. Docker 허브는 Docker 이미지 호스팅, 공개 또는 개인 레지스트리, 빌드 트리거 및 웹후크, GitHub 및 Bitbucket과 통합을 제공합니다.

-   **Azure Container Registry** Docker 이미지 및 Azure에서 해당 구성 요소를 사용 하 여 작업에 대 한 공용 리소스입니다. 여기서는 Azure에서 배포에 가깝고, 액세스에 대한 제어를 제공하는 레지스트리를 제공하여 Azure Active Directory 그룹 및 권한을 사용할 수 있도록 합니다.

-   **Docker 신뢰 레지스트리 DTR ()** Docker 레지스트리 (Docker)에서 설치할 수 있는 온-프레미스 서비스는 조직의 데이터 센터 및 네트워크에 상주 합니다. 엔터프라이즈 내에서 관리되어야 하는 개인 이미지에 유용합니다. Docker Trusted Registry는 Docker 데이터 센터 제품의 일부로 포함됩니다. 자세한 내용은 [ https://docs.docker.com/docker-trusted-registry/overview/ ](https://docs.docker.com/docker-trusted-registry/overview/)합니다.

-   **Docker CE (Community Edition)** Windows 및 macOS 용 빌드, 실행 및 컨테이너를 로컬로 테스트에 대 한 개발 도구입니다. Windows용 Docker CE는 Linux 및 Windows 컨테이너에 개발 환경을 제공합니다. Windows의 Linux Docker 호스트를 기반으로 한 [Hyper-v](https://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx) VM. Windows 컨테이너에 대한 호스트는 Windows를 직접 기반으로 합니다. Mac 용 docker CE는 Apple 하이퍼바이저 framework를 기반으로 하며 [xhyve 하이퍼바이저](https://github.com/mist64/xhyve), 제공 하는 Linux Docker 호스트 VM에서 Mac OS X. Docker CE에 대 한 Windows 및 Mac 용 Docker 도구 상자를 Oracle VirtualBox를 기반으로 했습니다를 대체 합니다.

-   **Docker EE (Enterprise Edition)** 는 엔터프라이즈급 버전의 Linux 및 Windows 개발에 대 한 Docker 도구입니다.

-   **Compose** 명령줄 도구 및 YAML 파일 형식을 정의 하 고 다중 컨테이너 응용 프로그램 실행에 대 한 메타 데이터를 사용 하 여 합니다. 환경에 따라 값을 재정의할 수 있는 하나 이상의 .yml 파일을 사용하여 여러 이미지를 기반으로 하는 단일 응용 프로그램을 정의합니다. 정의 만든 후 단일 명령을 사용 하 여 전체 다중 컨테이너 응용 프로그램을 배포할 수 있습니다 (docker-등록 구성)는 Docker 호스트에 이미지당 컨테이너를 만듭니다.

-   **클러스터** 클러스터 내에서 여러 호스트에 걸쳐 분산 응용 프로그램 서비스의 여러 인스턴스로 확장할 수 있도록 단일 가상 Docker 호스트인 것 처럼 노출 하는 Docker 호스트의 컬렉션입니다. Docker Swarm, Mesosphere DC/OS, Kubernetes 및 Azure Service Fabric을 사용 하 여 Docker 클러스터를 만들 수 있습니다. (클러스터를 관리하는 데 Docker Swarm을 사용하는 경우 일반적으로 클러스터 대신 클러스터를 *swarm*으로 참조합니다.)

-   **오 케 스트레이 터** 클러스터 및 Docker 호스트의 관리를 간소화 하는 도구입니다. 오 케 스트레이 터를 사용 하는 이미지, 컨테이너 및 CLI 또는 그래픽 사용자 인터페이스를 통해 호스트를 관리할 수 있습니다. 컨테이너 네트워킹, 구성, 부하 분산, 서비스 검색, 고가용성, Docker 호스트 구성 등을 관리할 수 있습니다. 오케스트레이터는 노드 컬렉션 간에 워크로드를 실행하고, 배포하고, 크기를 조정하고. 복구하는 작업을 담당합니다. 일반적으로 오케스트레이터 제품은 Mesosphere DC/OS, Kubernetes, Docker Swarm 및 Azure Service Fabric과 같은 클러스터 인프라를 제공하는 동일한 제품입니다.

>[!div class="step-by-step"]
>[이전](what-is-docker.md)
>[다음](docker-containers-images-and-registries.md)