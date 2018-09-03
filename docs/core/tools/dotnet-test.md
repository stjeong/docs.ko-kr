---
title: dotnet test 명령 - .NET Core CLI
description: dotnet test 명령은 지정된 프로젝트에서 단위 테스트를 실행하는 데 사용됩니다.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 2bee78ca44026f28c51fac3bcf87d976b53e48a7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43390692"
---
# <a name="dotnet-test"></a><span data-ttu-id="1f9b8-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="1f9b8-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="1f9b8-104">name</span><span class="sxs-lookup"><span data-stu-id="1f9b8-104">Name</span></span>

<span data-ttu-id="1f9b8-105">`dotnet test` - 단위 테스트를 실행하는 데 사용하는 .NET 테스트 드라이버입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="1f9b8-106">개요</span><span class="sxs-lookup"><span data-stu-id="1f9b8-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="1f9b8-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="1f9b8-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="1f9b8-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="1f9b8-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="1f9b8-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="1f9b8-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]
dotnet test [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="1f9b8-110">설명</span><span class="sxs-lookup"><span data-stu-id="1f9b8-110">Description</span></span>

<span data-ttu-id="1f9b8-111">`dotnet test` 명령은 지정된 프로젝트에서 단위 테스트를 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="1f9b8-112">`dotnet test` 명령은 프로젝트에 대해 지정된 테스트 러너 콘솔 응용 프로그램을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="1f9b8-113">테스트 러너는 단위 테스트 프레임워크(예: MSTest, NUnit 또는 xUnit)에 대해 정의된 테스트를 실행하고 각 테스트의 성공 여부를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="1f9b8-114">테스트 러너와 단위 테스트 라이브러리는 NuGet 패키지로 패키지되고 프로젝트에 대한 일반적인 종속성으로 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-114">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="1f9b8-115">테스트 프로젝트는 다음 샘플 프로젝트 파일에서 볼 수 있듯이 일반적인 `<PackageReference>` 요소를 사용하여 테스트 러너를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-115">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="1f9b8-116">인수</span><span class="sxs-lookup"><span data-stu-id="1f9b8-116">Arguments</span></span>

`PROJECT`

<span data-ttu-id="1f9b8-117">테스트 프로젝트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-117">Path to the test project.</span></span> <span data-ttu-id="1f9b8-118">지정하지 않으면 현재 디렉터리로 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-118">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="1f9b8-119">옵션</span><span class="sxs-lookup"><span data-stu-id="1f9b8-119">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="1f9b8-120">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="1f9b8-120">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="1f9b8-121">테스트 실행에 지정된 경로에서 사용자 지정 테스트 어댑터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-121">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="1f9b8-122">테스트를 원인 모드로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-122">Runs the tests in blame mode.</span></span> <span data-ttu-id="1f9b8-123">이 옵션은 테스트 호스트를 충돌시키는 문제가 있는 테스트를 격리하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-123">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="1f9b8-124">현재 디렉터리에 크래시 전에 테스트 실행 순서를 캡처하는 *Sequence.xml*이라는 출력 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-124">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="1f9b8-125">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-125">Defines the build configuration.</span></span> <span data-ttu-id="1f9b8-126">기본값은 `Debug`이지만 프로젝트의 구성으로 이 기본 SDK 설정이 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-126">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="1f9b8-127">테스트 실행에 대한 데이터 수집기를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-127">Enables data collector for the test run.</span></span> <span data-ttu-id="1f9b8-128">자세한 내용은 [테스트 실행 모니터링 및 분석](https://aka.ms/vstest-collect)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-128">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="1f9b8-129">테스트 플랫폼에 대한 진단 모드를 사용하도록 설정하고 지정된 파일에 진단 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-129">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="1f9b8-130">특정 [프레임워크](../../standard/frameworks.md)에 대한 테스트 이진 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-130">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="1f9b8-131">지정된 식을 사용하여 현재 프로젝트의 테스트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-131">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="1f9b8-132">자세한 내용은 [필터 옵션 세부 정보](#filter-option-details) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-132">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="1f9b8-133">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-133">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="1f9b8-134">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-134">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="1f9b8-135">테스트 결과에 대해 로거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-135">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="1f9b8-136">테스트 프로젝트를 실행하기 전에 빌드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-136">Doesn't build the test project before running it.</span></span> <span data-ttu-id="1f9b8-137">또한 `--no-restore` 플래그를 암시적으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-137">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="1f9b8-138">명령을 실행할 때 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-138">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="1f9b8-139">실행할 이진 파일을 찾을 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-139">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="1f9b8-140">테스트 결과가 배치될 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-140">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="1f9b8-141">지정한 디렉터리가 없으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-141">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="1f9b8-142">테스트를 실행할 때 사용할 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-142">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="1f9b8-143">현재 프로젝트에서 검색된 테스트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-143">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="1f9b8-144">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="1f9b8-145">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="1f9b8-146">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="1f9b8-146">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="1f9b8-147">테스트 실행에 지정된 경로에서 사용자 지정 테스트 어댑터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-147">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="1f9b8-148">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-148">Defines the build configuration.</span></span> <span data-ttu-id="1f9b8-149">기본값은 `Debug`이지만 프로젝트의 구성으로 이 기본 SDK 설정이 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-149">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="1f9b8-150">테스트 실행에 대한 데이터 수집기를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-150">Enables data collector for the test run.</span></span> <span data-ttu-id="1f9b8-151">자세한 내용은 [테스트 실행 모니터링 및 분석](https://aka.ms/vstest-collect)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-151">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="1f9b8-152">테스트 플랫폼에 대한 진단 모드를 사용하도록 설정하고 지정된 파일에 진단 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-152">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="1f9b8-153">특정 [프레임워크](../../standard/frameworks.md)에 대한 테스트 이진 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-153">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="1f9b8-154">지정된 식을 사용하여 현재 프로젝트의 테스트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-154">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="1f9b8-155">자세한 내용은 [필터 옵션 세부 정보](#filter-option-details) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-155">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="1f9b8-156">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-156">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="1f9b8-157">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-157">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="1f9b8-158">테스트 결과에 대해 로거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-158">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="1f9b8-159">테스트 프로젝트를 실행하기 전에 빌드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-159">Doesn't build the test project before running it.</span></span> <span data-ttu-id="1f9b8-160">또한 `--no-restore` 플래그를 암시적으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-160">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="1f9b8-161">명령을 실행할 때 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-161">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="1f9b8-162">실행할 이진 파일을 찾을 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-162">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="1f9b8-163">테스트 결과가 배치될 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-163">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="1f9b8-164">지정한 디렉터리가 없으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-164">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="1f9b8-165">테스트를 실행할 때 사용할 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-165">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="1f9b8-166">현재 프로젝트에서 검색된 테스트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-166">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="1f9b8-167">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-167">Sets the verbosity level of the command.</span></span> <span data-ttu-id="1f9b8-168">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-168">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="1f9b8-169">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="1f9b8-169">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="1f9b8-170">테스트 실행에 지정된 경로에서 사용자 지정 테스트 어댑터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-170">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="1f9b8-171">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-171">Defines the build configuration.</span></span> <span data-ttu-id="1f9b8-172">기본값은 `Debug`이지만 프로젝트의 구성으로 이 기본 SDK 설정이 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-172">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="1f9b8-173">테스트 플랫폼에 대한 진단 모드를 사용하도록 설정하고 지정된 파일에 진단 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-173">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="1f9b8-174">특정 [프레임워크](../../standard/frameworks.md)에 대한 테스트 이진 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-174">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="1f9b8-175">지정된 식을 사용하여 현재 프로젝트의 테스트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-175">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="1f9b8-176">자세한 내용은 [필터 옵션 세부 정보](#filter-option-details) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-176">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="1f9b8-177">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-177">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="1f9b8-178">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-178">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="1f9b8-179">테스트 결과에 대해 로거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-179">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="1f9b8-180">테스트 프로젝트를 실행하기 전에 빌드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-180">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="1f9b8-181">실행할 이진 파일을 찾을 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-181">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="1f9b8-182">테스트를 실행할 때 사용할 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-182">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="1f9b8-183">현재 프로젝트에서 검색된 테스트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-183">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="1f9b8-184">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-184">Sets the verbosity level of the command.</span></span> <span data-ttu-id="1f9b8-185">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-185">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="1f9b8-186">예제</span><span class="sxs-lookup"><span data-stu-id="1f9b8-186">Examples</span></span>

<span data-ttu-id="1f9b8-187">현재 디렉터리에 있는 프로젝트에서 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-187">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="1f9b8-188">`test1` 프로젝트에서 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-188">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

## <a name="filter-option-details"></a><span data-ttu-id="1f9b8-189">필터 옵션 세부 정보</span><span class="sxs-lookup"><span data-stu-id="1f9b8-189">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="1f9b8-190">`<Expression>`에 `<property><operator><value>[|&<Expression>]` 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-190">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="1f9b8-191">`<property>`은(는) `Test Case`의 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-191">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="1f9b8-192">다음은 인기 있는 단위 테스트 프레임 워크에서 지원되는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-192">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="1f9b8-193">테스트 프레임워크</span><span class="sxs-lookup"><span data-stu-id="1f9b8-193">Test Framework</span></span> | <span data-ttu-id="1f9b8-194">지원되는 속성</span><span class="sxs-lookup"><span data-stu-id="1f9b8-194">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="1f9b8-195">MSTest</span><span class="sxs-lookup"><span data-stu-id="1f9b8-195">MSTest</span></span>         | <ul><li><span data-ttu-id="1f9b8-196">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="1f9b8-196">FullyQualifiedName</span></span></li><li><span data-ttu-id="1f9b8-197">name</span><span class="sxs-lookup"><span data-stu-id="1f9b8-197">Name</span></span></li><li><span data-ttu-id="1f9b8-198">ClassName</span><span class="sxs-lookup"><span data-stu-id="1f9b8-198">ClassName</span></span></li><li><span data-ttu-id="1f9b8-199">우선 순위</span><span class="sxs-lookup"><span data-stu-id="1f9b8-199">Priority</span></span></li><li><span data-ttu-id="1f9b8-200">TestCategory</span><span class="sxs-lookup"><span data-stu-id="1f9b8-200">TestCategory</span></span></li></ul> |
| <span data-ttu-id="1f9b8-201">xUnit</span><span class="sxs-lookup"><span data-stu-id="1f9b8-201">xUnit</span></span>          | <ul><li><span data-ttu-id="1f9b8-202">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="1f9b8-202">FullyQualifiedName</span></span></li><li><span data-ttu-id="1f9b8-203">DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f9b8-203">DisplayName</span></span></li><li><span data-ttu-id="1f9b8-204">특성</span><span class="sxs-lookup"><span data-stu-id="1f9b8-204">Traits</span></span></li></ul>                                   |

<span data-ttu-id="1f9b8-205">`<operator>`은(는) 속성과 값 사이의 관계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-205">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="1f9b8-206">연산자</span><span class="sxs-lookup"><span data-stu-id="1f9b8-206">Operator</span></span> | <span data-ttu-id="1f9b8-207">함수</span><span class="sxs-lookup"><span data-stu-id="1f9b8-207">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="1f9b8-208">정확하게 일치</span><span class="sxs-lookup"><span data-stu-id="1f9b8-208">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="1f9b8-209">정확하게 일치하지 않음</span><span class="sxs-lookup"><span data-stu-id="1f9b8-209">Not exact match</span></span> |
| `~`      | <span data-ttu-id="1f9b8-210">포함</span><span class="sxs-lookup"><span data-stu-id="1f9b8-210">Contains</span></span>        |

<span data-ttu-id="1f9b8-211">`<value>`는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-211">`<value>` is a string.</span></span> <span data-ttu-id="1f9b8-212">모든 조회는 대/소문자를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-212">All the lookups are case insensitive.</span></span>

<span data-ttu-id="1f9b8-213">`<operator>`이(가) 없는 식은 `FullyQualifiedName` 속성의 `contains`(으)로 자동으로 간주됩니다(예를 들어 `dotnet test --filter xyz`과(와) `dotnet test --filter FullyQualifiedName~xyz`이(가) 동일).</span><span class="sxs-lookup"><span data-stu-id="1f9b8-213">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="1f9b8-214">식은 조건부 연산자와 조인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-214">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="1f9b8-215">연산자</span><span class="sxs-lookup"><span data-stu-id="1f9b8-215">Operator</span></span>            | <span data-ttu-id="1f9b8-216">함수</span><span class="sxs-lookup"><span data-stu-id="1f9b8-216">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="1f9b8-217">또는</span><span class="sxs-lookup"><span data-stu-id="1f9b8-217">OR</span></span>       |
| `&`                 | <span data-ttu-id="1f9b8-218">AND</span><span class="sxs-lookup"><span data-stu-id="1f9b8-218">AND</span></span>      |

<span data-ttu-id="1f9b8-219">조건부 연산자를 사용 하는 경우 식을 괄호로 묶을 수 있습니다(예: `(Name~TestMethod1) | (Name~TestMethod2)`).</span><span class="sxs-lookup"><span data-stu-id="1f9b8-219">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="1f9b8-220">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9b8-220">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1f9b8-221">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1f9b8-221">See also</span></span>

* [<span data-ttu-id="1f9b8-222">프레임워크 및 대상</span><span class="sxs-lookup"><span data-stu-id="1f9b8-222">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
* [<span data-ttu-id="1f9b8-223">.NET Core RID(런타임 식별자) 카탈로그</span><span class="sxs-lookup"><span data-stu-id="1f9b8-223">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
