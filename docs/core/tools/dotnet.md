---
title: dotnet 명령 - .NET Core CLI
description: dotnet 명령(.NET Core CLI 도구에 대한 일반 드라이버) 및 사용법에 대해 알아봅니다.
author: mairaw
ms.author: mairaw
ms.date: 06/04/2018
ms.openlocfilehash: 53e8f8bab1cbaabaa7926aa68197c18843b0b637
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45615579"
---
# <a name="dotnet-command"></a><span data-ttu-id="38726-103">dotnet 명령</span><span class="sxs-lookup"><span data-stu-id="38726-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="38726-104">name</span><span class="sxs-lookup"><span data-stu-id="38726-104">Name</span></span>

<span data-ttu-id="38726-105">`dotnet` - .NET 소스 코드 및 이진 파일을 관리하기 위한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="38726-106">개요</span><span class="sxs-lookup"><span data-stu-id="38726-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="38726-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="38726-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="38726-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="38726-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="38726-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="38726-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="38726-110">설명</span><span class="sxs-lookup"><span data-stu-id="38726-110">Description</span></span>

<span data-ttu-id="38726-111">`dotnet`은 .NET 소스 코드 및 이진 파일을 관리하기 위한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="38726-112">[`dotnet build`](dotnet-build.md) 및 [`dotnet run`](dotnet-run.md)와 같은 특정 작업을 수행하는 명령을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="38726-113">각 명령은 자체 인수를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-113">Each command defines its own arguments.</span></span> <span data-ttu-id="38726-114">각 명령 다음에 `--help`를 입력하면 간단한 도움말 설명서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38726-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="38726-115">`dotnet`은 `dotnet myapp.dll`과 같은 응용 프로그램 DLL을 지정하여 응용 프로그램을 실행하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38726-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="38726-116">배포 옵션에 대해 자세히 알아보려면 [.NET Core 응용 프로그램 배포](../deploying/index.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="38726-117">옵션</span><span class="sxs-lookup"><span data-stu-id="38726-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="38726-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="38726-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="38726-119">추가적인 *deps.json* 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="38726-120">검색 정책 및 검색할 어셈블리를 포함하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="38726-121">진단 출력을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="38726-122">응용 프로그램 실행에 사용할 .NET Core 런타임의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="38726-123">`dotnet build --help`와 같은 지정된 명령에 대한 설명서를 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="38726-124">`dotnet --help`는 사용 가능한 명령 목록을 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="38726-125">.NET Core 설치 및 머신 환경(예: 현재 운영 체제)에 대한 자세한 정보를 인쇄하고 .NET Core 버전의 SHA를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="38726-126">설치된 .NET Core 런타임을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="38726-127">설치된 .NET Core SDK를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="38726-128">`0`으로 설정된 경우 부 버전 롤포워드를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-128">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="38726-129">자세한 내용은 [롤포워드](../whats-new/dotnet-core-2-1.md#roll-forward)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-129">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="38726-130">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-130">Sets the verbosity level of the command.</span></span> <span data-ttu-id="38726-131">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-131">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="38726-132">모든 명령에서 지원되지 않습니다. 이 옵션을 사용할 수 있는지 확인하려면 특정 명령 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-132">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="38726-133">사용 중인 .NET Core SDK 버전을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-133">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="38726-134">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="38726-134">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="38726-135">추가적인 *deps.json* 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-135">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="38726-136">검색 정책 및 검색할 어셈블리를 포함하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-136">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="38726-137">진단 출력을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-137">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="38726-138">응용 프로그램 실행에 사용할 .NET Core 런타임의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-138">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="38726-139">`dotnet build --help`와 같은 지정된 명령에 대한 설명서를 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-139">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="38726-140">`dotnet --help`는 사용 가능한 명령 목록을 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-140">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="38726-141">.NET Core 설치 및 머신 환경(예: 현재 운영 체제)에 대한 자세한 정보를 인쇄하고 .NET Core 버전의 SHA를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-141">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="38726-142">`0`으로 설정된 경우 부 버전 롤포워드를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-142">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="38726-143">자세한 내용은 [롤포워드](../whats-new/dotnet-core-2-1.md#roll-forward)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-143">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="38726-144">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="38726-145">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="38726-146">모든 명령에서 지원되지 않습니다. 이 옵션을 사용할 수 있는지 확인하려면 특정 명령 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-146">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="38726-147">사용 중인 .NET Core SDK 버전을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-147">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="38726-148">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="38726-148">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="38726-149">검색 정책 및 검색할 어셈블리를 포함하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-149">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="38726-150">진단 출력을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-150">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="38726-151">응용 프로그램 실행에 사용할 .NET Core 런타임의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-151">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="38726-152">`dotnet build --help`와 같은 지정된 명령에 대한 설명서를 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-152">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="38726-153">`dotnet --help`는 사용 가능한 명령 목록을 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-153">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="38726-154">.NET Core 설치 및 머신 환경(예: 현재 운영 체제)에 대한 자세한 정보를 인쇄하고 .NET Core 버전의 SHA를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-154">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="38726-155">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-155">Sets the verbosity level of the command.</span></span> <span data-ttu-id="38726-156">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-156">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="38726-157">모든 명령에서 지원되지 않습니다. 이 옵션을 사용할 수 있는지 확인하려면 특정 명령 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-157">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="38726-158">사용 중인 .NET Core SDK 버전을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-158">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="38726-159">dotnet 명령</span><span class="sxs-lookup"><span data-stu-id="38726-159">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="38726-160">일반</span><span class="sxs-lookup"><span data-stu-id="38726-160">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="38726-161">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="38726-161">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="38726-162">명령</span><span class="sxs-lookup"><span data-stu-id="38726-162">Command</span></span>                                       | <span data-ttu-id="38726-163">함수</span><span class="sxs-lookup"><span data-stu-id="38726-163">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="38726-164">dotnet build</span><span class="sxs-lookup"><span data-stu-id="38726-164">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="38726-165">.NET Core 응용 프로그램을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-165">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="38726-166">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="38726-166">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="38726-167">빌드에서 시작된 서버와 상호 작용합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-167">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="38726-168">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="38726-168">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="38726-169">빌드 출력을 정리합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-169">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="38726-170">dotnet help</span><span class="sxs-lookup"><span data-stu-id="38726-170">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="38726-171">명령에 대한 자세한 온라인 설명서를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-171">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="38726-172">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="38726-172">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="38726-173">유효한 Preview 2 프로젝트를 .NET Core SDK 1.0 프로젝트로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-173">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="38726-174">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="38726-174">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="38726-175">MSBuild 명령줄에 대한 액세스 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-175">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="38726-176">dotnet new</span><span class="sxs-lookup"><span data-stu-id="38726-176">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="38726-177">지정한 템플릿에 대해 C# 또는 F# 프로젝트를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-177">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="38726-178">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="38726-178">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="38726-179">코드의 NuGet 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38726-179">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="38726-180">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="38726-180">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="38726-181">.NET Framework 종속형 또는 자체 포함 응용 프로그램을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-181">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="38726-182">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="38726-182">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="38726-183">지정된 응용 프로그램에 대한 종속성을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-183">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="38726-184">dotnet run</span><span class="sxs-lookup"><span data-stu-id="38726-184">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="38726-185">소스에서 응용 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-185">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="38726-186">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="38726-186">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="38726-187">솔루션 파일에 프로젝트를 추가, 제거 및 나열하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-187">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="38726-188">dotnet store</span><span class="sxs-lookup"><span data-stu-id="38726-188">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="38726-189">어셈블리를 런타임 패키지 저장소에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-189">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="38726-190">dotnet test</span><span class="sxs-lookup"><span data-stu-id="38726-190">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="38726-191">Test Runner를 사용하여 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-191">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="38726-192">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="38726-192">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="38726-193">명령</span><span class="sxs-lookup"><span data-stu-id="38726-193">Command</span></span>                             | <span data-ttu-id="38726-194">함수</span><span class="sxs-lookup"><span data-stu-id="38726-194">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="38726-195">dotnet build</span><span class="sxs-lookup"><span data-stu-id="38726-195">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="38726-196">.NET Core 응용 프로그램을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-196">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="38726-197">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="38726-197">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="38726-198">빌드 출력을 정리합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-198">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="38726-199">dotnet help</span><span class="sxs-lookup"><span data-stu-id="38726-199">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="38726-200">명령에 대한 자세한 온라인 설명서를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-200">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="38726-201">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="38726-201">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="38726-202">유효한 Preview 2 프로젝트를 .NET Core SDK 1.0 프로젝트로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-202">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="38726-203">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="38726-203">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="38726-204">MSBuild 명령줄에 대한 액세스 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-204">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="38726-205">dotnet new</span><span class="sxs-lookup"><span data-stu-id="38726-205">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="38726-206">지정한 템플릿에 대해 C# 또는 F# 프로젝트를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-206">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="38726-207">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="38726-207">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="38726-208">코드의 NuGet 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38726-208">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="38726-209">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="38726-209">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="38726-210">.NET Framework 종속형 또는 자체 포함 응용 프로그램을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-210">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="38726-211">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="38726-211">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="38726-212">지정된 응용 프로그램에 대한 종속성을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-212">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="38726-213">dotnet run</span><span class="sxs-lookup"><span data-stu-id="38726-213">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="38726-214">소스에서 응용 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-214">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="38726-215">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="38726-215">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="38726-216">솔루션 파일에 프로젝트를 추가, 제거 및 나열하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-216">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="38726-217">dotnet store</span><span class="sxs-lookup"><span data-stu-id="38726-217">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="38726-218">어셈블리를 런타임 패키지 저장소에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-218">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="38726-219">dotnet test</span><span class="sxs-lookup"><span data-stu-id="38726-219">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="38726-220">Test Runner를 사용하여 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-220">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="38726-221">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="38726-221">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="38726-222">명령</span><span class="sxs-lookup"><span data-stu-id="38726-222">Command</span></span>                             | <span data-ttu-id="38726-223">함수</span><span class="sxs-lookup"><span data-stu-id="38726-223">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="38726-224">dotnet build</span><span class="sxs-lookup"><span data-stu-id="38726-224">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="38726-225">.NET Core 응용 프로그램을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-225">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="38726-226">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="38726-226">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="38726-227">빌드 출력을 정리합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-227">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="38726-228">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="38726-228">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="38726-229">유효한 Preview 2 프로젝트를 .NET Core SDK 1.0 프로젝트로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-229">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="38726-230">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="38726-230">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="38726-231">MSBuild 명령줄에 대한 액세스 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-231">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="38726-232">dotnet new</span><span class="sxs-lookup"><span data-stu-id="38726-232">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="38726-233">지정한 템플릿에 대해 C# 또는 F# 프로젝트를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-233">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="38726-234">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="38726-234">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="38726-235">코드의 NuGet 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38726-235">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="38726-236">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="38726-236">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="38726-237">.NET Framework 종속형 또는 자체 포함 응용 프로그램을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-237">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="38726-238">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="38726-238">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="38726-239">지정된 응용 프로그램에 대한 종속성을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-239">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="38726-240">dotnet run</span><span class="sxs-lookup"><span data-stu-id="38726-240">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="38726-241">소스에서 응용 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-241">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="38726-242">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="38726-242">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="38726-243">솔루션 파일에 프로젝트를 추가, 제거 및 나열하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-243">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="38726-244">dotnet test</span><span class="sxs-lookup"><span data-stu-id="38726-244">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="38726-245">Test Runner를 사용하여 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-245">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="38726-246">프로젝트 참조</span><span class="sxs-lookup"><span data-stu-id="38726-246">Project references</span></span>

<span data-ttu-id="38726-247">명령</span><span class="sxs-lookup"><span data-stu-id="38726-247">Command</span></span> | <span data-ttu-id="38726-248">함수</span><span class="sxs-lookup"><span data-stu-id="38726-248">Function</span></span>
--- | ---
[<span data-ttu-id="38726-249">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="38726-249">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="38726-250">프로젝트 참조를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-250">Adds a project reference.</span></span>
[<span data-ttu-id="38726-251">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="38726-251">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="38726-252">프로젝트 참조를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-252">Lists project references.</span></span>
[<span data-ttu-id="38726-253">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="38726-253">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="38726-254">프로젝트 참조를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-254">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="38726-255">NuGet 패키지</span><span class="sxs-lookup"><span data-stu-id="38726-255">NuGet packages</span></span>

<span data-ttu-id="38726-256">명령</span><span class="sxs-lookup"><span data-stu-id="38726-256">Command</span></span> | <span data-ttu-id="38726-257">함수</span><span class="sxs-lookup"><span data-stu-id="38726-257">Function</span></span>
--- | ---
[<span data-ttu-id="38726-258">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="38726-258">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="38726-259">NuGet 패키지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-259">Adds a NuGet package.</span></span>
[<span data-ttu-id="38726-260">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="38726-260">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="38726-261">NuGet 패키지를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-261">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="38726-262">NuGet 명령</span><span class="sxs-lookup"><span data-stu-id="38726-262">NuGet commands</span></span>

<span data-ttu-id="38726-263">명령</span><span class="sxs-lookup"><span data-stu-id="38726-263">Command</span></span> | <span data-ttu-id="38726-264">함수</span><span class="sxs-lookup"><span data-stu-id="38726-264">Function</span></span>
--- | ---
[<span data-ttu-id="38726-265">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="38726-265">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="38726-266">서버에서 패키지를 삭제하거나 목록에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-266">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="38726-267">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="38726-267">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="38726-268">http-request 캐시, 임시 캐시 또는 시스템 전체의 글로벌 패키지 폴더와 같은 로컬 NuGet 리소스를 지우거나 목록에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-268">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="38726-269">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="38726-269">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="38726-270">서버에 패키지를 푸시하고 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-270">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="38726-271">전역 도구 명령</span><span class="sxs-lookup"><span data-stu-id="38726-271">Global Tools commands</span></span>

<span data-ttu-id="38726-272">[.NET Core 전역 도구](global-tools.md)는 .NET Core SDK 2.1.300부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38726-272">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="38726-273">명령</span><span class="sxs-lookup"><span data-stu-id="38726-273">Command</span></span> | <span data-ttu-id="38726-274">함수</span><span class="sxs-lookup"><span data-stu-id="38726-274">Function</span></span>
--- | ---
[<span data-ttu-id="38726-275">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="38726-275">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="38726-276">컴퓨터에 전역 도구를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-276">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="38726-277">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="38726-277">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="38726-278">컴퓨터의 기본 디렉터리 또는 지정된 경로에 현재 설치된 모든 전역 도구를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-278">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="38726-279">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="38726-279">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="38726-280">컴퓨터에서 전역 도구를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-280">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="38726-281">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="38726-281">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="38726-282">컴퓨터에서 전역 도구를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-282">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="38726-283">추가 도구</span><span class="sxs-lookup"><span data-stu-id="38726-283">Additional tools</span></span>

<span data-ttu-id="38726-284">.NET Core SDK 2.1.300부터는 `DotnetCliToolReference`을 사용하여 프로젝트별로만 사용할 수 있었던 여러 도구를 .NET Core SDK의 일부로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38726-284">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="38726-285">이러한 도구는 다음 표에 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38726-285">These tools are listed in the following table:</span></span>

| <span data-ttu-id="38726-286">도구</span><span class="sxs-lookup"><span data-stu-id="38726-286">Tool</span></span>                                              | <span data-ttu-id="38726-287">함수</span><span class="sxs-lookup"><span data-stu-id="38726-287">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="38726-288">dev-certs</span><span class="sxs-lookup"><span data-stu-id="38726-288">dev-certs</span></span>                                         | <span data-ttu-id="38726-289">개발 인증서를 만들고 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-289">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="38726-290">ef</span><span class="sxs-lookup"><span data-stu-id="38726-290">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="38726-291">Entity Framework Core 명령줄 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-291">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="38726-292">sql-cache</span><span class="sxs-lookup"><span data-stu-id="38726-292">sql-cache</span></span>                                         | <span data-ttu-id="38726-293">SQL Server 캐시 명령줄 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-293">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="38726-294">user-secrets</span><span class="sxs-lookup"><span data-stu-id="38726-294">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="38726-295">개발 사용자 비밀을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-295">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="38726-296">watch</span><span class="sxs-lookup"><span data-stu-id="38726-296">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="38726-297">파일이 변경될 때 명령을 실행하는 파일 감시자를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-297">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="38726-298">각 도구에 대한 자세한 내용을 보려면 `dotnet <tool-name> --help`를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-298">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="38726-299">예제</span><span class="sxs-lookup"><span data-stu-id="38726-299">Examples</span></span>

<span data-ttu-id="38726-300">새 .NET Core 콘솔 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38726-300">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="38726-301">지정된 응용 프로그램에 대한 종속성을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-301">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="38726-302">지정된 디렉터리에서 프로젝트 및 해당 종속성을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-302">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="38726-303">`myapp.dll`과 같은 응용 프로그램 DLL을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-303">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="38726-304">환경 변수</span><span class="sxs-lookup"><span data-stu-id="38726-304">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="38726-305">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="38726-305">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="38726-306">주 패키지 캐시입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-306">The primary package cache.</span></span> <span data-ttu-id="38726-307">설정하지 않으면 기본적으로 Unix에서는 `$HOME/.nuget/packages`, Windows에서는 `%HOME%\NuGet\Packages`로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="38726-307">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="38726-308">런타임을 로드할 때 공유 호스트에서 사용할 서비스 인덱스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-308">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="38726-309">.NET Core 도구 사용에 대한 데이터를 수집하여 Microsoft에 전송할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-309">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="38726-310">원격 분석 기능을 옵트아웃하려면 `true`로 설정합니다(값 `true`, `1` 또는 `yes`가 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-310">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="38726-311">이외의 경우 원격 분석 기능을 옵트인하려면 `false`로 설정합니다(`false`, `0` 또는 `no`가 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-311">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="38726-312">설정하지 않으면 기본적으로 `false`이고 원격 분석 기능은 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="38726-312">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="38726-313">전역 위치에서 .NET Core 런타임, 공유 프레임워크 또는 SDK가 확인되는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-313">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="38726-314">설정하지 않은 경우 기본값은 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-314">If not set, it defaults to `true`.</span></span> <span data-ttu-id="38726-315">전역 위치에서 확인하지 않고 격리된 .NET Core 설치를 가지려면 `false`로 설정합니다(값 `0` 또는 `false`는 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-315">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="38726-316">다중 수준의 조회에 대한 자세한 내용은 [다중 수준 SharedFX 조회](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-316">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="38726-317">`0`으로 설정된 경우 부 버전 롤포워드를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-317">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="38726-318">자세한 내용은 [롤포워드](../whats-new/dotnet-core-2-1.md#roll-forward)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-318">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="38726-319">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="38726-319">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="38726-320">주 패키지 캐시입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-320">The primary package cache.</span></span> <span data-ttu-id="38726-321">설정하지 않으면 기본적으로 Unix에서는 `$HOME/.nuget/packages`, Windows에서는 `%HOME%\NuGet\Packages`로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="38726-321">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="38726-322">런타임을 로드할 때 공유 호스트에서 사용할 서비스 인덱스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-322">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="38726-323">.NET Core 도구 사용에 대한 데이터를 수집하여 Microsoft에 전송할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-323">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="38726-324">원격 분석 기능을 옵트아웃하려면 `true`로 설정합니다(값 `true`, `1` 또는 `yes`가 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-324">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="38726-325">이외의 경우 원격 분석 기능을 옵트인하려면 `false`로 설정합니다(`false`, `0` 또는 `no`가 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-325">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="38726-326">설정하지 않으면 기본적으로 `false`이고 원격 분석 기능은 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="38726-326">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="38726-327">전역 위치에서 .NET Core 런타임, 공유 프레임워크 또는 SDK가 확인되는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-327">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="38726-328">설정하지 않은 경우 기본값은 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-328">If not set, it defaults to `true`.</span></span> <span data-ttu-id="38726-329">전역 위치에서 확인하지 않고 격리된 .NET Core 설치를 가지려면 `false`로 설정합니다(값 `0` 또는 `false`는 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-329">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="38726-330">다중 수준의 조회에 대한 자세한 내용은 [다중 수준 SharedFX 조회](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38726-330">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="38726-331">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="38726-331">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="38726-332">주 패키지 캐시입니다.</span><span class="sxs-lookup"><span data-stu-id="38726-332">The primary package cache.</span></span> <span data-ttu-id="38726-333">설정하지 않으면 기본적으로 Unix에서는 `$HOME/.nuget/packages`, Windows에서는 `%HOME%\NuGet\Packages`로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="38726-333">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="38726-334">런타임을 로드할 때 공유 호스트에서 사용할 서비스 인덱스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-334">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="38726-335">.NET Core 도구 사용에 대한 데이터를 수집하여 Microsoft에 전송할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38726-335">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="38726-336">원격 분석 기능을 옵트아웃하려면 `true`로 설정합니다(값 `true`, `1` 또는 `yes`가 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-336">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="38726-337">이외의 경우 원격 분석 기능을 옵트인하려면 `false`로 설정합니다(`false`, `0` 또는 `no`가 허용됨).</span><span class="sxs-lookup"><span data-stu-id="38726-337">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="38726-338">설정하지 않으면 기본적으로 `false`이고 원격 분석 기능은 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="38726-338">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
