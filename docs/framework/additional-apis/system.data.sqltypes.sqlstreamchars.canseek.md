---
title: SqlStreamChars.CanSeek 속성 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.CanSeek
- System.Data.SqlTypes.SqlStreamChars.get_CanSeek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 0145fe87e2c8aa3dd40e73f0089fe40b6b6cca30
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152736"
---
# <a name="sqlstreamcharscanseek-property"></a>SqlStreamChars.CanSeek 속성

파생된 클래스에서 재정의 되 면 현재 스트림이 검색 작업을 지원 하는지 여부를 나타내는 값을 가져옵니다. 이 속성을 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다. SQL Server에서 사용할 것입니다. 다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.

```csharp
public abstract bool CanSeek { get; }
```

## <a name="property-value"></a>속성 값

<xref:System.Boolean>\
`true` 현재 스트림이 seek 작업을 지 원하는 경우 그렇지 않으면 `false`합니다.

## <a name="remarks"></a>설명

> [!WARNING]
> `SqlStreamChars.CanSeek` 속성은 전용 이며 코드에서 직접 사용할 하려고 하지 않습니다.
>
> Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.

## <a name="requirements"></a>요구 사항

**네임스페이스:** <xref:System.Data.SqlTypes>

**어셈블리:** System.Data (System.Data.dll)

**.NET framework 버전:** 2.0부터 사용할 수 있습니다.