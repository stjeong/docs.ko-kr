---
title: dotnet clean 명령 - .NET Core CLI
description: dotnet clean 명령은 현재 디렉터리를 정리합니다.
ms.date: 12/04/2018
ms.openlocfilehash: 9930d2905f234e7125f27367cda36aa85ae23b87
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53144457"
---
# <a name="dotnet-clean"></a><span data-ttu-id="b7f33-103">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="b7f33-103">dotnet clean</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="b7f33-104">name</span><span class="sxs-lookup"><span data-stu-id="b7f33-104">Name</span></span>

<span data-ttu-id="b7f33-105">`dotnet clean` - 프로젝트의 출력을 정리합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-105">`dotnet clean` - Cleans the output of a project.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b7f33-106">개요</span><span class="sxs-lookup"><span data-stu-id="b7f33-106">Synopsis</span></span>

```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
dotnet clean [-h|--help]
```

## <a name="description"></a><span data-ttu-id="b7f33-107">설명</span><span class="sxs-lookup"><span data-stu-id="b7f33-107">Description</span></span>

<span data-ttu-id="b7f33-108">`dotnet clean` 명령은 이전 빌드의 출력을 정리합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-108">The `dotnet clean` command cleans the output of the previous build.</span></span> <span data-ttu-id="b7f33-109">이 명령은 [MSBuild 대상](/visualstudio/msbuild/msbuild-targets)으로 구현되므로 명령이 실행될 때 프로젝트가 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-109">It's implemented as an [MSBuild target](/visualstudio/msbuild/msbuild-targets), so the project is evaluated when the command is run.</span></span> <span data-ttu-id="b7f33-110">빌드 중 생성된 출력만 정리됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-110">Only the outputs created during the build are cleaned.</span></span> <span data-ttu-id="b7f33-111">중간(*obj*) 및 최종 출력(*bin*) 폴더가 모두 정리됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-111">Both intermediate (*obj*) and final output (*bin*) folders are cleaned.</span></span>

## <a name="arguments"></a><span data-ttu-id="b7f33-112">인수</span><span class="sxs-lookup"><span data-stu-id="b7f33-112">Arguments</span></span>

`PROJECT`

<span data-ttu-id="b7f33-113">정리할 MSBuild 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-113">The MSBuild project to clean.</span></span> <span data-ttu-id="b7f33-114">프로젝트 파일을 지정하지 않으면 MSBuild는 현재 작업 디렉터리에서 *proj*로 끝나는 파일 확장명이 있는 파일을 검색하고 해당 파일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-114">If a project file is not specified, MSBuild searches the current working directory for a file that has a file extension that ends in *proj* and uses that file.</span></span>

## <a name="options"></a><span data-ttu-id="b7f33-115">옵션</span><span class="sxs-lookup"><span data-stu-id="b7f33-115">Options</span></span>

* **`-c|--configuration {Debug|Release}`**

  <span data-ttu-id="b7f33-116">빌드 구성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-116">Defines the build configuration.</span></span> <span data-ttu-id="b7f33-117">기본값은 `Debug`입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-117">The default value is `Debug`.</span></span> <span data-ttu-id="b7f33-118">이 옵션은 빌드 시에 지정한 경우에만 정리 시에도 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-118">This option is only required when cleaning if you specified it during build time.</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="b7f33-119">빌드 시 지정한 [프레임워크](../../standard/frameworks.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-119">The [framework](../../standard/frameworks.md) that was specified at build time.</span></span> <span data-ttu-id="b7f33-120">프레임워크는 [프로젝트 파일](csproj.md)에 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-120">The framework must be defined in the [project file](csproj.md).</span></span> <span data-ttu-id="b7f33-121">빌드 시에 프레임워크를 지정한 경우 정리할 때도 프레임워크를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-121">If you specified the framework at build time, you must specify the framework when cleaning.</span></span>

* **`-h|--help`**

  <span data-ttu-id="b7f33-122">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-122">Prints out a short help for the command.</span></span>

* **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="b7f33-123">빌드 출력이 배치된 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-123">Directory in which the build outputs are placed.</span></span> <span data-ttu-id="b7f33-124">프로젝트를 빌드할 때 프레임워크를 지정한 경우 `-f|--framework <FRAMEWORK>` 스위치와 출력 디렉터리 스위치를 함께 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-124">Specify the `-f|--framework <FRAMEWORK>` switch with the output directory switch if you specified the framework when the project was built.</span></span>

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="b7f33-125">지정된 런타임의 출력 폴더를 정리합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-125">Cleans the output folder of the specified runtime.</span></span> <span data-ttu-id="b7f33-126">[자체 포함된 배포](../deploying/index.md#self-contained-deployments-scd)가 만들어진 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-126">This is used when a [self-contained deployment](../deploying/index.md#self-contained-deployments-scd) was created.</span></span> <span data-ttu-id="b7f33-127">.NET Core 2.0 SDK 이후 사용할 수 있는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-127">Option available since .NET Core 2.0 SDK.</span></span>

* **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="b7f33-128">명령의 세부 정보 표시 수준을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-128">Sets the verbosity level of the command.</span></span> <span data-ttu-id="b7f33-129">허용되는 수준은 q[uiet], m[inimal], n[ormal], d[etailed] 및 diag[nostic]입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f33-129">Allowed levels are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].</span></span>

## <a name="examples"></a><span data-ttu-id="b7f33-130">예제</span><span class="sxs-lookup"><span data-stu-id="b7f33-130">Examples</span></span>

* <span data-ttu-id="b7f33-131">프로젝트의 기본 빌드 정리:</span><span class="sxs-lookup"><span data-stu-id="b7f33-131">Clean a default build of the project:</span></span>

  ```console
  dotnet clean
  ```

* <span data-ttu-id="b7f33-132">릴리스 구성을 사용하여 빌드한 프로젝트 정리:</span><span class="sxs-lookup"><span data-stu-id="b7f33-132">Clean a project built using the Release configuration:</span></span>

  ```console
  dotnet clean --configuration Release
  ```