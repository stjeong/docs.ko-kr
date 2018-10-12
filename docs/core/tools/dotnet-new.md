---
title: dotnet new 명령 - .NET Core CLI
description: dotnet new 명령은 지정된 템플릿을 기반으로 새 .NET Core 프로젝트를 만듭니다.
author: mairaw
ms.author: mairaw
ms.date: 07/31/2018
ms.openlocfilehash: 396c4ddf09854fa4582226bdb1422f8c929e459b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47208635"
---
# <a name="dotnet-new"></a><span data-ttu-id="78991-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="78991-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="78991-104">name</span><span class="sxs-lookup"><span data-stu-id="78991-104">Name</span></span>

<span data-ttu-id="78991-105">`dotnet new` - 지정된 템플릿을 기반으로 새 프로젝트, 구성 파일 또는 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="78991-106">개요</span><span class="sxs-lookup"><span data-stu-id="78991-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="78991-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="78991-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="78991-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="78991-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="78991-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="78991-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="78991-110">설명</span><span class="sxs-lookup"><span data-stu-id="78991-110">Description</span></span>

<span data-ttu-id="78991-111">`dotnet new` 명령은 유효한 .NET Core 프로젝트를 초기화하는 편리한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="78991-112">이 명령은 [템플릿 엔진](https://github.com/dotnet/templating)을 호출하여 지정된 템플릿 및 옵션을 기반으로 디스크에 아티팩트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="78991-113">인수</span><span class="sxs-lookup"><span data-stu-id="78991-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="78991-114">명령이 호출될 때 인스턴스화할 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="78991-115">각 템플릿에는 전달할 수 있는 특정 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="78991-116">자세한 내용은 [템플릿 옵션](#template-options)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78991-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="78991-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="78991-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="78991-118">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-118">The command contains a default list of templates.</span></span> <span data-ttu-id="78991-119">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78991-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="78991-120">다음 표에는 .NET Core SDK 2.1.300과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="78991-121">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="78991-122">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="78991-122">Template description</span></span>                          | <span data-ttu-id="78991-123">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="78991-123">Template name</span></span>   | <span data-ttu-id="78991-124">언어</span><span class="sxs-lookup"><span data-stu-id="78991-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="78991-125">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="78991-125">Console application</span></span>                          | `console`       | <span data-ttu-id="78991-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-127">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="78991-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="78991-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-129">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="78991-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="78991-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-131">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="78991-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="78991-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-133">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="78991-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="78991-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-134">[C#]</span></span>          |
| <span data-ttu-id="78991-135">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="78991-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="78991-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-136">[C#]</span></span>          |
| <span data-ttu-id="78991-137">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="78991-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="78991-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-138">[C#]</span></span>          |
| <span data-ttu-id="78991-139">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="78991-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="78991-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-140">[C#], F#</span></span>      |
| <span data-ttu-id="78991-141">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="78991-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="78991-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-142">[C#], F#</span></span>      |
| <span data-ttu-id="78991-143">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="78991-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="78991-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-144">[C#]</span></span>          |
| <span data-ttu-id="78991-145">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="78991-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="78991-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-146">[C#]</span></span>          |
| <span data-ttu-id="78991-147">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="78991-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="78991-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-148">[C#]</span></span>          |
| <span data-ttu-id="78991-149">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="78991-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="78991-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-150">[C#]</span></span>          |
| <span data-ttu-id="78991-151">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="78991-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="78991-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-152">[C#], F#</span></span>      |
| <span data-ttu-id="78991-153">Razor 클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="78991-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="78991-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-154">[C#]</span></span>          |
| <span data-ttu-id="78991-155">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="78991-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="78991-156">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="78991-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="78991-157">웹 구성</span><span class="sxs-lookup"><span data-stu-id="78991-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="78991-158">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="78991-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="78991-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="78991-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="78991-160">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-160">The command contains a default list of templates.</span></span> <span data-ttu-id="78991-161">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78991-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="78991-162">다음 표에는 .NET Core SDK 2.0과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="78991-163">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="78991-164">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="78991-164">Template description</span></span>                          | <span data-ttu-id="78991-165">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="78991-165">Template name</span></span> | <span data-ttu-id="78991-166">언어</span><span class="sxs-lookup"><span data-stu-id="78991-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="78991-167">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="78991-167">Console application</span></span>                          | `console`     | <span data-ttu-id="78991-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-169">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="78991-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="78991-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-171">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="78991-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="78991-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-173">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="78991-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="78991-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="78991-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="78991-175">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="78991-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="78991-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-176">[C#], F#</span></span>      |
| <span data-ttu-id="78991-177">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="78991-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="78991-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-178">[C#], F#</span></span>      |
| <span data-ttu-id="78991-179">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="78991-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="78991-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-180">[C#]</span></span>          |
| <span data-ttu-id="78991-181">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="78991-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="78991-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-182">[C#]</span></span>          |
| <span data-ttu-id="78991-183">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="78991-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="78991-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-184">[C#]</span></span>          |
| <span data-ttu-id="78991-185">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="78991-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="78991-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-186">[C#]</span></span>          |
| <span data-ttu-id="78991-187">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="78991-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="78991-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-188">[C#], F#</span></span>      |
| <span data-ttu-id="78991-189">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="78991-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="78991-190">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="78991-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="78991-191">웹 구성</span><span class="sxs-lookup"><span data-stu-id="78991-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="78991-192">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="78991-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="78991-193">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="78991-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="78991-194">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="78991-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="78991-195">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="78991-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="78991-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="78991-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="78991-197">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-197">The command contains a default list of templates.</span></span> <span data-ttu-id="78991-198">`dotnet new -all`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78991-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="78991-199">다음 표에는 .NET Core SDK 1.x와 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="78991-200">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="78991-201">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="78991-201">Template description</span></span>  | <span data-ttu-id="78991-202">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="78991-202">Template name</span></span> | <span data-ttu-id="78991-203">언어</span><span class="sxs-lookup"><span data-stu-id="78991-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="78991-204">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="78991-204">Console application</span></span>  | `console`     | <span data-ttu-id="78991-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-205">[C#], F#</span></span>  |
| <span data-ttu-id="78991-206">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="78991-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="78991-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-207">[C#], F#</span></span>  |
| <span data-ttu-id="78991-208">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="78991-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="78991-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-209">[C#], F#</span></span>  |
| <span data-ttu-id="78991-210">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="78991-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="78991-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-211">[C#], F#</span></span>  |
| <span data-ttu-id="78991-212">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="78991-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="78991-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-213">[C#]</span></span>      |
| <span data-ttu-id="78991-214">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="78991-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="78991-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="78991-215">[C#], F#</span></span>  |
| <span data-ttu-id="78991-216">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="78991-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="78991-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="78991-217">[C#]</span></span>      |
| <span data-ttu-id="78991-218">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="78991-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="78991-219">웹 구성</span><span class="sxs-lookup"><span data-stu-id="78991-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="78991-220">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="78991-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="78991-221">옵션</span><span class="sxs-lookup"><span data-stu-id="78991-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="78991-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="78991-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="78991-223">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="78991-224">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="78991-225">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-225">Prints out help for the command.</span></span> <span data-ttu-id="78991-226">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="78991-227">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="78991-228">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="78991-229">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="78991-230">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78991-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="78991-231">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78991-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="78991-232">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="78991-233">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="78991-234">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="78991-235">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-235">The language of the template to create.</span></span> <span data-ttu-id="78991-236">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="78991-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="78991-237">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="78991-238">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="78991-239">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="78991-240">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-240">The name for the created output.</span></span> <span data-ttu-id="78991-241">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="78991-242">설치 중 사용할 NuGet 소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="78991-243">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-243">Location to place the generated output.</span></span> <span data-ttu-id="78991-244">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="78991-245">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-245">Filters templates based on available types.</span></span> <span data-ttu-id="78991-246">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="78991-247">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="78991-248">`PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="78991-249">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="78991-250">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="78991-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="78991-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="78991-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="78991-252">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="78991-253">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="78991-254">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-254">Prints out help for the command.</span></span> <span data-ttu-id="78991-255">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="78991-256">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="78991-257">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="78991-258">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="78991-259">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78991-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="78991-260">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78991-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="78991-261">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="78991-262">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="78991-263">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="78991-264">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-264">The language of the template to create.</span></span> <span data-ttu-id="78991-265">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="78991-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="78991-266">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="78991-267">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="78991-268">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="78991-269">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-269">The name for the created output.</span></span> <span data-ttu-id="78991-270">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="78991-271">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-271">Location to place the generated output.</span></span> <span data-ttu-id="78991-272">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="78991-273">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-273">Filters templates based on available types.</span></span> <span data-ttu-id="78991-274">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="78991-275">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="78991-276">소스 `PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-276">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="78991-277">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="78991-278">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="78991-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="78991-279">템플릿을 제거하는 데 필요한 `PATH` 또는 `NUGET_ID` 인수를 확인할 수 없는 경우, 인수 없이 `dotnet new --uninstall`을 실행하면 설치된 모든 템플릿 및 템플릿을 제거하는 데 필요한 인수가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-279">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="78991-280">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="78991-280">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="78991-281">`dotnet new` 명령의 컨텍스트에서만 실행되는 경우 특정 유형의 프로젝트에 대한 모든 템플릿을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-281">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="78991-282">`dotnet new web -all`처럼 특정 템플릿의 컨텍스트에서 실행되는 경우 `-all`은 강제 생성 플래그로 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-282">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="78991-283">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-283">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="78991-284">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-284">Prints out help for the command.</span></span> <span data-ttu-id="78991-285">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-285">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="78991-286">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-286">Lists templates containing the specified name.</span></span> <span data-ttu-id="78991-287">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-287">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="78991-288">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-288">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="78991-289">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-289">The language of the template to create.</span></span> <span data-ttu-id="78991-290">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="78991-290">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="78991-291">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-291">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="78991-292">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-292">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="78991-293">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-293">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="78991-294">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-294">The name for the created output.</span></span> <span data-ttu-id="78991-295">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-295">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="78991-296">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-296">Location to place the generated output.</span></span> <span data-ttu-id="78991-297">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-297">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="78991-298">템플릿 옵션</span><span class="sxs-lookup"><span data-stu-id="78991-298">Template options</span></span>

<span data-ttu-id="78991-299">각 프로젝트 템플릿에는 사용할 수 있는 추가 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-299">Each project template may have additional options available.</span></span> <span data-ttu-id="78991-300">코어 템플릿에는 다음과 같은 추가 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-300">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="78991-301">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="78991-301">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="78991-302">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="78991-302">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="78991-303">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-303">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-304">**classlib**</span><span class="sxs-lookup"><span data-stu-id="78991-304">**classlib**</span></span>

<span data-ttu-id="78991-305">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-305">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="78991-306">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="78991-306">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="78991-307">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-307">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="78991-308">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-308">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-309">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="78991-309">**mstest, xunit**</span></span>

<span data-ttu-id="78991-310">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-310">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="78991-311">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-311">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-312">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="78991-312">**globaljson**</span></span>

<span data-ttu-id="78991-313">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-313">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="78991-314">**web**</span><span class="sxs-lookup"><span data-stu-id="78991-314">**web**</span></span>

<span data-ttu-id="78991-315">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-315">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="78991-316">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-316">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-317">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-317">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="78991-318">이 옵션은 `IndividualAuth` 또는 `OrganizationalAuth`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-318">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="78991-319">**webapi**</span><span class="sxs-lookup"><span data-stu-id="78991-319">**webapi**</span></span>

<span data-ttu-id="78991-320">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-320">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="78991-321">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-321">The possible values are:</span></span>

- <span data-ttu-id="78991-322">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="78991-322">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="78991-323">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-323">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="78991-324">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-324">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="78991-325">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-325">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="78991-326">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-326">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="78991-327">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-327">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-328">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-328">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="78991-329">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-329">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="78991-330">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-330">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-331">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-331">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="78991-332">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-332">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-333">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-333">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="78991-334">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-334">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="78991-335">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-335">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-336">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-336">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="78991-337">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-337">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="78991-338">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-338">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-339">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-339">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="78991-340">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-340">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="78991-341">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-341">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-342">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-342">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="78991-343">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-343">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="78991-344">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-344">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="78991-345">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-345">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="78991-346">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-346">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="78991-347">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-347">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-348">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-348">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-349">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-349">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="78991-350">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-350">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="78991-351">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-351">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="78991-352">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="78991-352">**mvc, razor**</span></span>

<span data-ttu-id="78991-353">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-353">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="78991-354">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-354">The possible values are:</span></span>

- <span data-ttu-id="78991-355">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="78991-355">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="78991-356">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-356">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="78991-357">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-357">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="78991-358">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-358">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="78991-359">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-359">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="78991-360">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-360">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="78991-361">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-361">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="78991-362">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-362">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-363">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-363">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="78991-364">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-364">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="78991-365">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-365">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-366">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-366">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="78991-367">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-367">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-368">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-368">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="78991-369">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-369">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-370">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-370">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="78991-371">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-371">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="78991-372">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-372">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="78991-373">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-373">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="78991-374">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-374">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="78991-375">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-375">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="78991-376">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-376">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="78991-377">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-377">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-378">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-378">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="78991-379">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-379">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="78991-380">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-380">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-381">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-381">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="78991-382">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-382">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="78991-383">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-383">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-384">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-384">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="78991-385">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-385">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="78991-386">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-386">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="78991-387">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-387">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="78991-388">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-388">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="78991-389">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-389">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="78991-390">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-390">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-391">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-391">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-392">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-392">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="78991-393">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-393">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="78991-394">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-394">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="78991-395">**page**</span><span class="sxs-lookup"><span data-stu-id="78991-395">**page**</span></span>

<span data-ttu-id="78991-396">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-396">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="78991-397">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-397">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="78991-398">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-398">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="78991-399">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="78991-399">**viewimports**</span></span>

<span data-ttu-id="78991-400">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-400">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="78991-401">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-401">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="78991-402">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="78991-402">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="78991-403">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="78991-403">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="78991-404">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-404">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-405">**classlib**</span><span class="sxs-lookup"><span data-stu-id="78991-405">**classlib**</span></span>

<span data-ttu-id="78991-406">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-406">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="78991-407">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="78991-407">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="78991-408">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-408">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="78991-409">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-409">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-410">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="78991-410">**mstest, xunit**</span></span>

<span data-ttu-id="78991-411">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-411">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="78991-412">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-412">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-413">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="78991-413">**globaljson**</span></span>

<span data-ttu-id="78991-414">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-414">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="78991-415">**web**</span><span class="sxs-lookup"><span data-stu-id="78991-415">**web**</span></span>

<span data-ttu-id="78991-416">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-416">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="78991-417">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-417">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-418">**webapi**</span><span class="sxs-lookup"><span data-stu-id="78991-418">**webapi**</span></span>

<span data-ttu-id="78991-419">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-419">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="78991-420">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-420">The possible values are:</span></span>

- <span data-ttu-id="78991-421">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="78991-421">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="78991-422">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-422">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="78991-423">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-423">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="78991-424">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-424">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="78991-425">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-425">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="78991-426">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-426">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-427">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-427">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="78991-428">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-428">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="78991-429">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-429">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-430">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-430">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="78991-431">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-431">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-432">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-432">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="78991-433">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-433">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="78991-434">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-434">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-435">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-435">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="78991-436">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-436">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="78991-437">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-437">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-438">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-438">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="78991-439">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-439">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="78991-440">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-440">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-441">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-441">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="78991-442">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-442">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="78991-443">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-443">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="78991-444">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-444">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="78991-445">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-445">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="78991-446">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-446">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-447">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-447">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-448">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="78991-448">**mvc, razor**</span></span>

<span data-ttu-id="78991-449">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-449">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="78991-450">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-450">The possible values are:</span></span>

- <span data-ttu-id="78991-451">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="78991-451">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="78991-452">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-452">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="78991-453">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-453">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="78991-454">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-454">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="78991-455">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-455">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="78991-456">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-456">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="78991-457">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-457">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="78991-458">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-458">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-459">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-459">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="78991-460">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-460">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="78991-461">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-461">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-462">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-462">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="78991-463">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-463">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-464">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-464">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="78991-465">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-465">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-466">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-466">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="78991-467">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-467">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="78991-468">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-468">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="78991-469">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-469">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="78991-470">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-470">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="78991-471">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-471">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="78991-472">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-472">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="78991-473">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-473">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-474">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-474">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="78991-475">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-475">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="78991-476">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-476">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="78991-477">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-477">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="78991-478">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-478">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="78991-479">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-479">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="78991-480">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-480">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="78991-481">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-481">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="78991-482">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-482">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="78991-483">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-483">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="78991-484">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-484">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="78991-485">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-485">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="78991-486">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="78991-486">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="78991-487">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78991-487">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="78991-488">**page**</span><span class="sxs-lookup"><span data-stu-id="78991-488">**page**</span></span>

<span data-ttu-id="78991-489">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-489">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="78991-490">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-490">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="78991-491">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-491">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="78991-492">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="78991-492">**viewimports**</span></span>

<span data-ttu-id="78991-493">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-493">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="78991-494">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-494">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="78991-495">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="78991-495">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="78991-496">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="78991-496">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="78991-497">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-497">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="78991-498">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="78991-498">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="78991-499">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-499">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="78991-500">**classlib**</span><span class="sxs-lookup"><span data-stu-id="78991-500">**classlib**</span></span>

<span data-ttu-id="78991-501">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-501">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="78991-502">값: `netcoreapp1.0`, `netcoreapp1.1` 또는 `netstandard1.0`~`netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="78991-502">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="78991-503">기본값은 `netstandard1.4`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-503">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="78991-504">**mvc**</span><span class="sxs-lookup"><span data-stu-id="78991-504">**mvc**</span></span>

<span data-ttu-id="78991-505">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-505">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="78991-506">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="78991-506">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="78991-507">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-507">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="78991-508">`-au|--auth` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-508">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="78991-509">값: `None` 또는 `Individual`.</span><span class="sxs-lookup"><span data-stu-id="78991-509">Values: `None` or `Individual`.</span></span> <span data-ttu-id="78991-510">기본값은 `None`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-510">The default value is `None`.</span></span>

<span data-ttu-id="78991-511">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-511">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="78991-512">값: `true` 또는 `false`.</span><span class="sxs-lookup"><span data-stu-id="78991-512">Values: `true` or `false`.</span></span> <span data-ttu-id="78991-513">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="78991-513">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="78991-514">예제</span><span class="sxs-lookup"><span data-stu-id="78991-514">Examples</span></span>

<span data-ttu-id="78991-515">현재 디렉터리에 F# 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-515">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="78991-516">지정된 디렉터리에서 .NET Standard 클래스 라이브러리 프로젝트를 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="78991-516">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="78991-517">인증 없이 현재 디렉터리에 새 ASP.NET Core C# MVC 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-517">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="78991-518">새 xUnit 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78991-518">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="78991-519">MVC에 대해 사용할 수 있는 모든 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="78991-519">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="78991-520">ASP.NET Core용 단일 페이지 응용 프로그램 템플릿 버전 2.0을 설치합니다(.NET Core SDK 1.1 및 이후 버전에서만 사용할 수 있는 명령 옵션).</span><span class="sxs-lookup"><span data-stu-id="78991-520">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="78991-521">현재 디렉터리에서 SDK 버전을 2.0.0으로 설정하여 *global.json*을 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="78991-521">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="78991-522">참고 항목</span><span class="sxs-lookup"><span data-stu-id="78991-522">See also</span></span>

* [<span data-ttu-id="78991-523">dotnet new에 대한 사용자 지정 템플릿</span><span class="sxs-lookup"><span data-stu-id="78991-523">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="78991-524">dotnet용 사용자 지정 템플릿 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="78991-524">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* <span data-ttu-id="78991-525">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)(dotnet/dotnet-template-samples GitHub 리포지토리)</span><span class="sxs-lookup"><span data-stu-id="78991-525">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)</span></span>  
* <span data-ttu-id="78991-526">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)(dotnet new에 대한 사용 가능한 템플릿)</span><span class="sxs-lookup"><span data-stu-id="78991-526">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)</span></span>
