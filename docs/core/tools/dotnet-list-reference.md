---
title: dotnet list reference 명령 - .NET Core CLI
description: dotnet list reference 명령은 프로젝트 간 참조를 나열하는 편리한 옵션을 제공합니다.
ms.date: 12/03/2018
ms.openlocfilehash: 58b4e07abfe95d1febdd54d117825ecedf502e61
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152608"
---
# <a name="dotnet-list-reference"></a><span data-ttu-id="ebafd-103">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="ebafd-103">dotnet list reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="ebafd-104">name</span><span class="sxs-lookup"><span data-stu-id="ebafd-104">Name</span></span>

<span data-ttu-id="ebafd-105">`dotnet list reference` - 프로젝트 간 참조를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-105">`dotnet list reference` - Lists project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="ebafd-106">개요</span><span class="sxs-lookup"><span data-stu-id="ebafd-106">Synopsis</span></span>

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a><span data-ttu-id="ebafd-107">설명</span><span class="sxs-lookup"><span data-stu-id="ebafd-107">Description</span></span>

<span data-ttu-id="ebafd-108">`dotnet list reference` 명령은 지정된 프로젝트 또는 솔루션에 대한 프로젝트 참조를 나열하는 편리한 옵션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-108">The `dotnet list reference` command provides a convenient option to list project references for a given project or solution.</span></span>

## <a name="arguments"></a><span data-ttu-id="ebafd-109">인수</span><span class="sxs-lookup"><span data-stu-id="ebafd-109">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="ebafd-110">참조를 나열하기 위해 사용할 프로젝트 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-110">Specifies the project file to use for listing references.</span></span> <span data-ttu-id="ebafd-111">지정하지 않으면 이 명령은 현재 디렉터리에서 프로젝트 파일을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-111">If not specified, the command searches the current directory for a project file.</span></span>

## <a name="options"></a><span data-ttu-id="ebafd-112">옵션</span><span class="sxs-lookup"><span data-stu-id="ebafd-112">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="ebafd-113">명령에 대한 간단한 도움말을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="ebafd-114">예제</span><span class="sxs-lookup"><span data-stu-id="ebafd-114">Examples</span></span>

* <span data-ttu-id="ebafd-115">지정된 프로젝트에 대한 프로젝트 참조를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-115">List the project references for the specified project:</span></span>

  ```console
  dotnet list app/app.csproj reference
  ```

* <span data-ttu-id="ebafd-116">현재 디렉터리에 있는 프로젝트에 대한 프로젝트 참조를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ebafd-116">List the project references for the project in the current directory:</span></span>

  ```console
  dotnet list reference
  ```