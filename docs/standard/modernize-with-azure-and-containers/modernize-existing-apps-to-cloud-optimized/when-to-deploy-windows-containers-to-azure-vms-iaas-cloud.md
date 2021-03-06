---
title: Azure Vm (IaaS 클라우드)에 Windows 컨테이너를 배포 하는 경우
description: Azure 클라우드 및 Windows 컨테이너를 사용 하 여 기존.NET 응용 프로그램 현대화 | Azure Vm (IaaS 클라우드)에 Windows 컨테이너를 배포 하는 경우
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 51217e2c94fd9727c8f7907e791cdebaec98f14f
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152151"
---
# <a name="when-to-deploy-windows-containers-to-azure-vms-iaas-cloud"></a>Azure Vm (IaaS 클라우드)에 Windows 컨테이너를 배포 하는 경우

또한 Windows 컨테이너를 사용 하는 경우에 조직에서 Azure Vm을 사용 하는, 하는 경우 여전히 IaaS 사용 하 여 처리입니다. 즉, 인프라 운영, VM OS 패치 및 인프라의 복잡성을 사용 하 여 해당 처리 확장성이 높은 응용 프로그램에 대 한 부하 분산 된 인프라에서 여러 Vm에 배포 해야 하는 경우. Windows 컨테이너를 사용 하 여 Azure VM에 대 한 주요 시나리오는 다음과 같습니다.

-   **개발/테스트 환경을**: 클라우드에서 VM은 개발 및 테스트 클라우드에 적합 합니다. 신속 하 게 만들 수도 있고 필요에 따라 환경을 중지.

-   **소규모 및 중간 규모의 확장성 요구**: 프로덕션 환경에 몇 개의 Vm 해야 할 수 있습니다 시나리오에서 소수의 Vm 관리 경제적인 때까지 수 오 케 스트레이 터와 같은 고급 PaaS 환경으로 이동할 수 있습니다.

-   **기존 배포 도구를 사용 하 여 프로덕션 환경**: Vm 이나 베어 메탈 서버 (예: Puppet 또는 유사한 도구)에 게 복잡 한 배포 하는 도구에 투자는 온-프레미스 환경에서 사용자를 이동할 수 있습니다. 프로덕션 환경 배포 절차에 대 한 변경을 최소화 하면서 클라우드로 이동, Azure Vm을 배포 하려면 이러한 도구를 사용 하 여 계속 수 있습니다. 그러나 배포 단위로 배포 환경을 개선 하기 위해 Windows 컨테이너를 사용 합니다.

>[!div class="step-by-step"]
>[이전](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
>[다음](when-to-deploy-windows-containers-to-azure-container-instances-ACI.md)