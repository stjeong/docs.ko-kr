---
title: Linux에서 .NET Core의 필수 구성 요소
description: Linux 컴퓨터에서 .NET Core 애플리케이션을 개발, 배포 및 실행하기 위해 지원되는 Linux 버전 및 .NET Core 종속성입니다.
author: thraka
ms.author: adegeo
ms.date: 12/14/2018
ms.openlocfilehash: 5ef1737185ad41de7bd5e7a9b8db048ff577811f
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083888"
---
# <a name="prerequisites-for-net-core-on-linux"></a>Linux에서 .NET Core의 필수 구성 요소

이 문서에서는 Linux에서 .NET Core 애플리케이션을 개발하는 데 필요한 종속성을 보여 줍니다. 다음에 나오는 지원되는 Linux 배포/버전 및 종속성은 Linux에서 .NET Core 앱을 개발하기 위한 두 가지 방법에 적용됩니다.

* [즐겨 찾는 편집기를 사용하는 명령줄](tutorials/using-with-xplat-cli.md)
* [Visual Studio Code](https://code.visualstudio.com/)

> [!NOTE]
> .NET Core SDK 패키지는 프로덕션 서버/환경에서 필요하지 않습니다. .NET Core 런타임 패키지만 프로덕션 환경에 배포된 앱에 필요합니다. NET Core 런타임은 자체 포함된 배포의 일부로 앱으로 배포되지만 프레임워크 종속 배포된 앱에 대해 별도로 배포되어야 합니다. 프레임워크 종속 및 자체 포함된 배포 형식에 대한 자세한 내용은 [.NET Core 애플리케이션 배포](./deploying/index.md)를 참조하세요. 또한 특정 지침은 [자체 포함된 Linux 애플리케이션](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)을 참조하세요.

## <a name="supported-linux-versions"></a>지원되는 Linux 버전

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

.NET Core 2.x는 단일 운영 체제로 Linux를 처리합니다. 지원되는 Linux 배포에 대한 단일 Linux 빌드(칩 아키텍처당)가 있습니다. 

다운로드 링크 및 자세한 내용은 [.NET Core 2.2 다운로드](https://www.microsoft.com/net/download/dotnet-core/2.2) 또는 [.NET Core 2.1 다운로드](https://www.microsoft.com/net/download/dotnet-core/2.1)를 참조하세요.

.NET Core 2.x는 다음 Linux 배포/버전에서 지원됩니다.

* Red Hat Enterprise Linux 7, 6 - 64비트(`x86_64` 또는 `amd64`)
* CentOS 7 - 64비트(`x86_64` 또는 `amd64`) 
* Oracle Linux 7 - 64비트(`x86_64` 또는 `amd64`) 
* Fedora 28, 27 - 64비트(`x86_64` 또는 `amd64`) 
* Debian 9(64비트, `arm32`), 8.7 이상 버전 - 64비트(`x86_64` 또는 `amd64`)
* Ubuntu 18.04(64비트, `arm32`), 16.04, 14.04, 64비트(`x86_64` 또는 `amd64`)
* Linux Mint 18, 17 - 64비트(`x86_64` 또는 `amd64`)
* openSUSE 42.3 이상 버전 - 64비트(`x86_64` 또는 `amd64`)
* SUSE Enterprise Linux(SLES) 12 서비스 팩 2 이상 - 64비트(`x86_64` 또는 `amd64`)
* Alpine Linux 3.7 이상 버전 - 64비트(`x86_64` 또는 `amd64`)

.NET Core 2.1 및 .NET Core 2.2가 지원되는 운영 체제, 배포 및 버전, 지원되지 않는 OS 버전, 수명 주기 정책 링크의 전체 목록은 [.NET Core 2.1이 지원되는 OS 버전](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md) 및 [.NET Core 2.2가 지원되는 OS 버전](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md)을 참조하세요.

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

다운로드 링크 및 자세한 내용은 [.NET Core 1.1 다운로드](https://www.microsoft.com/net/download/dotnet-core/1.1) 또는 [.NET Core 1.0 다운로드](https://www.microsoft.com/net/download/dotnet-core/1.0)를 참조하세요.

.NET Core 1.x는 다음 Linux 64비트(`x86_64` 또는 `amd64`) 배포/버전에서 지원됩니다.

* Red Hat Enterprise Linux 7
* CentOS 7
* Oracle Linux 7
* Fedora 28(.NET Core 1.1), 27
* Debian 8.2 이상 버전
* Ubuntu 18.04(.NET Core 1.1), 16.04, 14.04
* Linux Mint 17
* openSUSE 42.3 이상 버전(.NET Core 1.1)

지원 OS 버전 중 .NET Core 1.x를 지원하는 운영 체제 및 수명 주기 정책 링크는 [.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)(.NET Core 1.x가 지원되는 OS 버전)를 참조하세요.

# <a name="net-core-30-preview-1tabnetcore30"></a>[.NET Core 3.0 Preview 1](#tab/netcore30)

.NET Core 3.0 Preview 1은 단일 운영 체제로 Linux를 처리합니다. 지원되는 Linux 배포에 대한 단일 Linux 빌드(칩 아키텍처당)가 있습니다. 

다운로드 링크 및 자세한 내용은 [.NET Core 3.0 다운로드](https://dotnet.microsoft.com/download/dotnet-core/3.0)를 참조하세요.

.NET Core 3.0 Preview 1은 다음 Linux 배포/버전에서 지원됩니다. 

OS                            | 버전               | 아키텍처  
------------------------------|-----------------------|----------------
Red Hat Enterprise Linux      | 6                     | X64
Red Hat Enterprise Linux<br>CentOS<br>Oracle Linux  | 7                     | X64
Fedora                        | 28                    | X64
Debian                        | 10                     | x64, ARM32\*, ARM64\*
Ubuntu                        | 16.04+, 18.04+        | x64, ARM32\*, ARM64\*
Linux Mint                    | 18                    | X64
openSUSE                      | 42.3+                 | X64
SLES(SUSE Enterprise Linux)  | 12 SP2+               | X64
Alpine Linux                  | 3.8+                  | x64, ARM64

\* ARM32 및 ARM64 지원은 Debian 9 및 Ubuntu 16.04에서 시작합니다. 해당 배포판의 이전 버전은 ARM 칩에서 지원되지 않습니다.

지원 OS 버전 중 .NET Core 3.0이 지원되는 운영 체제, 배포 및 버전, 수명 주기 정책 링크의 전체 목록은 [.NET Core 3.0이 지원되는 OS 버전](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md)을 참조하세요.

ARM64에 .NET Core 3.0을 설치하는 방법에 대한 자세한 내용은 [Linux ARM64에 .NET Core 3.0 설치](https://gist.github.com/richlander/467813274cea8abc624553ee72b28213)를 참조하세요.



---

## <a name="linux-distribution-dependencies"></a>Linux 배포 종속성

다음은 예제로 사용됩니다. 정확한 버전 및 이름은 선택한 Linux 배포에 따라 약간 다를 수 있습니다.

### <a name="ubuntu"></a>Ubuntu

Ubuntu 배포에는 다음과 같은 라이브러리 설치가 필요합니다.

* liblttng-ust0
* libcurl3(14.x 및 16.x용)
* libcurl4(18.x용)
* libssl1.0.0
* libkrb5-3
* zlib1g
* libicu52(14.x용)
* libicu55(16.x용)
* libicu57(17.x용)
* libicu60(18.x용)

.NET Core 2.1 이전 버전의 경우 다음 종속성도 필요합니다.

* libunwind8
* libuuid1

### <a name="centos-and-fedora"></a>CentOS 및 Fedora

CentOS 배포에는 다음과 같은 라이브러리 설치가 필요합니다.

* lttng-ust
* libcurl
* openssl-libs
* krb5-libs
* libicu
* zlib

Fedora 사용자: openssl 버전 >= 1.1인 경우 compat-openssl10을 설치해야 합니다.

.NET Core 2.1 이전 버전의 경우 다음 종속성도 필요합니다.

* libunwind
* libuuid

종속성에 대한 자세한 내용은 [자체 포함 Linux 애플리케이션](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)을 참조하세요.

## <a name="installing-net-core-dependencies-with-the-native-installers"></a>기본 설치 관리자를 사용하여 .NET Core 종속성 설치

.NET Core 기본 설치 관리자는 지원되는 Linux 배포/버전에서 사용할 수 있습니다. 기본 설치 관리자를 사용하려면 서버에 대한 관리자(sudo) 권한이 필요합니다. 기본 설치 관리자를 사용하는 장점은 모든 .NET Core 기본 종속성을 설치한다는 것입니다. 기본 설치 관리자는 .NET Core SDK 시스템 차원을 설치합니다.

Linux에는 두 가지 패키지 선택 항목이 있습니다.

* 피드 기반 패키지 관리자 사용(예: Ubuntu의 경우 apt-get, CentOS/RHEL의 경우 yum).
* 패키지 자체 사용(DEB 또는 RPM).

### <a name="scripting-installs-with-the-net-core-installer-script"></a>.NET Core 설치 관리자 스크립트를 사용하여 설치 스크립팅

[dotnet-install 스크립트](./tools/dotnet-install-script.md)는 CLI 도구 체인 및 공유 런타임의 관리자가 아닌 일반 설치를 수행하는 데 사용됩니다. [https://dot.net/v1/dotnet-install.sh](https://dot.net/v1/dotnet-install.sh)에서 스크립트를 다운로드할 수 있습니다.

스크립트는 기본적으로 현재 .NET Core 1.1인 최신 "LTS" 버전을 설치합니다. .NET Core 2.1을 설치하려면 다음 스위치를 사용하여 스크립트를 실행합니다.

```console
./dotnet-install.sh -c Current
```

설치 관리자 bash 스크립트는 자동화 시나리오 및 비관리자 설치에 사용됩니다. 또한 이 스크립트는 PowerShell 스위치를 읽으므로 Linux/OS X 시스템에서 스크립트와 함께 사용할 수 있습니다.

## <a name="troubleshoot"></a>문제 해결

지원되는 Linux 배포/버전에 .NET Core 설치에 문제가 있는 경우 설치된 배포/버전에 대한 다음 항목을 참조하세요.

* [.NET Core 3.0 알려진 문제](https://github.com/dotnet/core/tree/master/release-notes/3.0)
* [.NET Core 2.2 알려진 문제](https://github.com/dotnet/core/tree/master/release-notes/2.2)
* [.NET Core 2.1 알려진 문제](https://github.com/dotnet/core/tree/master/release-notes/2.1)
* [.NET Core 1.1 알려진 문제](https://github.com/dotnet/core/blob/master/release-notes/1.1)
* [.NET Core 1.0 알려진 문제](https://github.com/dotnet/core/blob/master/release-notes/1.0)
