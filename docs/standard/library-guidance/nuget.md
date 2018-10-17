---
title: NuGet 및.NET 라이브러리
description: .NET 라이브러리에 대 한 nuget 패키지에 대 한 권장 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: d0ea462a7f52dd9a6b2f14be9ed5770160bf66b1
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374504"
---
# <a name="nuget"></a><span data-ttu-id="5955f-103">NuGet</span><span class="sxs-lookup"><span data-stu-id="5955f-103">NuGet</span></span>

<span data-ttu-id="5955f-104">NuGet 용.NET 에코 시스템 패키지 관리자 이며 기본 방법은 개발자가 검색 하 고.NET 오픈 소스 라이브러리를 획득 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-104">NuGet is a package manager for the .NET ecosystem and is the primary way developers discover and acquire .NET open-source libraries.</span></span> <span data-ttu-id="5955f-105">[NuGet.org](https://www.nuget.org/)NuGet 패키지를 호스팅하기 위해 Microsoft에서 제공 하는 무료 서비스는 공용 NuGet 패키지에 대 한 기본 호스트 되지만 같은 사용자 지정 NuGet 서비스를 게시할 수 있습니다 [MyGet](https://www.myget.org/) 고 [Azure 아티팩트 ](https://azure.microsoft.com/services/devops/artifacts/).</span><span class="sxs-lookup"><span data-stu-id="5955f-105">[NuGet.org](https://www.nuget.org/), a free service provided by Microsoft for hosting NuGet packages, is the primary host for public NuGet packages, but you can publish to custom NuGet services like [MyGet](https://www.myget.org/) and [Azure Artifacts](https://azure.microsoft.com/services/devops/artifacts/).</span></span>

<span data-ttu-id="5955f-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span><span class="sxs-lookup"><span data-stu-id="5955f-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span></span>

## <a name="create-a-nuget-package"></a><span data-ttu-id="5955f-107">NuGet 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="5955f-107">Create a NuGet package</span></span>

<span data-ttu-id="5955f-108">NuGet 패키지 (`*.nupkg`)은.NET 어셈블리 및 관련된 메타 데이터가 포함 된 zip 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-108">A NuGet package (`*.nupkg`) is a zip file that contains .NET assemblies and associated metadata.</span></span>

<span data-ttu-id="5955f-109">NuGet 패키지를 만드는 두 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-109">There are two main ways to create a NuGet package.</span></span> <span data-ttu-id="5955f-110">최신 및 권장 되는 방식은 SDK 스타일 프로젝트에서 패키지를 만드는 (프로젝트 파일 내용이 시작 `<Project Sdk="Microsoft.NET.Sdk">`).</span><span class="sxs-lookup"><span data-stu-id="5955f-110">The newer and recommended way is to create a package from a SDK-style project (project file whose content starts with `<Project Sdk="Microsoft.NET.Sdk">`).</span></span> <span data-ttu-id="5955f-111">어셈블리 및 대상 패키지에 자동으로 추가 하 고 패키지 이름과 버전 번호와 같은 MSBuild 파일에 추가 됩니다 남은 메타 데이터 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-111">Assemblies and targets are automatically added to the package and remaining metadata is added to the MSBuild file, like package name and version number.</span></span> <span data-ttu-id="5955f-112">사용 하 여 컴파일하는 [ `dotnet pack` ](../../core/tools/dotnet-pack.md) 명령 출력을 `*.nupkg` 어셈블리 대신 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-112">Compiling with the [`dotnet pack`](../../core/tools/dotnet-pack.md) command outputs a `*.nupkg` file instead of assemblies.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFramework>netstandard2.0</TargetFramework>
    <AssemblyName>Contoso.Api</AssemblyName>
    <PackageVersion>1.1.0</PackageVersion>
    <Authors>John Doe</Authors>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="5955f-113">NuGet 패키지 만들기에 대 한 이전 방식의 된를 `*.nuspec` 파일 및 `nuget.exe` 명령줄 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-113">The older way of creating a NuGet package is with a `*.nuspec` file and the `nuget.exe` command-line tool.</span></span> <span data-ttu-id="5955f-114">Nuspec 파일을 유용한 제어를 제공 하지만 어떤 어셈블리 및 대상 최종 NuGet 패키지에 포함 하도록 신중 하 게 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-114">A nuspec file gives you great control but you must carefully specify what assemblies and targets to include in the final NuGet package.</span></span> <span data-ttu-id="5955f-115">실수 하기 쉽습니다 또는 다른 사용자에 게 변경 하는 경우 nuspec을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-115">It's easy to make a mistake or for someone to forget to update the nuspec when making changes.</span></span> <span data-ttu-id="5955f-116">Nuspec 장점은 사용할 수 있습니다 SDK 스타일 프로젝트 파일을 아직 지원 하지 않는 프레임 워크에 대 한 NuGet 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-116">The advantage of a nuspec is you can use it create NuGet packages for frameworks that don't yet support an SDK-style project file.</span></span>

