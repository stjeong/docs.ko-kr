---
title: dotnet build-server 명령 - .NET Core CLI
description: dotnet build-server 명령은 빌드에서 시작된 서버와 상호 작용합니다.
ms.date: 12/04/2018
ms.openlocfilehash: 2746ade12cc819089258483e84a8c0f02a64c755
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53125680"
---
# <a name="dotnet-build-server"></a><span data-ttu-id="fb758-103">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="fb758-103">dotnet build-server</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="fb758-104">name</span><span class="sxs-lookup"><span data-stu-id="fb758-104">Name</span></span>

<span data-ttu-id="fb758-105">`dotnet build-server` - 빌드에서 시작된 서버와 상호 작용합니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-105">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="fb758-106">개요</span><span class="sxs-lookup"><span data-stu-id="fb758-106">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="fb758-107">명령</span><span class="sxs-lookup"><span data-stu-id="fb758-107">Commands</span></span>

* **`shutdown`**

  <span data-ttu-id="fb758-108">Dotnet에서 시작된 빌드 서버를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-108">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="fb758-109">기본적으로 모든 서버가 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-109">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="fb758-110">옵션</span><span class="sxs-lookup"><span data-stu-id="fb758-110">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="fb758-111">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-111">Prints out a short help for the command.</span></span>

* **`--msbuild`**

  <span data-ttu-id="fb758-112">MSBuild 빌드 서버를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-112">Shuts down the MSBuild build server.</span></span>

* **`--razor`**

  <span data-ttu-id="fb758-113">Razor 빌드 서버를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-113">Shuts down the Razor build server.</span></span>

* **`--vbcscompiler`**

  <span data-ttu-id="fb758-114">VB/C# 컴파일러 빌드 서버를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="fb758-114">Shuts down the VB/C# compiler build server.</span></span>