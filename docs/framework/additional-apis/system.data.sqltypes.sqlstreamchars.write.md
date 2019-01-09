---
title: SqlStreamChars.Write (Char, Int32, Int32) 메서드 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: e8c8ee7ab7a744c1a1d18212f1c7f9788c91ea0d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152576"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a>(Char, Int32, Int32) SqlStreamChars.Write 메서드

파생된 클래스에서 재정의 문자의 시퀀스를 현재 스트림에 쓰고 쓴 문자 수 만큼이 스트림 내의 현재 위치를 이동 합니다. 이 메서드를 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다. SQL Server에서 사용할 것입니다. 다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a>매개 변수

`buffer`  
쓸 문자 배열입니다.

`offset`  
원점 기준으로 하는 오프셋입니다.

`count`  
현재 스트림에 쓸 문자 수입니다.

## <a name="remarks"></a>설명

> [!WARNING]
> `SqlStreamChars.Write` 메서드가 private 이며 코드에서 직접 사용할 하려고 하지 않습니다.
>
> Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.

## <a name="requirements"></a>요구 사항

**네임스페이스:** <xref:System.Data.SqlTypes>

**어셈블리:** System.Data (System.Data.dll)

**.NET framework 버전:** 2.0부터 사용할 수 있습니다.