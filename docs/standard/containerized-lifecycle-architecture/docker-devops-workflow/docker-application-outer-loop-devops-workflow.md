---
title: Docker 응용 프로그램에 대 한 외부 루프 DevOps 워크플로의 단계
description: "\"외부 루프\" DevOps 워크플로의 단계에 알아봅니다."
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: b75e9df1c31e8bcebcaa6d56336a6aa499d13e1d
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56220941"
---
# <a name="steps-in-the-outer-loop-devops-workflow-for-a-docker-application"></a>Docker 응용 프로그램에 대 한 외부 루프 DevOps 워크플로의 단계

그림 5-1 외부 루프 DevOps 워크플로 구성 하는 단계는 종단 간 묘사 하 여를 표시 합니다.

![](./media/image1.png)

그림 5-1: Microsoft 도구를 사용 하 여 Docker 응용 프로그램에 대 한 DevOps 외부 루프 워크플로

이제 이러한 각 단계를 자세히 살펴보겠습니다.

## <a name="step-1-inner-loop-development-workflow"></a>1단계: 내부 루프 개발 워크플로

이 단계는 4 장에에서 자세히 설명 되어 있지만 정리 하자면, 여기 있는 외부 루프 시작 되는, 현재는 개발자는 CI 파이프라인 작업을 시작 하는 소스 제어 관리 시스템 (예: Git) 코드를 푸시합니다.

## <a name="step-2-source-code-control-integration-and-management-with-azure-devops-services-and-git"></a>2단계: 소스 코드 컨트롤 통합과 Azure DevOps Services 및 Git를 사용 하 여 관리

이 단계에서 버전 제어 시스템이 통합된 버전을 팀의 다른 개발자 로부터 들어오는 모든 코드를 수집 하도록 해야 합니다.

소스 코드 제어 (SCC) 및 소스 코드 관리 습관적으로 대부분의 개발자, DevOps 수명에서 Docker 응용 프로그램을 만들 때 주기 것 처럼 보일 수, 하는 경우에 반드시 응용 프로그램을 사용 하 여 Docker 이미지를 전송 하지 해야 강조 하기 위해 레지스트리를 직접 전역 Docker (예: Azure Container Registry 또는 Docker 허브) 개발자의 컴퓨터에서. 반면, Docker 이미지를 해제 하 고 프로덕션 환경에 배포 된 전역 빌드 또는 소스 코드 리포지토리 (예: Git)에 따라 CI 파이프라인에 통합 되는 소스 코드에만 생성 되어야 합니다.

자신의 컴퓨터에서 테스트 하는 경우 개발자가 하 여 자체는 개발자가 생성 되는 로컬 이미지를 사용할지 합니다. 이 때문에 반드시는 SCC 코드에서 활성화 DevOps 파이프라인을 포함 해야 합니다.

Azure DevOps 서비스 및 Team Foundation Server Git 및 Team Foundation 버전 제어를 지원합니다. 선택 하 고 엔드-투-엔드 Microsoft 환경을 사용할 수 있습니다. 그러나을 관리할 수도 있습니다 (예: GitHub, 온-프레미스 Git 리포지토리 또는 Subversion) 외부 리포지토리에서 코드를 연결 하 여 DevOps CI 파이프라인에 대 한 시작 점으로 코드를 가져올 수 있습니다.

## <a name="step-3-build-ci-integrate-and-test-with-azure-devops-services-and-docker"></a>3단계: CI 빌드를 통합 하 고 Azure DevOps를 사용 하 여 테스트 서비스 및 Docker

CI는 최신 소프트웨어 테스트 및 배달에 대 한 표준으로 부상 했습니다. Docker 솔루션 개발 및 운영 팀 간의 명확히 분리를 유지 관리합니다. Docker 이미지의 불변성 개발, CI를 통해 테스트 및 프로덕션 환경에서 실행에 어떤 간의 반복 가능한 배포를 확인 합니다. Docker 엔진 개발자 노트북에서 배포 및 테스트 인프라 전반에서 컨테이너 노트북 환경입니다.

