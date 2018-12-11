---
title: .NET Core 가이드
description: .NET Core는 Windows, Linux 및 Mac 앱을 만들기 위한 모듈식 고성능 .NET 구현입니다. 시작하려면 .NET Core에 관해 알아봅니다.
author: richlander
ms.date: 08/01/2018
ms.custom: updateeachrelease
ms.openlocfilehash: ffa58600bea1f5514b25c18aa00e6d36679f2fd9
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170279"
---
# <a name="net-core-guide"></a><span data-ttu-id="a4901-104">.NET Core 가이드</span><span class="sxs-lookup"><span data-stu-id="a4901-104">.NET Core Guide</span></span>

<span data-ttu-id="a4901-105">[.NET Core](about.md)는 Microsoft 및 [GitHub](https://github.com/dotnet/core)의 .NET 커뮤니티에서 유지 관리하는 [오픈 소스](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT) 범용 개발 플랫폼입니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-105">[.NET Core](about.md) is an [open-source](https://github.com/dotnet/coreclr/blob/master/LICENSE.TXT), general-purpose development platform maintained by Microsoft and the .NET community on [GitHub](https://github.com/dotnet/core).</span></span> <span data-ttu-id="a4901-106">플랫폼 간으로 Windows, macOS 및 Linux를 지원하며 장치, 클라우드 및 IoT 응용 프로그램을 빌드하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-106">It's cross-platform (supporting Windows, macOS, and Linux) and can be used to build device, cloud, and IoT applications.</span></span>

<span data-ttu-id="a4901-107">특성, 지원되는 언어 및 프레임워크, 키 API를 비롯한 .NET Core에 대한 자세한 내용은 [.NET Core 정보](about.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4901-107">See [About .NET Core](about.md) to learn more about .NET Core, including its characteristics, supported languages and frameworks, and key APIs.</span></span>

<span data-ttu-id="a4901-108">.NET Core 응용 프로그램을 만드는 방법은 [.NET Core 자습서](tutorials/index.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4901-108">Check out [.NET Core Tutorials](tutorials/index.md) to learn how to create a simple .NET Core application.</span></span> <span data-ttu-id="a4901-109">첫 번째 앱을 만들고 실행하는 데 몇 분밖에 걸리지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-109">It only takes a few minutes to get your first app up and running.</span></span> <span data-ttu-id="a4901-110">브라우저에서 .NET Core를 사용하려면 [C#의 숫자](../csharp/tutorials/intro-to-csharp/numbers-in-csharp.yml) 온라인 자습서를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="a4901-110">If you want to try .NET Core in your browser, look at the [Numbers in C#](../csharp/tutorials/intro-to-csharp/numbers-in-csharp.yml) online tutorial.</span></span>

## <a name="download-net-core-21"></a><span data-ttu-id="a4901-111">.NET Core 2.1 다운로드</span><span class="sxs-lookup"><span data-stu-id="a4901-111">Download .NET Core 2.1</span></span>

<span data-ttu-id="a4901-112">[.NET Core 2.1 SDK](https://www.microsoft.com/net/download)를 다운로드하여 Windows, macOS 또는 Linux 머신에서 .NET Core를 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="a4901-112">Download the [.NET Core  2.1 SDK](https://www.microsoft.com/net/download) to try .NET Core on your Windows, macOS, or Linux machine.</span></span> <span data-ttu-id="a4901-113">Docker 컨테이너를 사용하려면 [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/)을 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="a4901-113">Visit [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) if you prefer to use Docker containers.</span></span>

<span data-ttu-id="a4901-114">다른 .NET Core 버전을 찾는 경우 [.NET Core 다운로드](https://www.microsoft.com/net/download/archives)에서 모든 .NET Core 버전을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-114">All .NET Core versions are available at [.NET Core Downloads](https://www.microsoft.com/net/download/archives) if you're looking for another .NET Core version.</span></span>

## <a name="net-core-21"></a><span data-ttu-id="a4901-115">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a4901-115">.NET Core 2.1</span></span>

<span data-ttu-id="a4901-116">최신 버전은 [.NET Core 2.1](whats-new/dotnet-core-2-1.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-116">The latest version is [.NET Core 2.1](whats-new/dotnet-core-2-1.md).</span></span> <span data-ttu-id="a4901-117">새로운 기능에는 전역 도구, 고성능 API(예: <xref:System.Span%601?displayProperty=nameWithType>), 계층형 JIT 컴파일, [빌드](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) 및 [런타임 성능 개선](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/), Alpine 및 ARM32 지원이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-117">New features include: global tools, high-performance APIs (such as <xref:System.Span%601?displayProperty=nameWithType>), tiered JIT compilation, [build](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) and [runtime performance improvements](https://blogs.msdn.microsoft.com/dotnet/2018/04/18/performance-improvements-in-net-core-2-1/), and support for Alpine and ARM32.</span></span>

## <a name="create-your-first-application"></a><span data-ttu-id="a4901-118">첫 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="a4901-118">Create your first application</span></span>

<span data-ttu-id="a4901-119">.NET Core SDK를 설치한 후 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-119">After installing the .NET Core SDK, open a command prompt.</span></span> <span data-ttu-id="a4901-120">다음 `dotnet` 명령을 입력하여 C# 응용 프로그램을 만들고 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-120">Type the following `dotnet` commands to create and run a C# application.</span></span>

```console
dotnet new console
dotnet run
```

<span data-ttu-id="a4901-121">다음과 같은 내용이 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-121">You should see the following output:</span></span>

```console
Hello World!
```

## <a name="support"></a><span data-ttu-id="a4901-122">Support(지원)</span><span class="sxs-lookup"><span data-stu-id="a4901-122">Support</span></span>

<span data-ttu-id="a4901-123">.NET Core는 [Microsoft에 의해](https://www.microsoft.com/net/support/policy) Windows, macOS 및 Linux에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-123">.NET Core is [supported by Microsoft](https://www.microsoft.com/net/support/policy), on Windows, macOS and Linux.</span></span> <span data-ttu-id="a4901-124">보안 및 품질을 위해 1년에 여러 번, 일반적으로 매월 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-124">It's updated for security and quality several times a year, typically monthly.</span></span>

<span data-ttu-id="a4901-125">.NET Core 이진 배포는 Azure의 Microsoft가 유지 관리하는 서버에서 빌드 및 테스트되고 Microsoft 제품처럼 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-125">.NET Core binary distributions are built and tested on Microsoft-maintained servers in Azure and supported just like any Microsoft product.</span></span>

<span data-ttu-id="a4901-126">RHEL(Red Hat Enterprise Linux)에서 [Red Hat이 .NET Core를 지원](http://redhatloves.net/)합니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-126">[Red Hat supports .NET Core](http://redhatloves.net/) on Red Hat Enterprise Linux (RHEL).</span></span> <span data-ttu-id="a4901-127">Red Hat은 소스에서 .NET Core를 빌드하여 [Red Hat 소프트웨어 컬렉션](https://developers.redhat.com/products/softwarecollections/overview/)에서 사용할 수 있게 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-127">Red Hat builds .NET Core from source and makes it available in the [Red Hat Software Collections](https://developers.redhat.com/products/softwarecollections/overview/).</span></span> <span data-ttu-id="a4901-128">Red Hat 및 Microsoft는 협력하여 RHEL에서 .NET Core가 잘 작동하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4901-128">Red Hat and Microsoft collaborate to ensure that .NET Core works well on RHEL.</span></span>
