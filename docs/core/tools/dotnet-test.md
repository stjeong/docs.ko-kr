---
title: dotnet test 명령 - .NET Core CLI
description: dotnet test 명령은 지정된 프로젝트에서 단위 테스트를 실행하는 데 사용됩니다.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 7946196b27489870da1c16b15cbf5f078ae89c61
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45666904"
---
# <a name="dotnet-test"></a><span data-ttu-id="909bc-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="909bc-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="909bc-104">name</span><span class="sxs-lookup"><span data-stu-id="909bc-104">Name</span></span>

<span data-ttu-id="909bc-105">`dotnet test` - 단위 테스트를 실행하는 데 사용하는 .NET 테스트 드라이버입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="909bc-106">개요</span><span class="sxs-lookup"><span data-stu-id="909bc-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="909bc-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="909bc-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="909bc-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="909bc-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="909bc-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="909bc-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]
dotnet test [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="909bc-110">설명</span><span class="sxs-lookup"><span data-stu-id="909bc-110">Description</span></span>

<span data-ttu-id="909bc-111">`dotnet test` 명령은 지정된 프로젝트에서 단위 테스트를 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="909bc-112">`dotnet test` 명령은 프로젝트에 대해 지정된 테스트 러너 콘솔 응용 프로그램을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="909bc-113">테스트 러너는 단위 테스트 프레임워크(예: MSTest, NUnit 또는 xUnit)에 대해 정의된 테스트를 실행하고 각 테스트의 성공 여부를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="909bc-114">테스트 러너와 단위 테스트 라이브러리는 NuGet 패키지로 패키지되고 프로젝트에 대한 일반적인 종속성으로 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-114">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="909bc-115">테스트 프로젝트는 다음 샘플 프로젝트 파일에서 볼 수 있듯이 일반적인 `<PackageReference>` 요소를 사용하여 테스트 러너를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-115">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="909bc-116">인수</span><span class="sxs-lookup"><span data-stu-id="909bc-116">Arguments</span></span>

`PROJECT`

<span data-ttu-id="909bc-117">테스트 프로젝트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-117">Path to the test project.</span></span> <span data-ttu-id="909bc-118">지정하지 않으면 현재 디렉터리로 기본 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-118">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="909bc-119">옵션</span><span class="sxs-lookup"><span data-stu-id="909bc-119">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="909bc-120">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="909bc-120">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="909bc-121">테스트 실행에 지정된 경로에서 사용자 지정 테스트 어댑터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-121">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="909bc-122">테스트를 원인 모드로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-122">Runs the tests in blame mode.</span></span> <span data-ttu-id="909bc-123">이 옵션은 테스트 호스트를 충돌시키는 문제가 있는 테스트를 격리하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-123">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="909bc-124">현재 디렉터리에 크래시 전에 테스트 실행 순서를 캡처하는 *Sequence.xml*이라는 출력 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-124">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="909bc-125">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-125">Defines the build configuration.</span></span> <span data-ttu-id="909bc-126">기본값은 `Debug`이지만 프로젝트의 구성으로 이 기본 SDK 설정이 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-126">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="909bc-127">테스트 실행에 대한 데이터 수집기를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-127">Enables data collector for the test run.</span></span> <span data-ttu-id="909bc-128">자세한 내용은 [테스트 실행 모니터링 및 분석](https://aka.ms/vstest-collect)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-128">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="909bc-129">테스트 플랫폼에 대한 진단 모드를 사용하도록 설정하고 지정된 파일에 진단 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-129">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="909bc-130">특정 [프레임워크](../../standard/frameworks.md)에 대한 테스트 이진 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-130">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="909bc-131">지정된 식을 사용하여 현재 프로젝트의 테스트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-131">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="909bc-132">자세한 내용은 [필터 옵션 세부 정보](#filter-option-details) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-132">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="909bc-133">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-133">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="909bc-134">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-134">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="909bc-135">테스트 결과에 대해 로거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-135">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="909bc-136">테스트 프로젝트를 실행하기 전에 빌드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-136">Doesn't build the test project before running it.</span></span> <span data-ttu-id="909bc-137">또한 `--no-restore` 플래그를 암시적으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-137">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="909bc-138">명령을 실행할 때 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-138">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="909bc-139">실행할 이진 파일을 찾을 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-139">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="909bc-140">테스트 결과가 배치될 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-140">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="909bc-141">지정한 디렉터리가 없으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-141">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="909bc-142">테스트를 실행할 때 사용할 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-142">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="909bc-143">현재 프로젝트에서 검색된 테스트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-143">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="909bc-144">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="909bc-145">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="909bc-146">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="909bc-146">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="909bc-147">테스트 실행에 지정된 경로에서 사용자 지정 테스트 어댑터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-147">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="909bc-148">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-148">Defines the build configuration.</span></span> <span data-ttu-id="909bc-149">기본값은 `Debug`이지만 프로젝트의 구성으로 이 기본 SDK 설정이 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-149">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="909bc-150">테스트 실행에 대한 데이터 수집기를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-150">Enables data collector for the test run.</span></span> <span data-ttu-id="909bc-151">자세한 내용은 [테스트 실행 모니터링 및 분석](https://aka.ms/vstest-collect)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-151">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="909bc-152">테스트 플랫폼에 대한 진단 모드를 사용하도록 설정하고 지정된 파일에 진단 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-152">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="909bc-153">특정 [프레임워크](../../standard/frameworks.md)에 대한 테스트 이진 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-153">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="909bc-154">지정된 식을 사용하여 현재 프로젝트의 테스트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-154">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="909bc-155">자세한 내용은 [필터 옵션 세부 정보](#filter-option-details) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-155">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="909bc-156">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-156">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="909bc-157">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-157">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="909bc-158">테스트 결과에 대해 로거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-158">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="909bc-159">테스트 프로젝트를 실행하기 전에 빌드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-159">Doesn't build the test project before running it.</span></span> <span data-ttu-id="909bc-160">또한 `--no-restore` 플래그를 암시적으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-160">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="909bc-161">명령을 실행할 때 암시적 복원을 실행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-161">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="909bc-162">실행할 이진 파일을 찾을 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-162">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="909bc-163">테스트 결과가 배치될 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-163">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="909bc-164">지정한 디렉터리가 없으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-164">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="909bc-165">테스트를 실행할 때 사용할 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-165">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="909bc-166">현재 프로젝트에서 검색된 테스트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-166">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="909bc-167">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-167">Sets the verbosity level of the command.</span></span> <span data-ttu-id="909bc-168">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-168">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="909bc-169">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="909bc-169">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="909bc-170">테스트 실행에 지정된 경로에서 사용자 지정 테스트 어댑터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-170">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="909bc-171">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-171">Defines the build configuration.</span></span> <span data-ttu-id="909bc-172">기본값은 `Debug`이지만 프로젝트의 구성으로 이 기본 SDK 설정이 재정의될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-172">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="909bc-173">테스트 플랫폼에 대한 진단 모드를 사용하도록 설정하고 지정된 파일에 진단 메시지를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-173">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="909bc-174">특정 [프레임워크](../../standard/frameworks.md)에 대한 테스트 이진 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-174">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="909bc-175">지정된 식을 사용하여 현재 프로젝트의 테스트를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-175">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="909bc-176">자세한 내용은 [필터 옵션 세부 정보](#filter-option-details) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-176">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="909bc-177">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-177">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="909bc-178">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-178">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="909bc-179">테스트 결과에 대해 로거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-179">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="909bc-180">테스트 프로젝트를 실행하기 전에 빌드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-180">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="909bc-181">실행할 이진 파일을 찾을 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-181">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="909bc-182">테스트를 실행할 때 사용할 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-182">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="909bc-183">현재 프로젝트에서 검색된 테스트를 모두 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-183">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="909bc-184">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-184">Sets the verbosity level of the command.</span></span> <span data-ttu-id="909bc-185">허용되는 값은 `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, `diag[nostic]`입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-185">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="909bc-186">예제</span><span class="sxs-lookup"><span data-stu-id="909bc-186">Examples</span></span>

<span data-ttu-id="909bc-187">현재 디렉터리에 있는 프로젝트에서 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-187">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="909bc-188">`test1` 프로젝트에서 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-188">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

<span data-ttu-id="909bc-189">현재 디렉터리의 프로젝트에서 테스트를 실행하고 trx 형식으로 테스트 결과 파일을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-189">Run the tests in the project in the current directory and generate a test results file in the trx format:</span></span>

`dotnet test --logger:trx`

## <a name="filter-option-details"></a><span data-ttu-id="909bc-190">필터 옵션 세부 정보</span><span class="sxs-lookup"><span data-stu-id="909bc-190">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="909bc-191">`<Expression>`에 `<property><operator><value>[|&<Expression>]` 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-191">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="909bc-192">`<property>`은(는) `Test Case`의 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-192">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="909bc-193">다음은 인기 있는 단위 테스트 프레임 워크에서 지원되는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-193">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="909bc-194">테스트 프레임워크</span><span class="sxs-lookup"><span data-stu-id="909bc-194">Test Framework</span></span> | <span data-ttu-id="909bc-195">지원되는 속성</span><span class="sxs-lookup"><span data-stu-id="909bc-195">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="909bc-196">MSTest</span><span class="sxs-lookup"><span data-stu-id="909bc-196">MSTest</span></span>         | <ul><li><span data-ttu-id="909bc-197">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="909bc-197">FullyQualifiedName</span></span></li><li><span data-ttu-id="909bc-198">name</span><span class="sxs-lookup"><span data-stu-id="909bc-198">Name</span></span></li><li><span data-ttu-id="909bc-199">ClassName</span><span class="sxs-lookup"><span data-stu-id="909bc-199">ClassName</span></span></li><li><span data-ttu-id="909bc-200">우선 순위</span><span class="sxs-lookup"><span data-stu-id="909bc-200">Priority</span></span></li><li><span data-ttu-id="909bc-201">TestCategory</span><span class="sxs-lookup"><span data-stu-id="909bc-201">TestCategory</span></span></li></ul> |
| <span data-ttu-id="909bc-202">xUnit</span><span class="sxs-lookup"><span data-stu-id="909bc-202">xUnit</span></span>          | <ul><li><span data-ttu-id="909bc-203">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="909bc-203">FullyQualifiedName</span></span></li><li><span data-ttu-id="909bc-204">DisplayName</span><span class="sxs-lookup"><span data-stu-id="909bc-204">DisplayName</span></span></li><li><span data-ttu-id="909bc-205">특성</span><span class="sxs-lookup"><span data-stu-id="909bc-205">Traits</span></span></li></ul>                                   |

<span data-ttu-id="909bc-206">`<operator>`은(는) 속성과 값 사이의 관계를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-206">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="909bc-207">연산자</span><span class="sxs-lookup"><span data-stu-id="909bc-207">Operator</span></span> | <span data-ttu-id="909bc-208">함수</span><span class="sxs-lookup"><span data-stu-id="909bc-208">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="909bc-209">정확하게 일치</span><span class="sxs-lookup"><span data-stu-id="909bc-209">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="909bc-210">정확하게 일치하지 않음</span><span class="sxs-lookup"><span data-stu-id="909bc-210">Not exact match</span></span> |
| `~`      | <span data-ttu-id="909bc-211">포함</span><span class="sxs-lookup"><span data-stu-id="909bc-211">Contains</span></span>        |

<span data-ttu-id="909bc-212">`<value>`는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-212">`<value>` is a string.</span></span> <span data-ttu-id="909bc-213">모든 조회는 대/소문자를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-213">All the lookups are case insensitive.</span></span>

<span data-ttu-id="909bc-214">`<operator>`이(가) 없는 식은 `FullyQualifiedName` 속성의 `contains`(으)로 자동으로 간주됩니다(예를 들어 `dotnet test --filter xyz`과(와) `dotnet test --filter FullyQualifiedName~xyz`이(가) 동일).</span><span class="sxs-lookup"><span data-stu-id="909bc-214">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="909bc-215">식은 조건부 연산자와 조인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="909bc-215">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="909bc-216">연산자</span><span class="sxs-lookup"><span data-stu-id="909bc-216">Operator</span></span>            | <span data-ttu-id="909bc-217">함수</span><span class="sxs-lookup"><span data-stu-id="909bc-217">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="909bc-218">또는</span><span class="sxs-lookup"><span data-stu-id="909bc-218">OR</span></span>       |
| `&`                 | <span data-ttu-id="909bc-219">AND</span><span class="sxs-lookup"><span data-stu-id="909bc-219">AND</span></span>      |

<span data-ttu-id="909bc-220">조건부 연산자를 사용 하는 경우 식을 괄호로 묶을 수 있습니다(예: `(Name~TestMethod1) | (Name~TestMethod2)`).</span><span class="sxs-lookup"><span data-stu-id="909bc-220">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="909bc-221">선택적 단위 테스트 필터링을 사용하는 방법에 대한 자세한 내용 및 예제는 [선택적 단위 테스트 실행](../testing/selective-unit-tests.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="909bc-221">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="909bc-222">참고 항목</span><span class="sxs-lookup"><span data-stu-id="909bc-222">See also</span></span>

* [<span data-ttu-id="909bc-223">프레임워크 및 대상</span><span class="sxs-lookup"><span data-stu-id="909bc-223">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
* [<span data-ttu-id="909bc-224">.NET Core RID(런타임 식별자) 카탈로그</span><span class="sxs-lookup"><span data-stu-id="909bc-224">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
