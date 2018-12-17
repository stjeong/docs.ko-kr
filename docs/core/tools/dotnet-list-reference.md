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
# <a name="dotnet-list-reference"></a>dotnet list reference

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>name

`dotnet list reference` - 프로젝트 간 참조를 나열합니다.

## <a name="synopsis"></a>개요

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a>설명

`dotnet list reference` 명령은 지정된 프로젝트 또는 솔루션에 대한 프로젝트 참조를 나열하는 편리한 옵션을 제공합니다.

## <a name="arguments"></a>인수

* **`PROJECT`**

  참조를 나열하기 위해 사용할 프로젝트 파일을 지정합니다. 지정하지 않으면 이 명령은 현재 디렉터리에서 프로젝트 파일을 검색합니다.

## <a name="options"></a>옵션

* **`-h|--help`**

  명령에 대한 간단한 도움말을 출력합니다.

## <a name="examples"></a>예제

* 지정된 프로젝트에 대한 프로젝트 참조를 나열합니다.

  ```console
  dotnet list app/app.csproj reference
  ```

* 현재 디렉터리에 있는 프로젝트에 대한 프로젝트 참조를 나열합니다.

  ```console
  dotnet list reference
  ```