<span data-ttu-id="5955f-117">**✔️ 하십시오** SDK 스타일 프로젝트 파일을 사용 하 여 NuGet 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-117">**✔️ CONSIDER** using an SDK-style project file to create the NuGet package.</span></span>

<span data-ttu-id="5955f-118">**✔️ 하십시오** SourceLink 어셈블리 및 NuGet 패키지에 원본 제어 메타 데이터를 추가 하려면 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-118">**✔️ CONSIDER** setting up SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

## <a name="package-dependencies"></a><span data-ttu-id="5955f-119">패키지 종속성</span><span class="sxs-lookup"><span data-stu-id="5955f-119">Package dependencies</span></span>

<span data-ttu-id="5955f-120">NuGet 패키지 종속성에 자세히 설명 되어는 [종속성](./dependencies.md) 문서.</span><span class="sxs-lookup"><span data-stu-id="5955f-120">NuGet package dependencies are covered in detail in the [Dependencies](./dependencies.md) article.</span></span>

## <a name="important-nuget-package-metadata"></a><span data-ttu-id="5955f-121">중요 한 NuGet 패키지 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="5955f-121">Important NuGet package metadata</span></span>

<span data-ttu-id="5955f-122">NuGet 패키지를 지 원하는 많은 [메타 데이터 속성](/nuget/reference/nuspec)합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-122">A NuGet package supports many [metadata properties](/nuget/reference/nuspec).</span></span> <span data-ttu-id="5955f-123">다음 표에서 모든 오픈 소스 프로젝트를 제공 해야 하는 핵심 메타 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-123">The following table contains the core metadata that every open-source project should provide:</span></span>

