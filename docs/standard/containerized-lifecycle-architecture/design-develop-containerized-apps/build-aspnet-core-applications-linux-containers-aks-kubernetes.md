---
title: Linux 컨테이너와 AKS/Kubernetes 클러스터에 배포 하는 ASP.NET Core 2.1 응용 프로그램 빌드
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 애플리케이션 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: b03b6fab9dcd53e97c2bc4d7e5c958ca4b931077
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221485"
---
# <a name="build-aspnet-core-21-applications-deployed-as-linux-containers-into-akskubernetes-orchestrator"></a>Linux 컨테이너와 AKS/Kubernetes 오 케 스트레이 터에 배포 하는 ASP.NET Core 2.1 응용 프로그램 빌드

Azure Kubernetes 서비스 (AKS)는 Azure의 관리 되는 Kubernetes 오케스트레이션 서비스 컨테이너 배포 및 관리를 간소화 하는입니다.

AKS 주요 기능은 다음과 같습니다.

- Azure 호스팅된 컨트롤 평면
- 자동된 업그레이드
- 자동 복구
- 사용자 구성 가능한 크기 조정
- 개발자와 클러스터 운영자 모두에 대 한 간단한 사용자 환경.

Linux에서 실행 되 고 개발은 수행 하는 동안 Azure에서 AKS 클러스터를 배포 하는 ASP.NET Core 2.1 응용 프로그램 만들기를 탐색 하는 다음 예제에서는 Visual Studio 2017을 사용 합니다.

## <a name="creating-the-aspnet-core-21-project-using-visual-studio-2017"></a>Visual Studio 2017을 사용 하 여 ASP.NET Core 2.1 프로젝트 만들기

ASP.NET Core는 Microsoft 및 GitHub의.NET 커뮤니티에서 유지 관리 하는 범용 개발 플랫폼입니다. 플랫폼 간으로 Windows, macOS 및 Linux를 지원하며 디바이스, 클라우드 및 포함/IoT 시나리오에서 사용할 수 있습니다.

이 예제에서는 간단한 기반이 되는 기반으로 프로젝트를 Visual Studio Web API 템플릿 샘플을 만드는 모든 추가 정보 필요 하지 않습니다. ASP.NET Core 2.1 기술을 사용 하 여 REST API를 사용 하 여 작은 프로젝트를 실행 하려면 모든 요소를 포함 하는 표준 템플릿을 사용 하 여 프로젝트를 만들려면 해야 합니다.

![ASP.NET Core 웹 응용 프로그램을 선택 하면 Visual Studio에서 새 프로젝트 창을 추가 합니다.](media/create-aspnet-core-application.png)

**그림 4-36**합니다. ASP.NET Core 응용 프로그램 만들기

샘플 프로젝트를 만들려면 선택 해야 **파일** > **새로 만들기** > **프로젝트** Visual Studio에서. 다음에 대 한 확인 해야 하는 여러 유형의 프로젝트에 대 한 템플릿의 목록이 표시 됩니다 **웹** > **.NET Core** 왼쪽된 패널에서 합니다. 이 예제에서는 선택 **ASP.NET Core 웹 응용 프로그램**합니다.

다음 대화 상자에서.NET Core 및 ASP.NET Core 2.1의 상위 pulldowns, 그림 4-37에에서 표시 된 것 처럼 대상 프레임 워크를 선택한 다음 ASP.NET Core Web API 응용 프로그램을 만들려면 API 옵션을 선택 하를 확인 합니다.

.NET Core 2.1 이상 Visual Studio 2017 버전 15.7.0 포함 되며 자동으로 설치 하 고 선택 하는 경우를 구성 합니다 **.NET Core 플랫폼 간 개발** 설치 하는 동안 작업 합니다.

![Visual Studio 대화 상자 API 옵션이 선택 된 ASP.NET Core 웹 응용 프로그램의 유형을 선택 합니다.](media/create-web-api-application.png)

**그림 4-37**합니다. ASP.NET CORE 2.1을 선택 하 고 Web API 프로젝트 형식

이전 버전의.NET Core를 사용 하는 경우 다운로드 하 고에서 2.1 버전을 설치할 수 <https://www.microsoft.com/net/download/core#/sdk>입니다.

이전 단계에서 또는 나중에 프로젝트를 시작한 후 필요할 경우 프로젝트를 만들 때 Docker 지원을 추가할 수 있습니다. 프로젝트를 만든 후에 Docker 지원을 추가 하려면 마우스 오른쪽 단추로 클릭에서 프로젝트 파일을 **솔루션 탐색기** 선택한 **추가** > **Docker 지원** 에서 상황에 맞는 메뉴입니다.

