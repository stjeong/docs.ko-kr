---
title: Microsoft 도구를 사용하는 Docker 응용 프로그램 DevOps 워크플로
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기 및 Microsoft 도구를 사용하는 DevOps 워크플로
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: d313cb8ff6762eba6534ca20b214063315a456f0
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45639187"
---
# <a name="docker-application-devops-workflow-with-microsoft-tools"></a>Microsoft 도구를 사용하는 Docker 응용 프로그램 DevOps 워크플로

Microsoft Visual Studio, Azure DevOps 서비스, Team Foundation Server 및 Application Insights는 포괄적인 에코 시스템 개발 및 팀 프로젝트를 관리 하 고 신속 하 게 빌드, 테스트 및 배포 하는 도구를 제공 하는 IT 운영에 대 한 제공 컨테이너 화 된 응용 프로그램입니다.

Visual Studio 및 Team Foundation Server 온-프레미스와 클라우드의 Azure DevOps 서비스를 사용 하 여 개발 팀 수 생산적으로 빌드, 테스트 및 모든 플랫폼 (Windows 또는 Linux)을 대상으로 하는 컨테이너 화 된 응용 프로그램을 릴리스 합니다.

Microsoft 도구는 컨테이너 화 된 응용 프로그램의 특정 구현에 대 한 파이프라인을 자동화할 수 있습니다-Docker,.NET Core 또는 다른 플랫폼 조합 등 전역 빌드 및 CI (지속적인 통합) 및 Azure DevOps 서비스 또는 팀을 사용 하 여 테스트 Foundation Server에 연속 배포 (CD) Docker 환경 (개발, 스테이징, 프로덕션), 및 Application Insights를 통해 개발 팀 서비스에 대 한 분석 정보를 전송 합니다. 모든 코드 커밋은 빌드(CI)를 시작하고 특정 컨테이너화된 환경(CD)에 자동으로 서비스를 배포할 수 있습니다.

개발자와 테스터는 Microsoft Azure의 템플릿을 사용하여 프로덕션 환경과 유사한 Docker 기반의 개발 및 배포 환경을 쉽고 빠르게 프로비전할 수 있습니다.

컨테이너화된 응용 프로그램 개발의 복잡성은 비즈니스 복잡성 및 확장성 요구 사항에 따라 꾸준히 증가합니다. 마이크로 서비스 아키텍처 기반 응용 프로그램이 좋은 예입니다. 이러한 환경에서 성공하려면 프로젝트가 빌드 및 배포뿐만 아니라 원격 분석 컬렉션과 버전 관리까지 전체 수명 주기를 자동화해야 합니다. Azure DevOps 서비스 및 Azure는 다음과 같은 기능을 제공합니다.

-   Azure DevOps Services/Team Foundation Server 소스 코드 관리 (Git 또는 Team Foundation 버전 제어에 따라), Agile 계획 (Agile, 스크럼 및 CMMI 지원 됨), CI, 릴리스 관리 및 Agile 팀을 위한 다른 도구입니다.

-   Azure DevOps Services/Team Foundation Server는 강력 하 고 증가 에코 시스템 쉽게 수 CI, 빌드, 테스트, 배달, 생성 하 고 있는 릴리스 관리 파이프라인 마이크로 서비스에 대 한 첫 번째 및 타사 확장을 포함 합니다.

-   Azure DevOps 서비스에서 빌드 파이프라인의 일부로 자동화 된 테스트를 실행 합니다.

-   Azure DevOps 서비스를 강화할 수 있습니다 DevOps 수명 주기 여러 환경에 업데이트를 사용 하 여 프로덕션 환경 뿐만 아니라도 테스트를 위해 A를 포함 하 여 / B 실험 [카나리아 릴리스](https://martinfowler.com/bliki/CanaryRelease.html)등입니다.

-   조직에서는 이미 사용법을 잘 알고 있는 도구와 Azure Resource Manager 템플릿을 사용하여 Azure 구성 요소(데이터, PaaS 등)에 대한 종속성과 함께 Azure Container Registry에 저장된 비공개 이미지에서 Docker 컨테이너를 쉽게 프로비전할 수 있습니다.


>[!div class="step-by-step"]
[이전](../design-develop-containerized-apps/set-up-windows-containers-with-powershell.md)
[다음](docker-application-outer-loop-devops-workflow.md)
