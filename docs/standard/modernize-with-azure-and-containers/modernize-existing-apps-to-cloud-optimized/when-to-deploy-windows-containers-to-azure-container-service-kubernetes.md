---
title: Azure Container Service (즉, Kubernetes)에 Windows 컨테이너를 배포 하는 경우
description: Azure 클라우드 및 Windows 컨테이너를 사용 하 여 기존.NET 응용 프로그램 현대화 | Azure Container Service (즉, Kubernetes)에 Windows 컨테이너를 배포 하는 경우
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: 0b803b104f905fddac7939d7b070c206aabffeda
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53144795"
---
# <a name="when-to-deploy-windows-containers-to-azure-container-service-that-is-kubernetes"></a>Azure Container Service (즉, Kubernetes)에 Windows 컨테이너를 배포 하는 경우

Azure Container Service에는 특별히 Azure 용으로 인기 있는 오픈 소스 도구 및 기술의 구성을 최적화합니다. 컨테이너와 응용 프로그램 구성에 대 한 이식성을 제공 하는 개방형 솔루션을 얻게 됩니다. 크기, 호스트 수 및 오 케 스트레이 터 도구를 선택 합니다. Azure Container Service를 인프라를 처리합니다.

Kubernetes, Docker Swarm 또는 DC/OS와 같은 오픈 소스 오 케 스트레이 터를 사용 하 여 이미 작업 하는 경우에 컨테이너 워크 로드를 클라우드로 이동 하 여 기존 관리 방법을 변경할 필요가 없습니다. 익숙한 이미 있는 응용 프로그램 관리 도구를 사용 하 고 사용자가 선택한 orchestrator에 대 한 표준 API 끝점을 통해 연결 합니다.

모든 이러한 오 케 스트레이이 터는 완성도 높은 환경 Linux Docker 컨테이너를 사용 하는 경우 Windows 컨테이너에 대 한 미리 보기 상태일 수만 있습니다.

예를 들어, kubernetes에서 컨테이너를 지원 하므로 Windows 컨테이너를 사용 하 여 Kubernetes에서 네이티브 (최고 수준의 시민), (2018 년 초부터 ACS에서 미리 보기)에서 효과적입니다.

중요 참고 사항: 진화 하 고 "자세한 PaaS" Kubernetes에 대 한 ACS (Azure Container Service)의 버전은 AKS (Azure Kubernetes Service), 단, Windows 컨테이너는 여전히 Q2 2018 년부터 지원 되지 않지만 곧 지원 될 예정입니다.

>[!div class="step-by-step"]
>[이전](when-to-deploy-windows-containers-to-service-fabric.md)
>[다음](choosing-azure-compute-options-for-container-based-applications.md)