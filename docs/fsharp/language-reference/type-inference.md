---
title: 형식 유추(F#)
description: 'F # 컴파일러 값, 변수, 매개 변수 및 반환 값의 형식을 유추 하는 방법에 대해 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: fd826ac48fb9a70aa6f4ff746599c11b7e21a02e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43865698"
---
# <a name="type-inference"></a>형식 유추

이 항목에서는 F # 컴파일러는 값, 변수, 매개 변수 및 반환 값 형식을 유추 하는 방법을 설명 합니다.

## <a name="type-inference-in-general"></a>형식 유추를 일반 사항

형식 유추는 컴파일러가 형식을 최종적으로 추론할 수 없습니다. 제외 하 고 F # 구문 형식을 지정할 필요가 없습니다 합니다. 명시적 형식 정보를 생략 하면는 F #은 동적으로 형식화 된 언어 또는 형식화 된 약한는 F # 값 의미 하지 않습니다. F #은 컴파일러가 컴파일 중 각 구문에 대 한 정확한 형식을 추론 하는 정적 형식의 언어입니다. 각 구문의 형식을 추론 하도록 컴파일러에 대 한 충분 한 정보가 없는 경우 코드 어딘가에 명시적 형식 주석을 추가 하 여 일반적으로 추가 형식 정보를 제공 해야 합니다.

## <a name="inference-of-parameter-and-return-types"></a>매개 변수 및 반환 형식 유추

매개 변수 목록, 각 매개 변수의 형식을 지정할 필요가 없습니다. 아직 F #은 정적으로 형식화 된 언어 및 따라서 모든 값과 식 형식이 한정 된 컴파일 타임에 합니다. 컴파일러는 명시적으로 지정 하지 않는 해당 형식에 대 한 컨텍스트를 기반으로 형식을 유추 합니다. 형식에 별도로 지정 하지 않은 경우에 제네릭으로 유추 됩니다. 코드에서는 값을 일관 되지 않게 하는 경우 이러한 방식으로 단일 이상 인지 유추 컴파일러 오류를 보고, 값의 모든 사용을 충족 하는 형식.

함수의 반환 형식은 함수에 있는 마지막 식의 형식에 의해 결정 됩니다.

예를 들어, 다음 코드에서는 형식 매개 변수에서에서 `a` 및 `b` 반환 형식 모두로 유추 하 고 `int` 때문에 리터럴 `100` 형식의 `int`합니다.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet301.fs)]

리터럴은 변경 하 여 형식 유추를 조작할 수 있습니다. 경우는 `100` 는 `uint32` 접미사를 추가 하 여 `u`, 유형을 `a`, `b`, 반환 값으로 유추 되 고 `uint32`입니다.

영향을 줄 수도 수, 함수 및 메서드를 특정 형식에만 사용 하는 같은 형식에 대 한 제한이 의미 하는 기타 항목을 사용 하 여 형식을 유추 합니다.

또한 적용할 수 있습니다 명시적 형식 주석을 함수 또는 메서드 매개 변수 또는 식에서 변수는 다음 예와에서 같이. 오류가 발생 하면 다른 제약 조건 간에 충돌이 발생 하면 발생 합니다.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet302.fs)]

형식 주석이 매개 변수를 모두 제공 하 여 함수의 반환 값을 명시적으로 지정할 수 있습니다.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet303.fs)]

일반적인 사례는 형식 주석을 유용 매개 변수의 경우 매개 변수는 개체 형식 및 멤버를 사용 하려는 경우

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet304.fs)]

## <a name="automatic-generalization"></a>자동 일반화

함수 코드 매개 변수의 형식에 종속 된 경우 컴파일러는 매개 변수를 제네릭를 고려 합니다. 이 이라고 *자동 일반화*, 복잡성을 늘리지 않고 일반 코드를 작성 하는 데 강력한 aid 수 있습니다.

예를 들어, 다음 함수는 튜플로 모든 형식의 두 매개 변수를 결합합니다.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet305.fs)]

형식 유추 됩니다.

```fsharp
'a -> 'b -> 'a * 'b
```

## <a name="additional-information"></a>추가 정보

형식 유추는 F # 언어 사양에 자세히 설명 되어 있습니다.

## <a name="see-also"></a>참고자료

- [자동 일반화](generics/automatic-generalization.md)