이 시점에서 제출 된 올바른 코드를 사용 하 여 버전 제어 시스템을 설정한 후 해야는 *빌드 서비스* 코드를 선택 하 여 전역 빌드 및 테스트를 실행 합니다.

(CI, 빌드, 테스트)이이 단계에 대 한 내부 워크플로 빌드 서버 (Azure DevOps 서비스), Docker 엔진 및 Docker 레지스트리 코드 리포지토리 (Git, 등)으로 구성 된 CI 파이프라인의 생성에 대 한 경우

사용할 수 있습니다 Azure DevOps 서비스를 기반으로 작성된 된 "아티팩트"를 게시 한 응용 프로그램을 빌드 및 CI 파이프라인을 설정 하기 위한 "아티팩트 리포지토리에," 다음 단계에 설명 된.

"최종 아티팩트" 배포에 대해 Docker를 사용 하는 경우 배포할 응용 프로그램 또는 서비스를 사용 하 여 Docker 이미지 내에 포함 되 고 있습니다. 이러한 이미지는 푸시 되거나 게시 된 *Docker 레지스트리* (Azure Container Registry에 있을 수 있는 것 처럼 Docker Hub 레지스트리에서 공식 기본 이미지에 대 한 일반적으로 사용 되는 또는 공용 같은 개인 리포지토리에서).

다음은 기본 개념이입니다. CI 파이프라인이 꺼집니다 시작-Git와 같은 소스 코드 제어 리포지토리에 커밋으로 합니다. 커밋 그림 5-2에서와 같이 Azure DevOps 서비스는 Docker 컨테이너 내에서 빌드 작업을 실행 하 고 해당 작업을 성공적으로 완료 되 면 Docker 레지스트리에 Docker 이미지를 푸시 하면 됩니다.

![](./media/image2.png)

그림 5-2: CI 단계

Docker 및 Azure DevOps 서비스를 사용 하 여 기본 CI 워크플로 단계는 다음과 같습니다.

1.  개발자 (Git/Azure DevOps Services, GitHub 등)는 SCC 리포지토리에 커밋을 푸시합니다.

2.  Azure DevOps Services 또는 Git를 사용 하는 경우 CI이 구축 되어 Azure DevOps 서비스에서 확인란을 선택 하 여 간단한 됨을 의미 합니다. 외부 SCC (예: GitHub)를 사용 하는 경우는 *웹 후크* Azure DevOps 서비스 업데이트를 미리 알리거나 Git/GitHub에 푸시 됩니다.

3.  Azure DevOps 서비스 응용 프로그램 및 테스트 코드 뿐만 아니라 이미지를 설명 하는 DockerFile을 포함 하 여 SCC 리포지토리를 가져옵니다.

4.  Azure DevOps 서비스에서는 Docker 이미지를 빌드하고 빌드 번호를 사용 하 여 레이블.

5.  Azure DevOps 서비스 프로 비전 된 Docker 호스트 내에서 Docker 컨테이너를 인스턴스화하고 적절 한 테스트를 실행 합니다.

6.  "축복 받은 빌드"는 것을 알 수 있도록 이미지를 먼저 의미 있는 이름을 재지정 된 테스트에 성공한 경우 (같은 "/ 1.0.0" 또는 다른 레이블), 한 다음 Docker 레지스트리 (Docker 허브, Azure Container Registry, DTR 등)까지 푸시되 고

### <a name="implementing-the-ci-pipeline-with-azure-devops-services-and-the-docker-extension-for-azure-devops-services"></a>Azure DevOps 서비스에 대 한 Azure DevOps 서비스 및 Docker 확장을 사용 하 여 CI 파이프라인 구현

