---
title: dotnet new 명령 - .NET Core CLI
description: dotnet new 명령은 지정된 템플릿을 기반으로 새 .NET Core 프로젝트를 만듭니다.
author: mairaw
ms.author: mairaw
ms.date: 10/24/2018
ms.openlocfilehash: 56d76f1dd54097f9cf20129d74057235290c273c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188206"
---
# <a name="dotnet-new"></a><span data-ttu-id="dcf00-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="dcf00-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="dcf00-104">name</span><span class="sxs-lookup"><span data-stu-id="dcf00-104">Name</span></span>

<span data-ttu-id="dcf00-105">`dotnet new` - 지정된 템플릿을 기반으로 새 프로젝트, 구성 파일 또는 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="dcf00-106">개요</span><span class="sxs-lookup"><span data-stu-id="dcf00-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="dcf00-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="dcf00-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="dcf00-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="dcf00-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="dcf00-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="dcf00-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="dcf00-110">설명</span><span class="sxs-lookup"><span data-stu-id="dcf00-110">Description</span></span>

<span data-ttu-id="dcf00-111">`dotnet new` 명령은 유효한 .NET Core 프로젝트를 초기화하는 편리한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="dcf00-112">이 명령은 [템플릿 엔진](https://github.com/dotnet/templating)을 호출하여 지정된 템플릿 및 옵션을 기반으로 디스크에 아티팩트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="dcf00-113">인수</span><span class="sxs-lookup"><span data-stu-id="dcf00-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="dcf00-114">명령이 호출될 때 인스턴스화할 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="dcf00-115">각 템플릿에는 전달할 수 있는 특정 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="dcf00-116">자세한 내용은 [템플릿 옵션](#template-options)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="dcf00-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="dcf00-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="dcf00-118">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-118">The command contains a default list of templates.</span></span> <span data-ttu-id="dcf00-119">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="dcf00-120">다음 표에는 .NET Core SDK 2.1.300과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="dcf00-121">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="dcf00-122">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="dcf00-122">Template description</span></span>                          | <span data-ttu-id="dcf00-123">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="dcf00-123">Template name</span></span>    | <span data-ttu-id="dcf00-124">언어</span><span class="sxs-lookup"><span data-stu-id="dcf00-124">Languages</span></span>     |
|----------------------------------------------|------------------|---------------|
| <span data-ttu-id="dcf00-125">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="dcf00-125">Console application</span></span>                          | `console`        | <span data-ttu-id="dcf00-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-127">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="dcf00-127">Class library</span></span>                                | `classlib`       | <span data-ttu-id="dcf00-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-129">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="dcf00-129">Unit test project</span></span>                            | `mstest`         | <span data-ttu-id="dcf00-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-131">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="dcf00-131">xUnit test project</span></span>                           | `xunit`          | <span data-ttu-id="dcf00-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-133">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="dcf00-133">Razor page</span></span>                                   | `page`           | <span data-ttu-id="dcf00-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-134">[C#]</span></span>          |
| <span data-ttu-id="dcf00-135">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="dcf00-135">MVC ViewImports</span></span>                              | `viewimports`    | <span data-ttu-id="dcf00-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-136">[C#]</span></span>          |
| <span data-ttu-id="dcf00-137">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="dcf00-137">MVC ViewStart</span></span>                                | `viewstart`      | <span data-ttu-id="dcf00-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-138">[C#]</span></span>          |
| <span data-ttu-id="dcf00-139">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="dcf00-139">ASP.NET Core empty</span></span>                           | `web`            | <span data-ttu-id="dcf00-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-140">[C#], F#</span></span>      |
| <span data-ttu-id="dcf00-141">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="dcf00-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`            | <span data-ttu-id="dcf00-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-142">[C#], F#</span></span>      |
| <span data-ttu-id="dcf00-143">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="dcf00-143">ASP.NET Core Web App</span></span>                         | <span data-ttu-id="dcf00-144">`razor`, `webapp`</span><span class="sxs-lookup"><span data-stu-id="dcf00-144">`razor`, `webapp`</span></span>| <span data-ttu-id="dcf00-145">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-145">[C#]</span></span>          |
| <span data-ttu-id="dcf00-146">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="dcf00-146">ASP.NET Core with Angular</span></span>                    | `angular`        | <span data-ttu-id="dcf00-147">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-147">[C#]</span></span>          |
| <span data-ttu-id="dcf00-148">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="dcf00-148">ASP.NET Core with React.js</span></span>                   | `react`          | <span data-ttu-id="dcf00-149">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-149">[C#]</span></span>          |
| <span data-ttu-id="dcf00-150">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="dcf00-150">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`     | <span data-ttu-id="dcf00-151">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-151">[C#]</span></span>          |
| <span data-ttu-id="dcf00-152">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="dcf00-152">ASP.NET Core Web API</span></span>                         | `webapi`         | <span data-ttu-id="dcf00-153">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-153">[C#], F#</span></span>      |
| <span data-ttu-id="dcf00-154">Razor 클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="dcf00-154">Razor class library</span></span>                          | `razorclasslib`  | <span data-ttu-id="dcf00-155">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-155">[C#]</span></span>          |
| <span data-ttu-id="dcf00-156">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="dcf00-156">global.json file</span></span>                             | `globaljson`     |               |
| <span data-ttu-id="dcf00-157">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="dcf00-157">NuGet config</span></span>                                 | `nugetconfig`    |               |
| <span data-ttu-id="dcf00-158">웹 구성</span><span class="sxs-lookup"><span data-stu-id="dcf00-158">Web config</span></span>                                   | `webconfig`      |               |
| <span data-ttu-id="dcf00-159">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="dcf00-159">Solution file</span></span>                                | `sln`            |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="dcf00-160">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="dcf00-160">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="dcf00-161">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-161">The command contains a default list of templates.</span></span> <span data-ttu-id="dcf00-162">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-162">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="dcf00-163">다음 표에는 .NET Core SDK 2.0과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-163">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="dcf00-164">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-164">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="dcf00-165">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="dcf00-165">Template description</span></span>                          | <span data-ttu-id="dcf00-166">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="dcf00-166">Template name</span></span> | <span data-ttu-id="dcf00-167">언어</span><span class="sxs-lookup"><span data-stu-id="dcf00-167">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="dcf00-168">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="dcf00-168">Console application</span></span>                          | `console`     | <span data-ttu-id="dcf00-169">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-169">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-170">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="dcf00-170">Class library</span></span>                                | `classlib`    | <span data-ttu-id="dcf00-171">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-171">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-172">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="dcf00-172">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="dcf00-173">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-173">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-174">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="dcf00-174">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="dcf00-175">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="dcf00-175">[C#], F#, VB</span></span>  |
| <span data-ttu-id="dcf00-176">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="dcf00-176">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="dcf00-177">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-177">[C#], F#</span></span>      |
| <span data-ttu-id="dcf00-178">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="dcf00-178">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="dcf00-179">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-179">[C#], F#</span></span>      |
| <span data-ttu-id="dcf00-180">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="dcf00-180">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="dcf00-181">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-181">[C#]</span></span>          |
| <span data-ttu-id="dcf00-182">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="dcf00-182">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="dcf00-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-183">[C#]</span></span>          |
| <span data-ttu-id="dcf00-184">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="dcf00-184">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="dcf00-185">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-185">[C#]</span></span>          |
| <span data-ttu-id="dcf00-186">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="dcf00-186">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="dcf00-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-187">[C#]</span></span>          |
| <span data-ttu-id="dcf00-188">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="dcf00-188">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="dcf00-189">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-189">[C#], F#</span></span>      |
| <span data-ttu-id="dcf00-190">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="dcf00-190">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="dcf00-191">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="dcf00-191">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="dcf00-192">웹 구성</span><span class="sxs-lookup"><span data-stu-id="dcf00-192">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="dcf00-193">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="dcf00-193">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="dcf00-194">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="dcf00-194">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="dcf00-195">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="dcf00-195">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="dcf00-196">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="dcf00-196">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="dcf00-197">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="dcf00-197">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="dcf00-198">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-198">The command contains a default list of templates.</span></span> <span data-ttu-id="dcf00-199">`dotnet new -all`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-199">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="dcf00-200">다음 표에는 .NET Core SDK 1.x와 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-200">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="dcf00-201">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-201">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="dcf00-202">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="dcf00-202">Template description</span></span>  | <span data-ttu-id="dcf00-203">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="dcf00-203">Template name</span></span> | <span data-ttu-id="dcf00-204">언어</span><span class="sxs-lookup"><span data-stu-id="dcf00-204">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="dcf00-205">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="dcf00-205">Console application</span></span>  | `console`     | <span data-ttu-id="dcf00-206">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-206">[C#], F#</span></span>  |
| <span data-ttu-id="dcf00-207">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="dcf00-207">Class library</span></span>        | `classlib`    | <span data-ttu-id="dcf00-208">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-208">[C#], F#</span></span>  |
| <span data-ttu-id="dcf00-209">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="dcf00-209">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="dcf00-210">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-210">[C#], F#</span></span>  |
| <span data-ttu-id="dcf00-211">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="dcf00-211">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="dcf00-212">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-212">[C#], F#</span></span>  |
| <span data-ttu-id="dcf00-213">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="dcf00-213">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="dcf00-214">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-214">[C#]</span></span>      |
| <span data-ttu-id="dcf00-215">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="dcf00-215">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="dcf00-216">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="dcf00-216">[C#], F#</span></span>  |
| <span data-ttu-id="dcf00-217">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="dcf00-217">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="dcf00-218">[C#]</span><span class="sxs-lookup"><span data-stu-id="dcf00-218">[C#]</span></span>      |
| <span data-ttu-id="dcf00-219">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="dcf00-219">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="dcf00-220">웹 구성</span><span class="sxs-lookup"><span data-stu-id="dcf00-220">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="dcf00-221">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="dcf00-221">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="dcf00-222">옵션</span><span class="sxs-lookup"><span data-stu-id="dcf00-222">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="dcf00-223">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="dcf00-223">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="dcf00-224">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-224">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="dcf00-225">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-225">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="dcf00-226">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-226">Prints out help for the command.</span></span> <span data-ttu-id="dcf00-227">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-227">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="dcf00-228">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-228">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="dcf00-229">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-229">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="dcf00-230">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-230">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="dcf00-231">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-231">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="dcf00-232">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-232">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="dcf00-233">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-233">Lists templates containing the specified name.</span></span> <span data-ttu-id="dcf00-234">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-234">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="dcf00-235">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-235">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="dcf00-236">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-236">The language of the template to create.</span></span> <span data-ttu-id="dcf00-237">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="dcf00-237">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="dcf00-238">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-238">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf00-239">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-239">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="dcf00-240">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-240">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="dcf00-241">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-241">The name for the created output.</span></span> <span data-ttu-id="dcf00-242">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-242">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="dcf00-243">설치 중 사용할 NuGet 소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-243">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="dcf00-244">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-244">Location to place the generated output.</span></span> <span data-ttu-id="dcf00-245">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-245">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="dcf00-246">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-246">Filters templates based on available types.</span></span> <span data-ttu-id="dcf00-247">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-247">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="dcf00-248">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-248">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf00-249">`PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-249">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="dcf00-250">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-250">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="dcf00-251">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-251">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="dcf00-252">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="dcf00-252">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="dcf00-253">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-253">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="dcf00-254">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-254">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="dcf00-255">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-255">Prints out help for the command.</span></span> <span data-ttu-id="dcf00-256">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-256">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="dcf00-257">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-257">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="dcf00-258">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-258">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="dcf00-259">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-259">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="dcf00-260">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-260">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="dcf00-261">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-261">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="dcf00-262">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-262">Lists templates containing the specified name.</span></span> <span data-ttu-id="dcf00-263">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-263">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="dcf00-264">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-264">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="dcf00-265">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-265">The language of the template to create.</span></span> <span data-ttu-id="dcf00-266">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="dcf00-266">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="dcf00-267">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-267">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf00-268">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-268">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="dcf00-269">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-269">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="dcf00-270">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-270">The name for the created output.</span></span> <span data-ttu-id="dcf00-271">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-271">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="dcf00-272">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-272">Location to place the generated output.</span></span> <span data-ttu-id="dcf00-273">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-273">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="dcf00-274">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-274">Filters templates based on available types.</span></span> <span data-ttu-id="dcf00-275">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-275">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="dcf00-276">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-276">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf00-277">소스 `PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-277">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="dcf00-278">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-278">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="dcf00-279">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="dcf00-279">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="dcf00-280">템플릿을 제거하는 데 필요한 `PATH` 또는 `NUGET_ID` 인수를 확인할 수 없는 경우, 인수 없이 `dotnet new --uninstall`을 실행하면 설치된 모든 템플릿 및 템플릿을 제거하는 데 필요한 인수가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-280">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="dcf00-281">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="dcf00-281">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="dcf00-282">`dotnet new` 명령의 컨텍스트에서만 실행되는 경우 특정 유형의 프로젝트에 대한 모든 템플릿을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-282">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="dcf00-283">`dotnet new web -all`처럼 특정 템플릿의 컨텍스트에서 실행되는 경우 `-all`은 강제 생성 플래그로 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-283">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="dcf00-284">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-284">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="dcf00-285">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-285">Prints out help for the command.</span></span> <span data-ttu-id="dcf00-286">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-286">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="dcf00-287">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-287">Lists templates containing the specified name.</span></span> <span data-ttu-id="dcf00-288">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-288">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="dcf00-289">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-289">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="dcf00-290">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-290">The language of the template to create.</span></span> <span data-ttu-id="dcf00-291">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="dcf00-291">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="dcf00-292">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-292">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf00-293">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-293">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="dcf00-294">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-294">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="dcf00-295">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-295">The name for the created output.</span></span> <span data-ttu-id="dcf00-296">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-296">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="dcf00-297">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-297">Location to place the generated output.</span></span> <span data-ttu-id="dcf00-298">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-298">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="dcf00-299">템플릿 옵션</span><span class="sxs-lookup"><span data-stu-id="dcf00-299">Template options</span></span>

<span data-ttu-id="dcf00-300">각 프로젝트 템플릿에는 사용할 수 있는 추가 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-300">Each project template may have additional options available.</span></span> <span data-ttu-id="dcf00-301">코어 템플릿에는 다음과 같은 추가 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-301">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="dcf00-302">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="dcf00-302">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="dcf00-303">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="dcf00-303">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="dcf00-304">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-304">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-305">**classlib**</span><span class="sxs-lookup"><span data-stu-id="dcf00-305">**classlib**</span></span>

<span data-ttu-id="dcf00-306">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-306">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="dcf00-307">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="dcf00-307">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="dcf00-308">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-308">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="dcf00-309">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-309">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-310">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="dcf00-310">**mstest, xunit**</span></span>

<span data-ttu-id="dcf00-311">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-311">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="dcf00-312">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-312">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-313">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="dcf00-313">**globaljson**</span></span>

<span data-ttu-id="dcf00-314">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-314">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="dcf00-315">**web**</span><span class="sxs-lookup"><span data-stu-id="dcf00-315">**web**</span></span>

<span data-ttu-id="dcf00-316">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-316">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="dcf00-317">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-317">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-318">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-318">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="dcf00-319">이 옵션은 `IndividualAuth` 또는 `OrganizationalAuth`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-319">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="dcf00-320">**webapi**</span><span class="sxs-lookup"><span data-stu-id="dcf00-320">**webapi**</span></span>

<span data-ttu-id="dcf00-321">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-321">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="dcf00-322">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-322">The possible values are:</span></span>

- <span data-ttu-id="dcf00-323">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="dcf00-323">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="dcf00-324">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-324">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="dcf00-325">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-325">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="dcf00-326">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-326">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="dcf00-327">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-327">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="dcf00-328">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-328">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-329">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-329">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="dcf00-330">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-330">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="dcf00-331">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-331">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-332">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-332">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="dcf00-333">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-333">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-334">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-334">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="dcf00-335">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-335">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="dcf00-336">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-336">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-337">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-337">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="dcf00-338">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-338">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="dcf00-339">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-339">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-340">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-340">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="dcf00-341">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-341">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="dcf00-342">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-342">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-343">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-343">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="dcf00-344">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-344">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="dcf00-345">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-345">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="dcf00-346">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-346">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="dcf00-347">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-347">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="dcf00-348">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-348">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-349">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-349">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-350">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-350">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="dcf00-351">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-351">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="dcf00-352">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-352">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="dcf00-353">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="dcf00-353">**mvc, razor**</span></span>

<span data-ttu-id="dcf00-354">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-354">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="dcf00-355">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-355">The possible values are:</span></span>

- <span data-ttu-id="dcf00-356">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="dcf00-356">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="dcf00-357">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-357">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="dcf00-358">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-358">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="dcf00-359">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-359">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="dcf00-360">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-360">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="dcf00-361">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-361">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="dcf00-362">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-362">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="dcf00-363">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-363">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-364">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-364">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="dcf00-365">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-365">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="dcf00-366">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-366">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-367">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-367">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="dcf00-368">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-369">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-369">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="dcf00-370">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-370">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-371">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-371">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="dcf00-372">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-372">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="dcf00-373">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-373">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="dcf00-374">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-374">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="dcf00-375">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-375">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="dcf00-376">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-376">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="dcf00-377">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-377">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="dcf00-378">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-378">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-379">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-379">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="dcf00-380">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-380">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="dcf00-381">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-381">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-382">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-382">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="dcf00-383">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-383">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="dcf00-384">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-384">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-385">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-385">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="dcf00-386">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-386">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="dcf00-387">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-387">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="dcf00-388">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-388">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="dcf00-389">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-389">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="dcf00-390">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-390">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="dcf00-391">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-391">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-392">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-392">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-393">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-393">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="dcf00-394">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-394">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="dcf00-395">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-395">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="dcf00-396">**page**</span><span class="sxs-lookup"><span data-stu-id="dcf00-396">**page**</span></span>

<span data-ttu-id="dcf00-397">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-397">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="dcf00-398">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-398">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="dcf00-399">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-399">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="dcf00-400">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="dcf00-400">**viewimports**</span></span>

<span data-ttu-id="dcf00-401">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-401">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="dcf00-402">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-402">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="dcf00-403">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="dcf00-403">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="dcf00-404">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="dcf00-404">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="dcf00-405">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-405">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-406">**classlib**</span><span class="sxs-lookup"><span data-stu-id="dcf00-406">**classlib**</span></span>

<span data-ttu-id="dcf00-407">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-407">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="dcf00-408">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="dcf00-408">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="dcf00-409">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-409">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="dcf00-410">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-410">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-411">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="dcf00-411">**mstest, xunit**</span></span>

<span data-ttu-id="dcf00-412">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-412">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="dcf00-413">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-413">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-414">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="dcf00-414">**globaljson**</span></span>

<span data-ttu-id="dcf00-415">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-415">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="dcf00-416">**web**</span><span class="sxs-lookup"><span data-stu-id="dcf00-416">**web**</span></span>

<span data-ttu-id="dcf00-417">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-417">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="dcf00-418">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-418">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-419">**webapi**</span><span class="sxs-lookup"><span data-stu-id="dcf00-419">**webapi**</span></span>

<span data-ttu-id="dcf00-420">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-420">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="dcf00-421">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-421">The possible values are:</span></span>

- <span data-ttu-id="dcf00-422">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="dcf00-422">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="dcf00-423">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-423">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="dcf00-424">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-424">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="dcf00-425">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-425">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="dcf00-426">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-426">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="dcf00-427">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-427">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-428">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-428">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="dcf00-429">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-429">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="dcf00-430">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-430">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-431">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-431">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="dcf00-432">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-432">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-433">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-433">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="dcf00-434">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-434">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="dcf00-435">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-435">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-436">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-436">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="dcf00-437">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-437">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="dcf00-438">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-438">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-439">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-439">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="dcf00-440">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-440">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="dcf00-441">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-441">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-442">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-442">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="dcf00-443">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-443">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="dcf00-444">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-444">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="dcf00-445">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-445">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="dcf00-446">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-446">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="dcf00-447">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-447">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-448">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-448">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-449">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="dcf00-449">**mvc, razor**</span></span>

<span data-ttu-id="dcf00-450">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-450">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="dcf00-451">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-451">The possible values are:</span></span>

- <span data-ttu-id="dcf00-452">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="dcf00-452">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="dcf00-453">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-453">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="dcf00-454">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-454">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="dcf00-455">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-455">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="dcf00-456">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-456">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="dcf00-457">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-457">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="dcf00-458">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-458">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="dcf00-459">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-459">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-460">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-460">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="dcf00-461">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-461">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="dcf00-462">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-462">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-463">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-463">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="dcf00-464">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-465">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-465">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="dcf00-466">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-466">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-467">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-467">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="dcf00-468">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-468">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="dcf00-469">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-469">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="dcf00-470">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-470">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="dcf00-471">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-471">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="dcf00-472">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-472">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="dcf00-473">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-473">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="dcf00-474">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-474">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-475">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-475">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="dcf00-476">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-476">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="dcf00-477">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-477">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="dcf00-478">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-478">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="dcf00-479">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-479">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="dcf00-480">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-480">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="dcf00-481">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-481">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="dcf00-482">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-482">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="dcf00-483">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-483">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="dcf00-484">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-484">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="dcf00-485">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-485">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="dcf00-486">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-486">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="dcf00-487">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-487">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="dcf00-488">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-488">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="dcf00-489">**page**</span><span class="sxs-lookup"><span data-stu-id="dcf00-489">**page**</span></span>

<span data-ttu-id="dcf00-490">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-490">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="dcf00-491">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-491">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="dcf00-492">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-492">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="dcf00-493">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="dcf00-493">**viewimports**</span></span>

<span data-ttu-id="dcf00-494">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-494">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="dcf00-495">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-495">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="dcf00-496">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="dcf00-496">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="dcf00-497">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="dcf00-497">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="dcf00-498">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-498">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="dcf00-499">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="dcf00-499">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="dcf00-500">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-500">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="dcf00-501">**classlib**</span><span class="sxs-lookup"><span data-stu-id="dcf00-501">**classlib**</span></span>

<span data-ttu-id="dcf00-502">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-502">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="dcf00-503">값: `netcoreapp1.0`, `netcoreapp1.1` 또는 `netstandard1.0`~`netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="dcf00-503">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="dcf00-504">기본값은 `netstandard1.4`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-504">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="dcf00-505">**mvc**</span><span class="sxs-lookup"><span data-stu-id="dcf00-505">**mvc**</span></span>

<span data-ttu-id="dcf00-506">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-506">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="dcf00-507">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="dcf00-507">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="dcf00-508">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-508">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="dcf00-509">`-au|--auth` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-509">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="dcf00-510">값: `None` 또는 `Individual`.</span><span class="sxs-lookup"><span data-stu-id="dcf00-510">Values: `None` or `Individual`.</span></span> <span data-ttu-id="dcf00-511">기본값은 `None`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-511">The default value is `None`.</span></span>

<span data-ttu-id="dcf00-512">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-512">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="dcf00-513">값: `true` 또는 `false`.</span><span class="sxs-lookup"><span data-stu-id="dcf00-513">Values: `true` or `false`.</span></span> <span data-ttu-id="dcf00-514">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-514">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="dcf00-515">예제</span><span class="sxs-lookup"><span data-stu-id="dcf00-515">Examples</span></span>

<span data-ttu-id="dcf00-516">현재 디렉터리에 F# 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-516">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="dcf00-517">지정된 디렉터리에서 .NET Standard 클래스 라이브러리 프로젝트를 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="dcf00-517">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="dcf00-518">인증 없이 현재 디렉터리에 새 ASP.NET Core C# MVC 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-518">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="dcf00-519">새 xUnit 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-519">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="dcf00-520">MVC에 대해 사용할 수 있는 모든 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dcf00-520">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="dcf00-521">ASP.NET Core용 단일 페이지 응용 프로그램 템플릿 버전 2.0을 설치합니다(.NET Core SDK 1.1 및 이후 버전에서만 사용할 수 있는 명령 옵션).</span><span class="sxs-lookup"><span data-stu-id="dcf00-521">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="dcf00-522">현재 디렉터리에서 SDK 버전을 2.0.0으로 설정하여 *global.json*을 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="dcf00-522">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="dcf00-523">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dcf00-523">See also</span></span>

* [<span data-ttu-id="dcf00-524">dotnet new에 대한 사용자 지정 템플릿</span><span class="sxs-lookup"><span data-stu-id="dcf00-524">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="dcf00-525">dotnet용 사용자 지정 템플릿 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="dcf00-525">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* <span data-ttu-id="dcf00-526">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)(dotnet/dotnet-template-samples GitHub 리포지토리)</span><span class="sxs-lookup"><span data-stu-id="dcf00-526">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)</span></span>  
* <span data-ttu-id="dcf00-527">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)(dotnet new에 대한 사용 가능한 템플릿)</span><span class="sxs-lookup"><span data-stu-id="dcf00-527">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)</span></span>
