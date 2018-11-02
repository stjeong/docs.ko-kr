---
title: '예외: failwith 함수(F#)'
description: "'Failwith' 함수에서 F # 예외를 생성 하는 방법에 대해 알아봅니다."
ms.date: 05/16/2016
ms.openlocfilehash: 69a2eb69e0157d3bde8cb8884cb0ae960634dddc
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43863431"
---
# <a name="exceptions-the-failwith-function"></a>예외: failwith 함수

`failwith` 함수에는 F # 예외가 발생 합니다.

## <a name="syntax"></a>구문

```fsharp
failwith error-message-string
```

## <a name="remarks"></a>설명

합니다 *오류 메시지 문자열* 리터럴 문자열이 나 형식의 값은 이전 구문에서 `string`합니다. 되기는 `Message` 예외의 속성입니다.

생성 되는 예외 `failwith` 은 `System.Exception` 이름이 참조 하는 예외를 `Failure` F # 코드에서. 다음 코드에서는 `failwith` 예외를 throw 합니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6001.fs)]

## <a name="see-also"></a>참고자료

- [예외 처리](index.md)
- [예외 형식](exception-types.md)
- [예외: `try...with` 식](the-try-with-expression.md)
- [예외: `try...finally` 식](the-try-finally-expression.md)
- [예외: `raise` 함수](the-raise-function.md)
