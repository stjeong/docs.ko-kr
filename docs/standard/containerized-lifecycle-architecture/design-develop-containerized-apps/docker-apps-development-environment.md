---
title: Docker 앱을 위한 개발 환경
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 471b52fd577e5560bd93e6da50f2032d63eb2e6f
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152418"
---
# <a name="development-environment-for-docker-apps"></a>Docker 앱을 위한 개발 환경

## <a name="development-tools-choices-ide-or-editor"></a>개발 도구 선택 정보: IDE 또는 편집기

든 관계 없이 완전 하 고 강력한 IDE 또는 가볍고 민첩 한 편집기를 선호 하는 경우 Microsoft는 Docker 응용 프로그램 개발에 있어.

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a>Visual Studio Code 및 Docker CLI (Mac, Linux 및 Windows 용 플랫폼 간 도구)

모든 개발 언어를 지 원하는 경량, 플랫폼 간 편집기를 원한다 면 Visual Studio Code 및 Docker CLI를 사용할 수 있습니다. 이러한 제품은 개발자 워크플로 간소화 하는 것에 대 한 중요 한 간단 하지만 강력한 환경을 제공 합니다. "Docker에 대 한 Mac" 또는 "Docker에 대 한 Windows" (개발 환경)를 설치 하 여 Docker 개발자 모두 Windows 또는 Linux (런타임 환경)에 대 한 앱을 빌드할 수는 단일 Docker CLI를 사용할 수 있습니다. 또한 Visual Studio Code 편집기에서 Docker 명령을 실행 하는 Dockerfile 및 바로 가기 작업에 대 한 IntelliSense 사용 하 여 Docker에 대 한 확장을 지원 합니다.

> [!NOTE]
> Visual Studio Code를 다운로드 하려면로 이동 <https://code.visualstudio.com/download>합니다.

Mac 및 Windows 용 Docker를 다운로드 하려면로 이동 <https://www.docker.com/products/docker>합니다.

### <a name="visual-studio-with-docker-tools"></a>Docker 도구를 사용 하 여 visual Studio

Visual Studio 2015를 사용 하는 경우 "Visual Studio 용 Docker 도구입니다." 추가 기능 도구를 설치할 수 있습니다. Visual Studio 2017 용 Docker 도구 기본적으로 제공 되에 이미 있습니다. 두 경우 모두를 개발할 수 있습니다를 실행 하 고 선택한 Docker 환경에서 직접 응용 프로그램을 확인 합니다. F5 응용 프로그램 (단일 컨테이너 또는 여러 컨테이너)을 Docker에 직접 디버깅을 사용 하 여 호스트 또는 Ctrl + f5를 눌러 편집 하 고 컨테이너를 다시 빌드하지 않고 앱을 새로 고칩니다. 이 Linux 또는 Windows 용 Docker 컨테이너를 만들고 Windows 개발자를 위한 간단 하 고 더 강력한 좋습니다.

> [!NOTE]
> Visual Studio 용 Docker 도구를 다운로드 하려면로 이동 <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>합니다.

## <a name="language-and-framework-choices"></a>언어 및 프레임 워크 선택

Docker 응용 프로그램 및 최신 언어를 사용 하 여 Microsoft 도구를 개발할 수 있습니다. 다음은 초기 목록을, 하지만에 제한 되지 않습니다.

-   .NET Core 및 ASP.NET Core
-   Node.js
-   Golang
-   Java
-   Ruby
-   Python

기본적으로, Linux 또는 Windows에서 Docker를 지 원하는 모든 최신 언어를 사용할 수 있습니다.

>[!div class="step-by-step"]
>[이전](orchestrate-high-scalability-availability.md)
>[다음](docker-apps-inner-loop-workflow.md)