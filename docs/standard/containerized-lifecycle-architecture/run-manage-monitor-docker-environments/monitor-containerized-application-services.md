---
title: 컨테이너 화 된 응용 프로그램 서비스를 모니터링 합니다.
description: 모니터링 컨테이너 아키텍처의 몇 가지 주요 측면에 알아봅니다.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 925db543617deb28590cf6631ebbda3ee96836c4
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56975747"
---
# <a name="monitor-containerized-application-services"></a>컨테이너 화 된 응용 프로그램 서비스를 모니터링 합니다.

이 응용 프로그램 컨테이너 및 마이크로 서비스를 여러 분할을 모니터링 하 고 전체 응용 프로그램의 동작을 분석 하는 방법이 중요 합니다.

## <a name="microsoft-application-insights"></a>Microsoft Application Insights

[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) 라이브 응용 프로그램을 모니터링 하는 확장 가능한 분석 서비스입니다. 성능 문제 감지 및 진단 하는 데 실제로 할 앱을 사용 하 여 이해할 수 있습니다. 지속적으로 성능을 향상 시킬 수 있도록 의도 및 서비스 또는 응용 프로그램의 사용 편의성을 사용 하 여 개발자를 위해 설계 되었습니다. Application Insights에서 다양 한 플랫폼 같은.NET, Java, Node.js 및 기타 여러 플랫폼, 호스팅된 온-프레미스 또는 클라우드에서 앱을 웹/서비스와 독립 실행형을 사용 하 여 작동 합니다.

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a>Application Insights를 사용 하 여 QA 환경에서 Docker 앱 분석

Docker에 관련 된 수명 주기 이벤트 및 Application Insights에서 Docker 컨테이너에서 성능 카운터를 차트로 나타낼 수 있습니다. 실행 해야 합니다 [Application Insights Docker 이미지](https://hub.docker.com/r/microsoft/applicationinsights/) 컨테이너 호스트에 다른 Docker 이미지 뿐만 아니라 호스트에 대 한 성능 카운터를 표시 합니다. 이 Application Insights Docker 이미지 (그림 6-1) 성능 및 Docker 호스트 (즉, Linux Vm), Docker 컨테이너 및 실행 중인 응용 프로그램의 활동에 대 한 원격 분석을 수집 하 여 컨테이너 화 된 응용 프로그램을 모니터링할 수 있습니다 내에 있습니다.

![예제](./media/image1.png)

**그림 6-1**. Application Insights Docker 호스트 및 컨테이너를 모니터링 합니다.

실행 하는 경우는 [Application Insights Docker 이미지](https://hub.docker.com/r/microsoft/applicationinsights/) Docker 호스트에서 다음 중 하나를 활용 합니다.

- 호스트에서 실행 중인 모든 컨테이너에 대 한 원격 분석 수명 주기-시작, 중지 및 등입니다.

- 모든 컨테이너에 대 한 성능 카운터: CPU, 메모리, 네트워크 사용량 등.

- 또한 설치 하는 경우 [Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) 컨테이너에서 실행 중인 앱에서 해당 앱의 모든 원격 분석에는 컨테이너와 호스트 컴퓨터를 식별 하는 추가적인 속성이 포함 됩니다. 따라서 예를 들어 둘 이상의 호스트에서 실행 되는 앱 인스턴스가 있는 경우 쉽게 수 있습니다 호스트에서 앱 원격 분석을 필터링 합니다.

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a>Docker 응용 프로그램 및 Docker 호스트를 모니터링 하도록 Application Insights 설정

Application Insights 리소스를 만들려면 다음에 나오는 목록에 표시 하는 문서에서 지침을 따릅니다. Azure portal 필요한 스크립트를 만듭니다.

- **Application Insights에서 Docker 응용 프로그램을 모니터링 합니다.** \
  <https://docs.microsoft.com/azure/application-insights/app-insights-docker>

- **Docker 허브 및 GitHub에서 application Insights Docker 이미지:** \
  <https://hub.docker.com/r/microsoft/applicationinsights/> 및 \
  <https://github.com/Microsoft/ApplicationInsights-Docker>

- **ASP.NET web apps 및 ASP.NET Core 용 Application Insights를 설정 합니다.** \
  <https://docs.microsoft.com/azure/application-insights/app-insights-asp-net>

- **웹 페이지 용 application Insights:**  
  <https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="security-backup-and-monitoring-services"></a>보안, 백업 및 모니터링 서비스

많은 응용 프로그램 및 인프라는 비즈니스 요구를 지 원하는 최상의 조건에서 확인을 처리 해야 하는 세부 정보를 사용 하 여 여러 지원 작업 되며 상황이 더 복잡해 집니다 마이크로 서비스 영역에서는 해야 하는 방법 상위 수준 및 세부 보기를 될 하 여 작업을 수행 해야 합니다.

Azure를 통해 클라우드 및 온-프레미스 리소스의 네 가지 중요 한 측면의 통합된 보기를 제공 하는 도구에 있습니다.

- **보안**합니다. 사용 하 여 [Azure Security Center](https://azure.microsoft.com/services/security-center/)합니다.
  - 완전 한 가시성과 제어권을 통해 virtual machines, 앱 및 워크 로드의 보안을 가져옵니다.
  - 보안 정책의 관리를 중앙 집중화 하 고 기존 프로세스 및 도구를 통합 합니다.
  - 고급 분석을 사용 하 여 실제 위협을 감지 합니다.

- **백업**합니다. 사용 하 여 [Azure Backup](https://azure.microsoft.com/services/backup/)합니다.
  - 비용이 많이 드는 업무 중단을 방지 하 고 규정 준수 목표를 충족 랜 섬 웨어 및 사람의 오류 로부터 데이터를 보호 합니다.
  - 전송 중 및 미사용 시 암호화 된 백업 데이터를 유지 합니다.
  - 무단된 사용을 방지 하기 위해 다단계 인증을 기반으로 하는 액세스를 확인 합니다.

- **모니터링**합니다. 사용 하 여 [Azure 모니터링](https://azure.microsoft.com/solutions/monitoring/)하십시오 [Log Analytics](https://azure.microsoft.com/services/log-analytics/), 및 [Application Insights](https://azure.microsoft.com/services/application-insights/)합니다.
  - Azure 워크 로드, 앱 및 인프라의 성능과 상태에 완전 한 가시성을 가져옵니다.
  - 모든 원본에서 데이터를 수집 및 virtual machines, 컨테이너 및 응용 프로그램에 풍부한 정보를 얻으세요.
  - 대화형 쿼리와 전체 텍스트 검색을 사용 하 여 필요한 정보를 찾습니다. 
  - 기계 학습 알고리즘을 비롯 한 고급 분석을 사용 하 여 근본 원인 분석을 수행 합니다.

- **온-프레미스 리소스**합니다. 사용 하 여 [일관 된 하이브리드 클라우드](https://azure.microsoft.com/resources/truly-consistent-hybrid-cloud-with-microsoft-azure/)합니다.

>[!div class="step-by-step"]
>[이전](manage-production-docker-environments.md)
>[다음](../key-takeaways/index.md)
