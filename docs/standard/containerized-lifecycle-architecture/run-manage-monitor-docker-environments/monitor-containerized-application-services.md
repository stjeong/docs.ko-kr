---
title: 컨테이너 화 된 응용 프로그램 서비스를 모니터링 합니다.
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 4bdc4470624ce6e905ab858a2bd8b607c8d3d646
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46698534"
---
# <a name="monitor-containerized-application-services"></a>컨테이너 화 된 응용 프로그램 서비스를 모니터링 합니다.

이 응용 프로그램 컨테이너 및 마이크로 서비스를 여러 분할을 모니터링 하 고 응용 프로그램의 동작을 분석 하는 방법이 중요 합니다.

## <a name="microsoft-application-insights"></a>Microsoft Application Insights

[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) 라이브 응용 프로그램을 모니터링 하는 확장 가능한 분석 서비스입니다. 성능 문제 감지 및 진단 하는 데 실제로 할 앱을 사용 하 여 이해할 수 있습니다. 지속적으로 성능을 향상 시킬 수 있도록 의도 및 서비스 또는 응용 프로그램의 사용 편의성을 사용 하 여 개발자를 위해 설계 되었습니다. Application Insights에서 다양 한 플랫폼 같은.NET, Java, Node.js 및 기타 여러 플랫폼, 호스팅된 온-프레미스 또는 클라우드에서 앱을 웹/서비스와 독립 실행형을 사용 하 여 작동 합니다.

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a>Application Insights를 사용 하 여 QA 환경에서 Docker 앱 분석

