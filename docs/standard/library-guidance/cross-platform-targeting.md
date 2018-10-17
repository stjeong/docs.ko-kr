---
title: 크로스 플랫폼 대상 지정
description: 플랫폼 간.NET 라이브러리를 만들기 위한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 72fa891d5b1054af485a98d89b4efb11d6b0018b
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374895"
---
# <a name="cross-platform-targeting"></a><span data-ttu-id="7e3e9-103">크로스 플랫폼 대상 지정</span><span class="sxs-lookup"><span data-stu-id="7e3e9-103">Cross-platform targeting</span></span>

<span data-ttu-id="7e3e9-104">최신.NET 여러 운영 체제 및 장치를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-104">Modern .NET supports multiple operating systems and devices.</span></span> <span data-ttu-id="7e3e9-105">Azure 또는 Unity에서.NET 게임에 호스트 된 ASP.NET 웹 사이트를 구축 하면서 여부 것 최대한 많은 개발자를 지원 하도록.NET 오픈 소스 라이브러리에 대 한 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-105">It's important for .NET open-source libraries to support as many developers as possible, whether they're building an ASP.NET website hosted in Azure, or a .NET game in Unity.</span></span>

## <a name="net-standard"></a><span data-ttu-id="7e3e9-106">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="7e3e9-106">.NET Standard</span></span>

<span data-ttu-id="7e3e9-107">.NET standard는 가장 좋은 방법은.NET 라이브러리에 플랫폼 간 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-107">.NET Standard is the best way to add cross-platform support to a .NET library.</span></span> <span data-ttu-id="7e3e9-108">[.NET standard](../net-standard.md) 은 모든.NET 구현에서 사용할 수 있는.NET Api 사양입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-108">[.NET Standard](../net-standard.md) is a specification of .NET APIs that are available on all .NET implementations.</span></span> <span data-ttu-id="7e3e9-109">.NET 표준을 대상으로 하는 지정된 된 버전의.NET Standard,.NET Standard의 해당 버전을 구현 하는 모든 플랫폼에서 사용할 수 있는 것을 의미 하는 Api 사용으로 제한 되는 라이브러리를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-109">Targeting .NET Standard lets you produce libraries that are constrained to use APIs that are in a given version of .NET Standard, which means it's usable by all platforms that implement that version of the .NET Standard.</span></span>

<span data-ttu-id="7e3e9-110">![.NET standard](./media/cross-platform-targeting/platforms-netstandard.png ".NET Standard")</span><span class="sxs-lookup"><span data-stu-id="7e3e9-110">![.NET Standard](./media/cross-platform-targeting/platforms-netstandard.png ".NET Standard")</span></span>

<span data-ttu-id="7e3e9-111">.NET 표준을 대상으로 하 고 프로젝트를 컴파일 했습니다. 모든 플랫폼에서 라이브러리를 성공적으로 실행을 보장 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-111">Targeting .NET Standard, and successfully compiling your project, doesn't guarantee the library will run successfully on all platforms:</span></span>

1. <span data-ttu-id="7e3e9-112">다른 플랫폼에서 플랫폼별 Api 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-112">Platform-specific APIs will fail on other platforms.</span></span> <span data-ttu-id="7e3e9-113">예를 들어 <xref:Microsoft.Win32.Registry?displayProperty=nameWithType> Windows에서 성공 하며 throw <xref:System.PlatformNotSupportedException> 모든 다른 OS에서 사용 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-113">For example, <xref:Microsoft.Win32.Registry?displayProperty=nameWithType> will succeed on Windows and throw <xref:System.PlatformNotSupportedException> when used on any other OS.</span></span>
2. <span data-ttu-id="7e3e9-114">Api는 다르게 동작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-114">APIs can behave differently.</span></span> <span data-ttu-id="7e3e9-115">예를 들어, 리플렉션 Api 성능 특성이 달라 iOS 또는 UWP 응용 프로그램에서 미리 컴파일 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-115">For example, reflection APIs have different performance characteristics when an application uses ahead-of-time compilation on iOS or UWP.</span></span>

> [!TIP]
> <span data-ttu-id="7e3e9-116">.NET 팀 [Roslyn 분석기 제공](../analyzers/api-analyzer.md) 가능한 문제를 검색할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-116">The .NET team [offers a Roslyn analyzer](../analyzers/api-analyzer.md) to help you discover possible issues.</span></span>

