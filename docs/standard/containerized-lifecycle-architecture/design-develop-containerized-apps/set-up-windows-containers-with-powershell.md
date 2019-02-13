---
title: DockerFile에서 Windows PowerShell 명령을 사용 하 여 Windows 컨테이너 (Docker 표준 기반) 설정
description: Windows 컨테이너에서 Docker를 사용 하는 경우 PowerShell을 사용 하는 방법 알아보기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: df9e98e3f963b6492e1008455251b61a8cb6e771
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219973"
---
# <a name="using-windows-powershell-commands-in-a-dockerfile-to-set-up-windows-containers-docker-standard-based"></a>DockerFile에서 Windows PowerShell 명령을 사용 하 여 Windows 컨테이너 (Docker 표준 기반) 설정

사용 하 여 [Windows 컨테이너](/virtualization/windowscontainers/about/index), Docker 이미지를 기존 Windows 응용 프로그램 변환 하 고 Docker 에코 시스템의 나머지 부분과 동일한 도구를 사용 하 여 배포할 수 있습니다.

Windows 컨테이너를 사용 하려면 하기만 하면 Windows PowerShell 명령은 DockerFile에서 쓸 다음 예제에서 설명한 대로:

```
FROM microsoft/windowsservercore
LABEL Description="IIS" Vendor="Microsoft" Version="10"
RUN powershell -Command Add-WindowsFeature Web-Server
CMD [ "ping", "localhost", "-t" ]
```

이 경우 IIS 뿐만 아니라 Windows Server Core 기본 이미지를 설치 하려면 Windows PowerShell을 사용 하는 것입니다.

이와 비슷한 방식으로도 사용 하 여 Windows PowerShell 명령을 기존의 ASP.NET과 같은 추가 구성 요소를 설정 하려면 4.x 및.NET 4.6 또는 다른 Windows 소프트웨어를 다음과 같이 합니다.

```
RUN powershell add-windowsfeature web-asp-net45
```

>[!div class="step-by-step"]
>[이전](visual-studio-tools-for-docker.md)
>[다음](build-aspnet-core-applications-linux-containers-aks-kubernetes.md)
