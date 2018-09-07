---
title: Docker 응용 프로그램의 상태 및 데이터
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 78db191bdec4c25c11728d819d89eaaaff4bd7da
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44070266"
---
# <a name="state-and-data-in-docker-applications"></a>Docker 응용 프로그램의 상태 및 데이터

컨테이너의 기본 형식은 불변성입니다. VM에 비해, 주로으로 컨테이너 사라지지 않도록 합니다. 소멸 프로세스, 오버 로드 된 CPU 또는 전체 또는 실패 한 디스크에서 다양 한 형태로 VM 실패할 수 있습니다. 아직 VM을 사용할 수 있는 것으로 예상 하 고 RAID 드라이브는 드라이브 오류 데이터를 유지 관리를 수행 하기 위해 일반화 합니다.

그러나 컨테이너 프로세스 인스턴스의 간주 됩니다. 프로세스는 영구 상태를 유지 되지 않습니다. 컨테이너를 로컬 저장소에 쓸 수 있지만 해당 인스턴스에 되도록 주위 무기한 가정 하 고 동일 단일 복사본 메모리는 지속적 이어야 하는 것으로 가정 합니다. 종료 프로세스와 같은 컨테이너는 중복 또는 컨테이너 오 케 스트레이 터를 사용 하 여 관리 되는 경우 이러한 이동 될 수 가정해 야 합니다.

Docker 이라고 하는 기능을 사용 하는 *오버레이 파일 시스템* 기반이 되는 원본 이미지에 비해 컨테이너의 루트 파일 시스템에 업데이트 된 정보를 저장 하는 모든 쓰기 시 복사 프로세스를 구현 합니다. 컨테이너 시스템에서 이후에 삭제 되 면 이러한 변경 내용은 손실 됩니다. 컨테이너를 따라서 없는 영구 저장소 기본적으로 합니다. 컨테이너의 상태를 저장 하는 가능한 경우에이 문제를 해결 하는 시스템 디자인 것 컨테이너 아키텍처의 원칙 충돌입니다.

Docker 응용 프로그램의 영구 데이터를 관리 하려면 일반적인 시나리오도 있습니다.

-   [**데이터 볼륨이**](https://docs.docker.com/engine/tutorials/dockervolumes/) 이러한 방금 설명한 것 처럼 호스트에 탑재 합니다.

-   [**데이터 볼륨 컨테이너**](https://docs.docker.com/engine/tutorials/dockervolumes/#/creating-and-mounting-a-data-volume-container) 이러한 주기 수는 외부 컨테이너를 사용 하 여 컨테이너에서 공유 저장소를 제공 합니다.

-   [**볼륨 플러그 인**](https://docs.docker.com/engine/tutorials/dockervolumes/#/mount-a-shared-storage-volume-as-a-data-volume) 이러한 장기 지 속성을 제공 하는 원격 위치에 볼륨을 탑재 합니다.

-   **원격 데이터 원본을** 예제 SQL 및 비 SQL 데이터베이스를 포함 하거나 Redis와 같은 캐시 서비스입니다.

-   [**Azure Storage**](https://docs.microsoft.com/azure/storage/) 컨테이너의 가장으로 장기 지 속성을 제공 하는 서비스 (PaaS) 저장소로 지역 배포 가능 플랫폼 제공 합니다.

데이터 볼륨은 무시 하는 하나 이상의 컨테이너 내의 디렉터리 지정 된 특수 합니다 [Union 파일 시스템](https://docs.docker.com/glossary/?term=Union%20file%20system)입니다. 데이터 볼륨 컨테이너의 수명 주기에 독립적으로 데이터를 유지 하도록 설계 되었습니다. Docker 따라서 자동으로 삭제 볼륨 컨테이너를 제거 하거나 컨테이너에서 더 이상 참조 하는 "가비지 수집" 볼륨을가 하는 경우. 호스트 운영 체제를 찾아 모든 볼륨의 데이터를 데이터 볼륨을 꼭 필요할 때만 사용 하는 또 다른 이유는 자유롭게 편집할 수 있습니다.

A [데이터 볼륨 컨테이너](https://docs.docker.com/glossary/?term=volume) 일반 데이터 볼륨은 향상 된 기능입니다. 기본적으로 유휴 포함 된 컨테이너를 하나 이상의 데이터 볼륨 (앞에서 설명한) 내에 만들어진 경우 데이터 볼륨 컨테이너는 중앙 탑재 지점에서 컨테이너에 대한 액세스를 제공합니다. 이 메서드의 액세스의 장점은 데이터 컨테이너를 논리 탑재 지점을 수행, 원래 데이터의 위치를 추출 하기. "Application" 컨테이너 만들어지고 소멸 전용된 컨테이너에 영구 데이터를 유지 하면서 컨테이너 데이터 볼륨에 액세스할 수 있습니다.

그림 4-5 일반 Docker 볼륨 저장소 컨테이너 자체가 되었지만 호스트 서버/v M 물리적 경계 내에 배치할 수 있는지 보여 줍니다. *Docker 볼륨을 다른 호스트 서버/v M에서 볼륨을 사용할 수 없는*합니다.

![](./media/image5.png)

그림 4-5: 데이터 볼륨 및 컨테이너 앱/컨테이너에 대 한 외부 데이터 원본

별도 물리적 호스트에서 실행 되는 컨테이너 간에 공유 된 데이터를 관리 하려면 않다는 것이 좋습니다는 사용 하면 볼륨 비즈니스 데이터에 대 한 Docker 호스트에 고정된 호스트/v M 아닌 때문에 오 케 스트레이 터에서 Docker 컨테이너를 사용 하는 경우 컨테이너는 클러스터에서 수행 하는 최적화에 따라 다른 호스트 간에 이동 해야 합니다.

따라서 일반 데이터 볼륨은 추적 파일, 임시 파일 또는 컨테이너를 여러 호스트 간에 이동할 때 아니면 비즈니스 데이터 일관성에 영향을 주지는 비슷한 개념이 작업할 수 있는 유용한 메커니즘입니다.

[볼륨 플러그 인](https://docs.docker.com/engine/extend/plugins_volume/) 클러스터의 모든 호스트 간에 데이터를 제공 합니다. 일부 볼륨 플러그 인을 동일 하 게 생성 되더라도 볼륨 플러그 인는 일반적으로 변경할 수 없는 컨테이너에서 표면화 된 영구적 신뢰할 수 있는 저장소를 제공 합니다.

원격 데이터 원본 및 SQL Database, DocumentDB 또는 Redis와 같은 원격 캐시와 같은 캐시 컨테이너 없이 개발할 같을 수는 있습니다. 비즈니스 응용 프로그램 데이터를 저장 하는 기본 및 검증 방법 중 하나입니다.


>[!div class="step-by-step"]
[이전](monolithic-applications.md)
[다음](soa-applications.md)
