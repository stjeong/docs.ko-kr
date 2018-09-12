---
title: 지연 계산(F#)
description: 'F # 지연 계산 앱 및 라이브러리의 성능을 향상 시킬 수 있습니다 하는 방법에 대해 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: 8afe815f26978de96291a52973d54a9dbcc5eaf2
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44508428"
---
# <a name="lazy-computations"></a>지연 계산

*지연 계산* 즉시 평가 되지 않습니다 하지만 결과가 필요한 경우 대신 평가 되는 계산 합니다. 이 코드의 성능을 향상 시킬 수 있습니다.

## <a name="syntax"></a>구문

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a>설명

이전 구문에서 *식* 결과가 필요한 경우에 평가 되는 코드 및 *식별자* 결과 저장 하는 값입니다. 형식의 값이 [ `Lazy<'T>` ](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489)여기서는 실제 형식은는 `'T` 식의 결과에서 결정 됩니다.

지연 계산을 사용 하면 결과가 필요할 때 해당 상황에만에 계산의 실행을 제한 하 여 성능을 향상 시킬 수 있습니다.

메서드를 호출 하면 수행할 계산을 적용할 `Force`합니다. `Force` 한 번만 수행 하 고 실행을 하면 됩니다. 에 대 한 후속 호출 `Force` 동일한 결과 실행 하지는 않습니다 모든 코드를 반환 합니다.

다음 코드에서는 지연 계산 사용 및 사용 `Force`합니다. 이 코드에서 형식의 `result` 됩니다 `Lazy<int>`, 및 `Force` 메서드가 반환 되는 `int`.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

지연 계산 하지 않고는 `Lazy` 입력, 시퀀스에도 사용 됩니다. 자세한 내용은 [시퀀스](sequences.md)합니다.

## <a name="see-also"></a>참고자료

- [F# 언어 참조](index.md)
- [LazyExtensions 모듈](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