![기존 프로젝트에 Docker 지원을 추가 하려면 상황에 맞는 메뉴 옵션: 마우스 오른쪽 단추로 클릭 (프로젝트) > 추가 > Docker 지원 합니다.](media/add-docker-support-to-project.png)

**그림 4-38**합니다. 기존 프로젝트에 Docker 지원 추가

Docker 지원 추가 완료 하려면 Windows 또는 Linux 중에서 선택을 해야 합니다. 이 경우 선택 **Linux**이므로 AKS (런타임에 2018)로 Windows 컨테이너를 지원 하지 않습니다.

![옵션 대화 상자를 Dockerfile에 대 한 대상 OS를 선택 합니다.](media/select-linux-docker-support.png)

**그림 4-39**합니다. Linux 컨테이너를 선택합니다.

이러한 간단한 단계를 사용 하 여 ASP.NET Core 2.1 응용 프로그램을 Linux 컨테이너에서 실행 해야 합니다.

알 수 있듯이 Visual Studio 2017 및 Docker 간의 통합은 개발자의 생산성을 완전히 방향인 합니다.

이제 눌러도 **F5** 를 빌드하고 응용 프로그램을 실행 합니다.

프로젝트를 실행 한 후 사용 하 여 이미지를 나열할 수 있습니다는 `docker images` 명령입니다. 표시 된 `mssampleapplication` Visual Studio 2017을 사용 하 여 프로젝트의 자동 배포를 사용 하 여 만든 이미지입니다.

```console
docker images
```

![콘솔 출력에서 docker images 명령을 사용 하 여 목록을 보여 줍니다. 리포지토리, 태그, 이미지 ID, Created (날짜) 및 크기입니다.](media/docker-images-command.png)

**그림 4 ~ 40**합니다. Docker 이미지 보기

## <a name="register-the-solution-in-the-azure-container-registry"></a>Azure Container Registry에 솔루션 등록

