---
title: SourceLink 및 .NET 라이브러리
description: SourceLink를 사용하여 .NET 라이브러리의 디버깅을 향상시키기 위한 모범 사례 권장 사항.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 3bc72e158a5773b656095f9ce58b442469f91e67
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128931"
---
# <a name="sourcelink"></a><span data-ttu-id="2770a-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="2770a-103">SourceLink</span></span>

<span data-ttu-id="2770a-104">SourceLink는 개발자가 NuGet에서 제공하는 .NET 어셈블리의 소스 코드 디버깅을 가능하게 해주는 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="2770a-105">SourceLink는 NuGet 패키지를 만들 때 실행되며 어셈블리 및 패키지 내부에 소스 제어 메타데이터를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="2770a-106">패키지를 다운로드하고 Visual Studio에서 SourceLink를 사용하도록 설정한 개발자는 소스 코드를 한 단계씩 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="2770a-107">SourceLink는 뛰어난 디버깅 환경을 만들기 위해 소스 제어 메타데이터를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="2770a-108">SourceLink 데모</span><span class="sxs-lookup"><span data-stu-id="2770a-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="2770a-109">SourceLink 사용</span><span class="sxs-lookup"><span data-stu-id="2770a-109">Using SourceLink</span></span>

<span data-ttu-id="2770a-110">SourceLink 사용에 대한 지침은 [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub 리포지토리에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="2770a-111">[NuGet 패키지 탐색기](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer)를 사용하여 SourceLink 메타데이터가 패키지에 성공적으로 포함되었는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="2770a-112">주석 식별자가 포함된 `Repository` 메타데이터가 있는지와 .pdb 파일이 각 대상의 .dll과 함께 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="2770a-113">![NuGet 패키지 탐색기의 SourceLink](./media/sourcelink/nuget-package-explorer-sourcelink.png "NuGet 패키지 탐색기의 SourceLink")</span><span class="sxs-lookup"><span data-stu-id="2770a-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="2770a-114">**✔️** SourceLink를 사용하여 어셈블리 및 NuGet 패키지에 소스 제어 메타데이터를 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="2770a-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet packages.</span></span>

> [!TIP]
> <span data-ttu-id="2770a-115">사용자 유형에 디버거 특성을 추가하여 개발자의 디버깅 환경을 향상시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-115">You can further enhance a developer's debugging experience by adding debugger attributes to your types.</span></span>
> * <span data-ttu-id="2770a-116"><xref:System.Diagnostics.DebuggerDisplayAttribute>는 클래스 또는 필드가 디버거 변수 창에 표시되는 방법을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> can customize how a class or field is displayed in the debugger variable windows.</span></span>
> * <span data-ttu-id="2770a-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute>는 디버거가 코드를 한 단계씩 실행하는 대신 코드를 단계별로 실행하도록 디버거에 지시합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> instructs the debugger to step through the code instead of stepping into the code.</span></span>
> * <span data-ttu-id="2770a-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute>는 멤버가 디버거 변수 창에 표시되는지 여부를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> controls whether a member is displayed in the debugger variable windows.</span></span>

<span data-ttu-id="2770a-119">**✔️** 기호 파일(`*.pdb`)을 NuGet 패키지에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-119">**✔️ CONSIDER** including symbol files (`*.pdb`) in the NuGet package.</span></span>

> <span data-ttu-id="2770a-120">일반적으로 [기호 패키지](./nuget.md#symbol-packages)에 기호 파일을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-120">Ordinarily, you'd publish symbol files in a [symbol package](./nuget.md#symbol-packages).</span></span> <span data-ttu-id="2770a-121">현재, 기호 패키지의 기본 공용 호스트는 SDK 스타일 프로젝트에서 생성되는 이식 가능한 기호 파일(`*.pdb`)을 지원하지 않으며, 기호 패키지가 유용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2770a-121">Currently the main public host for symbol packages doesn't support the portable symbol files (`*.pdb`) created by SDK-style projects, and symbol packages aren't useful.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="2770a-122">[이전](dependencies.md)
>[다음](publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="2770a-122">[Previous](dependencies.md)
[Next](publish-nuget-package.md)</span></span>