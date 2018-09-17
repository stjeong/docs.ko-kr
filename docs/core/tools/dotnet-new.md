---
title: dotnet new 명령 - .NET Core CLI
description: dotnet new 명령은 지정된 템플릿을 기반으로 새 .NET Core 프로젝트를 만듭니다.
author: mairaw
ms.author: mairaw
ms.date: 07/31/2018
ms.openlocfilehash: 2c82dda2d93225edb360316637e22964135cd5e4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512557"
---
# <a name="dotnet-new"></a><span data-ttu-id="fc1af-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="fc1af-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="fc1af-104">name</span><span class="sxs-lookup"><span data-stu-id="fc1af-104">Name</span></span>

<span data-ttu-id="fc1af-105">`dotnet new` - 지정된 템플릿을 기반으로 새 프로젝트, 구성 파일 또는 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="fc1af-106">개요</span><span class="sxs-lookup"><span data-stu-id="fc1af-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fc1af-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fc1af-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fc1af-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fc1af-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fc1af-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fc1af-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="fc1af-110">설명</span><span class="sxs-lookup"><span data-stu-id="fc1af-110">Description</span></span>

<span data-ttu-id="fc1af-111">`dotnet new` 명령은 유효한 .NET Core 프로젝트를 초기화하는 편리한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="fc1af-112">이 명령은 [템플릿 엔진](https://github.com/dotnet/templating)을 호출하여 지정된 템플릿 및 옵션을 기반으로 디스크에 아티팩트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="fc1af-113">인수</span><span class="sxs-lookup"><span data-stu-id="fc1af-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="fc1af-114">명령이 호출될 때 인스턴스화할 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="fc1af-115">각 템플릿에는 전달할 수 있는 특정 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="fc1af-116">자세한 내용은 [템플릿 옵션](#template-options)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fc1af-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fc1af-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="fc1af-118">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-118">The command contains a default list of templates.</span></span> <span data-ttu-id="fc1af-119">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="fc1af-120">다음 표에는 .NET Core SDK 2.1.300과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="fc1af-121">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="fc1af-122">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="fc1af-122">Template description</span></span>                          | <span data-ttu-id="fc1af-123">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="fc1af-123">Template name</span></span>   | <span data-ttu-id="fc1af-124">언어</span><span class="sxs-lookup"><span data-stu-id="fc1af-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="fc1af-125">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fc1af-125">Console application</span></span>                          | `console`       | <span data-ttu-id="fc1af-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-127">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="fc1af-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="fc1af-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-129">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="fc1af-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="fc1af-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-131">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="fc1af-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="fc1af-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-133">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="fc1af-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="fc1af-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-134">[C#]</span></span>          |
| <span data-ttu-id="fc1af-135">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="fc1af-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="fc1af-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-136">[C#]</span></span>          |
| <span data-ttu-id="fc1af-137">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="fc1af-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="fc1af-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-138">[C#]</span></span>          |
| <span data-ttu-id="fc1af-139">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="fc1af-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="fc1af-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-140">[C#], F#</span></span>      |
| <span data-ttu-id="fc1af-141">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="fc1af-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="fc1af-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-142">[C#], F#</span></span>      |
| <span data-ttu-id="fc1af-143">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="fc1af-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="fc1af-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-144">[C#]</span></span>          |
| <span data-ttu-id="fc1af-145">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="fc1af-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="fc1af-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-146">[C#]</span></span>          |
| <span data-ttu-id="fc1af-147">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="fc1af-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="fc1af-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-148">[C#]</span></span>          |
| <span data-ttu-id="fc1af-149">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="fc1af-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="fc1af-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-150">[C#]</span></span>          |
| <span data-ttu-id="fc1af-151">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="fc1af-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="fc1af-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-152">[C#], F#</span></span>      |
| <span data-ttu-id="fc1af-153">Razor 클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="fc1af-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="fc1af-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-154">[C#]</span></span>          |
| <span data-ttu-id="fc1af-155">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="fc1af-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="fc1af-156">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="fc1af-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="fc1af-157">웹 구성</span><span class="sxs-lookup"><span data-stu-id="fc1af-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="fc1af-158">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="fc1af-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fc1af-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fc1af-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="fc1af-160">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-160">The command contains a default list of templates.</span></span> <span data-ttu-id="fc1af-161">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="fc1af-162">다음 표에는 .NET Core SDK 2.0과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="fc1af-163">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="fc1af-164">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="fc1af-164">Template description</span></span>                          | <span data-ttu-id="fc1af-165">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="fc1af-165">Template name</span></span> | <span data-ttu-id="fc1af-166">언어</span><span class="sxs-lookup"><span data-stu-id="fc1af-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="fc1af-167">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fc1af-167">Console application</span></span>                          | `console`     | <span data-ttu-id="fc1af-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-169">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="fc1af-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="fc1af-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-171">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="fc1af-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="fc1af-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-173">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="fc1af-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="fc1af-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fc1af-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fc1af-175">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="fc1af-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="fc1af-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-176">[C#], F#</span></span>      |
| <span data-ttu-id="fc1af-177">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="fc1af-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="fc1af-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-178">[C#], F#</span></span>      |
| <span data-ttu-id="fc1af-179">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="fc1af-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="fc1af-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-180">[C#]</span></span>          |
| <span data-ttu-id="fc1af-181">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="fc1af-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="fc1af-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-182">[C#]</span></span>          |
| <span data-ttu-id="fc1af-183">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="fc1af-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="fc1af-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-184">[C#]</span></span>          |
| <span data-ttu-id="fc1af-185">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="fc1af-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="fc1af-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-186">[C#]</span></span>          |
| <span data-ttu-id="fc1af-187">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="fc1af-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="fc1af-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-188">[C#], F#</span></span>      |
| <span data-ttu-id="fc1af-189">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="fc1af-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="fc1af-190">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="fc1af-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="fc1af-191">웹 구성</span><span class="sxs-lookup"><span data-stu-id="fc1af-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="fc1af-192">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="fc1af-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="fc1af-193">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="fc1af-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="fc1af-194">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="fc1af-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="fc1af-195">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="fc1af-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fc1af-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fc1af-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="fc1af-197">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-197">The command contains a default list of templates.</span></span> <span data-ttu-id="fc1af-198">`dotnet new -all`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="fc1af-199">다음 표에는 .NET Core SDK 1.x와 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="fc1af-200">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="fc1af-201">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="fc1af-201">Template description</span></span>  | <span data-ttu-id="fc1af-202">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="fc1af-202">Template name</span></span> | <span data-ttu-id="fc1af-203">언어</span><span class="sxs-lookup"><span data-stu-id="fc1af-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="fc1af-204">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fc1af-204">Console application</span></span>  | `console`     | <span data-ttu-id="fc1af-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-205">[C#], F#</span></span>  |
| <span data-ttu-id="fc1af-206">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="fc1af-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="fc1af-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-207">[C#], F#</span></span>  |
| <span data-ttu-id="fc1af-208">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="fc1af-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="fc1af-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-209">[C#], F#</span></span>  |
| <span data-ttu-id="fc1af-210">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="fc1af-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="fc1af-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-211">[C#], F#</span></span>  |
| <span data-ttu-id="fc1af-212">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="fc1af-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="fc1af-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-213">[C#]</span></span>      |
| <span data-ttu-id="fc1af-214">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="fc1af-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="fc1af-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fc1af-215">[C#], F#</span></span>  |
| <span data-ttu-id="fc1af-216">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="fc1af-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="fc1af-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="fc1af-217">[C#]</span></span>      |
| <span data-ttu-id="fc1af-218">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="fc1af-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="fc1af-219">웹 구성</span><span class="sxs-lookup"><span data-stu-id="fc1af-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="fc1af-220">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="fc1af-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="fc1af-221">옵션</span><span class="sxs-lookup"><span data-stu-id="fc1af-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fc1af-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fc1af-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="fc1af-223">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="fc1af-224">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="fc1af-225">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-225">Prints out help for the command.</span></span> <span data-ttu-id="fc1af-226">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="fc1af-227">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="fc1af-228">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="fc1af-229">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="fc1af-230">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="fc1af-231">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="fc1af-232">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="fc1af-233">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="fc1af-234">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="fc1af-235">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-235">The language of the template to create.</span></span> <span data-ttu-id="fc1af-236">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="fc1af-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="fc1af-237">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="fc1af-238">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="fc1af-239">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="fc1af-240">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-240">The name for the created output.</span></span> <span data-ttu-id="fc1af-241">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="fc1af-242">설치 중 사용할 NuGet 소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="fc1af-243">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-243">Location to place the generated output.</span></span> <span data-ttu-id="fc1af-244">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="fc1af-245">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-245">Filters templates based on available types.</span></span> <span data-ttu-id="fc1af-246">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="fc1af-247">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="fc1af-248">`PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="fc1af-249">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="fc1af-250">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fc1af-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fc1af-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="fc1af-252">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="fc1af-253">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="fc1af-254">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-254">Prints out help for the command.</span></span> <span data-ttu-id="fc1af-255">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="fc1af-256">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="fc1af-257">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="fc1af-258">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="fc1af-259">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="fc1af-260">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="fc1af-261">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="fc1af-262">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="fc1af-263">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="fc1af-264">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-264">The language of the template to create.</span></span> <span data-ttu-id="fc1af-265">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="fc1af-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="fc1af-266">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="fc1af-267">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="fc1af-268">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="fc1af-269">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-269">The name for the created output.</span></span> <span data-ttu-id="fc1af-270">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="fc1af-271">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-271">Location to place the generated output.</span></span> <span data-ttu-id="fc1af-272">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="fc1af-273">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-273">Filters templates based on available types.</span></span> <span data-ttu-id="fc1af-274">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="fc1af-275">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="fc1af-276">`PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-276">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="fc1af-277">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="fc1af-278">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="fc1af-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fc1af-279">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fc1af-279">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="fc1af-280">`dotnet new` 명령의 컨텍스트에서만 실행되는 경우 특정 유형의 프로젝트에 대한 모든 템플릿을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-280">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="fc1af-281">`dotnet new web -all`처럼 특정 템플릿의 컨텍스트에서 실행되는 경우 `-all`은 강제 생성 플래그로 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-281">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="fc1af-282">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-282">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="fc1af-283">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-283">Prints out help for the command.</span></span> <span data-ttu-id="fc1af-284">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-284">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="fc1af-285">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-285">Lists templates containing the specified name.</span></span> <span data-ttu-id="fc1af-286">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-286">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="fc1af-287">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-287">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="fc1af-288">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-288">The language of the template to create.</span></span> <span data-ttu-id="fc1af-289">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="fc1af-289">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="fc1af-290">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-290">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="fc1af-291">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-291">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="fc1af-292">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-292">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="fc1af-293">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-293">The name for the created output.</span></span> <span data-ttu-id="fc1af-294">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-294">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="fc1af-295">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-295">Location to place the generated output.</span></span> <span data-ttu-id="fc1af-296">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-296">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="fc1af-297">템플릿 옵션</span><span class="sxs-lookup"><span data-stu-id="fc1af-297">Template options</span></span>

<span data-ttu-id="fc1af-298">각 프로젝트 템플릿에는 사용할 수 있는 추가 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-298">Each project template may have additional options available.</span></span> <span data-ttu-id="fc1af-299">코어 템플릿에는 다음과 같은 추가 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-299">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fc1af-300">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fc1af-300">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="fc1af-301">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="fc1af-301">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="fc1af-302">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-302">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-303">**classlib**</span><span class="sxs-lookup"><span data-stu-id="fc1af-303">**classlib**</span></span>

<span data-ttu-id="fc1af-304">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-304">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fc1af-305">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="fc1af-305">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="fc1af-306">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-306">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="fc1af-307">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-307">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-308">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="fc1af-308">**mstest, xunit**</span></span>

<span data-ttu-id="fc1af-309">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-309">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="fc1af-310">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-310">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-311">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="fc1af-311">**globaljson**</span></span>

<span data-ttu-id="fc1af-312">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-312">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="fc1af-313">**web**</span><span class="sxs-lookup"><span data-stu-id="fc1af-313">**web**</span></span>

<span data-ttu-id="fc1af-314">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-314">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="fc1af-315">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-315">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-316">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-316">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="fc1af-317">이 옵션은 `IndividualAuth` 또는 `OrganizationalAuth`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-317">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="fc1af-318">**webapi**</span><span class="sxs-lookup"><span data-stu-id="fc1af-318">**webapi**</span></span>

<span data-ttu-id="fc1af-319">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-319">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fc1af-320">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-320">The possible values are:</span></span>

- <span data-ttu-id="fc1af-321">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="fc1af-321">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fc1af-322">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-322">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fc1af-323">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-323">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fc1af-324">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-324">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fc1af-325">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-325">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fc1af-326">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-326">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-327">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-327">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fc1af-328">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-328">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fc1af-329">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-329">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-330">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-330">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fc1af-331">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-331">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-332">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-332">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fc1af-333">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-333">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fc1af-334">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-334">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-335">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-335">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fc1af-336">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-336">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fc1af-337">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-337">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-338">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-338">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fc1af-339">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-339">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fc1af-340">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-340">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-341">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-341">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fc1af-342">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-342">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fc1af-343">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-343">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fc1af-344">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-344">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="fc1af-345">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-345">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fc1af-346">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-346">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-347">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-347">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-348">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-348">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="fc1af-349">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-349">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="fc1af-350">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-350">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="fc1af-351">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="fc1af-351">**mvc, razor**</span></span>

<span data-ttu-id="fc1af-352">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-352">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fc1af-353">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-353">The possible values are:</span></span>

- <span data-ttu-id="fc1af-354">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="fc1af-354">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fc1af-355">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-355">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="fc1af-356">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-356">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fc1af-357">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-357">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fc1af-358">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-358">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="fc1af-359">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-359">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fc1af-360">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-360">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fc1af-361">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-361">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-362">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-362">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fc1af-363">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-363">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fc1af-364">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-364">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-365">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-365">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="fc1af-366">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-366">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-367">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-367">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="fc1af-368">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-369">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-369">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fc1af-370">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-370">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="fc1af-371">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-371">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fc1af-372">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-372">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fc1af-373">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-373">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="fc1af-374">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-374">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fc1af-375">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-375">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fc1af-376">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-376">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-377">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-377">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fc1af-378">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-378">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fc1af-379">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-379">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-380">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-380">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fc1af-381">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-381">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="fc1af-382">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-382">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-383">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-383">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="fc1af-384">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-384">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fc1af-385">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-385">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fc1af-386">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-386">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="fc1af-387">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-387">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="fc1af-388">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-388">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fc1af-389">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-389">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-390">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-390">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-391">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-391">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="fc1af-392">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-392">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="fc1af-393">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-393">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="fc1af-394">**page**</span><span class="sxs-lookup"><span data-stu-id="fc1af-394">**page**</span></span>

<span data-ttu-id="fc1af-395">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-395">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fc1af-396">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-396">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="fc1af-397">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-397">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="fc1af-398">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="fc1af-398">**viewimports**</span></span>

<span data-ttu-id="fc1af-399">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-399">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fc1af-400">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-400">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fc1af-401">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fc1af-401">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="fc1af-402">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="fc1af-402">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="fc1af-403">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-403">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-404">**classlib**</span><span class="sxs-lookup"><span data-stu-id="fc1af-404">**classlib**</span></span>

<span data-ttu-id="fc1af-405">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-405">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fc1af-406">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="fc1af-406">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="fc1af-407">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-407">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="fc1af-408">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-408">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-409">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="fc1af-409">**mstest, xunit**</span></span>

<span data-ttu-id="fc1af-410">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-410">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="fc1af-411">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-411">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-412">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="fc1af-412">**globaljson**</span></span>

<span data-ttu-id="fc1af-413">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-413">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="fc1af-414">**web**</span><span class="sxs-lookup"><span data-stu-id="fc1af-414">**web**</span></span>

<span data-ttu-id="fc1af-415">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-415">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="fc1af-416">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-416">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-417">**webapi**</span><span class="sxs-lookup"><span data-stu-id="fc1af-417">**webapi**</span></span>

<span data-ttu-id="fc1af-418">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-418">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fc1af-419">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-419">The possible values are:</span></span>

- <span data-ttu-id="fc1af-420">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="fc1af-420">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fc1af-421">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-421">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fc1af-422">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-422">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fc1af-423">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-423">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fc1af-424">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-424">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fc1af-425">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-425">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-426">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-426">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fc1af-427">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-427">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fc1af-428">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-428">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-429">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-429">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fc1af-430">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-430">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-431">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-431">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fc1af-432">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-432">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fc1af-433">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-433">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-434">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-434">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fc1af-435">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-435">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fc1af-436">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-436">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-437">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-437">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fc1af-438">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-438">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fc1af-439">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-439">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-440">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-440">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fc1af-441">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-441">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fc1af-442">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-442">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fc1af-443">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-443">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="fc1af-444">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-444">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fc1af-445">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-445">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-446">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-446">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-447">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="fc1af-447">**mvc, razor**</span></span>

<span data-ttu-id="fc1af-448">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-448">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fc1af-449">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-449">The possible values are:</span></span>

- <span data-ttu-id="fc1af-450">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="fc1af-450">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fc1af-451">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-451">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="fc1af-452">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-452">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fc1af-453">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-453">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fc1af-454">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-454">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="fc1af-455">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-455">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fc1af-456">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-456">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fc1af-457">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-457">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-458">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-458">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fc1af-459">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-459">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fc1af-460">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-460">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-461">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-461">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="fc1af-462">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-462">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-463">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-463">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="fc1af-464">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-465">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-465">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fc1af-466">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-466">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="fc1af-467">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-467">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fc1af-468">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-468">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fc1af-469">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-469">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="fc1af-470">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-470">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fc1af-471">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-471">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fc1af-472">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-472">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-473">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-473">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fc1af-474">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-474">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fc1af-475">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-475">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fc1af-476">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-476">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fc1af-477">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-477">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="fc1af-478">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-478">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fc1af-479">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-479">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="fc1af-480">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-480">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fc1af-481">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-481">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fc1af-482">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-482">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="fc1af-483">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-483">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="fc1af-484">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-484">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fc1af-485">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-485">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fc1af-486">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-486">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fc1af-487">**page**</span><span class="sxs-lookup"><span data-stu-id="fc1af-487">**page**</span></span>

<span data-ttu-id="fc1af-488">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-488">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fc1af-489">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-489">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="fc1af-490">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-490">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="fc1af-491">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="fc1af-491">**viewimports**</span></span>

<span data-ttu-id="fc1af-492">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-492">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fc1af-493">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-493">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fc1af-494">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fc1af-494">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="fc1af-495">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="fc1af-495">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="fc1af-496">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-496">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fc1af-497">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="fc1af-497">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="fc1af-498">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-498">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="fc1af-499">**classlib**</span><span class="sxs-lookup"><span data-stu-id="fc1af-499">**classlib**</span></span>

<span data-ttu-id="fc1af-500">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-500">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fc1af-501">값: `netcoreapp1.0`, `netcoreapp1.1` 또는 `netstandard1.0`~`netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="fc1af-501">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="fc1af-502">기본값은 `netstandard1.4`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-502">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="fc1af-503">**mvc**</span><span class="sxs-lookup"><span data-stu-id="fc1af-503">**mvc**</span></span>

<span data-ttu-id="fc1af-504">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-504">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fc1af-505">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="fc1af-505">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="fc1af-506">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-506">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="fc1af-507">`-au|--auth` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-507">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="fc1af-508">값: `None` 또는 `Individual`.</span><span class="sxs-lookup"><span data-stu-id="fc1af-508">Values: `None` or `Individual`.</span></span> <span data-ttu-id="fc1af-509">기본값은 `None`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-509">The default value is `None`.</span></span>

<span data-ttu-id="fc1af-510">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-510">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="fc1af-511">값: `true` 또는 `false`.</span><span class="sxs-lookup"><span data-stu-id="fc1af-511">Values: `true` or `false`.</span></span> <span data-ttu-id="fc1af-512">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-512">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="fc1af-513">예제</span><span class="sxs-lookup"><span data-stu-id="fc1af-513">Examples</span></span>

<span data-ttu-id="fc1af-514">현재 디렉터리에 F# 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-514">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="fc1af-515">지정된 디렉터리에서 .NET Standard 클래스 라이브러리 프로젝트를 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="fc1af-515">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="fc1af-516">인증 없이 현재 디렉터리에 새 ASP.NET Core C# MVC 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-516">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="fc1af-517">새 xUnit 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-517">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="fc1af-518">MVC에 대해 사용할 수 있는 모든 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1af-518">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="fc1af-519">ASP.NET Core용 단일 페이지 응용 프로그램 템플릿 버전 2.0을 설치합니다(.NET Core SDK 1.1 및 이후 버전에서만 사용할 수 있는 명령 옵션).</span><span class="sxs-lookup"><span data-stu-id="fc1af-519">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="fc1af-520">현재 디렉터리에서 SDK 버전을 2.0.0으로 설정하여 *global.json*을 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="fc1af-520">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="fc1af-521">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fc1af-521">See also</span></span>

* [<span data-ttu-id="fc1af-522">dotnet new에 대한 사용자 지정 템플릿</span><span class="sxs-lookup"><span data-stu-id="fc1af-522">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="fc1af-523">dotnet용 사용자 지정 템플릿 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="fc1af-523">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* <span data-ttu-id="fc1af-524">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)(dotnet/dotnet-template-samples GitHub 리포지토리)</span><span class="sxs-lookup"><span data-stu-id="fc1af-524">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)</span></span>  
* <span data-ttu-id="fc1af-525">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)(dotnet new에 대한 사용 가능한 템플릿)</span><span class="sxs-lookup"><span data-stu-id="fc1af-525">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)</span></span>
