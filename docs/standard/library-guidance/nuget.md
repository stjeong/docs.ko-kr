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
# <a name="nuget"></a>NuGet

NuGet 용.NET 에코 시스템 패키지 관리자 이며 기본 방법은 개발자가 검색 하 고.NET 오픈 소스 라이브러리를 획득 합니다. [NuGet.org](https://www.nuget.org/)NuGet 패키지를 호스팅하기 위해 Microsoft에서 제공 하는 무료 서비스는 공용 NuGet 패키지에 대 한 기본 호스트 되지만 같은 사용자 지정 NuGet 서비스를 게시할 수 있습니다 [MyGet](https://www.myget.org/) 고 [Azure 아티팩트 ](https://azure.microsoft.com/services/devops/artifacts/).

![NuGet](./media/nuget/nuget-logo.png "NuGet")

## <a name="create-a-nuget-package"></a>NuGet 패키지 만들기

NuGet 패키지 (`*.nupkg`)은.NET 어셈블리 및 관련된 메타 데이터가 포함 된 zip 파일입니다.

NuGet 패키지를 만드는 두 가지 방법이 있습니다. 최신 및 권장 되는 방식은 SDK 스타일 프로젝트에서 패키지를 만드는 (프로젝트 파일 내용이 시작 `<Project Sdk="Microsoft.NET.Sdk">`). 어셈블리 및 대상 패키지에 자동으로 추가 하 고 패키지 이름과 버전 번호와 같은 MSBuild 파일에 추가 됩니다 남은 메타 데이터 키를 누릅니다. 사용 하 여 컴파일하는 [ `dotnet pack` ](../../core/tools/dotnet-pack.md) 명령 출력을 `*.nupkg` 어셈블리 대신 파일입니다.

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

NuGet 패키지 만들기에 대 한 이전 방식의 된를 `*.nuspec` 파일 및 `nuget.exe` 명령줄 도구입니다. Nuspec 파일을 유용한 제어를 제공 하지만 어떤 어셈블리 및 대상 최종 NuGet 패키지에 포함 하도록 신중 하 게 지정 해야 합니다. 실수 하기 쉽습니다 또는 다른 사용자에 게 변경 하는 경우 nuspec을 업데이트 해야 합니다. Nuspec 장점은 사용할 수 있습니다 SDK 스타일 프로젝트 파일을 아직 지원 하지 않는 프레임 워크에 대 한 NuGet 패키지를 만듭니다.

**✔️ 하십시오** SDK 스타일 프로젝트 파일을 사용 하 여 NuGet 패키지를 만듭니다.

**✔️ 하십시오** SourceLink 어셈블리 및 NuGet 패키지에 원본 제어 메타 데이터를 추가 하려면 설정 합니다.

## <a name="package-dependencies"></a>패키지 종속성

NuGet 패키지 종속성에 자세히 설명 되어는 [종속성](./dependencies.md) 문서.

## <a name="important-nuget-package-metadata"></a>중요 한 NuGet 패키지 메타 데이터

NuGet 패키지를 지 원하는 많은 [메타 데이터 속성](/nuget/reference/nuspec)합니다. 다음 표에서 모든 오픈 소스 프로젝트를 제공 해야 하는 핵심 메타 데이터를 포함 합니다.

| MSBuild 속성 이름              | Nuspec 이름              | 설명  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | 패키지 식별자입니다. 충족 하는 경우에 식별자의 접두사를 예약할 수 있습니다 합니다 [조건을](/nuget/reference/id-prefix-reservation)합니다. |
| `PackageVersion`                   | `version`                  | NuGet 패키지 버전입니다. 자세한 내용은 [NuGet 패키지 버전](./versioning.md#nuget-package-version)합니다.             |
| `Title`                            | `title`                    | 패키지의 사람이 읽기 편한 제목입니다. 기본적으로 `PackageId`합니다.             |
| `Description`                      | `description`              | UI에 표시 되는 패키지의 긴 설명입니다.             |
| `Authors`                          | `authors`                  | 패키지 작성자, nuget.org에서 프로필 이름과 일치 하는 쉼표로 구분 된 목록입니다.             |
| `PackageTags`                      | `tags`                     | 태그 및 패키지를 설명 하는 키워드의 공백으로 구분 된 목록입니다. 태그는 패키지를 검색할 때 사용 됩니다.             |
| `PackageIconUrl`                   | `iconUrl`                  | 패키지에 대 한 아이콘으로 사용할 이미지에 대 한 URL입니다. URL은 HTTPS 여야 및 이미지 64x64 하 고 투명 한 배경을 해야 합니다.             |
| `PackageProjectUrl`                | `projectUrl`               | 프로젝트 홈 페이지 또는 소스 리포지토리에 대 한 URL입니다.             |
| `PackageLicenseUrl`                | `licenseUrl`               | 프로젝트 라이선스 URL입니다. URL을이 수는 `LICENSE` 소스 제어에서 파일입니다.             |

**✔️ 것이 좋습니다** NuGet의 접두사 예약을 충족 하는 접두사를 사용 하 여 NuGet 패키지 이름을 선택 [조건을](/nuget/reference/id-prefix-reservation)합니다.

**✔️ 것이 좋습니다** 를 사용 하는 `LICENSE` 으로 소스 제어에서 파일을 `LicenseUrl`. 예를 들어 [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md)합니다.

> [!IMPORTANT]
> 기본값은 라이선스 없이 프로젝트 [배타적 저작권](https://choosealicense.com/no-permission/), 다른 사람이 사용할 수 없도록 하 합니다.

**✔️ 수행** HTTPS href 패키지 아이콘을 사용 합니다.

> NuGet.org와 같은 사이트에서 사용 하도록 설정 하는 HTTPS를 사용 하 여 실행 및 HTTPS가 아닌 이미지를 표시는 혼합 된 콘텐츠 경고를 만듭니다.

**✔️ 수행** 64x64 이며 최고의 결과 보기에 대 한 투명 한 배경이 패키지 아이콘 이미지를 사용 합니다.

## <a name="pre-release-packages"></a>시험판 패키지

버전 접미사를 사용 하 여 NuGet 패키지를 사용 하는 것으로 간주 [시험판](/nuget/create-packages/prerelease-packages)합니다. 기본적으로 NuGet 패키지 관리자 UI를 사용자 opts에 시험판 패키지를 테스트 하는 제한 된 사용자에 대 한 이상적인 시험판 패키지를 만드는 경우가 아니면 안정적인 릴리스를 표시 합니다.

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> 안정적인 패키지를 시험판 패키지에 종속 될 수 없습니다. 사용자 고유의 패키지 시험판 버전을 확인 하거나 이전 안정적인 버전에 따라 달라 집니다.

![NuGet 시험판 패키지 종속성](./media/nuget/nuget-prerelease-package.png "NuGet 시험판 패키지 종속성")

**✔️ 수행** 테스트, 미기 보기 또는 실험 하는 경우 시험판 패키지를 게시 합니다.

**✔️ 수행** 해당 준비 하므로 다른 안정적인 패키지를 참조할 수 있는 경우 안정적인 패키지를 게시 합니다.

## <a name="symbol-packages"></a>기호 패키지

NuGet 지원 [별도 기호 패키지를 생성](/nuget/create-packages/symbol-packages) 포함 된.NET 어셈블리를 포함 하는 기본 패키지와 함께 PDB 파일을 디버그 합니다. 기호 패키지는 기호 서버에서 호스트 되는지 하며 필요에 따라 Visual Studio와 같은 도구에만 다운로드 됩니다.

기본 공용 호스트-기호에 대 한 현재 [SymbolSource](http://www.symbolsource.org/) -이식 가능한 Pdb 생성을 지원 하지 않습니다 SDK 스타일 프로젝트 및 기호 패키지 유용 하지.

**✔️ 하십시오** 기본 NuGet 패키지에 Pdb를 포함 합니다.

**❌ 하지 말고** Pdb를 포함 하는 기호 패키지 만들기.

>[!div class="step-by-step"]
[이전](./strong-naming.md)
[다음](./dependencies.md)