예: 모든 Docker 레지스트리로 이미지를 업로드 [ACR Azure Container Registry ()](https://azure.microsoft.com/services/container-registry/) 또는 Docker Hub 이미지는 레지스트리에서 AKS 클러스터에 배포할 수 있도록 합니다. 이 경우 Azure Container Registry에 이미지를 업로드 하는 것입니다.

### <a name="create-the-image-in-release-mode"></a>릴리스 모드에서 이미지 만들기

이미지를 만들 **릴리스** 다음과 같이 모드 (프로덕션용으로 준비 된) 릴리스를 변경 하 고 응용 프로그램을 다시 실행 하려면 F5 키를 누릅니다.

![릴리스 모드에서 빌드를 VS에서 도구 모음 옵션입니다.](media/select-release-mode.png)

**그림 4-41**합니다. 릴리스 모드를 선택합니다.

실행 하는 경우는 `docker image` 명령을 만든 이미지를 모두 표시 됩니다. 프로그램용 `debug` 및 다른 `release` 모드입니다.

### <a name="create-a-new-tag-for-the-image"></a>이미지에 대 한 새 태그 만들기

각 컨테이너 이미지를 사용 하 여 태그를 지정 해야 합니다.는 `loginServer` 레지스트리 이름입니다. 이 태그는 컨테이너 이미지를 이미지 레지스트리에 밀어넣을 때 라우팅에 사용 됩니다.

볼 수는 `loginServer` Azure Container Registry에서 정보를 얻고, Azure portal에서 이름

![브라우저 보기는 Azure 컨테이너 레지스트리 이름의 오른쪽 상단의입니다.](media/loginServer-name.png)

**그림 4-42**합니다. 레지스트리 이름 보기

또는 다음 명령을 실행 하 여:

```console
az acr list --resource-group MSSampleResourceGroup --query "[].{acrLoginServer:loginServer}" --output table
```

![위 명령의 출력을 콘솔입니다.](media/az-cli-loginServer-name.png)

**그림 4-43**합니다. PowerShell을 사용 하 여 레지스트리의 이름으로 가져오기

두 경우 모두 이름을 얻을 수 있습니다. 예에서 `mssampleacr.azurecr.io`합니다.

이제 다음 명령을 사용 하 여 최신 이미지 (릴리스 이미지)를 수행 이미지를 태그로 지정할 수 있습니다.

```console
docker tag mssampleaksapplication:latest mssampleacr.azurecr.io/mssampleaksapplication:v1
```

실행 한 후 합니다 `docker tag` 명령에 사용 하 여 이미지를 나열 합니다 `docker images` 명령입니다. 새 태그를 사용 하 여 이미지를 표시 됩니다.

![콘솔 출력에서 docker images 명령을 합니다.](media/tagged-docker-images-list.png)

**그림 4-44**합니다. 태그가 지정 된 이미지의 보기

### <a name="push-the-image-into-the-azure-acr"></a>Azure ACR에 이미지 푸시

다음 명령을 사용 하 여 Azure ACR에 이미지를 푸시하십시오.

```console
docker push mssampleacr.azurecr.io/mssampleaksapplication:v1
```

이 명령을 걸립니다 이미지 업로드 되지만 프로세스의 피드백을 제공 합니다.

![콘솔 출력에서 docker push 명령은: 각 계층에 대 한 문자 기반 진행률 표시줄을 보여 줍니다.](media/uploading-image-to-acr.png)

**그림 4-45**합니다. ACR에 이미지 업로드

프로세스가 완료 되는 경우 얻게 결과 아래 확인할 수 있습니다.

![콘솔에서 완료 되 면 모든 레이어 또는 노드를 보여 주는 docker push 명령은 출력 합니다.](media/uploading-docker-images-complete.png)

**그림 4-46**합니다. 노드 보기

다음 단계 AKS Kubernetes 클러스터에 컨테이너를 배포 하는 것입니다. 파일을 필요 (**.yml 파일 배포**),이 경우에 포함:

```yml
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: mssamplesbook
spec:
  replicas: 1
  template:
    metadata:
      labels:
        app: mssample-kub-app
    spec:
      containers:
        - mane: mssample-services-app
          image: mssampleacr.azurecr.io/mssampleaksapplication:v1
          ports:
            - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
    name: mssample-kub-app
spec:
  ports:
    - name: http-port
      port: 80
      targetPort: 80
  selector:
    app: mssample-kub-app
  type: LoadBalancer
```

> [!NOTE]
> Kubernetes 사용 하 여 배포에 대 한 자세한 내용은 다음을 참조 하세요. <https://kubernetes.io/docs/reference/kubectl/cheatsheet/>

이제 사용 하 여 배포할 준비가 거의 **Kubectl**,이 명령 사용 하 여 AKS 클러스터에 자격 증명을 먼저 가져와야 하지만:

```console
az aks get-credentials --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

![위 명령의 출력을 콘솔: 현재 컨텍스트에서 /root/.kube/config으로 병합 된 "MSSampleK8Cluster](media/getting-aks-credentials.png)

**그림 4-47**합니다. 자격 증명 가져오기

사용 하 여는 `kubectl create` 배포를 시작 하는 명령입니다.

```console
kubectl create -f mssample-deploy.yml
```

![위 명령의 출력을 콘솔: 배포 "mssamplesbook"을 생성 합니다. "mssample-kub-" 만든 앱 서비스입니다.](media/kubectl-create-command.png)

**그림 4-48**합니다. Kubernetes에 배포

배포가 완료 되 면이 명령을 사용 하 여 일시적으로 액세스할 수 있는 로컬 프록시를 사용 하 여 Kubernetes 콘솔을 액세스할 수 있습니다.

```console
az aks browse --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

Url에 액세스 하 고 `http://127.0.0.1:8001`입니다.

![Kubernetes 대시보드를 배포, Pod, 복제본 집합 및 서비스를 보여 주는의 브라우저 보기입니다.](media/kubernetes-cluster-information.png)

**그림 4-49**합니다. Kubernetes 클러스터 정보를 보려면

이제 azure에서 Linux 컨테이너와 AKS Kubernetes 클러스터를 사용 하 여 배포 된 응용 프로그램을 수 있습니다. Azure portal에서 가져올 수 있는 서비스의 공용 IP로 이동 하 여 앱에 액세스할 수 있습니다.

> [!NOTE]
> 섹션에서이 샘플에 대 한 AKS 클러스터를 만드는 방법 보시 [ **Azure Kubernetes Service (AKS)를 배포** ](deploy-azure-kubernetes-service.md) 이 가이드에서.

>[!div class="step-by-step"]
>[이전](set-up-windows-containers-with-powershell.md)
>[다음](../docker-devops-workflow/index.md)
