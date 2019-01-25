---
title: .NET Core 3.0의 새로운 기능
description: .NET Core 3.0에 있는 새로운 기능에 대해 알아봅니다.
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/04/2018
ms.openlocfilehash: 26fb7cb25b9bf7f00f87059fbe1848763f7f175d
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415548"
---
# <a name="whats-new-in-net-core-30-preview-1"></a><span data-ttu-id="30783-103">.NET Core 3.0(Preview 1)의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="30783-103">What's new in .NET Core 3.0 (Preview 1)</span></span>

<span data-ttu-id="30783-104">이 문서에서는 .NET Core 3.0(Preview 1)의 새로운 기능에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-104">This article describes what is new in .NET Core 3.0 (preview 1).</span></span> <span data-ttu-id="30783-105">가장 중요한 개선 사항 중 하나는 Windows 데스크톱 애플리케이션에 대한 지원(Windows만 해당)입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-105">One of the biggest enhancements is support for Windows desktop applications (Windows only).</span></span> <span data-ttu-id="30783-106">Windows 데스크톱이라는 .NET Core 3.0 구성 요소를 활용하여 Windows Forms WPF(Windows Presentation Foundation) 애플리케이션을 포팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-106">By utilizing a .NET Core 3.0 component called Windows Desktop, you can port your Windows Forms Windows Presentation Foundation (WPF) applications.</span></span> <span data-ttu-id="30783-107">분명히 말하지만, Windows 데스크톱 구성 요소는 Windows에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-107">To be clear, the Windows Desktop component is only supported on Windows.</span></span> <span data-ttu-id="30783-108">자세한 내용은 아래의 [Windows 데스크톱](#windows-desktop) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-108">For more information, see the section [Windows desktop](#windows-desktop) below.</span></span>

<span data-ttu-id="30783-109">.NET Core 3.0에서는 C# 8.0에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-109">.NET Core 3.0 adds support for C# 8.0.</span></span>

<span data-ttu-id="30783-110">Windows, Mac 및 Linux에서 지금 바로 [.NET Core 3 Preview 1을 다운로드하여 시작](https://aka.ms/netcore3download)하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-110">[Download and get started with .NET Core 3 Preview 1](https://aka.ms/netcore3download) right now on Windows, Mac and Linux.</span></span> <span data-ttu-id="30783-111">[.NET Core 3 Preview 1 릴리스 정보](https://aka.ms/netcore3releasenotes)에서 자세한 릴리스 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-111">You can see complete details of the release in the [.NET Core 3 Preview 1 release notes](https://aka.ms/netcore3releasenotes).</span></span>

<span data-ttu-id="30783-112">자세한 내용은 [.NET Core 3.0 Preview 1 알림](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-112">For more information, see the [.NET Core 3.0 Preview 1 announcement](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/).</span></span>

## <a name="net-standard-21"></a><span data-ttu-id="30783-113">.NET Standard 2.1</span><span class="sxs-lookup"><span data-stu-id="30783-113">.NET Standard 2.1</span></span>

<span data-ttu-id="30783-114">.NET Core 3.0에서는 .NET Standard 2.1을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-114">.NET Core 3.0 implements .NET Standard 2.1.</span></span>

## <a name="default-executables"></a><span data-ttu-id="30783-115">기본 실행 파일</span><span class="sxs-lookup"><span data-stu-id="30783-115">Default executables</span></span>

<span data-ttu-id="30783-116">이제 .NET Core에서 기본적으로 [프레임워크 종속 실행 파일](../deploying/index.md#framework-dependent-executables-fde)을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-116">.NET Core will now build [framework-dependent executables](../deploying/index.md#framework-dependent-executables-fde) by default.</span></span> <span data-ttu-id="30783-117">이는 전역으로 설치된 .NET Core 버전을 사용하는 애플리케이션을 위한 새로운 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-117">This is new for applications that use a globally installed version of .NET Core.</span></span> <span data-ttu-id="30783-118">지금까지는 [자체 포함 배포](../deploying/index.md#self-contained-deployments-scd)만 실행 파일을 생성했습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-118">Until now, only [self-contained deployments](../deploying/index.md#self-contained-deployments-scd) would produce an executable.</span></span>

<span data-ttu-id="30783-119">사용 중인 SDK의 환경 및 플랫폼과 일치하는 경우 `dotnet build` 또는 `dotnet publish` 중에 실행 파일이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-119">During `dotnet build` or `dotnet publish`, an executable is created provided that matches the environment and platform of the SDK you are using.</span></span> <span data-ttu-id="30783-120">다른 네이티브 실행 파일과 마찬가지로 이러한 실행 파일에서도 다음과 같은 동일한 기능을 예상할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-120">You can expect the same things with these executables as you would other native executables, such as:</span></span>

* <span data-ttu-id="30783-121">실행 파일을 두 번 클릭할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-121">You can double-click on the executable.</span></span>
* <span data-ttu-id="30783-122">Windows의 `myapp.exe`, Linux 및 macOS의 `./myapp`과 같은 애플리케이션을 명령 프롬프트에서 직접 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-122">You can launch the application from a command prompt directly, such as `myapp.exe` on Windows, and `./myapp` on Linux and macOS.</span></span>

## <a name="build-copies-dependencies"></a><span data-ttu-id="30783-123">빌드 복사본 종속성</span><span class="sxs-lookup"><span data-stu-id="30783-123">Build copies dependencies</span></span>

<span data-ttu-id="30783-124">이제 `dotnet build`가 애플리케이션에 대한 NuGet 종속성을 NuGet 캐시에서 빌드 출력 폴더로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-124">`dotnet build` now copies NuGet dependencies for your application from the NuGet cache to the build output folder.</span></span> <span data-ttu-id="30783-125">이전에는 종속성이 `dotnet publish` 중에만 복사되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-125">Previously, dependencies were only copied as part of `dotnet publish`.</span></span> 

<span data-ttu-id="30783-126">연결, Razor 페이지 게시 등 여전히 게시해야 하는 일부 작업이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-126">There are some operations, like linking and razor page publishing that will still require publishing.</span></span>


## <a name="local-dotnet-tools"></a><span data-ttu-id="30783-127">로컬 dotnet 도구</span><span class="sxs-lookup"><span data-stu-id="30783-127">Local dotnet tools</span></span>

<span data-ttu-id="30783-128">.NET Core 2.1은 전역 도구를 지원한 한편, .NET Core 3.0은 이제 로컬 도구를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-128">While .NET Core 2.1 supported global tools, .NET Core 3.0 now has local tools.</span></span> <span data-ttu-id="30783-129">로컬 도구는 전역 도구와 유사하지만 디스크의 특정 위치와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-129">Local tools are similar to global tools but are associated with a particular location on disk.</span></span> <span data-ttu-id="30783-130">이를 통해 프로젝트별 및 리포지토리별 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-130">This enables per-project and per-repository tooling.</span></span> <span data-ttu-id="30783-131">로컬로 설치된 도구는 전역으로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-131">Any tool installed locally isn't available globally.</span></span>

<span data-ttu-id="30783-132">로컬 도구는 현재 디렉터리에 있는 매니페스트 파일 이름 `dotnet-tools.json`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-132">Local tools rely on a manifest file name `dotnet-tools.json` in your current directory.</span></span> <span data-ttu-id="30783-133">이 매니페스트 파일은 사용 가능한 도구를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-133">This manifest file defines the tools to be available.</span></span> <span data-ttu-id="30783-134">리포지토리 루트에 이 매니페스트 파일을 만들면 코드를 복제하는 누구든지 성공적인 코드 작업에 필요한 도구를 복원하고 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-134">By creating this manifest file at the root of your repository, you ensure anyone cloning your code can restore and use the tools that are needed to successfully work with your code.</span></span>

<span data-ttu-id="30783-135">로컬 도구 매니페스트 파일을 사용할 수 있는 경우 다음 명령을 사용하여 해당 도구를 자동으로 다운로드하고 로컬에 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-135">When the local tools manifest file is available, use the following command to automatically download and install those tools locally:</span></span>

```console
dotnet tool restore
```

<span data-ttu-id="30783-136">다음 명령을 사용하여 로컬 도구를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-136">Run a local tool with the following command:</span></span>

```console
dotnet tool run <tool-command-name>
```

<span data-ttu-id="30783-137">로컬 도구가 호출되면 dotnet은 디렉터리 구조 위로 매니페스트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-137">When a local tool is called, dotnet searches for a manifest up the directory structure.</span></span> <span data-ttu-id="30783-138">도구 매니페스트 파일이 있으면 해당 파일에서 요청된 도구를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-138">When a tool manifest file is found, it is searched for the requested tool.</span></span> <span data-ttu-id="30783-139">도구가 발견되면 도구를 찾는 데 필요한 정보를 NuGet 전역 패키지 위치에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-139">If the tool is found, it includes the information needed to find the tool in the NuGet global packages location.</span></span> 

<span data-ttu-id="30783-140">도구가 매니페스트에서 발견되었지만 캐시에 없는 경우 사용자에게 오류가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-140">If the tool is found in the manifest, but not the cache, the user receives an error.</span></span> <span data-ttu-id="30783-141">사용자에게 `dotnet tool restore`를 실행하도록 요청하기 위해 미리 보기 1 이후에 메시지가 개선될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-141">The message will be improved after Preview 1 to request the user run `dotnet tool restore`.</span></span>

<span data-ttu-id="30783-142">디렉터리에 로컬 도구를 추가하려면 먼저 도구 매니페스트 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-142">To add local tools to a directory, you need to first create the tool manifest file.</span></span> <span data-ttu-id="30783-143">dotnet 새 템플릿과 같은 도구 매니페스트 파일 생성 메커니즘이 미리 보기 1 이후에 제공될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-143">After Preview 1, we will offer a mechanism for creating tool manifest files, such as a dotnet new template.</span></span> <span data-ttu-id="30783-144">미리 보기 1에서는 다음 내용을 포함하는 `dotnet-tools.json` 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-144">For Preview 1 you must create the file named `dotnet-tools.json` with the following contents:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {}
}
```

<span data-ttu-id="30783-145">매니페스트가 생성되고 나면 다음을 사용하여 매니페스트에 로컬 도구를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-145">Once the manifest is created, you can add local tools to it using:</span></span>

```console
dotnet tool install <toolPackageId>
```

<span data-ttu-id="30783-146">다른 버전을 지정하지 않을 경우 이 명령에 따라 최신 버전의 도구가 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-146">This command installs the latest version of the tool, unless another version is specified.</span></span>  <span data-ttu-id="30783-147">최신 버전이 자동으로 선택된 경우에도 올바른 버전의 도구를 복원 또는 실행할 수 있도록 도구 버전이 도구 매니페스트 파일에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-147">Even if the latest version was automatically chosen, the version of the tool is written into the tool manifest file to allow the correct version of the tool to be restored or run.</span></span>

<span data-ttu-id="30783-148">도구 매니페스트 파일은 리포지토리 작업에 필요한 버전 업데이트 등을 위한 수동 편집을 허용하도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-148">The tool manifest file is designed to allow hand editing – which you might do to update the required version for working with the repository.</span></span>

<span data-ttu-id="30783-149">예제 `dotnet-tools.json` 파일은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-149">Here is an example `dotnet-tools.json` file:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

<span data-ttu-id="30783-150">도구 매니페스트 파일에서 도구를 제거하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-150">To remove a tool from the tool manifest file, run the following command:</span></span>

```console
dotnet tool uninstall <toolPackageId>
```

<span data-ttu-id="30783-151">전역 도구와 로컬 도구 둘 다, 호환되는 버전의 런타임이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-151">For both global and local tools, a compatible version of the runtime is required.</span></span> <span data-ttu-id="30783-152">현재 NuGet.org의 많은 도구는 .NET Core 런타임 2.1을 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-152">Many tools currently on NuGet.org target .NET Core Runtime 2.1.</span></span> <span data-ttu-id="30783-153">이러한 도구를 전역 또는 로컬로 설치하려면 여전히 [NET Core 2.1 런타임](https://dotnet.microsoft.com/download/dotnet-core/2.1)을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-153">To install those globally or locally, you would still need to install the [NET Core 2.1 Runtime](https://dotnet.microsoft.com/download/dotnet-core/2.1).</span></span>

<span data-ttu-id="30783-154">자세한 내용은 [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288)(로컬 도구 초기 미리 보기 문서)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-154">For more information, see [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288).</span></span>

## <a name="windows-desktop"></a><span data-ttu-id="30783-155">Windows 바탕 화면</span><span class="sxs-lookup"><span data-stu-id="30783-155">Windows desktop</span></span>

<span data-ttu-id="30783-156">.NET Core 3.0 Preview 1부터 WPF 및 Windows Forms를 사용하여 Windows 데스크톱 애플리케이션을 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-156">Starting with .NET Core 3.0 Preview 1, you can build Windows desktop applications using WPF and Windows Forms.</span></span> <span data-ttu-id="30783-157">이러한 프레임워크는 [XAML 아일랜드](/windows/uwp/xaml-platform/xaml-host-controls)를 통해 Windows UI XAML 라이브러리(WinUI)의 최신 컨트롤 및 Fluent 스타일을 사용하는 것도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-157">These frameworks also support using modern controls and Fluent styling from the Windows UI XAML Library (WinUI) via [XAML islands](/windows/uwp/xaml-platform/xaml-host-controls).</span></span>

<span data-ttu-id="30783-158">Windows 데스크톱 구성 요소는 Windows .NET Core 3.0 SDK의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-158">The Windows Desktop component is part of the Windows .NET Core 3.0 SDK.</span></span>

<span data-ttu-id="30783-159">다음 `dotnet` 명령을 사용하여 새 WPF 또는 Windows Forms 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-159">You can create a new WPF or Windows Forms app with the following `dotnet` commands:</span></span>

```console
dotnet new wpf
dotnet new winforms
```

<span data-ttu-id="30783-160">Visual Studio 2019 Preview 1에서 .NET Core 3.0 WPF 및 Windows Forms 프로젝트를 열고 시작 및 디버그할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-160">You can also open, launch, and debug .NET Core 3.0 WPF and Windows Forms projects in Visual Studio 2019 Preview 1.</span></span> <span data-ttu-id="30783-161">현재 Visual Studio 2017 15.9에서 이러한 프로젝트를 열 수 있지만 지원되는 시나리오는 아니며, [미리 보기를 사용](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-161">It's currently possible to open these projects in Visual Studio 2017 15.9, however, it isn't a supported scenario (and you need to [enable previews](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)).</span></span>

<span data-ttu-id="30783-162">새 프로젝트는 몇 가지 내용만 추가되고, 기존 .NET Core 프로젝트와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-162">The new projects are the same as existing .NET Core projects, with a couple additions.</span></span> <span data-ttu-id="30783-163">기본 .NET Core 콘솔 프로젝트와 기본 Windows Forms 및 WPF 프로젝트의 비교는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-163">Here is the comparison of the basic .NET Core console project and a basic Windows Forms and WPF project.</span></span>

<span data-ttu-id="30783-164">.NET Core 콘솔 프로젝트에서 프로젝트는 `Microsoft.NET.Sdk` SDK를 사용하고 `netcoreapp3.0` 대상 프레임워크를 통해 .NET Core 3.0에 대한 종속성을 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-164">In a .NET Core console project, the project uses the `Microsoft.NET.Sdk` SDK and declares a dependency on .NET Core 3.0 via the `netcoreapp3.0` target framework.</span></span> <span data-ttu-id="30783-165">Windows 데스크톱 앱을 만들려면 `Microsoft.NET.Sdk.WindowsDesktop` SDK를 사용하고, 사용할 UI 프레임워크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-165">To create a Windows Desktop app, use the `Microsoft.NET.Sdk.WindowsDesktop` SDK and choose which UI framework to use:</span></span>

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="30783-166">WPF가 아닌 Windows Forms를 선택하려면 `UseWPF` 대신 `UseWindowsForms`를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-166">To choose Windows Forms over WPF, set `UseWindowsForms` instead of `UseWPF`:</span></span>

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="30783-167">앱이 두 프레임워크를 모두 사용하는 경우(예: Windows Forms 대화 상자에서 WPF 컨트롤을 호스트하는 경우) `UseWPF` 및 `UseWindowsForms`를 둘 다 `true`로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-167">Both `UseWPF` and `UseWindowsForms` can be set to `true` if the app uses both frameworks, for example when a Windows Forms dialog is hosting a WPF control.</span></span>

<span data-ttu-id="30783-168">[dotnet/winforms](https://github.com/dotnet/winforms/issues),  [dotnet/wpf](https://github.com/dotnet/wpf/issues) 및 [dotnet/core](https://github.com/dotnet/core/issues) 리포지토리에서 피드백을 공유하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-168">Please share your feedback on the [dotnet/winforms](https://github.com/dotnet/winforms/issues),  [dotnet/wpf](https://github.com/dotnet/wpf/issues) and [dotnet/core](https://github.com/dotnet/core/issues) repos.</span></span>

## <a name="fast-built-in-json-support"></a><span data-ttu-id="30783-169">빠른 기본 제공 JSON 지원</span><span class="sxs-lookup"><span data-stu-id="30783-169">Fast built-in JSON support</span></span>

<span data-ttu-id="30783-170">`System.Text.Json.Utf8JsonReader`는 `ReadOnlySpan<byte>`에서 읽어온 UTF-8 인코드된 JSON 텍스트를 위한 고성능, 저할당, 전달 전용 판독기입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-170">`System.Text.Json.Utf8JsonReader` is a high-performance, low allocation, forward-only reader for UTF-8 encoded JSON text, read from a `ReadOnlySpan<byte>`.</span></span> <span data-ttu-id="30783-171">`Utf8JsonReader`는 사용자 지정 구문 분석기 및 역직렬 변환기를 빌드하는 데 활용할 수 있는 하위 수준의 기초 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-171">The `Utf8JsonReader` is a foundational, low-level type, that can be leveraged to build custom parsers and deserializers.</span></span> <span data-ttu-id="30783-172">새 `Utf8JsonReader`를 사용하여 JSON 페이로드를 읽을 경우 [Json.NET](https://www.newtonsoft.com/json)의 판독기를 사용하는 것에 비해 2배 더 빠릅니다.</span><span class="sxs-lookup"><span data-stu-id="30783-172">Reading through a JSON payload using the new `Utf8JsonReader` is 2x faster than using the reader from [Json.NET](https://www.newtonsoft.com/json).</span></span> <span data-ttu-id="30783-173">JSON 토큰을 (UTF-16) 문자열로 실현해야 할 때까지 할당하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-173">It does not allocate until you need to actualize JSON tokens as (UTF-16) strings.</span></span>

<span data-ttu-id="30783-174">이 새로운 API에는 다음 구성 요소가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-174">This new API will include the following components:</span></span>

* <span data-ttu-id="30783-175">미리 보기 1: JSON 판독기(순차적 액세스)</span><span class="sxs-lookup"><span data-stu-id="30783-175">In Preview 1: JSON reader (sequential access)</span></span>
* <span data-ttu-id="30783-176">향후 제공 예정: JSON 기록기, DOM(임의 액세스), poco 직렬 변환기, poco 역직렬 변환기</span><span class="sxs-lookup"><span data-stu-id="30783-176">Coming next: JSON writer, DOM (random access), poco serializer, poco deserializer</span></span>

<span data-ttu-id="30783-177">시작점으로 사용할 수 있는 `Utf8JsonReader`의 기본 판독기 루프는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-177">Here is the basic reader loop for the `Utf8JsonReader` that can be used as a starting point:</span></span>

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

<span data-ttu-id="30783-178">.NET 에코시스템은 [Json.NET](https://www.newtonsoft.com/json) 및 여전히 유용한 기타 인기 있는 JSON 라이브러리를 사용해 왔습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-178">The .NET ecosystem has relied on [Json.NET](https://www.newtonsoft.com/json) and other popular JSON libraries, which continue to be good choices.</span></span> <span data-ttu-id="30783-179">Json.NET는 내부적으로 UTF-16인 .NET 문자열을 기본 데이터 형식으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-179">JSON.NET uses .NET strings as its base datatype, which are UTF-16 under the hood.</span></span> 

<span data-ttu-id="30783-180">.NET Core 2.1 및 3.0에서는 `Span<T>` 및 UTF-8 문자열 사용을 기준으로 훨씬 적은 메모리가 필요하며 Kestrel, ASP.NET Core 웹 서버와 같은 처리량이 높은 애플리케이션 요구의 처리가 개선된 JSON API(예: `Utf8JsonReader`)를 작성할 수 있는 새로운 API가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-180">In .NET Core 2.1 and 3.0, we added new APIs that makes it possible to write JSON APIs (such as `Utf8JsonReader`) that require much less memory, based on using `Span<T>` and UTF-8 strings, and better serve the needs of high-throughput applications like Kestrel, ASP.NET Core web server.</span></span>

## <a name="ranges-and-indices"></a><span data-ttu-id="30783-181">범위 및 인덱스</span><span class="sxs-lookup"><span data-stu-id="30783-181">Ranges and indices</span></span>

<span data-ttu-id="30783-182">새 `Index` 형식을 인덱싱에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-182">The new `Index` type can be used for indexing.</span></span> <span data-ttu-id="30783-183">시작부터 계산되는 `int`의 인덱스를 만들거나, 접두사 `^` 연산자(C#)를 사용하여 끝부터 계산되는 인덱스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-183">You can create one from an `int` that counts from the beginning, or with a prefix `^` operator (C#) that counts from the end:</span></span>

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

<span data-ttu-id="30783-184">시작 인덱스와 끝 인덱스의 두 `Index` 값으로 구성되고 `x..y` 범위 식(C#)으로 작성할 수 있는 `Range` 유형도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-184">There is also a `Range` type, which consists of two `Index` values, one for the start and one for the end, and can be written with a `x..y` range expression (C#).</span></span> <span data-ttu-id="30783-185">조각을 생성하기 위해 `Range`를 사용하여 인덱싱할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-185">You can then index with a `Range` in order to produce a slice:</span></span>

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

> [!NOTE]
> <span data-ttu-id="30783-186">[C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/)에서만 `Range` 및 `Index` 구문을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-186">Only [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) supports syntax for `Range` and `Index`.</span></span>

## <a name="async-streams"></a><span data-ttu-id="30783-187">비동기 스트림</span><span class="sxs-lookup"><span data-stu-id="30783-187">Async streams</span></span>

<span data-ttu-id="30783-188">`IAsyncEnumerable<T>` 형식은 `IEnumerable<T>`의 새로운 비동기 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-188">The `IAsyncEnumerable<T>` type is a new asynchronous version of `IEnumerable<T>`.</span></span> <span data-ttu-id="30783-189">이 언어에서는 `await foreach`을 통해 해당 요소를 사용하고, `yield return`을 통해 요소를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-189">The language lets you `await foreach` over these to consume their elements, and `yield return` to them to produce elements.</span></span>

<span data-ttu-id="30783-190">다음 예제에서는 비동기 스트림의 생성 및 사용을 둘 다 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30783-190">The following example demonstrates both production and consumption of async streams.</span></span> <span data-ttu-id="30783-191">`foreach` 문은 비동기이며, `yield return`을 사용하여 호출자에 대한 비동기 스트림을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-191">The `foreach` statement is async and itself uses `yield return` to produce an async stream for callers.</span></span> <span data-ttu-id="30783-192">이 패턴(`yield return` 사용)은 비동기 스트림 생성을 위한 권장 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-192">This pattern (using `yield return`) is the recommended model for producing async streams.</span></span>

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

> [!WARNING]
> <span data-ttu-id="30783-193">.NET Core 3.0 Preview 1에는 현재 `await foreach` 관련 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-193">.NET Core 3.0 Preview 1 currently has a bug with `await foreach`.</span></span> <span data-ttu-id="30783-194">대신, `GetEnumerator` 및 `MoveNext`를 사용하여 요소를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-194">Instead, use `GetEnumerator` and `MoveNext` to process elements.</span></span> <span data-ttu-id="30783-195">자세한 내용은 [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-195">For more information, see [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268).</span></span>

<span data-ttu-id="30783-196">`await foreach`를 수행할 수 있을 뿐 아니라, 비동기 반복기(예: `await` 및 `yield`가 둘 다 가능한 `IAsyncEnumerable/IAsyncEnumerator`를 반환하는 반복기)를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-196">In addition to being able to `await foreach`, you can also create async iterators, for example, an iterator that returns an `IAsyncEnumerable/IAsyncEnumerator` that you can both `await` and `yield` in.</span></span> <span data-ttu-id="30783-197">삭제해야 하는 개체의 경우 `Stream` 및 `Timer`와 같은 다양한 BCL 유형이 구현하는 `IAsyncDisposable`을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-197">For objects that need to be disposed, you can use `IAsyncDisposable`, which various BCL types implement, such as `Stream` and `Timer`.</span></span>

> [!NOTE]
> <span data-ttu-id="30783-198">[C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/)에서만 `await foreach` 구문을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-198">Only [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) supports `await foreach` syntax.</span></span>

## <a name="type-sequencereader"></a><span data-ttu-id="30783-199">유형: SequenceReader</span><span class="sxs-lookup"><span data-stu-id="30783-199">Type: SequenceReader</span></span>

<span data-ttu-id="30783-200">.NET Core 3.0에서는 `ReadOnlySequence<T>`용 판독기로 사용할 수 있는 `System.Buffers.SequenceReader`가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-200">In .NET Core 3.0, `System.Buffers.SequenceReader` has been added which can be used as a reader for `ReadOnlySequence<T>`.</span></span> <span data-ttu-id="30783-201">이를 통해 여러 지원 버퍼에 걸쳐 있을 수 있는 `System.IO.Pipelines` 데이터의 고성능, 저할당 구문 분석이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-201">This allows easy, high performance, low allocation parsing of `System.IO.Pipelines` data that can cross multiple backing buffers.</span></span> 

<span data-ttu-id="30783-202">다음 예제에서는 입력 `Sequence`를 유효한 `CR/LF` 구분 줄로 분석합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-202">The following example breaks an input `Sequence` into valid `CR/LF` delimited lines:</span></span>

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a><span data-ttu-id="30783-203">유형: MetadataLoadContext</span><span class="sxs-lookup"><span data-stu-id="30783-203">Type: MetadataLoadContext</span></span>

<span data-ttu-id="30783-204">호출자의 애플리케이션 도메인에 영향을 주지 않고 어셈블리 메타데이터를 읽을 수 있도록 하는 `MetadataLoadContext` 형식이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-204">The `MetadataLoadContext` type has been added that enables reading assembly metadata without affecting the caller’s application domain.</span></span> <span data-ttu-id="30783-205">현재 런타임 환경과 다른 아키텍처 및 플랫폼용으로 빌드된 어셈블리를 포함하여, 어셈블리는 데이터로 읽힙니다.</span><span class="sxs-lookup"><span data-stu-id="30783-205">Assemblies are read as data, including assemblies built for different architectures and platforms than the current runtime environment.</span></span> <span data-ttu-id="30783-206">`MetadataLoadContext`는 .NET Framework에서만 사용할 수 있는 <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>와 겹칩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-206">`MetadataLoadContext` overlaps with the <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, which is only available in the .NET Framework.</span></span>

<span data-ttu-id="30783-207">`MetdataLoadContext`는 [System.Reflection.MetadataLoadContext 패키지](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-207">`MetdataLoadContext` is available in the [System.Reflection.MetadataLoadContext package](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext).</span></span> <span data-ttu-id="30783-208">.NET Standard 2.0 패키지입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-208">It is a .NET Standard 2.0 package.</span></span>

<span data-ttu-id="30783-209">`MetadataLoadContext`는 <xref:System.Runtime.Loader.AssemblyLoadContext> 형식과 마찬가지로 API를 노출하지만 해당 형식을 기반으로 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-209">The `MetadataLoadContext` exposes APIs similar to the <xref:System.Runtime.Loader.AssemblyLoadContext> type, but is not based on that type.</span></span> <span data-ttu-id="30783-210"><xref:System.Runtime.Loader.AssemblyLoadContext>와 마찬가지로, `MetadataLoadContext`를 사용하면 격리된 어셈블리 로드 Universe 내에서 어셈블리를 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-210">Much like <xref:System.Runtime.Loader.AssemblyLoadContext>, the `MetadataLoadContext` enables loading assemblies within an isolated assembly loading universe.</span></span> <span data-ttu-id="30783-211">`MetdataLoadContext` API는 <xref:System.Reflection.Assembly> 개체를 반환하여 익숙한 리플렉션 API를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-211">`MetdataLoadContext` APIs return <xref:System.Reflection.Assembly> objects, enabling the use of familiar reflection APIs.</span></span> <span data-ttu-id="30783-212">[MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127) 등의 실행 지향 API는 허용되지 않으며 InvalidOperationException을 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-212">Execution-oriented APIs, such as [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), are not allowed and will throw InvalidOperationException.</span></span>

<span data-ttu-id="30783-213">다음 샘플은 지정된 인터페이스를 구현하는 어셈블리에서 구체적인 형식을 찾는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30783-213">The following sample demonstrates how to find concrete types in an assembly that implements a given interface:</span></span>

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

<span data-ttu-id="30783-214">`MetadataLoadContext`에 대한 시나리오에는 어셈블리 세트를 데이터로 검사하고, 검사가 수행된 후 모든 파일 잠금 및 메모리가 해제되어야 하는 디자인 타임 기능, 빌드 타임 도구 및 런타임 강화 기능이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-214">Scenarios for `MetadataLoadContext` include design-time features, build-time tooling, and runtime light-up features that need to inspect a set of assemblies as data and have all file locks and memory freed after inspection is performed.</span></span>

<span data-ttu-id="30783-215">`MetadataLoadContext`에는 생성자에게 전달되는 확인자 클래스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-215">The `MetadataLoadContext` has a resolver class passed to its constructor.</span></span> <span data-ttu-id="30783-216">확인자의 작업은 `AssemblyName`이 제공될 경우 `Assembly`를 로드하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-216">The resolver's job is to load an `Assembly` given its `AssemblyName`.</span></span> <span data-ttu-id="30783-217">확인자 클래스는 추상 `MetadataAssemblyResolver` 클래스에서 파생됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-217">The resolver class derives from the abstract `MetadataAssemblyResolver` class.</span></span> <span data-ttu-id="30783-218">경로 기반 시나리오에 대한 확인자 구현은 `PathAssemblyResolver`를 사용하여 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-218">An implementation of the resolver for path-based scenarios is provided with `PathAssemblyResolver`.</span></span>

<span data-ttu-id="30783-219">[MetadataLoadContext 테스트](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests)는 많은 사용 사례를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30783-219">The [MetadataLoadContext tests](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) demonstrate many use cases.</span></span> <span data-ttu-id="30783-220">[어셈블리 테스트](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs)에서 시작하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-220">The [Assembly tests](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) are a good place to start.</span></span>

## <a name="tls-13--openssl-111-on-linux"></a><span data-ttu-id="30783-221">Linux의 TLS 1.3 및 OpenSSL 1.1.1</span><span class="sxs-lookup"><span data-stu-id="30783-221">TLS 1.3 & OpenSSL 1.1.1 on Linux</span></span>

<span data-ttu-id="30783-222">이제 .NET Core는 지정된 환경에서 사용 가능한 경우 [OpenSSL 1.1.1의 TLS 1.3 지원](https://www.openssl.org/blog/blog/2018/09/11/release111/)을 이용합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-222">.NET Core will now take advantage of [TLS 1.3 support in OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), when it is available in a given environment.</span></span> <span data-ttu-id="30783-223">[OpenSSL 팀](https://www.openssl.org/blog/blog/2018/09/11/release111/)을 기준으로, TLS 1.3의 여러 가지 혜택이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-223">There are multiple benefits of TLS 1.3, per the [OpenSSL team](https://www.openssl.org/blog/blog/2018/09/11/release111/):</span></span>

* <span data-ttu-id="30783-224">클라이언트와 서버 간에 필요한 왕복 횟수가 감소하여 연결 시간이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-224">Improved connection times due to a reduction in the number of round trips required between the client and server.</span></span>

* <span data-ttu-id="30783-225">사용되지 않는 다양한 비보안 암호화 알고리즘이 제거되고 연결 핸드셰이크가 더 많이 암호화되어 보안이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-225">Improved security due to the removal of various obsolete and insecure cryptographic algorithms and encryption of more of the connection handshake.</span></span>

<span data-ttu-id="30783-226">.NET Core 3.0 Preview 1은 **OpenSSL 1.1.1**, **OpenSSL 1.1.0** 또는 **OpenSSL 1.0.2**(Linux 시스템에서 발견된 가장 적합한 버전)를 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-226">.NET Core 3.0 Preview 1 is capable of utilizing **OpenSSL 1.1.1**, **OpenSSL 1.1.0**, or **OpenSSL 1.0.2** (whatever the best version found is, on a Linux system).</span></span>  <span data-ttu-id="30783-227">**OpenSSL 1.1.1**이 사용 가능한 경우 SslStream 및 HttpClient 형식은 클라이언트와 서버가 둘 다 **TLS 1.3**을 지원할 경우 `SslProtocols.None`(시스템 기본 프로토콜)을 사용할 때 **TLS 1.3**을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-227">When **OpenSSL 1.1.1** is available the SslStream and HttpClient types will use **TLS 1.3** when using `SslProtocols.None` (system default protocols), assuming both the client and server support **TLS 1.3**.</span></span>

<span data-ttu-id="30783-228">다음 샘플은 <https://www.cloudflare.com>에 연결하는 Ubuntu 18.10의 .NET Core 3.0 Preview 1을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30783-228">The following sample demonstrates .NET Core 3.0 Preview 1 on Ubuntu 18.10 connecting to <https://www.cloudflare.com>:</span></span>

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
><span data-ttu-id="30783-229">Windows 및 macOS에서는 아직 **TLS 1.3**을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-229">Windows and macOS do not yet support **TLS 1.3**.</span></span> <span data-ttu-id="30783-230">지원이 제공되면 .NET Core 3.0은 이러한 운영 체제에서 **TLS 1.3**을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-230">.NET Core 3.0 will support **TLS 1.3** on these operating systems when support becomes available.</span></span>

## <a name="cryptography"></a><span data-ttu-id="30783-231">암호화</span><span class="sxs-lookup"><span data-stu-id="30783-231">Cryptography</span></span>

<span data-ttu-id="30783-232">`System.Security.Cryptography.AesGcm` 및 `System.Security.Cryptography.AesCcm`을 통해 구현된 **AES-GCM** 및 **AES-CCM** 암호에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-232">Support has been added for **AES-GCM** and **AES-CCM** ciphers, implemented via `System.Security.Cryptography.AesGcm` and `System.Security.Cryptography.AesCcm`.</span></span> <span data-ttu-id="30783-233">이러한 알고리즘은 [AEAD(연결 데이터를 사용한 인증된 암호화) 알고리즘](https://en.wikipedia.org/wiki/Authenticated_encryption)이자, .NET Core에 추가된 최초의 AE(인증된 암호화) 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-233">These algorithms are both [Authenticated Encryption with Association Data (AEAD) algorithms](https://en.wikipedia.org/wiki/Authenticated_encryption), and the first Authenticated Encryption (AE) algorithms added to .NET Core.</span></span>

<span data-ttu-id="30783-234">다음 코드는 **AesGcm** 암호를 사용하여 임의 데이터를 암호화하고 암호를 해독하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30783-234">The following code demonstrates using **AesGcm** cipher to encrypt and decrypt random data.</span></span>

<span data-ttu-id="30783-235">**AesCcm**에 대한 코드는 거의 동일하게 표시됩니다(클래스 변수 이름만 다름)</span><span class="sxs-lookup"><span data-stu-id="30783-235">The code for **AesCcm** would look almost identical (only the class variable names would be different).</span></span>

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a><span data-ttu-id="30783-236">암호화 키 가져오기/내보내기</span><span class="sxs-lookup"><span data-stu-id="30783-236">Cryptographic Key Import/Export</span></span>

<span data-ttu-id="30783-237">.NET Core 3.0 Preview 1은 X.509 인증서를 사용하지 않고도 표준 형식에서 비대칭 공개 키와 개인 키를 가져오고 내보낼 수 있도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-237">.NET Core 3.0 Preview 1 supports the import and export of asymmetric public and private keys from standard formats, without needing to use an X.509 certificate.</span></span>

<span data-ttu-id="30783-238">모든 키 유형(RSA, DSA, ECDsa, ECDiffieHellman)은 공개 키에 대한 **X.509 SubjectPublicKeyInfo** 형식과 개인 키에 대한 **PKCS#8 PrivateKeyInfo** 및 **PKCS#8 EncryptedPrivateKeyInfo** 형식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-238">All key types (RSA, DSA, ECDsa, ECDiffieHellman) support the **X.509 SubjectPublicKeyInfo** format for public keys, and the **PKCS#8 PrivateKeyInfo** and **PKCS#8 EncryptedPrivateKeyInfo** formats for private keys.</span></span> <span data-ttu-id="30783-239">RSA는 **PKCS#1 RSAPublicKey** 및 **PKCS#1 RSAPrivateKey**를 추가로 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-239">RSA additionally supports **PKCS#1 RSAPublicKey** and **PKCS#1 RSAPrivateKey**.</span></span> <span data-ttu-id="30783-240">내보내기 메서드는 모두 DER로 인코드된 이진 데이터를 생성하고, 가져오기 메서드도 동일한 동작을 예상합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-240">The export methods all produce DER-encoded binary data, and the import methods expect the same.</span></span> <span data-ttu-id="30783-241">키가 텍스트에 편리한 PEM 형식으로 저장된 경우 호출자는 가져오기 메서드를 호출하기 전에 콘텐츠를 base64로 디코드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-241">If a key is stored in the text-friendly PEM format, the caller will need to base64-decode the content before calling an import method.</span></span>

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

<span data-ttu-id="30783-242">PKCS#8 파일은 `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` 클래스를 통해 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-242">PKCS#8 files can be inspected with the `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` class.</span></span>

<span data-ttu-id="30783-243">PFX/PKCS#12 파일은 각각 `System.Security.Cryptography.Pkcs.Pkcs12Info` 및 `System.Security.Cryptography.Pkcs.Pkcs12Builder`를 통해 검사하고 조작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-243">PFX/PKCS#12 files can be inspected and manipulated with `System.Security.Cryptography.Pkcs.Pkcs12Info` and `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectively.</span></span>

## <a name="serialport-for-linux"></a><span data-ttu-id="30783-244">Linux용 SerialPort</span><span class="sxs-lookup"><span data-stu-id="30783-244">SerialPort for Linux</span></span>

<span data-ttu-id="30783-245">.NET Core 3.0은 이제 Linux에서 <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType>을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-245">.NET Core 3.0 now supports <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> on Linux.</span></span>

<span data-ttu-id="30783-246">이전에는 .NET Core가 Windows에서만 `SerialPort` 형식 사용을 지원했습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-246">Previously, .NET Core only supported using the `SerialPort` type on Windows.</span></span>

## <a name="more-bcl-improvements"></a><span data-ttu-id="30783-247">더 많은 BCL 개선 사항</span><span class="sxs-lookup"><span data-stu-id="30783-247">More BCL Improvements</span></span>

<span data-ttu-id="30783-248">.NET Core 2.1에서 도입된 `Span<T>`, `Memory<T>` 및 관련 형식이 .NET Core 3.0에서 최적화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-248">The `Span<T>`, `Memory<T>`, and related types that were introduced in .NET Core 2.1, have been optimized in .NET Core 3.0.</span></span> <span data-ttu-id="30783-249">이제 범위 구성, 조각화, 구문 분석, 서식 지정과 같은 일반적인 작업의 성능이 향상됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-249">Common operations such as span construction, slicing, parsing, and formatting now perform better.</span></span> 

<span data-ttu-id="30783-250">또한 `String` 등의 형식이 내부적으로 개선되어, `Dictionary<TKey, TValue>` 및 기타 컬렉션에서 키로 사용할 때 보다 효율적으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="30783-250">Additionally, types like `String` have seen under-the-cover improvements to make them more efficient when used as keys with `Dictionary<TKey, TValue>` and other collections.</span></span> <span data-ttu-id="30783-251">코드 변경 없이도 이러한 개선 사항을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-251">No code changes are required to benefit from these improvements.</span></span>

<span data-ttu-id="30783-252">또한 다음 개선 사항이 .NET Core 3 Preview 1에서 새로 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-252">The following improvements are also new in .NET Core 3 Preview 1:</span></span>

* <span data-ttu-id="30783-253">HttpClient에 기본 제공되는 Brotli 지원</span><span class="sxs-lookup"><span data-stu-id="30783-253">Brotli support built in to HttpClient</span></span>
* <span data-ttu-id="30783-254">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span><span class="sxs-lookup"><span data-stu-id="30783-254">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span></span>
* <span data-ttu-id="30783-255">Unsafe.Unbox</span><span class="sxs-lookup"><span data-stu-id="30783-255">Unsafe.Unbox</span></span>
* <span data-ttu-id="30783-256">CancellationToken.Unregister</span><span class="sxs-lookup"><span data-stu-id="30783-256">CancellationToken.Unregister</span></span>
* <span data-ttu-id="30783-257">복합 산술 연산자</span><span class="sxs-lookup"><span data-stu-id="30783-257">Complex arithmetic operators</span></span>
* <span data-ttu-id="30783-258">TCP 연결 유지용 소켓 API</span><span class="sxs-lookup"><span data-stu-id="30783-258">Socket APIs for TCP keep alive</span></span>
* <span data-ttu-id="30783-259">StringBuilder.GetChunks</span><span class="sxs-lookup"><span data-stu-id="30783-259">StringBuilder.GetChunks</span></span>
* <span data-ttu-id="30783-260">IPEndPoint 구문 분석</span><span class="sxs-lookup"><span data-stu-id="30783-260">IPEndPoint parsing</span></span>
* <span data-ttu-id="30783-261">RandomNumberGenerator.GetInt32</span><span class="sxs-lookup"><span data-stu-id="30783-261">RandomNumberGenerator.GetInt32</span></span>

## <a name="tiered-compilation"></a><span data-ttu-id="30783-262">계층화된 컴파일</span><span class="sxs-lookup"><span data-stu-id="30783-262">Tiered compilation</span></span>

<span data-ttu-id="30783-263">[계층화된 컴파일](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/)은 .NET Core 3.0에서 기본적으로 켜져 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-263">[Tiered compilation](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/) is on by default with .NET Core 3.0.</span></span> <span data-ttu-id="30783-264">런타임 시 JIT(Just-In-Time) 컴파일러를 보다 유연하게 사용해서 시작 시 성능과 처리량 극대화를 위한 성능을 둘 다 개선할 수 있도록 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="30783-264">It is a feature that enables the runtime to more adaptively use the Just-In-Time (JIT) compiler to get better performance, both at startup and to maximize throughput.</span></span>

<span data-ttu-id="30783-265">이 기능은 [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/)에서 옵트인 기능으로 추가되었으며, [.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/)에서 기본적으로 사용할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-265">This feature was added as an opt-in feature in [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) and then was enabled by default in [.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/).</span></span> <span data-ttu-id="30783-266">이후에 .NET Core 2.2 릴리스에서 다시 옵트인으로 되돌려졌습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-266">Subsequently, it has been reverted back to opt in with the .NET Core 2.2 release.</span></span>

## <a name="arm64-linux-support"></a><span data-ttu-id="30783-267">ARM64 Linux 지원</span><span class="sxs-lookup"><span data-stu-id="30783-267">ARM64 Linux support</span></span>

<span data-ttu-id="30783-268">이 릴리스에서는 Linux에 대한 ARM64 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-268">We are adding support for ARM64 for Linux this release.</span></span> <span data-ttu-id="30783-269">컨텍스트를 위해 .NET Core 2.1에서 Linux에 대한 ARM32 지원이 추가되었고, .NET Core 2.2에서 Windows에 대한 ARM32 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-269">For context, we added support for ARM32 for Linux with .NET Core 2.1 and Windows with .NET Core 2.2.</span></span> <span data-ttu-id="30783-270">ARM64는 현재 IoT 시나리오에서 주로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="30783-270">The primary use case for ARM64 is currently with IoT scenarios.</span></span>

<span data-ttu-id="30783-271">Alpine, Debian 및 Ubuntu [Docker 이미지를 ARM64용 .NET Core에 사용할 수 있습니다](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="30783-271">Alpine, Debian and Ubuntu [Docker images are available for .NET Core for ARM64](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

<span data-ttu-id="30783-272">자세한 내용은 [.NET Core ARM64 상태](https://github.com/dotnet/announcements/issues/82)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30783-272">Please check [.NET Core ARM64 Status](https://github.com/dotnet/announcements/issues/82) for more information.</span></span>

>[!NOTE]
> <span data-ttu-id="30783-273">**ARM64** Windows 지원은 아직 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="30783-273">**ARM64** Windows support isn't yet available.</span></span>