<span data-ttu-id="7e3e9-117">**✔️ 마십시오** 포함 하 여 시작을 `netstandard2.0` 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-117">**✔️ DO** start with including a `netstandard2.0` target.</span></span>

> <span data-ttu-id="7e3e9-118">가장 하는 범용 라이브러리는.NET Standard 2.0 외부 Api 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-118">Most general-purpose libraries should not need APIs outside of .NET Standard 2.0.</span></span> <span data-ttu-id="7e3e9-119">.NET standard 2.0은 모든 최신 플랫폼에서 지원 되며 하나의 대상 사용 하 여 여러 플랫폼을 지원할 수 있는 좋은 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-119">.NET Standard 2.0 is supported by all modern platforms and is the recommended way to support multiple platforms with one target.</span></span>

<span data-ttu-id="7e3e9-120">**❌ 하지 말고** 등을 `netstandard1.x` 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-120">**❌ AVOID** including a `netstandard1.x` target.</span></span>

> <span data-ttu-id="7e3e9-121">.NET 표준 1.x 대용량 패키지가 종속성 그래프를 만들고 빌드할 때 많은 패키지를 다운로드 하는 개발자가 발생 하는 세분화 된 NuGet 패키지 집합으로 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-121">.NET Standard 1.x is distributed as a granular set of NuGet packages, which creates a large package dependency graph and results in developers downloading a lot of packages when building.</span></span> <span data-ttu-id="7e3e9-122">최신.NET 플랫폼,.NET Framework 4.6.1, UWP 및 Xamarin을 비롯 한 모든.NET Standard 2.0 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-122">Modern .NET platforms, including .NET Framework 4.6.1, UWP and Xamarin, all support .NET Standard 2.0.</span></span> <span data-ttu-id="7e3e9-123">만 두어야.NET 표준 1.x 특히 이전 플랫폼을 대상으로 해야 할 경우.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-123">You should only target .NET Standard 1.x if you specifically need to target an older platform.</span></span>

<span data-ttu-id="7e3e9-124">**✔️ 수행** 포함을 `netstandard2.0` 대상으로 해야 하는 경우는 `netstandard1.x` 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-124">**✔️ DO** include a `netstandard2.0` target if you require a `netstandard1.x` target.</span></span>

> <span data-ttu-id="7e3e9-125">사용 하 여.NET Standard 2.0을 지 원하는 모든 플랫폼의 `netstandard2.0` 대상과 이전 플랫폼도 작동 되며 사용 하도록 대체 하는 동안 패키지 그래프를 더 작은 것의 이점을 `netstandard1.x` 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-125">All platforms supporting .NET Standard 2.0 will use the `netstandard2.0` target and benefit from having a smaller package graph while older platforms will still work and fall back to using the `netstandard1.x` target.</span></span>

<span data-ttu-id="7e3e9-126">**❌ 하지** 라이브러리는 플랫폼별 앱 모델에 의존 하는 경우.NET 표준 대상을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-126">**❌ DO NOT** include a .NET Standard target if the library relies on a platform-specific app model.</span></span>

> <span data-ttu-id="7e3e9-127">예를 들어 UWP 컨트롤 도구 키트 라이브러리 에서만 UWP에서 사용할 수 있는 앱 모델에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-127">For example, a UWP control toolkit library depends on an app model that is only available on UWP.</span></span> <span data-ttu-id="7e3e9-128">앱 모델 관련 Api는.NET Standard에서 사용할 수 있는 하지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-128">App model specific APIs will not be available in .NET Standard.</span></span>

## <a name="multi-targeting"></a><span data-ttu-id="7e3e9-129">멀티 타기팅</span><span class="sxs-lookup"><span data-stu-id="7e3e9-129">Multi-targeting</span></span>

<span data-ttu-id="7e3e9-130">라이브러리에서 프레임 워크 관련 Api에 액세스 해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-130">Sometimes you need to access framework-specific APIs from your libraries.</span></span> <span data-ttu-id="7e3e9-131">프레임 워크별 Api를 호출 하는 가장 좋은 방법은 멀티 타기 팅 많은 프로젝트를 빌드하는 사용 하는 [.NET 대상 프레임 워크](../frameworks.md) 아닌 하나만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-131">The best way to call framework-specific APIs is using multi-targeting, which builds your project for many [.NET target frameworks](../frameworks.md) rather than for just one.</span></span>

