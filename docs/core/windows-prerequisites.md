---
title: Windows에서 .NET Core의 필수 구성 요소
description: Windows 컴퓨터에서 .NET Core 응용프로그램을 개발 및 실행하기 위해 필요한 종속성이 무엇인지 살펴보세요.
author: mairaw
ms.author: mairaw
ms.date: 08/31/2018
ms.openlocfilehash: bbf54c8d215783656830f0fa035708be82a7c39c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482612"
---
# <a name="prerequisites-for-net-core-on-windows"></a><span data-ttu-id="3a417-103">Windows에서 .NET Core의 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="3a417-103">Prerequisites for .NET Core on Windows</span></span>

<span data-ttu-id="3a417-104">이 문서에서는 Windows에서 .NET Core 응용 프로그램을 개발하는 데 필요한 종속성을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-104">This article shows the dependencies needed to develop .NET Core applications on Windows.</span></span> <span data-ttu-id="3a417-105">다음에 나오는 지원되는 OS 버전 및 종속성은 Windows에서 .NET Core 앱을 개발하기 위한 세 가지 방법에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-105">The supported OS versions and dependencies that follow apply to the three ways of developing .NET Core apps on Windows:</span></span>

* [<span data-ttu-id="3a417-106">명령줄</span><span class="sxs-lookup"><span data-stu-id="3a417-106">Command line</span></span>](tutorials/using-with-xplat-cli.md)
* [<span data-ttu-id="3a417-107">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="3a417-107">Visual Studio 2017</span></span>](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)
* [<span data-ttu-id="3a417-108">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="3a417-108">Visual Studio Code</span></span>](https://code.visualstudio.com/)

## <a name="net-core-supported-windows-versions"></a><span data-ttu-id="3a417-109">.NET Core가 지원되는 Windows 버전</span><span class="sxs-lookup"><span data-stu-id="3a417-109">.NET Core supported Windows versions</span></span>

<span data-ttu-id="3a417-110">.NET Core는 다음 버전에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-110">.NET Core is supported on the following versions of:</span></span>

* <span data-ttu-id="3a417-111">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="3a417-111">Windows 7 SP1</span></span>
* <span data-ttu-id="3a417-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3a417-112">Windows 8.1</span></span>
* <span data-ttu-id="3a417-113">Windows 10 1주년 업데이트(버전 1607) 이상 버전</span><span class="sxs-lookup"><span data-stu-id="3a417-113">Windows 10 Anniversary Update (version 1607) or later versions</span></span>
* <span data-ttu-id="3a417-114">Windows Server 2008 R2 SP1(전체 서버 또는 Server Core)</span><span class="sxs-lookup"><span data-stu-id="3a417-114">Windows Server 2008 R2 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="3a417-115">Windows Server 2012 SP1(전체 서버 또는 Server Core)</span><span class="sxs-lookup"><span data-stu-id="3a417-115">Windows Server 2012 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="3a417-116">Windows Server 2012 R2(전체 서버 또는 Server Core)</span><span class="sxs-lookup"><span data-stu-id="3a417-116">Windows Server 2012 R2 (Full Server or Server Core)</span></span>
* <span data-ttu-id="3a417-117">Windows Server 2016 이상 버전(전체 서버, Server Core 또는 Nano Server)</span><span class="sxs-lookup"><span data-stu-id="3a417-117">Windows Server 2016 or later versions (Full Server, Server Core, or Nano Server)</span></span>

<span data-ttu-id="3a417-118">다음 문서에는 버전별 .NET Core 지원 운영 체제의 전체 목록이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-118">The following articles have a complete list of .NET Core supported operating systems per version:</span></span>

* [<span data-ttu-id="3a417-119">.NET Core 2.1 - 지원되는 OS 버전</span><span class="sxs-lookup"><span data-stu-id="3a417-119">.NET Core 2.1 - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)
* [<span data-ttu-id="3a417-120">.NET Core 2.0 - 지원되는 OS 버전</span><span class="sxs-lookup"><span data-stu-id="3a417-120">.NET Core 2.0 - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md)
* [<span data-ttu-id="3a417-121">.NET Core 1.x - 지원되는 OS 버전</span><span class="sxs-lookup"><span data-stu-id="3a417-121">.NET Core 1.x - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)

## <a name="net-core-dependencies"></a><span data-ttu-id="3a417-122">.NET Core 종속성</span><span class="sxs-lookup"><span data-stu-id="3a417-122">.NET Core dependencies</span></span>

<span data-ttu-id="3a417-123">.NET Core 1.1 이전 버전을 Windows 10 및 Windows Server 2016보다 이전 버전의 Windows에서 실행하는 경우 Visual C++ 재배포 가능 패키지가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-123">.NET Core 1.1 and earlier versions require the Visual C++ Redistributable when running on Windows versions earlier than Windows 10 and Windows Server 2016.</span></span> <span data-ttu-id="3a417-124">이 종속성은 .NET Core 설치 관리자에 의해 자동으로 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-124">This dependency is automatically installed by the .NET Core installer.</span></span>

<span data-ttu-id="3a417-125">다음과 같은 경우에는 [Microsoft Visual C++ 2015 재배포 가능 패키지 업데이트 3](https://www.microsoft.com/download/details.aspx?id=52685)을 수동으로 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-125">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) must be manually installed when:</span></span>

* <span data-ttu-id="3a417-126">[설치 관리자 스크립트](./tools/dotnet-install-script.md)를 사용하여 .NET Core 설치.</span><span class="sxs-lookup"><span data-stu-id="3a417-126">Installing .NET Core with the [installer script](./tools/dotnet-install-script.md).</span></span>
* <span data-ttu-id="3a417-127">자체 포함된 .NET Core 응용 프로그램 배포.</span><span class="sxs-lookup"><span data-stu-id="3a417-127">Deploying a self-contained .NET Core application.</span></span>
* <span data-ttu-id="3a417-128">원본에서 제품 빌드.</span><span class="sxs-lookup"><span data-stu-id="3a417-128">Building the product from source.</span></span>
* <span data-ttu-id="3a417-129">*.zip* 파일을 통해 .NET Core 설치.</span><span class="sxs-lookup"><span data-stu-id="3a417-129">Installing .NET Core via a *.zip* file.</span></span> <span data-ttu-id="3a417-130">여기에는 빌드/CI/CD 서버가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-130">This can include build/CI/CD servers.</span></span>

> [!NOTE]
> <span data-ttu-id="3a417-131">**Windows 8.1 이전 버전 또는 Windows Server 2012 R2 이전 버전의 경우:**</span><span class="sxs-lookup"><span data-stu-id="3a417-131">**For Windows 8.1 and earlier versions, or Windows Server 2012 R2 and earlier versions:**</span></span>
>
> <span data-ttu-id="3a417-132">설치된 Windows가 최신 버전이며 Windows 업데이트를 통해 설치할 수 있는 [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows)이 포함되어 있는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="3a417-132">Make sure that your Windows installation is up-to-date and includes [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows), which can be installed through Windows Update.</span></span> <span data-ttu-id="3a417-133">이 업데이트를 설치하지 않는 경우 .NET Core 응용 프로그램을 시작할 때 `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`과 같은 오류가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-133">If you don't have this update installed, you'll see an error like the following when you launch a .NET Core application: `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span></span>
>
> <span data-ttu-id="3a417-134">**Windows 7 또는 Windows Server 2008 R2의 경우:**</span><span class="sxs-lookup"><span data-stu-id="3a417-134">**For Windows 7 or Windows Server 2008 R2:**</span></span>
>
> <span data-ttu-id="3a417-135">KB2999226 외에 [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot)도 설치되어 있는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="3a417-135">In addition to KB2999226, make sure you also have [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot) installed.</span></span> <span data-ttu-id="3a417-136">이 업데이트를 설치하지 않는 경우 .NET Core 응용 프로그램을 시작할 때 `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`와 같은 오류가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-136">If you don't have this update installed, you'll see an error similar to the following when you launch a .NET Core application: `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`.</span></span>

## <a name="prerequisites-with-visual-studio-2017"></a><span data-ttu-id="3a417-137">Visual Studio 2017 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="3a417-137">Prerequisites with Visual Studio 2017</span></span>

<span data-ttu-id="3a417-138">.NET Core SDK를 사용하여 .NET Core 응용 프로그램을 개발하기 위해 원하는 편집기를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-138">You can use any editor to develop .NET Core applications using the .NET Core SDK.</span></span> <span data-ttu-id="3a417-139">[Visual Studio 2017](#visual-studio-2017)에서는 Windows 기반 .NET Core 앱에 대한 통합 개발 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-139">[Visual Studio 2017](#visual-studio-2017) provides an integrated development environment for .NET Core apps on Windows.</span></span>

<span data-ttu-id="3a417-140">[릴리스 정보](/visualstudio/releasenotes/vs2017-relnotes)에서 Visual Studio 2017의 변경 내용에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-140">You can read more about the changes in Visual Studio 2017 in the [release notes](/visualstudio/releasenotes/vs2017-relnotes).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="3a417-141">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="3a417-141">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="3a417-142">Visual Studio 2017에서 .NET Core 2.1 앱을 개발하려면:</span><span class="sxs-lookup"><span data-stu-id="3a417-142">To develop .NET Core 2.1 apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="3a417-143">**기타 도구 집합** 섹션에서 **.NET Core 플랫폼 간 개발** 워크로드를 선택하고 [Visual Studio 2017 버전 15.7.0 이상을 다운로드하여 설치](/visualstudio/install/install-visual-studio)합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-143">[Download and install Visual Studio 2017 version 15.7.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![".NET Core 플랫폼 간 개발" 워크플로가 선택된 Visual Studio 2017 설치 스크린샷](./media/windows-prerequisites/vs-15-8-workloads.jpg)

<span data-ttu-id="3a417-145">**.NET Core 플랫폼 간 개발** 도구 집합이 설치되면 기본적으로 Visual Studio 2017 15.7에서는 .NET Core 2.0 SDK를 사용하고 Visual Studio 2017 15.8에서는 2.1 SDK를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-145">After the **.NET Core cross-platform development** toolset is installed, by default, Visual Studio 2017 15.7 uses .NET Core 2.0 SDK and Visual Studio 2017 15.8 uses 2.1 SDK.</span></span>

 2. <span data-ttu-id="3a417-146">Visual Studio 2017 15.7을 사용하는 경우 [.NET Core 2.1 SDK](https://www.microsoft.com/net/download/core)를 설치하거나 Visual Studio 2017 15.8로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-146">If you're using Visual Studio 2017 15.7, install the [.NET Core 2.1 SDK](https://www.microsoft.com/net/download/core) or upgrade to Visual Studio 2017 15.8.</span></span>

 3. <span data-ttu-id="3a417-147">다음 지침에 따라 기존 또는 새로운 .NET Core 프로젝트의 대상을 .NET Core 2.1로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-147">Retarget existing or new .NET Core projects to .NET Core 2.1 using the following instructions:</span></span>
    * <span data-ttu-id="3a417-148">**프로젝트** 메뉴에서 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-148">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="3a417-149">**대상 프레임워크** 선택 메뉴에서 값을 **.NET Core 2.1**로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-149">In the **Target framework** selection menu, set the value to **.NET Core 2.1**.</span></span>

![“.NET Core 2.0” 대상 프레임워크 메뉴 항목을 선택한 Visual Studio 2017 응용 프로그램 프로젝트 속성의 스크린샷](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="3a417-151">Visual Studio를 .NET Core 2.1 SDK로 구성한 후에는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-151">Once you have Visual Studio configured with .NET Core 2.1 SDK, you can do the following actions:</span></span>

* <span data-ttu-id="3a417-152">기존 .NET Core 1.x 및 2.x 프로젝트를 열고, 빌드하고, 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-152">Open, build, and run existing .NET Core 1.x and 2.x projects.</span></span>
* <span data-ttu-id="3a417-153">.NET Core 1.x 및 2.0 프로젝트의 대상을 .NET Core 2.1로 변경하고 빌드 및 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-153">Retarget .NET Core 1.x and 2.0 projects to .NET Core 2.1, build, and run.</span></span>
* <span data-ttu-id="3a417-154">새로운 .NET Core 2.1 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-154">Create new .NET Core 2.1 projects.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="3a417-155">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="3a417-155">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="3a417-156">Visual Studio 2017에서 .NET Core 2.0 앱을 개발하려면:</span><span class="sxs-lookup"><span data-stu-id="3a417-156">To develop .NET Core 2.0 apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="3a417-157">**기타 도구 집합** 섹션에서 **.NET Core 플랫폼 간 개발** 워크로드를 선택하고 [Visual Studio 2017 버전 15.3.0 이상을 다운로드하여 설치](/visualstudio/install/install-visual-studio)합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-157">[Download and install Visual Studio 2017 version 15.3.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![".NET Core 플랫폼 간 개발" 워크플로가 선택된 Visual Studio 2017 설치 스크린샷](./media/windows-prerequisites/vs-15-3-workloads.jpg)

<span data-ttu-id="3a417-159">**.NET Core 플랫폼 간 개발** 도구 집합이 설치된 후 Visual Studio 2017에서는 기본적으로 .NET Core 1.x를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-159">After the **.NET Core cross-platform development** toolset is installed, Visual Studio 2017 uses .NET Core 1.x by default.</span></span> <span data-ttu-id="3a417-160">.NET Core 2.0 SDK를 설치하여 Visual Studio 2017에 .NET Core 2.0 지원을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-160">Install the .NET Core 2.0 SDK to get .NET Core 2.0 support in Visual Studio 2017.</span></span>

 2. <span data-ttu-id="3a417-161">[.NET Core 2.0 SDK](https://www.microsoft.com/net/download/dotnet-core/2.0)를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-161">Install the [.NET Core 2.0 SDK](https://www.microsoft.com/net/download/dotnet-core/2.0).</span></span>
 3. <span data-ttu-id="3a417-162">다음 지침에 따라 기존 또는 새로운 .NET Core 1.x 프로젝트의 대상을 .NET Core 2.0으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-162">Retarget existing or new .NET Core 1.x projects to .NET Core 2.0 using the following instructions:</span></span>
    * <span data-ttu-id="3a417-163">**프로젝트** 메뉴에서 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-163">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="3a417-164">**대상 프레임워크** 선택 메뉴에서 값을 **.NET Core 2.0**으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-164">In the **Target framework** selection menu, set the value to **.NET Core 2.0**.</span></span>

![“.NET Core 2.0” 대상 프레임워크 메뉴 항목을 선택한 Visual Studio 2017 응용 프로그램 프로젝트 속성의 스크린샷](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="3a417-166">.NET Core 2.0 SDK가 설치된 후 Visual Studio 2017에서는 기본적으로 .NET Core SDK 2.0를 사용하고 다음 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-166">Once the .NET Core 2.0 SDK is installed, Visual Studio 2017 uses the .NET Core SDK 2.0 by default, and supports the following actions:</span></span>

* <span data-ttu-id="3a417-167">기존 .NET Core 1.x 프로젝트를 열고, 빌드하고, 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-167">Open, build, and run existing .NET Core 1.x projects.</span></span>
* <span data-ttu-id="3a417-168">.NET Core 1.x 프로젝트의 대상을 .NET Core 2.0으로 변경하고 빌드 및 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-168">Retarget .NET Core 1.x projects to .NET Core 2.0, build, and run.</span></span>
* <span data-ttu-id="3a417-169">새로운 .NET Core 2.0 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-169">Create new .NET Core 2.0 projects.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="3a417-170">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="3a417-170">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="3a417-171">Visual Studio에서 .NET Core 1.x 앱을 개발하려면 **기타 도구 집합** 섹션에서 **“.NET Core 플랫폼 간 개발”** 워크로드를 선택하고 [Visual Studio 2017을 다운로드하여 설치](/visualstudio/install/install-visual-studio)합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-171">To develop .NET Core 1.x apps in Visual Studio, [download and install Visual Studio 2017](/visualstudio/install/install-visual-studio) with the **".NET Core cross-platform development"** workload (in the **Other Toolsets** section) selected.</span></span>

![".NET Core 플랫폼 간 개발" 워크플로가 선택된 Visual Studio 2017 설치 스크린샷](./media/windows-prerequisites/vs_workloads.jpg)

> [!IMPORTANT]
> <span data-ttu-id="3a417-173">.NET Core 1.x 개발에 Visual Studio 2015를 사용할 수 있지만 다음 이유로 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-173">It's possible to use Visual Studio 2015 for .NET Core 1.x development, but it's not recommended for the following reasons:</span></span>
  > * <span data-ttu-id="3a417-174">.NET Core 도구는 지원되지 않는 미리 보기 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-174">The .NET Core tooling is a preview version, which is not supported.</span></span>
  > * <span data-ttu-id="3a417-175">프로젝트는 더 이상 사용되지 않는 project.json을 기반으로 작성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-175">The projects are project.json-based, which is deprecated.</span></span>
>
> <span data-ttu-id="3a417-176">프로젝트 형식 변경에 대한 자세한 내용은 [변경 내용에 대한 대략적인 개요](./tools/cli-msbuild-architecture.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3a417-176">For more information about the project format changes, see [High-level overview of changes](./tools/cli-msbuild-architecture.md).</span></span>
---

<a name="vs-mapping"></a>

> [!TIP]
> <span data-ttu-id="3a417-177">Visual Studio 2017 버전을 확인하려면:</span><span class="sxs-lookup"><span data-stu-id="3a417-177">To verify your Visual Studio 2017 version:</span></span>
>
> * <span data-ttu-id="3a417-178">**도움말** 메뉴에서 **Microsoft Visual Studio 정보**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-178">On the **Help** menu, choose **About Microsoft Visual Studio**.</span></span>
> * <span data-ttu-id="3a417-179">**Microsoft Visual Studio 정보** 대화 상자에서 버전 번호를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3a417-179">In the **About Microsoft Visual Studio** dialog, verify the version number.</span></span>
>   * <span data-ttu-id="3a417-180">.NET Core 2.2 미리 보기 1 앱의 경우 Visual Studio 2017 버전 15.9(현재 미리 보기) 이상.</span><span class="sxs-lookup"><span data-stu-id="3a417-180">For .NET Core 2.2 Preview 1 apps, Visual Studio 2017 version 15.9 (currently in Preview) or higher.</span></span>
>   * <span data-ttu-id="3a417-181">.NET Core 2.1 앱의 경우 Visual Studio 2017 버전 15.7 이상.</span><span class="sxs-lookup"><span data-stu-id="3a417-181">For .NET Core 2.1 apps, Visual Studio 2017 version 15.7 or higher.</span></span>
>   * <span data-ttu-id="3a417-182">.NET Core 2.0 앱의 경우 Visual Studio 2017 버전 15.3 이상.</span><span class="sxs-lookup"><span data-stu-id="3a417-182">For .NET Core 2.0 apps, Visual Studio 2017 version 15.3 or higher.</span></span>
>   * <span data-ttu-id="3a417-183">.NET Core 1.x 앱의 경우 Visual Studio 2017 버전 15.0 이상.</span><span class="sxs-lookup"><span data-stu-id="3a417-183">For .NET Core 1.x apps, Visual Studio 2017 version 15.0 or higher.</span></span>
