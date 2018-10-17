---
title: SourceLink 및.NET 라이브러리
description: SourceLink를 사용 하 여.NET 라이브러리에 대 한 디버깅을 향상 시키기 위한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: fa4af47eaa5dd1510640c2bf0ebb2187b56efae0
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49370318"
---
# <a name="sourcelink"></a><span data-ttu-id="07c7b-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="07c7b-103">SourceLink</span></span>

<span data-ttu-id="07c7b-104">SourceLink는 개발자가 NuGet에서.NET 어셈블리의 소스 코드 디버깅이 사용 하도록 설정 하는 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="07c7b-105">SourceLink은 NuGet 패키지를 만들 때 실행 하 고 어셈블리 및 패키지 내에서 원본 제어 메타 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="07c7b-106">패키지를 다운로드 하 고 Visual Studio에서 사용 하도록 설정 하는 SourceLink 있는 개발자는 소스 코드 한 단계씩 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="07c7b-107">SourceLink 뛰어난 디버깅 환경을 만들려면 원본 제어 메타 데이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="07c7b-108">SourceLink 데모</span><span class="sxs-lookup"><span data-stu-id="07c7b-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="07c7b-109">SourceLink를 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="07c7b-109">Using SourceLink</span></span>

<span data-ttu-id="07c7b-110">SourceLink 사용에 대 한 지침을 확인할 수 있습니다 합니다 [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub 리포지토리.</span><span class="sxs-lookup"><span data-stu-id="07c7b-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="07c7b-111">사용할 수 있습니다 [NuGet 패키지 탐색기](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) SourceLink 메타 데이터 패키지에 성공적으로 포함 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="07c7b-112">확인 된 `Repository` 메타 데이터 주석 식별자를 사용 하 여 있고.pdb 파일에 있는 각 대상의.dll을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="07c7b-113">![NuGet 패키지 탐색기에서 SourceLink](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink NuGet 패키지 탐색기에서")</span><span class="sxs-lookup"><span data-stu-id="07c7b-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="07c7b-114">**✔️ 하십시오** SourceLink를 사용 하 여 어셈블리 및 NuGet 패키지에 원본 제어 메타 데이터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

<span data-ttu-id="07c7b-115">**✔️ 하십시오** NuGet 패키지에 PDB 파일을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c7b-115">**✔️ CONSIDER** including PDB files in the NuGet package.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="07c7b-116">[이전](./dependencies.md)
[다음](./publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="07c7b-116">[Previous](./dependencies.md)
[Next](./publish-nuget-package.md)</span></span>