<span data-ttu-id="7e3e9-132">개별 프레임 워크에 대해 작성할 필요가 소비자를 보호 하에 대 한.NET 표준 출력 물론 하나 이상의 프레임 워크별 출력 하도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-132">To shield your consumers from having to build for individual frameworks, you should strive to have a .NET Standard output plus one or more framework-specific outputs.</span></span> <span data-ttu-id="7e3e9-133">멀티 타기 팅을 사용 하 여 모든 어셈블리는 단일 NuGet 패키지 내에서 패키지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-133">With multi-targeting, all assemblies are packaged inside a single NuGet package.</span></span> <span data-ttu-id="7e3e9-134">소비자는 동일한 패키지를 참조할 수 있습니다 및 NuGet은 적절 한 구현을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-134">Consumers can then reference the same package and NuGet will pick the appropriate implementation.</span></span> <span data-ttu-id="7e3e9-135">.NET Standard 라이브러리는 NuGet 패키지는 프레임 워크별 구현을 제공 하는 있는 경우를 제외한 모든 범위는 대체 (fallback) 라이브러리 사용에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-135">Your .NET Standard library serves as the fallback library that is used everywhere, except for the cases where your NuGet package offers a framework-specific implementation.</span></span> <span data-ttu-id="7e3e9-136">멀티 타기 팅 코드의 조건부 컴파일을 사용 및 프레임 워크별 Api를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-136">Multi-targeting allows you to use conditional compilation in your code and call framework-specific APIs.</span></span>

<span data-ttu-id="7e3e9-137">![여러 어셈블리를 사용 하 여 NuGet 패키지](./media/cross-platform-targeting/nuget-package-multiple-assemblies.png "여러 어셈블리를 사용 하 여 NuGet 패키지")</span><span class="sxs-lookup"><span data-stu-id="7e3e9-137">![NuGet package with multiple assemblies](./media/cross-platform-targeting/nuget-package-multiple-assemblies.png "NuGet package with multiple assemblies")</span></span>

<span data-ttu-id="7e3e9-138">**✔️ 하십시오** .NET 구현 외에도.NET Standard를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-138">**✔️ CONSIDER** targeting .NET implementations in addition to .NET Standard.</span></span>

> <span data-ttu-id="7e3e9-139">.NET 구현을 대상으로.NET Standard 외부에 있는 플랫폼 특정 Api를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-139">Targeting .NET implementations allows you to call platform-specific APIs that are outside of .NET Standard.</span></span>
>
> <span data-ttu-id="7e3e9-140">이렇게 하면.NET Standard에 대 한 지원을 삭제 안 함.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-140">Do not drop support for .NET Standard when you do this.</span></span> <span data-ttu-id="7e3e9-141">대신, 구현에서 throw 하 고 Api 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-141">Instead, throw from the implementation and offer capability APIs.</span></span> <span data-ttu-id="7e3e9-142">이 이렇게 하면 라이브러리 어디서 나 사용할 수 고 기능의 런타임 강화를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-142">This way, your library can be used anywhere and supports runtime light-up of features.</span></span>

<span data-ttu-id="7e3e9-143">**❌ 하지 말고** 멀티 타기 팅.NET Standard를 사용 하 여 모든 대상에 대 한 소스 코드 같으면 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-143">**❌ AVOID** using multi-targeting with .NET Standard if your source code is the same for all targets.</span></span>

> <span data-ttu-id="7e3e9-144">어셈블리를.NET Standard NuGet에서 자동으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-144">The .NET Standard assembly will automatically be used by NuGet.</span></span> <span data-ttu-id="7e3e9-145">증가 개별.NET 구현을 대상으로 하는 `*.nupkg` 아무 이점 없이 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-145">Targeting individual .NET implementations increases the `*.nupkg` size for no benefit.</span></span>

<span data-ttu-id="7e3e9-146">**✔️ 것이 좋습니다** 에 대 한 대상을 추가 `net461` 제공 하는 경우는 `netstandard2.0` 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-146">**✔️ CONSIDER** adding a target for `net461` when you're offering a `netstandard2.0` target.</span></span> 