| <span data-ttu-id="5955f-124">MSBuild 속성 이름</span><span class="sxs-lookup"><span data-stu-id="5955f-124">MSBuild Property name</span></span>              | <span data-ttu-id="5955f-125">Nuspec 이름</span><span class="sxs-lookup"><span data-stu-id="5955f-125">Nuspec name</span></span>              | <span data-ttu-id="5955f-126">설명</span><span class="sxs-lookup"><span data-stu-id="5955f-126">Description</span></span>  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | <span data-ttu-id="5955f-127">패키지 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-127">The package identifier.</span></span> <span data-ttu-id="5955f-128">충족 하는 경우에 식별자의 접두사를 예약할 수 있습니다 합니다 [조건을](/nuget/reference/id-prefix-reservation)합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-128">A prefix from the identifier can be reserved if it meets the [criteria](/nuget/reference/id-prefix-reservation).</span></span> |
| `PackageVersion`                   | `version`                  | <span data-ttu-id="5955f-129">NuGet 패키지 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-129">NuGet package version.</span></span> <span data-ttu-id="5955f-130">자세한 내용은 [NuGet 패키지 버전](./versioning.md#nuget-package-version)합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-130">For more information, see [NuGet package version](./versioning.md#nuget-package-version).</span></span>             |
| `Title`                            | `title`                    | <span data-ttu-id="5955f-131">패키지의 사람이 읽기 편한 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-131">A human-friendly title of the package.</span></span> <span data-ttu-id="5955f-132">기본적으로 `PackageId`합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-132">It defaults to the `PackageId`.</span></span>             |
| `Description`                      | `description`              | <span data-ttu-id="5955f-133">UI에 표시 되는 패키지의 긴 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-133">A long description of the package displayed in UI.</span></span>             |
| `Authors`                          | `authors`                  | <span data-ttu-id="5955f-134">패키지 작성자, nuget.org에서 프로필 이름과 일치 하는 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-134">A comma-separated list of package authors, matching the profile names on nuget.org.</span></span>             |
| `PackageTags`                      | `tags`                     | <span data-ttu-id="5955f-135">태그 및 패키지를 설명 하는 키워드의 공백으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-135">A space-delimited list of tags and keywords that describe the package.</span></span> <span data-ttu-id="5955f-136">태그는 패키지를 검색할 때 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-136">Tags are used when searching for packages.</span></span>             |
| `PackageIconUrl`                   | `iconUrl`                  | <span data-ttu-id="5955f-137">패키지에 대 한 아이콘으로 사용할 이미지에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-137">A URL for an image to use as the icon for the package.</span></span> <span data-ttu-id="5955f-138">URL은 HTTPS 여야 및 이미지 64x64 하 고 투명 한 배경을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-138">URL should be HTTPS and the image should be 64x64 and have a transparent background.</span></span>             |
| `PackageProjectUrl`                | `projectUrl`               | <span data-ttu-id="5955f-139">프로젝트 홈 페이지 또는 소스 리포지토리에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-139">A URL for the project homepage or source repository.</span></span>             |
| `PackageLicenseUrl`                | `licenseUrl`               | <span data-ttu-id="5955f-140">프로젝트 라이선스 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-140">A URL to the project license.</span></span> <span data-ttu-id="5955f-141">URL을이 수는 `LICENSE` 소스 제어에서 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-141">Can be the URL to the `LICENSE` file in source control.</span></span>             |

<span data-ttu-id="5955f-142">**✔️ 것이 좋습니다** NuGet의 접두사 예약을 충족 하는 접두사를 사용 하 여 NuGet 패키지 이름을 선택 [조건을](/nuget/reference/id-prefix-reservation)합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-142">**✔️ CONSIDER** choosing a NuGet package name with a prefix that meets NuGet's prefix reservation [criteria](/nuget/reference/id-prefix-reservation).</span></span>

<span data-ttu-id="5955f-143">**✔️ 것이 좋습니다** 를 사용 하는 `LICENSE` 으로 소스 제어에서 파일을 `LicenseUrl`.</span><span class="sxs-lookup"><span data-stu-id="5955f-143">**✔️ CONSIDER** using the `LICENSE` file in source control as the `LicenseUrl`.</span></span> <span data-ttu-id="5955f-144">예를 들어 [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-144">For example, [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5955f-145">기본값은 라이선스 없이 프로젝트 [배타적 저작권](https://choosealicense.com/no-permission/), 다른 사람이 사용할 수 없도록 하 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-145">A project without a license defaults to [exclusive copyright](https://choosealicense.com/no-permission/), making it impossible for other people to use.</span></span>

<span data-ttu-id="5955f-146">**✔️ 수행** HTTPS href 패키지 아이콘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-146">**✔️ DO** use an HTTPS href to your package icon.</span></span>

> <span data-ttu-id="5955f-147">NuGet.org와 같은 사이트에서 사용 하도록 설정 하는 HTTPS를 사용 하 여 실행 및 HTTPS가 아닌 이미지를 표시는 혼합 된 콘텐츠 경고를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-147">Sites like NuGet.org run with HTTPS enabled and displaying a non-HTTPS image will create a mixed content warning.</span></span>

<span data-ttu-id="5955f-148">**✔️ 수행** 64x64 이며 최고의 결과 보기에 대 한 투명 한 배경이 패키지 아이콘 이미지를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-148">**✔️ DO** use a package icon image that is 64x64 and has a transparent background for best viewing results.</span></span>

## <a name="pre-release-packages"></a><span data-ttu-id="5955f-149">시험판 패키지</span><span class="sxs-lookup"><span data-stu-id="5955f-149">Pre-release packages</span></span>

<span data-ttu-id="5955f-150">버전 접미사를 사용 하 여 NuGet 패키지를 사용 하는 것으로 간주 [시험판](/nuget/create-packages/prerelease-packages)합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-150">NuGet packages with a version suffix are considered [pre-release](/nuget/create-packages/prerelease-packages).</span></span> <span data-ttu-id="5955f-151">기본적으로 NuGet 패키지 관리자 UI를 사용자 opts에 시험판 패키지를 테스트 하는 제한 된 사용자에 대 한 이상적인 시험판 패키지를 만드는 경우가 아니면 안정적인 릴리스를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-151">By default, the NuGet Package Manager UI shows stable releases unless a user opts-in to pre-release packages, making pre-release packages ideal for limited user testing.</span></span>

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> <span data-ttu-id="5955f-152">안정적인 패키지를 시험판 패키지에 종속 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-152">A stable package cannot depend on a pre-release package.</span></span> <span data-ttu-id="5955f-153">사용자 고유의 패키지 시험판 버전을 확인 하거나 이전 안정적인 버전에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-153">You must either make your own package pre-release or depend on an older stable version.</span></span>

<span data-ttu-id="5955f-154">![NuGet 시험판 패키지 종속성](./media/nuget/nuget-prerelease-package.png "NuGet 시험판 패키지 종속성")</span><span class="sxs-lookup"><span data-stu-id="5955f-154">![NuGet pre-release package dependency](./media/nuget/nuget-prerelease-package.png "NuGet pre-release package dependency")</span></span>

<span data-ttu-id="5955f-155">**✔️ 수행** 테스트, 미기 보기 또는 실험 하는 경우 시험판 패키지를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-155">**✔️ DO** publish a pre-release package when testing, previewing, or experimenting.</span></span>

<span data-ttu-id="5955f-156">**✔️ 수행** 해당 준비 하므로 다른 안정적인 패키지를 참조할 수 있는 경우 안정적인 패키지를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-156">**✔️ DO** publish a stable package when its ready so other stable packages can reference it.</span></span>

## <a name="symbol-packages"></a><span data-ttu-id="5955f-157">기호 패키지</span><span class="sxs-lookup"><span data-stu-id="5955f-157">Symbol packages</span></span>

<span data-ttu-id="5955f-158">NuGet 지원 [별도 기호 패키지를 생성](/nuget/create-packages/symbol-packages) 포함 된.NET 어셈블리를 포함 하는 기본 패키지와 함께 PDB 파일을 디버그 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-158">NuGet supports [generating a separate symbol package](/nuget/create-packages/symbol-packages) containing debug PDB files alongside the main package containing .NET assemblies.</span></span> <span data-ttu-id="5955f-159">기호 패키지는 기호 서버에서 호스트 되는지 하며 필요에 따라 Visual Studio와 같은 도구에만 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-159">The idea of symbol packages is they're hosted on a symbol server and are only downloaded by a tool like Visual Studio on demand.</span></span>

<span data-ttu-id="5955f-160">기본 공용 호스트-기호에 대 한 현재 [SymbolSource](http://www.symbolsource.org/) -이식 가능한 Pdb 생성을 지원 하지 않습니다 SDK 스타일 프로젝트 및 기호 패키지 유용 하지.</span><span class="sxs-lookup"><span data-stu-id="5955f-160">Currently the main public host for symbols - [SymbolSource](http://www.symbolsource.org/) - doesn't support the portable PDBs created by SDK-style projects and symbol packages aren't useful.</span></span>

<span data-ttu-id="5955f-161">**✔️ 하십시오** 기본 NuGet 패키지에 Pdb를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="5955f-161">**✔️ CONSIDER** embedding PDBs in the main NuGet package.</span></span>

<span data-ttu-id="5955f-162">**❌ 하지 말고** Pdb를 포함 하는 기호 패키지 만들기.</span><span class="sxs-lookup"><span data-stu-id="5955f-162">**❌ AVOID** creating a symbols package containing PDBs.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="5955f-163">[이전](./strong-naming.md)
[다음](./dependencies.md)</span><span class="sxs-lookup"><span data-stu-id="5955f-163">[Previous](./strong-naming.md)
[Next](./dependencies.md)</span></span>
