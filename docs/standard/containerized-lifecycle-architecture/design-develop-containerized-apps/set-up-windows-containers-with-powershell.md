---
title: DockerFile에서 Windows PowerShell 명령을 사용 하 여 Windows 컨테이너 (Docker 표준 기반) 설정
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/19/2017
ms.openlocfilehash: 5e85beea0efbee6a2b6594e3a49d705505a36e1c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149395"
---
# <a name="using-windows-powershell-commands-in-a-dockerfile-to-set-up-windows-containers-docker-standard-based"></a><span data-ttu-id="de7fc-103">DockerFile에서 Windows PowerShell 명령을 사용 하 여 Windows 컨테이너 (Docker 표준 기반) 설정</span><span class="sxs-lookup"><span data-stu-id="de7fc-103">Using Windows PowerShell commands in a DockerFile to set up Windows Containers (Docker standard based)</span></span>

<span data-ttu-id="de7fc-104">사용 하 여 [Windows 컨테이너](/virtualization/windowscontainers/about/index), Docker 이미지를 기존 Windows 응용 프로그램 변환 하 고 Docker 에코 시스템의 나머지 부분과 동일한 도구를 사용 하 여 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de7fc-104">With [Windows Containers](/virtualization/windowscontainers/about/index), you can convert your existing Windows applications to Docker images and deploy them with the same tools as the rest of the Docker ecosystem.</span></span>

<span data-ttu-id="de7fc-105">Windows 컨테이너를 사용 하려면 하기만 하면 Windows PowerShell 명령은 DockerFile에서 쓸 다음 예제에서 설명한 대로:</span><span class="sxs-lookup"><span data-stu-id="de7fc-105">To use Windows Containers, you just need to write Windows PowerShell commands in the DockerFile, as demonstrated in the following example:</span></span>

```
FROM microsoft/windowsservercore
LABEL Description="IIS" Vendor="Microsoft" Version="10"
RUN powershell -Command Add-WindowsFeature Web-Server
CMD [ "ping", "localhost", "-t" ]
```

<span data-ttu-id="de7fc-106">이 경우 IIS 뿐만 아니라 Windows Server Core 기본 이미지를 설치 하려면 Windows PowerShell을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="de7fc-106">In this case, we're using Windows PowerShell to install a Windows Server Core base image as well as IIS.</span></span>

<span data-ttu-id="de7fc-107">이와 비슷한 방식으로도 사용 하 여 Windows PowerShell 명령을 기존의 ASP.NET과 같은 추가 구성 요소를 설정 하려면 4.x 및.NET 4.6 또는 다른 Windows 소프트웨어를 다음과 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="de7fc-107">In a similar way, you also could use Windows PowerShell commands to set up additional components like the traditional ASP.NET 4.x and .NET 4.6 or any other Windows software, as shown here:</span></span>

```
RUN powershell add-windowsfeature web-asp-net45
```

>[!div class="step-by-step"]
><span data-ttu-id="de7fc-108">[이전](visual-studio-tools-for-docker.md)
>[다음](../docker-devops-workflow/index.md)</span><span class="sxs-lookup"><span data-stu-id="de7fc-108">[Previous](visual-studio-tools-for-docker.md)
[Next](../docker-devops-workflow/index.md)</span></span>