> <span data-ttu-id="7e3e9-147">.NET Framework에서.NET Standard 2.0을 사용 하 여.NET Framework 4.7.2에서에서 처리 된 몇 가지 문제에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-147">Using .NET Standard 2.0 from .NET Framework has some issues that were addressed in .NET Framework 4.7.2.</span></span> <span data-ttu-id="7e3e9-148">.NET Framework 4.6.1-.NET Framework 4.6.1에 대 한 기본 제공 되는 이진을 제공 하 여 4.7.1에는 개발자를 위한 환경을 개선할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-148">You can improve the experience for developers that are still on .NET Framework 4.6.1 - 4.7.1 by offering them a binary that is built for .NET Framework 4.6.1.</span></span>

<span data-ttu-id="7e3e9-149">**✔️ 수행** NuGet 패키지를 사용 하 여 라이브러리를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-149">**✔️ DO** distribute your library using a NuGet package.</span></span>

> <span data-ttu-id="7e3e9-150">NuGet는 개발자를 위한 최상의 대상을 선택 하 고 적절 한 구현을 선택 하지 않아도 해당 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-150">NuGet will select the best target for the developer and shield them having to pick the appropriate implementation.</span></span>

<span data-ttu-id="7e3e9-151">**✔️ 수행** 프로젝트 파일을 사용 하 여 `TargetFrameworks` 멀티 타기 팅 하는 경우에 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-151">**✔️ DO** use a project file's `TargetFrameworks` property when multi-targeting.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <!-- This project will output netstandard2.0 and net461 assemblies -->
    <TargetFrameworks>netstandard2.0;net461</TargetFrameworks>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="7e3e9-152">**✔️ 것이 좋습니다** 를 사용 하 여 [MSBuild.Sdk.Extras](https://github.com/onovotny/MSBuildSdkExtras) 멀티 타기 팅 시 UWP 및 Xamarin에 대 한 프로젝트 파일을 크게 단순화 하므로 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-152">**✔️ CONSIDER** using [MSBuild.Sdk.Extras](https://github.com/onovotny/MSBuildSdkExtras) when multi-targeting for UWP and Xamarin as it greatly simplifies your project file.</span></span>

## <a name="older-targets"></a><span data-ttu-id="7e3e9-153">이전 대상</span><span class="sxs-lookup"><span data-stu-id="7e3e9-153">Older targets</span></span>

<span data-ttu-id="7e3e9-154">.NET 지원 뿐만 아니라 일반적으로 더 이상 사용 되는 플랫폼에서 오래 된 버전의.NET Framework 타기 팅을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-154">.NET supports targeting versions of the .NET Framework that are long out of support as well as platforms that are no longer commonly used.</span></span> <span data-ttu-id="7e3e9-155">값을 만드는 라이브러리 작업에 추가할 수 없습니다. Api 해결할 필요가 최대한 많은 대상으로 상당한 오버 헤드가 있습니다 하지만.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-155">While there's value in making your library work on as many targets as possible, having to work around missing APIs can add significant overhead.</span></span> <span data-ttu-id="7e3e9-156">믿습니다 특정 프레임 워크는 더 이상 대상 가치가 범위와 제한 사항을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-156">We believe certain frameworks are no longer worth targeting, considering their reach and limitations.</span></span>

<span data-ttu-id="7e3e9-157">**❌ 하지** 이식 가능한 클래스 라이브러리 (PCL) 대상을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-157">**❌ DO NOT** include a Portable Class Library (PCL) target.</span></span> <span data-ttu-id="7e3e9-158">예를 들어, `portable-net45+win8+wpa81+wp8`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-158">For example, `portable-net45+win8+wpa81+wp8`.</span></span>

> <span data-ttu-id="7e3e9-159">.NET standard는 최신 플랫폼 간.NET 라이브러리를 지 원하는 방법 및 Pcl을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-159">.NET Standard is the modern way to support cross-platform .NET libraries and replaces PCLs.</span></span>

<span data-ttu-id="7e3e9-160">**❌ 하지** 더 이상 지원 되지 않는.NET 플랫폼에 대 한 목표를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3e9-160">**❌ DO NOT** include targets for .NET platforms that are no longer supported.</span></span> <span data-ttu-id="7e3e9-161">예: `SL4`, `WP`</span><span class="sxs-lookup"><span data-stu-id="7e3e9-161">For example, `SL4`, `WP`.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="7e3e9-162">[이전](./get-started.md)
[다음](./strong-naming.md)</span><span class="sxs-lookup"><span data-stu-id="7e3e9-162">[Previous](./get-started.md)
[Next](./strong-naming.md)</span></span>
