---
title: dotnet help 명령 - .NET Core CLI
description: dotnet help 명령은 지정된 명령에 대한 자세한 온라인 설명서를 표시합니다.
ms.date: 12/04/2018
ms.openlocfilehash: 60d1cc706ca5c78fa3be877bd679888181213e88
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152177"
---
# <a name="dotnet-help-reference"></a><span data-ttu-id="9e750-103">dotnet help reference</span><span class="sxs-lookup"><span data-stu-id="9e750-103">dotnet help reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-2plus.md)]

## <a name="name"></a><span data-ttu-id="9e750-104">name</span><span class="sxs-lookup"><span data-stu-id="9e750-104">Name</span></span>

<span data-ttu-id="9e750-105">`dotnet help` - 지정된 명령에 대한 자세한 온라인 설명서를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9e750-105">`dotnet help` - Shows more detailed documentation online for the specified command.</span></span>

## <a name="synopsis"></a><span data-ttu-id="9e750-106">개요</span><span class="sxs-lookup"><span data-stu-id="9e750-106">Synopsis</span></span>

`dotnet help <COMMAND_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="9e750-107">설명</span><span class="sxs-lookup"><span data-stu-id="9e750-107">Description</span></span>

<span data-ttu-id="9e750-108">`dotnet help` 명령은 docs.microsoft.com에서 지정된 명령에 대한 자세한 정보를 제공하는 참조 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9e750-108">The `dotnet help` command opens up the reference page for more detailed information about the specified command at docs.microsoft.com.</span></span>

## <a name="arguments"></a><span data-ttu-id="9e750-109">인수</span><span class="sxs-lookup"><span data-stu-id="9e750-109">Arguments</span></span>

* **`COMMAND_NAME`**

  <span data-ttu-id="9e750-110">.NET Core CLI 명령의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e750-110">Name of the .NET Core CLI command.</span></span> <span data-ttu-id="9e750-111">유효한 CLI 명령 목록은 [CLI 명령](index.md#cli-commands)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e750-111">For a list of the valid CLI commands, see [CLI commands](index.md#cli-commands).</span></span>

## <a name="options"></a><span data-ttu-id="9e750-112">옵션</span><span class="sxs-lookup"><span data-stu-id="9e750-112">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="9e750-113">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="9e750-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="9e750-114">예제</span><span class="sxs-lookup"><span data-stu-id="9e750-114">Examples</span></span>

* <span data-ttu-id="9e750-115">[dotnet new](dotnet-new.md) 명령에 대한 설명서 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9e750-115">Opens the documentation page for the [dotnet new](dotnet-new.md) command:</span></span>

  ```console
  dotnet help new
  ```