합니다 [Azure DevOps 서비스 Docker 확장](https://aka.ms/vstsdockerextension) CI 파이프라인 된 Docker 이미지 빌드, 인증 된 Docker 레지스트리에 Docker 이미지 푸시, Docker 이미지를 실행 하거나 실행할 수는 Docker에서 제공 하는 다른 작업에 태스크 추가 CLI입니다. 또한 빌드, 푸시 및 다중 컨테이너 Docker 응용 프로그램을 실행 또는 그림 5-3에서와 같이 Docker 작성 CLI에서 제공 하는 다른 작업을 실행 하는 데 사용할 수 있는 Docker Compose 작업을 추가 합니다.

![](./media/image3.png)

그림 5-3: Azure DevOps 서비스에서 Docker CI 파이프라인

Docker 확장 컨테이너 또는 이미지 레지스트리 및 Docker 호스트에 대 한 서비스 끝점을 사용할 수 있습니다. (이 현재 사용자 지정 Azure DevOps 서비스 에이전트가 필요); 사용 가능한 경우 로컬 Docker 호스트를 사용 하 여 작업 기본값 이 고, 그렇지 Docker 호스트 연결을 제공 해야 합니다. Docker 레지스트리에 이미지 푸시하기 등을 사용 하 여 인증에 종속 된 작업에 제공 하는 Docker 레지스트리 연결 해야 합니다.

Azure DevOps 서비스 Docker 확장 Azure DevOps 서비스 계정에 다음 구성 요소를 설치 합니다.

-   Docker 레지스트리 연결에 대 한 서비스 끝점

-   Docker 컨테이너 호스트에 연결 하는 것에 대 한 서비스 끝점

-   다음을 수행 하는 Docker 작업:

-   이미지 빌드

-   레지스트리에 이미지 또는 리포지토리 푸시

-   컨테이너 이미지 실행

-   Docker 명령을 실행 합니다.

-   Docker Compose 명령을 실행 하는 Docker Compose 작업

이러한 Azure DevOps 서비스 작업을 사용 하 여 빌드를 Linux Docker 호스트/v M Azure에서 프로 비전 하 고 기본 Docker 레지스트리 (Azure Container Registry, Docker 허브에서 개인 Docker DTR 또는 다른 Docker 레지스트리)에서 Docker CI 파이프라인을 어셈블할 수 있습니다는 매우 일관 된 방법입니다.

***요구 사항:***

-   Azure DevOps 서비스 또는 온-프레미스 설치를 Team Foundation Server 2015 업데이트 3 이상에 대 한 합니다.

-   Docker 이진 파일에 있는 Azure DevOps 서비스 에이전트.

다음 중 하나를 만드는 쉬운 Azure DevOps 서비스 에이전트가 Docker 이미지를 기반으로 컨테이너를 실행 하 Docker를 사용 하는 것입니다.

**자세한 내용은** 읽기 Azure DevOps 서비스 Docker CI를 조합 하는 방법에 대 한 자세한 내용은 파이프라인 연습을 보려면 다음 사이트를 방문 하십시오.

Docker 컨테이너로 Azure DevOps 서비스 에이전트를 실행 합니다. [ https://hub.docker.com/r/\ microsoft/vsts 에이전트 /](https://hub.docker.com/r/microsoft/vsts-agent/)

Azure DevOps 서비스 Docker 확장: <https://aka.ms/vstsdockerextension>

Azure DevOps 서비스를 사용 하 여.NET Core Linux Docker 이미지를 작성 합니다. <https://blogs.msdn.microsoft.com/stevelasker/2016/06/13/building-net-core-linux-docker-images-with-visual-studio-team-services/>

Docker 지원 사용 하 여 Linux 기반 Visual Studio Team Service 빌드 컴퓨터 구축: <http://donovanbrown.com/post/2016/06/03/Building-a-Linux-Based-Visual-Studio-Team-Service-Build-Machine-with-Docker-Support>

### <a name="integrate-test-and-validate-multicontainer-docker-applications"></a>통합, 테스트 및 다중 컨테이너 Docker 응용 프로그램의 유효성을 검사합니다

일반적으로 단일 컨테이너 대신 다중 컨테이너 Docker 응용 프로그램 대부분의 구성 됩니다. 좋은 예는 마이크로 서비스 지향 응용 프로그램을 마이크로 서비스 당 하나의 컨테이너를 해야 합니다. 그러나 마이크로 서비스 접근 방식을 패턴을 엄격 하 게 수행 하지 않고도 Docker 응용 프로그램의 여러 컨테이너 또는 서비스가 구성 된 것 가능성이 매우 높습니다.

따라서 CI 파이프라인에서 응용 프로그램 컨테이너를 빌드한 후 해야 배포, 통합 및 모든 컨테이너 되는 테스트 클러스터를 또는 통합 Docker 호스트 내에서 해당 컨테이너를 사용 하 여 전체적으로 응용 프로그램 테스트 분산 합니다.

단일 호스트를 사용 하는 경우 docker와 같은 Docker 명령을 사용할 수 있습니다-빌드 및 테스트 하 고 단일 VM에서 Docker 환경 유효성 검사에 관련 된 컨테이너 배포를 구성 합니다. 그러나 다른 메커니즘 또는 선택한 클러스터/스케줄러에 따라 오 케 스트레이 터를 통해 컨테이너를 배포 해야 하는 DC/OS, Kubernetes 또는 Docker Swarm과 같은 오 케 스트레이 터 클러스터와 함께 작업 하는 경우.

다음은 몇 가지 유형의 테스트는 Docker 컨테이너에 대해 실행할 수 있습니다.

-   Docker 컨테이너에 대 한 단위 테스트

-   상호 관련 된 응용 프로그램 또는 마이크로 서비스의 테스트 그룹

-   프로덕션 및 "카나리아" 릴리스에서 테스트

중요 한 점은 통합 및 기능 테스트를 실행할 때 컨테이너 외부에서 이러한 테스트 실행 해야 합니다. 테스트를 정의 수 및 컨테이너는 프로덕션 환경에 배포 하는 것과 같은 정확 하 게 해야 하는 정적 이미지에 기반 하므로, 배포 하는 컨테이너 내에서 실행 해야 합니다.

여러 클러스터 (클러스터, 클러스터 준비 및 프로덕션 클러스터 테스트) 테스트 같은 고급 시나리오를 테스트 하는 경우에 매우 적합 옵션을 다양 한 클러스터에서 테스트를 레지스트리로 이미지를 게시 하는 것입니다.

### <a name="push-the-custom-application-docker-image-into-your-global-docker-registry"></a>전역 Docker 레지스트리의 사용자 지정 응용 프로그램 Docker 이미지 푸시

Docker 이미지를 테스트 하 고 유효성을 검사 한 후 태그 Docker 레지스트리에 게시 하는 것이 좋습니다. Docker 레지스트리에 이므로 중요 한 부분을 Docker 응용 프로그램 수명 주기에서 QA 및 프로덕션 환경에 배포 하 여 사용자 지정 테스트 (즉, "축복 받은 이미지")을 저장할 중앙 위치입니다.

Docker 레지스트리는 "진실의 원본" QA 또는 프로덕션 환경에 배포할 응용 프로그램 이진 또는 비트에 대 한 어떻게 SCC 리포지토리 (Git 등)에 저장 하는 응용 프로그램 코드는 "진실의 원본" 비슷합니다.

일반적으로 있습니다 (예: 제한 된 액세스를 사용 하 여 공용 클라우드 레지스트리 또는 Azure Container Registry 또는 Docker Trusted Registry와 같은 온-프레미스 레지스트리를 사용자 지정 이미지에 대 한 개인 리포지토리에 개인 리포지토리에 해야 할 수 있습니다. Docker 허브), 하지만이 예제의 마지막 코드 오픈 소스, 없는 경우 공급 업체의 보안을 신뢰 해야 합니다. 어떤 방법을 사용 하는이 작업을 수행 하는 방법을 상당히 유사 하 고 docker push 명령은 궁극적으로 따라 그림 5-4에서 언급 했 듯이.

![](./media/image4.png)

그림 5-4: Docker 레지스트리에 사용자 지정 이미지 게시

Azure Container Registry, Amazon 웹 서비스 컨테이너 레지스트리, Google Container Registry, Quay 레지스트리 등 클라우드 공급 업체에서 Docker 레지스트리의 여러 제품 있습니다.

Azure DevOps 서비스 Docker 확장을 사용 하 여 그림 5-5에 나와 있는 것 처럼 docker compose.yml 파일 (예: Azure Container Registry)에 인증 된 Docker 레지스트리에 여러 태그를 사용 하 여 정의한 서비스 이미지 집합을 푸시할 수 있습니다.

![](./media/image5.png)

그림 5-5: Azure DevOps 서비스를 사용 하 여 Docker 레지스트리로 사용자 지정 이미지를 게시 하려면

**자세한 내용은** 자세한 Azure DevOps 서비스에 대 한 Docker 확장을 하는 방법에 대 한 이동 <https://aka.ms/vstsdockerextension>합니다. Azure Container Registry에 대 한 자세한 내용은 이동 <https://aka.ms/azurecontainerregistry>합니다.

## <a name="step-4-cd-deploy"></a>4단계: CD 배포

Docker 이미지의 불변성 개발, CI를 통해 테스트 및 프로덕션 환경에서 실행에 무엇을 사용 하 여 반복 가능한 배포를 확인 합니다. Docker 레지스트리 (사설 또는 공용)에 게시 된 응용 프로그램 Docker 이미지를 만든 후 발생할 수 있는 여러 환경에 배포할 수 있습니다 (프로덕션, QA, 스테이징 등) Azure DevOps 서비스를 사용 하 여 CD 파이프라인에서 파이프라인 작업 또는 Azure DevOps 서비스 릴리스 관리 합니다.

그러나이 시점에서 종속 배포 된 Docker 응용 프로그램의 종류입니다. 간단한 응용 프로그램 (컴퍼지션 및 배포의 관점에서)는 모놀리식 소수의 컨테이너 또는 서비스를 구성 하는 응용 프로그램 및 배포 된 소수의 서버 또는 Vm을 배포 하는 것이 같은 더 복잡 한 응용 프로그램을 배포 하는 데 다르지는 마이크로 서비스 지향 응용 프로그램에 대규모 기능입니다. 이러한 두 시나리오는 다음 섹션에 설명 되어 있습니다.

### <a name="deploying-composed-docker-applications-to-multiple-docker-environments"></a>구성 된 여러 Docker 환경에 Docker 응용 프로그램 배포

덜 복잡 한 시나리오에서 첫 번째를 살펴보겠습니다: 단일 환경 또는 여러 환경에서 간단한 Docker 호스트 (Vm 또는 서버)에 배포 (QA, 스테이징 및 프로덕션). 이 시나리오에서는 내부적으로 CD 파이프라인에 따르면 docker-그림 5 ~ 6에서와 같이 컨테이너 또는 서비스의 관련된 집합을 사용 하 여 Docker 응용 프로그램을 배포 (Azure DevOps 서비스 배포 작업)에서 구성 합니다.

![](./media/image6.png)

그림 5 ~ 6: 간단한 Docker 호스트 환경 레지스트리에 응용 프로그램 컨테이너 배포

그림 5-7 작업 추가 대화 상자에서 Docker Compose를 클릭 하 여 Azure DevOps 서비스를 통해 QA/테스트 환경에 빌드 CI를 연결할 수는 방법을 강조 표시 합니다. 그러나 스테이징 또는 프로덕션 환경에 배포할 때 일반적으로 사용 여러 환경을 처리 하는 릴리스 관리 기능 (같은 QA, 스테이징 및 프로덕션). Azure DevOps 서비스를 사용 하는 단일 Docker 호스트에 배포 하는 경우 "Docker Compose" 작업 (docker를 호출 하는 것입니다-내부에서 명령을 작성). Azure Container Service에 배포 하는 경우 다음에 나오는 섹션에서 설명 했 듯이 Docker 배포 작업을 사용 합니다.

![](./media/image7.png)

그림 5-7: Azure DevOps 서비스 파이프라인의 Docker Compose 작업을 추가합니다.

Azure DevOps Services에서 릴리스를 만들 때 입력된 아티팩트 집합을 사용 합니다. 그 이유는 다양 한 환경에서 릴리스 수명 동안 변경할 수 없어야 하기 위해서입니다. 컨테이너를 도입 하는 경우 입력된 아티팩트를 배포 하는 레지스트리에서 이미지를 식별 합니다. 를 확인 하는 방법에 따라 docker-compose 파일에서 "myimage:latest"를 참조 하는 경우 가장 뚜렷한 사례는 릴리스 기간 동안 동일 하 게 보장 되지 않습니다.

Azure DevOps 서비스에 대 한 Docker 확장을 사용 하면 특정 레지스트리에 이미지를 포함 하는 빌드 아티팩트를 생성 하는 기능 다이제스트 고유 하 게 식별 하는 이미지를 이진 보장 된 합니다. 이들은 정말로 원하는 릴리스에 대 한 입력으로 사용 합니다.

### <a name="managing-releases-to-docker-environments-by-using-azure-devops-services-release-management"></a>Azure DevOps 서비스 Release Management를 사용 하 여 Docker 환경에 릴리스 관리

Azure DevOps 서비스 확장을 통해 하 수 새 이미지를 빌드하고, Docker 레지스트리에 게시, Linux 또는 Windows 호스트에서 실행 및 docker와 같은 명령을 사용 하 여-Azure DevOps 전체에 걸쳐 전체 응용 프로그램으로 여러 컨테이너를 배포 하려면 작성 그림 5 ~ 8에 나와 있는 것 처럼 여러 환경을 위한 릴리스 관리 기능을 서비스 합니다.

![](./media/image8.png)

그림 5 ~ 8: Azure DevOps 서비스 Release Management에서 Azure DevOps 서비스 Docker Compose 작업 구성

그러나 그림 5-6에서 표시 하 고 그림 5-8의 구현 시나리오 간단한 Docker 호스트 및 Vm에 배포 되는 것과 단일 컨테이너 또는 이미지 당 인스턴스 수는 상당히 기본적 이며 아마도 sc 개발 또는 테스트에 대해서만 사용할 수 해야 염두에서에 둡니다 enarios 합니다. 대부분의 엔터프라이즈 프로덕션 시나리오에서 HA (고가용성)가 하려는 및 분산 하 여 여러 노드, 서버 및 Vm의 경우와 "지능형 장애 조치"에서 따라서 하는 경우 서버 또는 노드를 관리 하기 쉬운 확장성에 실패 하면 해당 서비스 및 컨테이너는 다른 호스트 서버 또는 VM으로 이동 됩니다. 이 경우 컨테이너 클러스터, 오 케 스트레이 터, 스케줄러 등 고급 기술이 필요합니다. 따라서 해당 클러스터에 배포 하는 방법은 다음 섹션에 설명 된 고급 시나리오를 통해 정확 하 게 됩니다.

### <a name="deploying-complex-docker-applications-to-docker-clusters-dcos-kubernetes-and-docker-swarm"></a>Docker 클러스터 (DC/OS, Kubernetes 및 Docker Swarm)에 복잡 한 Docker 응용 프로그램 배포

분산된 응용 프로그램의 특성에는 또한 배포 되는 계산 리소스가 필요 합니다. 풀링된 리소스를 기반으로 한 HA 및 높은 확장성을 제공 하는 기능을 클러스터링 프로덕션 규모 기능 하도록 해야 합니다.

Docker Swarm과 같은 CLI 도구에서 위에 해당 클러스터에 컨테이너를 수동으로 배포할 수 있습니다 (사용과 같은 [docker 서비스를 만들](https://docs.docker.com/engine/swarm/swarm-tutorial/deploy-service/)) 또는 웹 UI와 같은 [Mesosphere Marathon](https://mesosphere.github.io/marathon/docs/marathon-ui.html) DC/os 클러스터에 있지만 해야 같은 확장 또는 모니터링 목적으로 관리 목적을 위해 또는 punctual 배포 테스트에 있는 예약 합니다.

Azure DevOps 서비스는 CD의 관점에서 특히에서 실행할 수 있습니다 특별히 만든된 배포 작업 컨테이너의 분산된 클러스터에 컨테이너 화 된 응용 프로그램 배포는 Azure DevOps 서비스 릴리스 관리 환경 그림 5-9에서와 같이 서비스입니다.

![](./media/image9.png)

그림 5-9: 컨테이너 서비스에 분산된 된 응용 프로그램 배포

처음에 특정 클러스터 또는 오 케 스트레이 터에 배포할 때 일반적으로 사용 특정 배포 스크립트 및 각 오 케 스트레이 터 (즉, Mesosphere DC/OS 또는 Kubernetes는 Docker 및 Docker 보다 다양 한 배포 메커니즘이 메커니즘 Swarm) 대신를 간단 하 고 사용 하기 쉬운 docker compose docker compose.yml 정의 파일을 기반으로 하는 도구입니다. 그러나 그림 5-10에서 표시 된 Microsoft Azure DevOps 서비스 Docker 배포 작업 덕분 있습니다 이제도 배포할 수 DC/OS에만 Microsoft는 해당 "변환"를 수행 하기 때문에 친숙 한 docker compose.yml 파일을 사용 하 여 (에서 프로그램 docker compose.yml 파일 DC/OS에 필요한 다른 형식으로).

![](./media/image10.png)

그림 5-10: 환경 RM에서 Docker 배포 작업 추가

그림 5-11 Docker 배포 작업을 편집 대상 유형 (Azure Container Service DC/OS,이 경우), Docker Compose 파일 및 Docker 레지스트리 연결 (예: Azure Container Registry 또는 Docker 허브)을 지정 하는 방법을 보여 줍니다. 태스크는 DC/OS 클러스터에서 컨테이너를 배포할 준비 쉬운 사용자 지정 Docker 이미지를 검색 하는 위치입니다.

![](./media/image11.png)

그림 5-11: Docker 배포 작업 정의 배포 하려면 Azure Container Service DC/OS

**자세한 내용은** 자세한 Azure DevOps 서비스 및 Docker를 사용 하 여 CD 파이프라인에 대 한 다음 사이트를 방문 하십시오.

Docker 및 Azure Container Service에 대 한 azure DevOps 서비스 확장: [ https://aka.ms/\ vstsdockerextension](https://aka.ms/vstsdockerextension)

Azure Container Service: <https://aka.ms/azurecontainerservice>

Mesosphere DC/OS: <https://mesosphere.com/product/>

## <a name="step-5-run-and-manage"></a>5단계: 실행 및 관리

실행 하 고 응용 프로그램을 관리 하기 때문에 엔터프라이즈 프로덕션에서 수준에서 자체의 및 작업의 형식으로 인해 주요 주제 이며이 영역의 큰 범위와 해당 수준 (IT 작업)에서 작업 하는 사람들을에서는 사용 되는 전체 다음 설명에 장입니다.

## <a name="step-6-monitor-and-diagnose"></a>6단계: 모니터링 및 진단

이 항목에서는 또한 가려집니다 다음 장에서 IT 운영 프로덕션 시스템에서 수행 하는 작업의 일부로 그러나이 응용 프로그램은 지속적으로 개선 되도록이 단계에서 얻은 통찰력을 개발 팀에 다시 넣어야 강조 표시 해야 합니다. 해당 관점에서 일부 이기도 하므로 DevOps의 태스크 및 작업에서 일반적으로 수행 하지만 IT.

모니터링 및 진단 DevOps 영역 내에서 100%가 하는 경우에 모니터링 하는 프로세스 및 테스트 또는 베타 환경에 대 한 개발 팀에서 수행 하는 분석 됩니다. 부하 테스트를 수행 하 여 또는 베타 또는 QA 환경에서 베타 테스터 새 버전을 시도 하는 모니터링 하 여 수행 됩니다.

>[!div class="step-by-step"]
>[이전](index.md)
>[다음](create-ci-cd-pipelines-azure-devops-services-aspnetcore-kubernetes.md)
