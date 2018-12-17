---
title: dotnet new 명령 - .NET Core CLI
description: dotnet new 명령은 지정된 템플릿을 기반으로 새 .NET Core 프로젝트를 만듭니다.
author: mairaw
ms.author: mairaw
ms.date: 10/24/2018
ms.openlocfilehash: a8d486f569f31d68d5659ac6a80d615474ef2506
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131484"
---
# <a name="dotnet-new"></a><span data-ttu-id="c9817-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="c9817-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="c9817-104">name</span><span class="sxs-lookup"><span data-stu-id="c9817-104">Name</span></span>

<span data-ttu-id="c9817-105">`dotnet new` - 지정된 템플릿을 기반으로 새 프로젝트, 구성 파일 또는 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="c9817-106">개요</span><span class="sxs-lookup"><span data-stu-id="c9817-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="c9817-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="c9817-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="c9817-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c9817-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="c9817-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="c9817-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="c9817-110">설명</span><span class="sxs-lookup"><span data-stu-id="c9817-110">Description</span></span>

<span data-ttu-id="c9817-111">`dotnet new` 명령은 유효한 .NET Core 프로젝트를 초기화하는 편리한 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="c9817-112">이 명령은 [템플릿 엔진](https://github.com/dotnet/templating)을 호출하여 지정된 템플릿 및 옵션을 기반으로 디스크에 아티팩트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="c9817-113">인수</span><span class="sxs-lookup"><span data-stu-id="c9817-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="c9817-114">명령이 호출될 때 인스턴스화할 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="c9817-115">각 템플릿에는 전달할 수 있는 특정 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="c9817-116">자세한 내용은 [템플릿 옵션](#template-options)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="c9817-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="c9817-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="c9817-118">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-118">The command contains a default list of templates.</span></span> <span data-ttu-id="c9817-119">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="c9817-120">다음 표에는 .NET Core SDK 2.1.300과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="c9817-121">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="c9817-122">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="c9817-122">Template description</span></span>                          | <span data-ttu-id="c9817-123">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="c9817-123">Template name</span></span>    | <span data-ttu-id="c9817-124">언어</span><span class="sxs-lookup"><span data-stu-id="c9817-124">Languages</span></span>     |
|----------------------------------------------|------------------|---------------|
| <span data-ttu-id="c9817-125">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c9817-125">Console application</span></span>                          | `console`        | <span data-ttu-id="c9817-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-127">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="c9817-127">Class library</span></span>                                | `classlib`       | <span data-ttu-id="c9817-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-129">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-129">Unit test project</span></span>                            | `mstest`         | <span data-ttu-id="c9817-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-131">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-131">xUnit test project</span></span>                           | `xunit`          | <span data-ttu-id="c9817-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-133">NUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-133">NUnit test project</span></span>                           | `nunit`          | <span data-ttu-id="c9817-134">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-134">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-135">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="c9817-135">Razor page</span></span>                                   | `page`           | <span data-ttu-id="c9817-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-136">[C#]</span></span>          |
| <span data-ttu-id="c9817-137">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="c9817-137">MVC ViewImports</span></span>                              | `viewimports`    | <span data-ttu-id="c9817-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-138">[C#]</span></span>          |
| <span data-ttu-id="c9817-139">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="c9817-139">MVC ViewStart</span></span>                                | `viewstart`      | <span data-ttu-id="c9817-140">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-140">[C#]</span></span>          |
| <span data-ttu-id="c9817-141">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="c9817-141">ASP.NET Core empty</span></span>                           | `web`            | <span data-ttu-id="c9817-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-142">[C#], F#</span></span>      |
| <span data-ttu-id="c9817-143">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="c9817-143">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`            | <span data-ttu-id="c9817-144">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-144">[C#], F#</span></span>      |
| <span data-ttu-id="c9817-145">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="c9817-145">ASP.NET Core Web App</span></span>                         | <span data-ttu-id="c9817-146">`razor`, `webapp`</span><span class="sxs-lookup"><span data-stu-id="c9817-146">`razor`, `webapp`</span></span>| <span data-ttu-id="c9817-147">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-147">[C#]</span></span>          |
| <span data-ttu-id="c9817-148">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="c9817-148">ASP.NET Core with Angular</span></span>                    | `angular`        | <span data-ttu-id="c9817-149">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-149">[C#]</span></span>          |
| <span data-ttu-id="c9817-150">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="c9817-150">ASP.NET Core with React.js</span></span>                   | `react`          | <span data-ttu-id="c9817-151">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-151">[C#]</span></span>          |
| <span data-ttu-id="c9817-152">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="c9817-152">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`     | <span data-ttu-id="c9817-153">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-153">[C#]</span></span>          |
| <span data-ttu-id="c9817-154">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="c9817-154">ASP.NET Core Web API</span></span>                         | `webapi`         | <span data-ttu-id="c9817-155">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-155">[C#], F#</span></span>      |
| <span data-ttu-id="c9817-156">Razor 클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="c9817-156">Razor class library</span></span>                          | `razorclasslib`  | <span data-ttu-id="c9817-157">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-157">[C#]</span></span>          |
| <span data-ttu-id="c9817-158">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="c9817-158">global.json file</span></span>                             | `globaljson`     |               |
| <span data-ttu-id="c9817-159">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="c9817-159">NuGet config</span></span>                                 | `nugetconfig`    |               |
| <span data-ttu-id="c9817-160">웹 구성</span><span class="sxs-lookup"><span data-stu-id="c9817-160">Web config</span></span>                                   | `webconfig`      |               |
| <span data-ttu-id="c9817-161">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="c9817-161">Solution file</span></span>                                | `sln`            |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="c9817-162">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c9817-162">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="c9817-163">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-163">The command contains a default list of templates.</span></span> <span data-ttu-id="c9817-164">`dotnet new -l`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-164">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="c9817-165">다음 표에는 .NET Core SDK 2.0과 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-165">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="c9817-166">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-166">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="c9817-167">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="c9817-167">Template description</span></span>                          | <span data-ttu-id="c9817-168">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="c9817-168">Template name</span></span> | <span data-ttu-id="c9817-169">언어</span><span class="sxs-lookup"><span data-stu-id="c9817-169">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="c9817-170">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c9817-170">Console application</span></span>                          | `console`     | <span data-ttu-id="c9817-171">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-171">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-172">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="c9817-172">Class library</span></span>                                | `classlib`    | <span data-ttu-id="c9817-173">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-173">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-174">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-174">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="c9817-175">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-175">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-176">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-176">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="c9817-177">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="c9817-177">[C#], F#, VB</span></span>  |
| <span data-ttu-id="c9817-178">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="c9817-178">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="c9817-179">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-179">[C#], F#</span></span>      |
| <span data-ttu-id="c9817-180">ASP.NET Core 웹앱(모델-뷰-컨트롤러)</span><span class="sxs-lookup"><span data-stu-id="c9817-180">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="c9817-181">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-181">[C#], F#</span></span>      |
| <span data-ttu-id="c9817-182">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="c9817-182">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="c9817-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-183">[C#]</span></span>          |
| <span data-ttu-id="c9817-184">ASP.NET Core(Angular 사용)</span><span class="sxs-lookup"><span data-stu-id="c9817-184">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="c9817-185">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-185">[C#]</span></span>          |
| <span data-ttu-id="c9817-186">ASP.NET Core(React.js 사용)</span><span class="sxs-lookup"><span data-stu-id="c9817-186">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="c9817-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-187">[C#]</span></span>          |
| <span data-ttu-id="c9817-188">ASP.NET Core(React.js 및 Redux 사용)</span><span class="sxs-lookup"><span data-stu-id="c9817-188">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="c9817-189">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-189">[C#]</span></span>          |
| <span data-ttu-id="c9817-190">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="c9817-190">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="c9817-191">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-191">[C#], F#</span></span>      |
| <span data-ttu-id="c9817-192">global.json 파일</span><span class="sxs-lookup"><span data-stu-id="c9817-192">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="c9817-193">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="c9817-193">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="c9817-194">웹 구성</span><span class="sxs-lookup"><span data-stu-id="c9817-194">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="c9817-195">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="c9817-195">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="c9817-196">Razor 페이지</span><span class="sxs-lookup"><span data-stu-id="c9817-196">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="c9817-197">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="c9817-197">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="c9817-198">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="c9817-198">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="c9817-199">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="c9817-199">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="c9817-200">명령에는 템플릿의 기본 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-200">The command contains a default list of templates.</span></span> <span data-ttu-id="c9817-201">`dotnet new -all`을 사용하여 사용 가능한 템플릿 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-201">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="c9817-202">다음 표에는 .NET Core SDK 1.x와 함께 사전 설치된 템플릿이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-202">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="c9817-203">템플릿의 기본 언어는 대괄호 안에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-203">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="c9817-204">템플릿 설명</span><span class="sxs-lookup"><span data-stu-id="c9817-204">Template description</span></span>  | <span data-ttu-id="c9817-205">템플릿 이름</span><span class="sxs-lookup"><span data-stu-id="c9817-205">Template name</span></span> | <span data-ttu-id="c9817-206">언어</span><span class="sxs-lookup"><span data-stu-id="c9817-206">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="c9817-207">콘솔 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="c9817-207">Console application</span></span>  | `console`     | <span data-ttu-id="c9817-208">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-208">[C#], F#</span></span>  |
| <span data-ttu-id="c9817-209">클래스 라이브러리</span><span class="sxs-lookup"><span data-stu-id="c9817-209">Class library</span></span>        | `classlib`    | <span data-ttu-id="c9817-210">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-210">[C#], F#</span></span>  |
| <span data-ttu-id="c9817-211">단위 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-211">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="c9817-212">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-212">[C#], F#</span></span>  |
| <span data-ttu-id="c9817-213">xUnit 테스트 프로젝트</span><span class="sxs-lookup"><span data-stu-id="c9817-213">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="c9817-214">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-214">[C#], F#</span></span>  |
| <span data-ttu-id="c9817-215">ASP.NET Core 비어 있음</span><span class="sxs-lookup"><span data-stu-id="c9817-215">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="c9817-216">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-216">[C#]</span></span>      |
| <span data-ttu-id="c9817-217">ASP.NET Core 웹앱</span><span class="sxs-lookup"><span data-stu-id="c9817-217">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="c9817-218">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="c9817-218">[C#], F#</span></span>  |
| <span data-ttu-id="c9817-219">ASP.NET Core 웹 API</span><span class="sxs-lookup"><span data-stu-id="c9817-219">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="c9817-220">[C#]</span><span class="sxs-lookup"><span data-stu-id="c9817-220">[C#]</span></span>      |
| <span data-ttu-id="c9817-221">NuGet 구성</span><span class="sxs-lookup"><span data-stu-id="c9817-221">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="c9817-222">웹 구성</span><span class="sxs-lookup"><span data-stu-id="c9817-222">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="c9817-223">솔루션 파일</span><span class="sxs-lookup"><span data-stu-id="c9817-223">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="c9817-224">옵션</span><span class="sxs-lookup"><span data-stu-id="c9817-224">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="c9817-225">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="c9817-225">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="c9817-226">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-226">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="c9817-227">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-227">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="c9817-228">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-228">Prints out help for the command.</span></span> <span data-ttu-id="c9817-229">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-229">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="c9817-230">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-230">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="c9817-231">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-231">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="c9817-232">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-232">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="c9817-233">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-233">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="c9817-234">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-234">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="c9817-235">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-235">Lists templates containing the specified name.</span></span> <span data-ttu-id="c9817-236">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-236">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="c9817-237">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-237">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="c9817-238">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-238">The language of the template to create.</span></span> <span data-ttu-id="c9817-239">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="c9817-239">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="c9817-240">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-240">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="c9817-241">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-241">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="c9817-242">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-242">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="c9817-243">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-243">The name for the created output.</span></span> <span data-ttu-id="c9817-244">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-244">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="c9817-245">설치 중 사용할 NuGet 소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-245">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="c9817-246">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-246">Location to place the generated output.</span></span> <span data-ttu-id="c9817-247">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-247">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="c9817-248">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-248">Filters templates based on available types.</span></span> <span data-ttu-id="c9817-249">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-249">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="c9817-250">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-250">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="c9817-251">`PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-251">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="c9817-252">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-252">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="c9817-253">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-253">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="c9817-254">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c9817-254">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="c9817-255">기존 파일을 변경할 경우에도 콘텐츠를 강제 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-255">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="c9817-256">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-256">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="c9817-257">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-257">Prints out help for the command.</span></span> <span data-ttu-id="c9817-258">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-258">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="c9817-259">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-259">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="c9817-260">시험판 버전의 템플릿 패키지를 설치하려면 버전을 `<package-name>::<package-version>` 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-260">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="c9817-261">기본적으로 `dotnet new`는 마지막 안정 패키지 버전을 나타내는 버전에 대해 \*를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-261">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="c9817-262">[예제](#examples) 섹션의 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-262">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="c9817-263">사용자 지정 템플릿을 만드는 방법에 대한 자세한 내용은 [dotnet new에 대한 사용자 지정 템플릿](custom-templates.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-263">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="c9817-264">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-264">Lists templates containing the specified name.</span></span> <span data-ttu-id="c9817-265">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-265">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="c9817-266">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-266">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="c9817-267">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-267">The language of the template to create.</span></span> <span data-ttu-id="c9817-268">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="c9817-268">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="c9817-269">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-269">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="c9817-270">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-270">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="c9817-271">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-271">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="c9817-272">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-272">The name for the created output.</span></span> <span data-ttu-id="c9817-273">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-273">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="c9817-274">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-274">Location to place the generated output.</span></span> <span data-ttu-id="c9817-275">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-275">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="c9817-276">사용 가능한 형식에 따라 템플릿을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-276">Filters templates based on available types.</span></span> <span data-ttu-id="c9817-277">미리 정의된 값은 “project”, “item” 또는 “other”입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-277">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="c9817-278">제공된 `PATH` 또는 `NUGET_ID`에서 소스 또는 템플릿 팩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-278">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="c9817-279">소스 `PATH`를 사용하여 템플릿을 제거하려면 경로를 정규화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-279">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="c9817-280">예를 들어 *C:/Users/\<사용자>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지만 상위 폴더의 *./GarciaSoftware.ConsoleTemplate.CSharp*는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-280">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="c9817-281">마지막의 종료하는 디렉터리 슬래시도 템플릿 경로에 포함하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c9817-281">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="c9817-282">템플릿을 제거하는 데 필요한 `PATH` 또는 `NUGET_ID` 인수를 확인할 수 없는 경우, 인수 없이 `dotnet new --uninstall`을 실행하면 설치된 모든 템플릿 및 템플릿을 제거하는 데 필요한 인수가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-282">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="c9817-283">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="c9817-283">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="c9817-284">`dotnet new` 명령의 컨텍스트에서만 실행되는 경우 특정 유형의 프로젝트에 대한 모든 템플릿을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-284">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="c9817-285">`dotnet new web -all`처럼 특정 템플릿의 컨텍스트에서 실행되는 경우 `-all`은 강제 생성 플래그로 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-285">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="c9817-286">출력 디렉터리에 이미 프로젝트가 포함되어 있는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-286">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="c9817-287">명령에 대한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-287">Prints out help for the command.</span></span> <span data-ttu-id="c9817-288">`dotnet new` 명령 자체 또는 `dotnet new mvc --help` 같은 템플릿에 대해 호출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-288">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="c9817-289">지정된 이름을 포함하는 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-289">Lists templates containing the specified name.</span></span> <span data-ttu-id="c9817-290">`dotnet new` 명령에 대해 호출되는 경우 지정된 디렉터리에서 사용 가능한 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-290">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="c9817-291">예를 들어 디렉터리에 이미 프로젝트가 포함되어 있는 경우 일부 프로젝트 템플릿을 나열하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-291">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="c9817-292">만들 템플릿의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-292">The language of the template to create.</span></span> <span data-ttu-id="c9817-293">허용되는 언어는 템플릿에 따라 다릅니다([인수](#arguments) 섹션에서 기본값 참조).</span><span class="sxs-lookup"><span data-stu-id="c9817-293">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="c9817-294">일부 템플릿의 경우 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-294">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="c9817-295">일부 셸은 `#`을 특수 문자로 해석합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-295">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="c9817-296">이러한 경우 `dotnet new console -lang "F#"`과 같은 언어 매개 변수 값을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-296">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="c9817-297">생성된 출력에 대한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-297">The name for the created output.</span></span> <span data-ttu-id="c9817-298">이름을 지정하지 않으면 현재 디렉터리의 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-298">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="c9817-299">생성된 출력을 배치할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-299">Location to place the generated output.</span></span> <span data-ttu-id="c9817-300">기본값은 현재 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-300">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="c9817-301">템플릿 옵션</span><span class="sxs-lookup"><span data-stu-id="c9817-301">Template options</span></span>

<span data-ttu-id="c9817-302">각 프로젝트 템플릿에는 사용할 수 있는 추가 옵션이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-302">Each project template may have additional options available.</span></span> <span data-ttu-id="c9817-303">코어 템플릿에는 다음과 같은 추가 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-303">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="c9817-304">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="c9817-304">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="c9817-305">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="c9817-305">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="c9817-306">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-306">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-307">**classlib**</span><span class="sxs-lookup"><span data-stu-id="c9817-307">**classlib**</span></span>

<span data-ttu-id="c9817-308">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-308">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="c9817-309">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="c9817-309">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="c9817-310">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-310">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="c9817-311">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-311">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-312">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="c9817-312">**mstest, xunit**</span></span>

<span data-ttu-id="c9817-313">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-313">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="c9817-314">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-314">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-315">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="c9817-315">**globaljson**</span></span>

<span data-ttu-id="c9817-316">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-316">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="c9817-317">**web**</span><span class="sxs-lookup"><span data-stu-id="c9817-317">**web**</span></span>

<span data-ttu-id="c9817-318">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-318">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="c9817-319">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-319">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-320">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-320">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="c9817-321">이 옵션은 `IndividualAuth` 또는 `OrganizationalAuth`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-321">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="c9817-322">**webapi**</span><span class="sxs-lookup"><span data-stu-id="c9817-322">**webapi**</span></span>

<span data-ttu-id="c9817-323">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-323">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="c9817-324">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-324">The possible values are:</span></span>

- <span data-ttu-id="c9817-325">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="c9817-325">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="c9817-326">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-326">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="c9817-327">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-327">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="c9817-328">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-328">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="c9817-329">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-329">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="c9817-330">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-330">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-331">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-331">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="c9817-332">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-332">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="c9817-333">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-333">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-334">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-334">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="c9817-335">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-335">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-336">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-336">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="c9817-337">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-337">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="c9817-338">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-338">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-339">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-339">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="c9817-340">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-340">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="c9817-341">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-341">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-342">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-342">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="c9817-343">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-343">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="c9817-344">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-344">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-345">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-345">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="c9817-346">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-346">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="c9817-347">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-347">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="c9817-348">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-348">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="c9817-349">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-349">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="c9817-350">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-350">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-351">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-351">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-352">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-352">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="c9817-353">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-353">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="c9817-354">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-354">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="c9817-355">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="c9817-355">**mvc, razor**</span></span>

<span data-ttu-id="c9817-356">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-356">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="c9817-357">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-357">The possible values are:</span></span>

- <span data-ttu-id="c9817-358">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="c9817-358">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="c9817-359">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-359">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="c9817-360">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-360">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="c9817-361">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-361">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="c9817-362">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-362">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="c9817-363">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-363">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="c9817-364">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-364">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="c9817-365">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-365">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-366">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-366">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="c9817-367">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-367">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="c9817-368">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-369">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-369">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="c9817-370">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-370">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-371">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-371">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="c9817-372">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-372">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-373">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-373">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="c9817-374">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-374">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="c9817-375">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-375">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="c9817-376">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-376">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="c9817-377">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-377">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="c9817-378">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-378">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="c9817-379">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-379">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="c9817-380">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-380">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-381">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-381">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="c9817-382">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-382">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="c9817-383">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-383">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-384">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-384">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="c9817-385">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-385">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="c9817-386">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-386">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-387">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-387">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="c9817-388">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-388">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="c9817-389">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-389">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="c9817-390">`--exclude-launch-settings` - 생성된 템플릿에서 *launchSettings.json*을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-390">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="c9817-391">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-391">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="c9817-392">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-392">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="c9817-393">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-393">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-394">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-394">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-395">`--no-https` - 프로젝트에는 HTTPS가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-395">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="c9817-396">`app.UseHsts` 및 `app.UseHttpsRedirection`은 `Startup.Configure`에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-396">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="c9817-397">이 옵션은 `Individual`, `IndividualB2C`, `SingleOrg` 또는 `MultiOrg`를 사용하지 않는 경우에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-397">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="c9817-398">**page**</span><span class="sxs-lookup"><span data-stu-id="c9817-398">**page**</span></span>

<span data-ttu-id="c9817-399">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-399">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="c9817-400">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-400">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="c9817-401">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-401">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="c9817-402">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="c9817-402">**viewimports**</span></span>

<span data-ttu-id="c9817-403">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-403">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="c9817-404">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-404">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="c9817-405">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c9817-405">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="c9817-406">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="c9817-406">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="c9817-407">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-407">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-408">**classlib**</span><span class="sxs-lookup"><span data-stu-id="c9817-408">**classlib**</span></span>

<span data-ttu-id="c9817-409">`-f|--framework <FRAMEWORK>` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-409">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="c9817-410">값: `netcoreapp2.0`(.NET Core 클래스 라이브러리를 만드는 경우) 또는 `netstandard2.0`(.NET Standard 클래스 라이브러리를 만드는 경우).</span><span class="sxs-lookup"><span data-stu-id="c9817-410">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="c9817-411">기본값은 `netstandard2.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-411">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="c9817-412">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-412">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-413">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="c9817-413">**mstest, xunit**</span></span>

<span data-ttu-id="c9817-414">`-p|--enable-pack` - [dotnet pack](dotnet-pack.md)을 사용하여 프로젝트에 대한 패키징을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-414">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="c9817-415">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-415">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-416">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="c9817-416">**globaljson**</span></span>

<span data-ttu-id="c9817-417">`--sdk-version <VERSION_NUMBER>` - *global.json* 파일에서 사용할 .NET Core SDK 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-417">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="c9817-418">**web**</span><span class="sxs-lookup"><span data-stu-id="c9817-418">**web**</span></span>

<span data-ttu-id="c9817-419">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-419">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="c9817-420">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-420">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-421">**webapi**</span><span class="sxs-lookup"><span data-stu-id="c9817-421">**webapi**</span></span>

<span data-ttu-id="c9817-422">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-422">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="c9817-423">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-423">The possible values are:</span></span>

- <span data-ttu-id="c9817-424">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="c9817-424">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="c9817-425">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-425">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="c9817-426">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-426">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="c9817-427">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-427">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="c9817-428">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-428">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="c9817-429">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-429">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-430">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-430">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="c9817-431">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-431">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="c9817-432">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-432">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-433">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-433">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="c9817-434">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-434">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-435">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-435">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="c9817-436">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-436">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="c9817-437">`IndividualB2C` 또는 `SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-437">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-438">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-438">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="c9817-439">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-439">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="c9817-440">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-440">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-441">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-441">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="c9817-442">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-442">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="c9817-443">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-443">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-444">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-444">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="c9817-445">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-445">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="c9817-446">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-446">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="c9817-447">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-447">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="c9817-448">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-448">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="c9817-449">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-449">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-450">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-450">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-451">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="c9817-451">**mvc, razor**</span></span>

<span data-ttu-id="c9817-452">`-au|--auth <AUTHENTICATION_TYPE>` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-452">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="c9817-453">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-453">The possible values are:</span></span>

- <span data-ttu-id="c9817-454">`None` - 인증하지 않습니다(기본값).</span><span class="sxs-lookup"><span data-stu-id="c9817-454">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="c9817-455">`Individual` - 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-455">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="c9817-456">`IndividualB2C` - Azure AD B2C를 사용한 개별 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-456">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="c9817-457">`SingleOrg` - 단일 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-457">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="c9817-458">`MultiOrg` - 여러 테넌트에 대한 조직적 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-458">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="c9817-459">`Windows` - Windows 인증입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-459">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="c9817-460">`--aad-b2c-instance <INSTANCE>` - 연결할 Azure Active Directory B2C 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-460">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="c9817-461">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-461">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-462">기본값은 `https://login.microsoftonline.com/tfp/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-462">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="c9817-463">`-ssp|--susi-policy-id <ID>` - 이 프로젝트에 대한 로그인 및 등록 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-463">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="c9817-464">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-465">`-rp|--reset-password-policy-id <ID>` - 이 프로젝트에 대한 암호 재설정 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-465">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="c9817-466">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-466">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-467">`-ep|--edit-profile-policy-id <ID>` - 이 프로젝트에 대한 프로필 편집 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-467">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="c9817-468">`IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-468">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-469">`--aad-instance <INSTANCE>` - 연결할 Azure Active Directory 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-469">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="c9817-470">`SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-470">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="c9817-471">기본값은 `https://login.microsoftonline.com/`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-471">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="c9817-472">`--client-id <ID>` - 이 프로젝트의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-472">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="c9817-473">`IndividualB2C`, `SingleOrg` 또는 `MultiOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-473">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="c9817-474">기본값은 `11111111-1111-1111-11111111111111111`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-474">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="c9817-475">`--domain <DOMAIN>` - 디렉터리 테넌트에 대한 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-475">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="c9817-476">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-476">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-477">기본값은 `qualified.domain.name`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-477">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="c9817-478">`--tenant-id <ID>` - 연결할 디렉터리의 TenantId ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-478">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="c9817-479">`SingleOrg` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-479">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="c9817-480">기본값은 `22222222-2222-2222-2222-222222222222`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-480">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="c9817-481">`--callback-path <PATH>` - 리디렉션 URI의 응용 프로그램 기본 경로 내 요청 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-481">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="c9817-482">`SingleOrg` 또는 `IndividualB2C` 인증과 함께 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-482">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="c9817-483">기본값은 `/signin-oidc`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-483">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="c9817-484">`-r|--org-read-access` - 디렉터리에 대한 이 응용 프로그램 읽기 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-484">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="c9817-485">`SingleOrg` 또는 `MultiOrg` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-485">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="c9817-486">`--use-launch-settings` - 생성된 템플릿 출력에 *launchSettings.json*을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-486">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="c9817-487">`--use-browserlink` - 프로젝트에 BrowserLink를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-487">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="c9817-488">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-488">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="c9817-489">`Individual` 또는 `IndividualB2C` 인증에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-489">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="c9817-490">`--no-restore` - 프로젝트를 만드는 동안 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-490">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="c9817-491">**page**</span><span class="sxs-lookup"><span data-stu-id="c9817-491">**page**</span></span>

<span data-ttu-id="c9817-492">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-492">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="c9817-493">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-493">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="c9817-494">`-np|--no-pagemodel` - PageModel 없이 페이지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-494">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="c9817-495">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="c9817-495">**viewimports**</span></span>

<span data-ttu-id="c9817-496">`-na|--namespace <NAMESPACE_NAME>` - 생성된 코드에 대한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-496">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="c9817-497">기본값은 `MyApp.Namespace`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-497">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="c9817-498">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="c9817-498">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="c9817-499">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="c9817-499">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="c9817-500">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-500">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="c9817-501">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="c9817-501">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="c9817-502">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-502">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="c9817-503">**classlib**</span><span class="sxs-lookup"><span data-stu-id="c9817-503">**classlib**</span></span>

<span data-ttu-id="c9817-504">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-504">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="c9817-505">값: `netcoreapp1.0`, `netcoreapp1.1` 또는 `netstandard1.0`~`netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="c9817-505">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="c9817-506">기본값은 `netstandard1.4`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-506">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="c9817-507">**mvc**</span><span class="sxs-lookup"><span data-stu-id="c9817-507">**mvc**</span></span>

<span data-ttu-id="c9817-508">`-f|--framework` - 대상으로 할 [프레임워크](../../standard/frameworks.md)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-508">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="c9817-509">값: `netcoreapp1.0` 또는 `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="c9817-509">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="c9817-510">기본값은 `netcoreapp1.0`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-510">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="c9817-511">`-au|--auth` - 사용할 인증 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-511">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="c9817-512">값: `None` 또는 `Individual`.</span><span class="sxs-lookup"><span data-stu-id="c9817-512">Values: `None` or `Individual`.</span></span> <span data-ttu-id="c9817-513">기본값은 `None`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-513">The default value is `None`.</span></span>

<span data-ttu-id="c9817-514">`-uld|--use-local-db` - SQLite 대신 LocalDB를 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-514">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="c9817-515">값: `true` 또는 `false`.</span><span class="sxs-lookup"><span data-stu-id="c9817-515">Values: `true` or `false`.</span></span> <span data-ttu-id="c9817-516">기본값은 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-516">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="c9817-517">예제</span><span class="sxs-lookup"><span data-stu-id="c9817-517">Examples</span></span>

<span data-ttu-id="c9817-518">현재 디렉터리에 F# 콘솔 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-518">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="c9817-519">지정된 디렉터리에서 .NET Standard 클래스 라이브러리 프로젝트를 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="c9817-519">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="c9817-520">인증 없이 현재 디렉터리에 새 ASP.NET Core C# MVC 응용 프로그램 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-520">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="c9817-521">새 xUnit 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-521">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="c9817-522">MVC에 대해 사용할 수 있는 모든 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9817-522">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="c9817-523">ASP.NET Core용 단일 페이지 응용 프로그램 템플릿 버전 2.0을 설치합니다(.NET Core SDK 1.1 및 이후 버전에서만 사용할 수 있는 명령 옵션).</span><span class="sxs-lookup"><span data-stu-id="c9817-523">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="c9817-524">현재 디렉터리에서 SDK 버전을 2.0.0으로 설정하여 *global.json*을 만듭니다(.NET Core SDK 2.0 이상 버전에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="c9817-524">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="c9817-525">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c9817-525">See also</span></span>

* [<span data-ttu-id="c9817-526">dotnet new에 대한 사용자 지정 템플릿</span><span class="sxs-lookup"><span data-stu-id="c9817-526">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="c9817-527">dotnet용 사용자 지정 템플릿 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="c9817-527">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* <span data-ttu-id="c9817-528">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)(dotnet/dotnet-template-samples GitHub 리포지토리)</span><span class="sxs-lookup"><span data-stu-id="c9817-528">[dotnet/dotnet-template-samples GitHub repo](https://github.com/dotnet/dotnet-template-samples)</span></span>  
* <span data-ttu-id="c9817-529">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)(dotnet new에 대한 사용 가능한 템플릿)</span><span class="sxs-lookup"><span data-stu-id="c9817-529">[Available templates for dotnet new](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)</span></span>
