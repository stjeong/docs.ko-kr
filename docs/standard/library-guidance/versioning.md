---
title: 버전 관리 및 .NET 라이브러리
description: .NET 라이브러리의 버전을 관리하는 모범 사례 권장 사항입니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: f95c8ade1f91af5c13184b839b327c9397c6fe5a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50187860"
---
# <a name="versioning"></a><span data-ttu-id="030b7-103">버전 관리</span><span class="sxs-lookup"><span data-stu-id="030b7-103">Versioning</span></span>

<span data-ttu-id="030b7-104">소프트웨어 라이브러리가 버전 1.0에서 완성되는 경우는 거의 없습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-104">A software library is rarely complete in version 1.0.</span></span> <span data-ttu-id="030b7-105">훌륭한 라이브러리는 시간이 지남에 따라 발전하며, 기능을 추가하고, 버그를 수정하고, 성능을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-105">Good libraries evolve over time, adding features, fixing bugs and improving performance.</span></span> <span data-ttu-id="030b7-106">기존 사용자를 중단하지 않고 각 버전에서 추가 가치를 제공하여 .NET 라이브러리의 새 버전을 릴리스하는 것이 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-106">It is important that you can release new versions of a .NET library, providing additional value with each version, without breaking existing users.</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="030b7-107">호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="030b7-107">Breaking changes</span></span>

