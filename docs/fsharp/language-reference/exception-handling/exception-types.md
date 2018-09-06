---
title: 예외 형식(F#)
description: '정의 및 F # 예외 형식을 사용 하는 방법을 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: b8d648a3649153a3604856deb61ce41db8c40bf2
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858823"
---
# <a name="exception-types"></a>예외 형식

두 종류의 F # 예외:.NET 예외 형식 및 F # 예외 형식입니다. 이 항목에서는 정의 하 고 F # 예외 형식을 사용 하는 방법을 설명 합니다.

## <a name="syntax"></a>구문

```fsharp
exception exception-type of argument-type
```

## <a name="remarks"></a>설명

이전 구문에서 *예외 형식을* 새 F # 예외 형식, 이름 및 *인수 형식* 이 유형의 예외를 발생 시킬 때 제공할 수 있는 인수 형식을 나타냅니다. 튜플 형식을 사용 하 여 여러 인수를 지정할 수 있습니다 *인수 형식*합니다.

F # 예외에 대 한 일반적인 정의 다음과 같습니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5501.fs)]

사용 하 여이 형식의 예외를 생성할 수는 `raise` 함수를 다음과 같이 합니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5502.fs)]

F # 예외 형식을 사용 하 여 직접의 필터에에서는 `try...with` 다음 예와에서 같이 식입니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5503.fs)]

사용 하 여 정의 하는 예외 형식 합니다 `exception` F #의 키워드는에서 상속 되는 새로운 유형 `System.Exception`합니다.

## <a name="see-also"></a>참고자료

- [예외 처리](index.md)
- [예외: `raise` 함수](the-raise-function.md)
- [예외 계층](https://msdn.microsoft.com/library/z4c5tckx.aspx)
