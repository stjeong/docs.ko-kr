---
title: dotnet sln 명령
description: dotnet-sln 명령은 솔루션 파일의 프로젝트를 추가, 제거 및 나열하는 간편한 옵션을 제공합니다.
ms.date: 06/13/2018
ms.openlocfilehash: a88e22c68f639f2a42e59f9a271e431f04e24a2b
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169146"
---
# <a name="dotnet-sln"></a><span data-ttu-id="13f62-103">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="13f62-103">dotnet sln</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="13f62-104">name</span><span class="sxs-lookup"><span data-stu-id="13f62-104">Name</span></span>

<span data-ttu-id="13f62-105">`dotnet sln` - .NET Core 솔루션 파일을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-105">`dotnet sln` - Modifies a .NET Core solution file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="13f62-106">개요</span><span class="sxs-lookup"><span data-stu-id="13f62-106">Synopsis</span></span>

```
dotnet sln [<SOLUTION_NAME>] add <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] add <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] remove <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] remove <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] list
dotnet sln [-h|--help]
```

## <a name="description"></a><span data-ttu-id="13f62-107">설명</span><span class="sxs-lookup"><span data-stu-id="13f62-107">Description</span></span>

<span data-ttu-id="13f62-108">`dotnet sln` 명령은 솔루션 파일의 프로젝트를 추가, 제거 및 나열하는 간편한 옵션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-108">The `dotnet sln` command provides a convenient way to add, remove, and list projects in a solution file.</span></span>

<span data-ttu-id="13f62-109">`dotnet sln` 명령을 사용하려면 솔루션 파일이 이미 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-109">To use the `dotnet sln` command, the solution file must already exist.</span></span> <span data-ttu-id="13f62-110">하나를 생성해야 하는 경우, 다음 예제와 같이 [dotnet new](dotnet-new.md) 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-110">If you need to create one, use the [dotnet new](dotnet-new.md) command, like in the following example:</span></span>

```
dotnet new sln
```

## <a name="commands"></a><span data-ttu-id="13f62-111">명령</span><span class="sxs-lookup"><span data-stu-id="13f62-111">Commands</span></span>

`add <PROJECT> ...`

`add <GLOBBING_PATTERN>`

<span data-ttu-id="13f62-112">솔루션 파일에 하나 이상의 프로젝트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-112">Adds a project or multiple projects to the solution file.</span></span> <span data-ttu-id="13f62-113">Unix/Linux 기반 터미널에서는 [와일드카드 사용 패턴](https://en.wikipedia.org/wiki/Glob_(programming))이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-113">[Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

`remove <PROJECT> ...`

`remove <GLOBBING_PATTERN>`

<span data-ttu-id="13f62-114">솔루션 파일에서 하나 이상의 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-114">Removes a project or multiple projects from the solution file.</span></span> <span data-ttu-id="13f62-115">Unix/Linux 기반 터미널에서는 [와일드카드 사용 패턴](https://en.wikipedia.org/wiki/Glob_(programming))이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-115">[Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

`list`

<span data-ttu-id="13f62-116">솔루션 파일의 모든 프로젝트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-116">Lists all projects in a solution file.</span></span>

## <a name="arguments"></a><span data-ttu-id="13f62-117">인수</span><span class="sxs-lookup"><span data-stu-id="13f62-117">Arguments</span></span>

`SOLUTION_NAME`

<span data-ttu-id="13f62-118">사용할 솔루션 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-118">Solution file to use.</span></span> <span data-ttu-id="13f62-119">지정하지 않으면 이 명령은 현재 디렉터리에서 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-119">If not specified, the command searches the current directory for one.</span></span> <span data-ttu-id="13f62-120">디렉터리에 여러 솔루션 파일이 있으면 하나를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-120">If there are multiple solution files in the directory, one must be specified.</span></span>

## <a name="options"></a><span data-ttu-id="13f62-121">옵션</span><span class="sxs-lookup"><span data-stu-id="13f62-121">Options</span></span>

`-h|--help`

<span data-ttu-id="13f62-122">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-122">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="13f62-123">예제</span><span class="sxs-lookup"><span data-stu-id="13f62-123">Examples</span></span>

<span data-ttu-id="13f62-124">솔루션에 C# 프로젝트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-124">Add a C# project to a solution:</span></span>

`dotnet sln todo.sln add todo-app/todo-app.csproj`

<span data-ttu-id="13f62-125">솔루션에서 C# 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-125">Remove a C# project from a solution:</span></span>

`dotnet sln todo.sln remove todo-app/todo-app.csproj`

<span data-ttu-id="13f62-126">솔루션에 여러 C# 프로젝트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-126">Add multiple C# projects to a solution:</span></span>

`dotnet sln todo.sln add todo-app/todo-app.csproj back-end/back-end.csproj`

<span data-ttu-id="13f62-127">솔루션에서 여러 C# 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-127">Remove multiple C# projects from a solution:</span></span>

`dotnet sln todo.sln remove todo-app/todo-app.csproj back-end/back-end.csproj`

<span data-ttu-id="13f62-128">와일드카드 사용 패턴을 사용하여 솔루션에 여러 C# 프로젝트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-128">Add multiple C# projects to a solution using a globbing pattern:</span></span>

`dotnet sln todo.sln add **/*.csproj`

<span data-ttu-id="13f62-129">와일드카드 사용 패턴을 사용하여 솔루션에서 여러 C# 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-129">Remove multiple C# projects from a solution using a globbing pattern:</span></span>

`dotnet sln todo.sln remove **/*.csproj`

> [!NOTE]
> <span data-ttu-id="13f62-130">와일드카드 사용은 CLI 기능이 아니라 명령 셸의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-130">Globbing is not a CLI feature but rather a feature of the command shell.</span></span> <span data-ttu-id="13f62-131">파일을 확장하려면 와일드카드 사용을 지원하는 셸을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f62-131">To successfully expand the files, you must use a shell that supports globbing.</span></span> <span data-ttu-id="13f62-132">와일드카드 사용에 대한 자세한 내용은 [Wikipedia](https://en.wikipedia.org/wiki/Glob_(programming))를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13f62-132">For more information about globbing, see [Wikipedia](https://en.wikipedia.org/wiki/Glob_(programming)).</span></span>