<span data-ttu-id="030b7-108">버전 간의 호환성이 손상되는 변경 처리에 대한 자세한 내용은 [호환성이 손상되는 변경](./breaking-changes.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="030b7-108">For information about handling breaking changes between versions, see [Breaking changes](./breaking-changes.md).</span></span>

## <a name="version-numbers"></a><span data-ttu-id="030b7-109">버전 번호</span><span class="sxs-lookup"><span data-stu-id="030b7-109">Version numbers</span></span>

<span data-ttu-id="030b7-110">.NET 라이브러리에는 버전을 지정하는 여러 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-110">A .NET library has many ways to specify a version.</span></span> <span data-ttu-id="030b7-111">가장 중요한 버전은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-111">These versions are the most important:</span></span>

### <a name="nuget-package-version"></a><span data-ttu-id="030b7-112">NuGet 패키지 버전</span><span class="sxs-lookup"><span data-stu-id="030b7-112">NuGet package version</span></span>

<span data-ttu-id="030b7-113">[NuGet 패키지 버전](/nuget/reference/package-versioning)은 Visual Studio NuGet 패키지 관리자인 NuGet.org에 표시되고 패키지를 사용할 때 소스 코드에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-113">The [NuGet package version](/nuget/reference/package-versioning) is displayed on NuGet.org, the Visual Studio NuGet package manager, and is added to source code when the package is used.</span></span> <span data-ttu-id="030b7-114">NuGet 패키지 버전은 사용자에게 일반적으로 표시되는 버전 번호이며, 사용 중인 라이브러리 버전을 말할 때는 이 버전을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-114">The NuGet package version is the version number users will commonly see, and they'll refer to it when they talk about the version of a library they're using.</span></span> <span data-ttu-id="030b7-115">NuGet 패키지 버전은 NuGet에서 사용되며 런타임 동작에는 영향을 미치지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-115">The NuGet package version is used by NuGet and has no effect on runtime behavior.</span></span>

```xml
<PackageVersion>1.0.0-alpha1</PackageVersion>
```

<span data-ttu-id="030b7-116">NuGet 패키지 식별자와 NuGet 패키지 버전을 결합하여 NuGet에서 패키지를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-116">The NuGet package identifier combined with the NuGet package version is used to identify a package in NuGet.</span></span> <span data-ttu-id="030b7-117">예: `Newtonsoft.Json` + `11.0.2`.</span><span class="sxs-lookup"><span data-stu-id="030b7-117">For example, `Newtonsoft.Json` + `11.0.2`.</span></span> <span data-ttu-id="030b7-118">접미사가 있는 패키지는 시험판 패키지이며, 테스트에 적합하게 하는 특수 동작이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-118">A package with a suffix is a pre-release package and has special behavior that makes it ideal for testing.</span></span> <span data-ttu-id="030b7-119">자세한 내용은 [시험판 패키지](./nuget.md#pre-release-packages)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="030b7-119">For more information, see [Pre-release packages](./nuget.md#pre-release-packages).</span></span>

<span data-ttu-id="030b7-120">NuGet 패키지 버전은 개발자가 가장 보기 쉬운 버전이므로 [SemVer(유의적 버전)](https://semver.org/)를 사용하여 업데이트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-120">Because the NuGet package version is the most visible version to developers, it's a good idea to update it using [Semantic Versioning (SemVer)](https://semver.org/).</span></span> <span data-ttu-id="030b7-121">SemVer는 릴리스 간 변경 내용의 중요도를 나타내며, 개발자가 사용할 버전을 선택할 때 정확하고 합리적으로 결정할 수 있도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-121">SemVer indicates the significance of changes between release and helps developers make an informed decision when choosing what version to use.</span></span> <span data-ttu-id="030b7-122">예를 들어 `1.0`에서 `2.0`으로 이동하는 경우 호환성이 손상되는 변경이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-122">For example, going from `1.0` to `2.0` indicates that there are potentially breaking changes.</span></span>

<span data-ttu-id="030b7-123">**✔️ 고려** [SemVer 2.0.0](https://semver.org/)을 사용하여 NuGet 패키지 버전을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-123">**✔️ CONSIDER** using [SemVer 2.0.0](https://semver.org/) to version your NuGet package.</span></span>

<span data-ttu-id="030b7-124">**✔️** 사용자에게 일반적으로 표시되는 버전 번호인 NuGet 패키지 버전을 공용 문서에서 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-124">**✔️ DO** use the NuGet package version in public documentation as it's the version number that users will commonly see.</span></span>

<span data-ttu-id="030b7-125">**✔️** 불안정한 패키지를 릴리스할 때는 시험판 접미사를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-125">**✔️ DO** include a pre-release suffix when releasing a non-stable package.</span></span>

> <span data-ttu-id="030b7-126">사용자는 시험판 패키지를 가져오기 위해 옵트인해야 하므로 패키지가 불완전함을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-126">Users must opt in to getting pre-release packages, so they will understand that the package is not complete.</span></span>

### <a name="assembly-version"></a><span data-ttu-id="030b7-127">어셈블리 버전</span><span class="sxs-lookup"><span data-stu-id="030b7-127">Assembly version</span></span>

<span data-ttu-id="030b7-128">어셈블리 버전은 CLR에서 런타임 시 로드할 어셈블리 버전을 선택하는 데 사용하는 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-128">The assembly version is what the CLR uses at runtime to select which version of an assembly to load.</span></span> <span data-ttu-id="030b7-129">버전 관리를 사용한 어셈블리 선택은 강력한 이름의 어셈블리에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-129">Selecting an assembly using versioning only applies to assemblies with a strong name.</span></span>

```xml
<AssemblyVersion>1.0.0.0</AssemblyVersion>
```

<span data-ttu-id="030b7-130">Windows .NET Framework CLR에서는 정확히 일치해야 강력한 이름의 어셈블리를 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-130">The Windows .NET Framework CLR demands an exact match to load a strong named assembly.</span></span> <span data-ttu-id="030b7-131">예를 들어 `Libary1, Version=1.0.0.0`은 `Newtonsoft.Json, Version=11.0.0.0`을 참조하여 컴파일되었습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-131">For example, `Libary1, Version=1.0.0.0` was compiled with a reference to `Newtonsoft.Json, Version=11.0.0.0`.</span></span> <span data-ttu-id="030b7-132">.NET Framework는 정확한 버전인 `11.0.0.0`만 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-132">The .NET Framework will only load that exact version `11.0.0.0`.</span></span> <span data-ttu-id="030b7-133">런타임 시 다른 버전을 로드하려면 .NET 응용 프로그램의 구성 파일에 바인딩 리디렉션을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-133">To load a different version at runtime, a binding redirect must be added to the .NET application's config file.</span></span>

<span data-ttu-id="030b7-134">강력한 이름 지정과 어셈블리 버전을 결합하면 [엄격한 어셈블리 버전 로드](../../framework/app-domains/assembly-versioning.md)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-134">Strong naming combined with assembly version enables [strict assembly version loading](../../framework/app-domains/assembly-versioning.md).</span></span> <span data-ttu-id="030b7-135">라이브러리에 강력한 이름을 지정하면 여러 가지 혜택이 있지만, 어셈블리를 찾을 수 없는 런타임 예외가 자주 발생하며 `app.config`/`web.config`의 [바인딩 리디렉션](../../framework/configure-apps/redirect-assembly-versions.md)을 수정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-135">While strong naming a library has a number of benefits, it often results in runtime exceptions that an assembly can't be found and [requires binding redirects](../../framework/configure-apps/redirect-assembly-versions.md) in `app.config`/`web.config` to be fixed.</span></span> <span data-ttu-id="030b7-136">.NET Core 어셈블리 로드가 완화되었으며, .NET Core CLR이 런타임에 상위 버전의 어셈블리를 자동으로 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-136">.NET Core assembly loading has been relaxed, and the .NET Core CLR will automatically load assemblies at runtime with a higher version.</span></span>

<span data-ttu-id="030b7-137">**✔️** AssemblyVersion에 주 버전만 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-137">**✔️ CONSIDER** only including a major version in the AssemblyVersion.</span></span>

> <span data-ttu-id="030b7-138">예: 라이브러리 1.0 및 라이브러리 1.0.1의 AssemblyVersion은 둘 다 `1.0.0.0`인 반면, 라이브러리 2.0의 AssemblyVersion은 `2.0.0.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-138">e.g. Library 1.0 and Library 1.0.1 both have an AssemblyVersion of `1.0.0.0`, while Library 2.0 has AssemblyVersion of `2.0.0.0`.</span></span> <span data-ttu-id="030b7-139">어셈블리 버전의 변경 빈도가 낮으면 바인딩 리디렉션이 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-139">When the assembly version changes less often, it reduces binding redirects.</span></span>

<span data-ttu-id="030b7-140">**✔️** AssemblyVersion의 주 버전 번호와 NuGet 패키지 버전을 동기화 상태로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-140">**✔️ CONSIDER** keeping the major version number of the AssemblyVersion and the NuGet package version in sync.</span></span>

> <span data-ttu-id="030b7-141">AssemblyVersion은 사용자에게 표시되는 일부 정보 메시지(예: 예외 메시지의 어셈블리 이름 및 어셈블리 한정 형식 이름)에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-141">The AssemblyVersion is included in some informational messages displayed to the user, e.g. the assembly name and assembly qualified type names in exception messages.</span></span> <span data-ttu-id="030b7-142">버전 간의 관계를 유지 관리하면 사용 중인 버전에 대한 자세한 정보가 개발자에게 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-142">Maintaining a relationship between the versions provides more information to developers about which version they are using.</span></span>

<span data-ttu-id="030b7-143">**❌** 고정된 AssemblyVersion을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-143">**❌ DO NOT** have a fixed AssemblyVersion.</span></span>

> <span data-ttu-id="030b7-144">AssemblyVersion이 변경되지 않는 경우 바인딩 리디렉션이 필요하지 않지만, 단일 어셈블리 버전만 GAC(전역 어셈블리 캐시)에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-144">While an unchanging AssemblyVersion avoids the need for binding redirects, it means that only a single version of the assembly can be installed in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="030b7-145">또한 다른 응용 프로그램이 GAC 어셈블리를 호환성이 손상되는 변경으로 업데이트하는 경우 GAC에 있는 어셈블리를 참조하는 응용 프로그램이 손상됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-145">Also, the applications that reference the assembly in the GAC will break if another application updates the GAC assembly with breaking changes.</span></span>

### <a name="assembly-file-version"></a><span data-ttu-id="030b7-146">어셈블리 파일 버전</span><span class="sxs-lookup"><span data-stu-id="030b7-146">Assembly file version</span></span>

<span data-ttu-id="030b7-147">어셈블리 파일 버전은 Windows에서 파일 버전을 표시하는 데 사용되며 런타임 동작에는 영향을 미치지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-147">The assembly file version is used to display a file version in Windows and has no effect on runtime behavior.</span></span> <span data-ttu-id="030b7-148">이 버전 설정은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-148">Setting this version is optional.</span></span> <span data-ttu-id="030b7-149">Windows 탐색기의 파일 속성 대화 상자에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-149">It's visible in the File Properties dialog in Windows Explorer:</span></span>

```xml
<FileVersion>11.0.2.21924</FileVersion>
```

<span data-ttu-id="030b7-150">![Windows 탐색기](./media/versioning/win-properties.png "Windows 탐색기")</span><span class="sxs-lookup"><span data-stu-id="030b7-150">![Windows Explorer](./media/versioning/win-properties.png "Windows Explorer")</span></span>

> [!NOTE]
> <span data-ttu-id="030b7-151">이 버전이 `Major.Minor.Build.Revision` 형식을 따르지 않는 경우 무해한 빌드 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-151">An innocuous build warning is raised if this version does not follow the format `Major.Minor.Build.Revision`.</span></span> <span data-ttu-id="030b7-152">경고는 무시해도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-152">The warning can be safely ignored.</span></span>

<span data-ttu-id="030b7-153">**✔️** 연속 통합 빌드 번호를 AssemblyFileVersion 수정으로 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-153">**✔️ CONSIDER** including a continuous integration build number as the AssemblyFileVersion revision.</span></span>

> <span data-ttu-id="030b7-154">예를 들어 프로젝트 버전 1.0.0을 빌드 중이며 연속 통합 빌드 번호가 99인 경우 AssemblyFileVersion은 1.0.0.99입니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-154">For example, you are building version 1.0.0 of your project, and the continuous integration build number is 99 so your AssemblyFileVersion is 1.0.0.99.</span></span>

### <a name="assembly-informational-version"></a><span data-ttu-id="030b7-155">어셈블리 정보 버전</span><span class="sxs-lookup"><span data-stu-id="030b7-155">Assembly informational version</span></span>

<span data-ttu-id="030b7-156">어셈블리 정보 버전은 추가 버전 정보를 기록하는 데 사용되며 런타임 동작에는 영향을 미치지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-156">The assembly informational version is used to record additional version information and has no effect on runtime behavior.</span></span> <span data-ttu-id="030b7-157">이 버전 설정은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-157">Setting this version is optional.</span></span> <span data-ttu-id="030b7-158">SourceLink를 사용하는 경우 이 버전은 NuGet 패키지 버전과 소스 제어 버전을 사용하여 빌드에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-158">If you're using SourceLink, this version will be set on build with the NuGet package version plus a source control version.</span></span> <span data-ttu-id="030b7-159">예를 들어 `1.0.0-beta1+204ff0a`는 어셈블리 빌드에 사용된 소스 코드의 커밋 해시를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-159">For example, `1.0.0-beta1+204ff0a` includes the commit hash of the source code the assembly was built from.</span></span> <span data-ttu-id="030b7-160">자세한 내용은 [SourceLink](./sourcelink.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="030b7-160">For more information, see [SourceLink](./sourcelink.md).</span></span>

```xml
<AssemblyInformationalVersion>The quick brown fox jumped over the lazy dog.</AssemblyInformationalVersion>
```

<span data-ttu-id="030b7-161">**❌** 어셈블리 정보 버전을 직접 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-161">**❌ AVOID** setting the assembly informational version yourself.</span></span>

> <span data-ttu-id="030b7-162">SourceLink에서 NuGet 및 소스 제어 메타데이터가 포함된 버전을 자동으로 생성하도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="030b7-162">Allow SourceLink to automatically generate the version containing NuGet and source control metadata.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="030b7-163">[이전](./publish-nuget-package.md)
[다음](./breaking-changes.md)</span><span class="sxs-lookup"><span data-stu-id="030b7-163">[Previous](./publish-nuget-package.md)
[Next](./breaking-changes.md)</span></span>