Docker에 관련 된 수명 주기 이벤트 및 Application Insights에서 Docker 컨테이너에서 성능 카운터를 차트로 나타낼 수 있습니다. 실행 해야 합니다 [Application Insights Docker 이미지](https://hub.docker.com/r/microsoft/applicationinsights/) 컨테이너 호스트에 다른 Docker 이미지 뿐만 아니라 호스트에 대 한 성능 카운터를 표시 합니다. 이 Application Insights Docker 이미지 (그림 6-1) 성능 및 Docker 호스트 (즉, Linux Vm), Docker 컨테이너 및 실행 중인 응용 프로그램의 활동에 대 한 원격 분석을 수집 하 여 컨테이너 화 된 응용 프로그램을 모니터링할 수 있습니다 내에 있습니다.

![예제](./media/image1.png)

그림 6-1: Application Insights Docker 호스트 및 컨테이너를 모니터링 합니다.

실행 하는 경우는 [Application Insights Docker 이미지](https://hub.docker.com/r/microsoft/applicationinsights/) Docker 호스트에서 다음 중 하나를 활용 합니다.

-   호스트에서 실행 중인 모든 컨테이너에 대 한 원격 분석 수명 주기-시작, 중지 및 등입니다.

-   모든 컨테이너에 대 한 성능 카운터: CPU, 메모리, 네트워크 사용량 등.

-   또한 설치 하는 경우 [Application Insights SDK](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) 컨테이너에서 실행 중인 앱에서 해당 앱의 모든 원격 분석에는 컨테이너와 호스트 컴퓨터를 식별 하는 추가적인 속성이 포함 됩니다. 따라서 예를 들어 둘 이상의 호스트에서 실행 되는 앱 인스턴스가 있는 경우 쉽게 수 있습니다 호스트에서 앱 원격 분석을 필터링 합니다.

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a>Docker 응용 프로그램 및 Docker 호스트를 모니터링 하도록 Application Insights 설정

Application Insights 리소스를 만들려면 다음에 나오는 목록에 표시 하는 문서에서 지침을 따릅니다. Azure Portal 필요한 스크립트를 만듭니다.

-   **Application Insights에서 Docker 응용 프로그램을 모니터링 합니다.**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)

-   **Docker 허브 및 Github에서 application Insights Docker 이미지:**  
[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) 및 <https://github.com/Microsoft/ApplicationInsights-Docker>

-   **ASP.NET 용 Application Insights를 설정 합니다.**  
[https://docs.microsoft.com/azure/application-insights/app-insights-asp-net](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)

-   **웹 페이지 용 application Insights:**  
<https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="microsoft-operations-management-suite"></a>Microsoft 작업 관리 도구 모음

[Operations Management Suite](https://microsoft.com/oms) 는 log analytics, automation, backup, 사이트 복구를 제공 하는 간소화 된 IT 관리 솔루션입니다. 에 따라 [쿼리](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/) Operations Management Suite에 올리면 [경고](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts) 재구성을 통해 설정 [Azure Automation](https://docs.microsoft.com/azure/automation/)합니다. 단일 투명 효과 창의 보기를 제공 하 여 기존 관리 솔루션과 원활 하 게 통합 됩니다. Operations Management Suite를 사용 하면 온-프레미스 보호 및 클라우드 인프라 및 관리 하도록 도와줍니다.

### <a name="operations-management-suitehttpsmicrosoftcomoms-container-solution-for-docker"></a>[Operations Management Suite](https://microsoft.com/oms) Docker 용 컨테이너 솔루션

자체적으로 중요 한 서비스를 제공 하는 것 외에도 Operations Management Suite 컨테이너 솔루션 관리 및 모니터링할 수 Docker 호스트 및 컨테이너에 대 한 정보는 사용자 컨테이너 및 컨테이너 호스트를 표시 하 여 실행 중인 컨테이너는 실패 또는 Docker 디먼 및 컨테이너 로그를 전송 하 고 *stdout* 하 고 *stderr*합니다. 또한 CPU, 메모리, 네트워크 및 저장소 등 컨테이너 및 호스트에 대한 성능 메트릭을 표시하여 문제를 해결하고, 노이지 네이버(noisy neighbor) 컨테이너를 찾을 수 있게 해줍니다.

![](./media/image2.png)

Operations Management Suite에서 표시 하는 Docker 컨테이너에 대 한 그림 6-2: 정보

Application Insights 및 Operations Management Suite 작업;를 모니터링에 중점 그러나 Application Insights는 앱 내에서 실행 되는 SDK 통해 앱 모니터링에 더 집중 합니다. 그러나 Operations Management Suite에 중점을 둡니다 훨씬 호스트 관련 인프라와 매우 유연한 데이터 기반 검색/쿼리 시스템을 제공 하는 동안 로그 규모에 대 한 심층 분석을 제공 합니다.

Operations Management Suite를 클라우드 기반 서비스로 구현 되므로 있습니다 해당 실행 신속 하 게 인프라 서비스에 대 한 최소한의 투자로. 새로운 기능이 자동적으로 전달 되므로 지속적인 유지 관리에서 절약할 및 비용을 업그레이드 합니다.

Operations Management Suite 컨테이너 솔루션을 사용 하 여, 있습니다 다음을 수행할 수 있습니다.:

-   중앙 집중화 하 고 수백만 개의 대규모 Docker 컨테이너에서 로그를 상호 연결

-   단일 위치에서 모든 컨테이너 호스트에 대 한 정보를 참조 하세요.

-   알고 있는 컨테이너를 실행 하는 어떤 이미지를 실행 및 실행 하는 위치

-   컨테이너 호스트에서 문제가 발생할 수 있는 "시끄러운 이웃" 컨테이너를 빠르게 진단

-   컨테이너에 대 한 작업에 대 한 감사 내역을 참조 하세요.

-   원격 Docker 호스트에 없이 중앙 집중식된 로그를 검색 하 여 문제 해결

-   "시끄러운 이웃" 및 호스트에 과도 한 리소스 소비 될 수 있는 컨테이너를 찾을

-   중앙화 된 CPU, 메모리, 저장소 및 컨테이너에 대 한 네트워크 사용량 및 성능 정보를 보려면

-   생성 Azure Automation을 사용 하 여 Docker 컨테이너를 테스트 합니다.

형식이 같은 쿼리를 실행 하 여 성능 정보를 볼 수 = Perf 그림 6-3에 나와 있는 것 처럼 합니다.

![DockerPerfMetricsView](./media/image3.png){width="5.78625in" height="3.25in"}

Operations Management Suite에서 표시 하는 Docker 호스트의 그림 6-3: 성능 메트릭

Operations Management Suite의 표준 기능은 또한 쿼리를 저장 및 도움이 될 수 있습니다 유용한 및 시스템의 추세를 검색 하는 쿼리를 유지 합니다.

**자세한 내용은** 의 컨테이너 솔루션 설치 및 Docker를 구성에 대 한 정보를 찾으려면 [Operations Management Suite](https://microsoft.com/oms)으로 이동 하 여 <https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>입니다.

>[!div class="step-by-step"]
[이전](manage-production-docker-environments.md)
[다음](../key-takeaways/index.md)
