---
title: NuGet 패키지 게시
description: .NET 라이브러리를 NuGet에 게시 하기 위한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 0602712311411ef3d59825bec8c5e550bc8d8265
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370326"
---
# <a name="publishing-a-nuget-package"></a>NuGet 패키지 게시

NuGet 패키지 게시 되 고 패키지 리포지토리에서 사용 합니다. 상태인 NuGet.org 가장 널리 알려져 있고 리포지토리는 NuGet 패키지를 게시 하려면 여러 위치

* **[NuGet.org](https://www.nuget.org/)**  는 NuGet 패키지에 대 한 기본 온라인 리포지토리입니다. NuGet.org의 모든 패키지는 모든 사용자에 게 공개적으로 사용할 수 있습니다. 기본적으로 Visual Studio에는 NuGet.org를 패키지 소스로 하 고 많은 개발자가 NuGet.org 상호 작용 하는 것만 패키지 저장소입니다. NuGet.org가 커뮤니티 피드백에 원하는 안정적인 패키지 및 시험판 버전을 게시 하는 것이 좋습니다.

* **[MyGet](https://myget.org/)**  저장소 서비스가 지 원하는 [오픈 소스 프로젝트에 대 한 무료 사용자 지정 패키지 피드](https://www.myget.org/opensource)합니다. MyGet 공용 사용자 지정 피드는 CI 서비스에 의해 생성 된 시험판 패키지를 게시 하는 데 적합 합니다. 또한 MyGet 개인 피드를 상업적으로 제공 합니다.

* A **[로컬 피드](/nuget/hosting-packages/local-feeds)** 해지고 패키지 리포지토리를 같은 폴더를 처리할 수 있습니다는 `*.nupkg` NuGet에서 액세스할 수 있는 폴더의 파일입니다. 로컬 피드 NuGet 패키지를 NuGet.org에 게시 하기 전에 테스트 하는 데 유용 합니다.

> [!NOTE]
> NuGet.org [패키지를 삭제할 수 없도록](/nuget/policies/deleting-packages) 업로드 되 면 합니다. UI에 공개적으로 표시 되지 않도록 패키지 나열 될 수 있습니다 하지만 `*.nupkg` 복원에 계속 다운로드할 수 있습니다. 또한 nuget.org는 중복 된 패키지 버전을 허용 하지 않습니다. 잘못 된 패키지의 나열을 취소 해야 하는 오류를 사용 하 여 NuGet 패키지를 수정 하려면 버전 번호를 증가 하 고 패키지의 새 버전을 게시 합니다.

**✔️ 마십시오** [안정적인 패키지 및 시험판 패키지를 게시](/nuget/create-packages/publish-a-package) NuGet.org에 커뮤니티 사용자 의견을 원하는 합니다.

**✔️ 하십시오** 연속 통합 빌드에서 피드 시험판 패키지를 MyGet에 게시 합니다.

**✔️ 하십시오** 로컬 피드 또는 MyGet을 사용 하 여 개발 환경에서 패키지를 테스트 합니다. 패키지 작동을 확인 한 다음 NuGet.org에 게시 합니다.

## <a name="nugetorg-security"></a>NuGet.org 보안

것이 중요 믿지 못할 자 NuGet 계정에 액세스 하 고 라이브러리의 악의적인 버전을 업로드할 수 없습니다. NuGet.org는 패키지를 게시할 때 2 단계 인증 및 전자 메일 알림을 제공 합니다. NuGet.org에 로그인 한 후 이러한 기능을 사용 하도록 설정 합니다 **계정 설정** 페이지입니다.

![대체 텍스트](./media/publish-nuget-package/nuget-2fa.png "NuGet 계정 보안")

**✔️ 수행** NuGet에 로그인 하려면 Microsoft 계정을 사용 합니다.

**✔️ 수행** NuGet에 액세스 하기 위한 2 단계 인증을 사용 하도록 설정 합니다.

**✔️ 수행** 패키지 게시 되 면 전자 메일 알림을 사용 하도록 설정 합니다.

>[!div class="step-by-step"]
[이전](./sourcelink.md)
[다음](./versioning.md)
