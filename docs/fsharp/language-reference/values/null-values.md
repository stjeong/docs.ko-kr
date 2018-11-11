---
title: Null 값(F#)
description: F# 프로그래밍 언어에서 null 값은 사용 하는 방법을 알아봅니다.
ms.date: 05/16/2016
ms.openlocfilehash: 8751ac402c43ddb07fb62e08b6c6d5403cbe9acc
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43787904"
---
# <a name="null-values"></a>Null 값

이 항목에서는 F#에서 null 값을 어떻게 사용 되는지 설명 합니다.

## <a name="null-value"></a>Null 값

Null 값을 사용 되지 않습니다 일반적으로 F#의 값 또는 변수. 그러나 null 특정 상황에서 비정상적인 값으로 표시 됩니다. 하지 않은 경우 null 일반 값으로 허용 하지를 F#에서 형식을 정의 하는 경우는 [AllowNullLiteral](https://msdn.microsoft.com/library/4f315196-f444-4cca-ba07-1176ff71eb0f) 특성 형식에 적용 됩니다. 형식을 정의 하는 몇 가지 다른.NET 언어로, null 인지 가능한 값을 하 고 이러한 형식과 상호 작용 하는, 하는 경우 F# 코드에서는 null 값이 발생할 수 있습니다.

정의 F# 및 F#에서 엄격 하 게 사용 하는 형식에 대 한 F# 라이브러리를 직접 사용 하 여 null 값을 만들어야 하는 유일한 방법은 사용 하는 것 [Unchecked.defaultof](https://msdn.microsoft.com/library/9ff97f2a-1bd4-4f4c-afbe-5886a74ab977) 하거나 [Array.zeroCreate](https://msdn.microsoft.com/library/fa5b8e7a-1b5b-411c-8622-b58d7a14d3b2)합니다. 그러나 다른.NET 언어에서 사용 되는 F# 형식에 대해 또는 F#에서.NET Framework 같은 작성 되지 않은 API를 사용 하 여 해당 형식을 사용 하는 경우에 null 값 발생할 수 있습니다.

사용할 수는 `option` F# 다른.NET 언어를 사용할 수 있는 null 값을 사용 하 여 참조 변수를 사용할 수 있는 경우에 형식입니다. F#을 사용 하 여 null 대신 `option` 형식 옵션 값을 사용 하면 `None` 개체가 없는 경우. 옵션 값을 사용 하면 `Some(obj)` 개체를 사용 하 여 `obj` 개체인 경우. 자세한 내용은 [옵션](../options.md)합니다.

`null` 키워드는 F# 언어에서 유효한 키워드 및.NET Framework Api 또는 다른.NET 언어로 작성 된 다른 Api를 사용 하 여 작업할 때 사용 해야 합니다. Null 값을 해야 할 수도 있습니다는 두 가지 경우.NET API를 호출 하 고 null 값을 인수로 전달 하는 경우 반환 값 또는.NET 메서드 호출에서 출력 매개 변수를 해석할 때 되며.

Null 값에는.NET 메서드를 전달 하려면 사용 된 `null` 호출 코드의 키워드입니다. 다음 코드 예제에서는 그 구체적인 방법을 보여 줍니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet701.fs)]

.NET 메서드에서 가져온 null 값을 해석할 수 있는 경우 패턴 일치를 사용 합니다. 다음 코드 예제에서 반환 되는 null 값을 해석 하 패턴 일치를 사용 하는 방법을 보여 줍니다 `ReadLine` 입력 스트림의 끝을 넘어 읽으려고 시도할 때.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet702.fs)]

를 사용 하는 경우와 같이 다른 방법으로 F# 형식에 대해 null 값을 생성할 수도 있습니다 `Array.zeroCreate`를 호출 하는 `Unchecked.defaultof`합니다. 캡슐화 된 null 값을 유지 하는 이러한 코드를 사용 하 여 주의 해야 합니다. 만 위한 F# 라이브러리에서 모든 함수에서 null 값을 검사할 필요가 없습니다. 다른.NET 언어와의 상호 운용성에 대 한 라이브러리를 작성 하는 것이 있으면 null 검사 입력 매개 변수 및 throw를 추가 하는 `ArgumentNullException`, C# 또는 Visual Basic 코드에서와 마찬가지로 합니다.

임의의 값을 null 인지 확인 하려면 다음 코드를 사용할 수 있습니다.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet703.fs)]

## <a name="see-also"></a>참고자료

- [값](index.md)
- [일치 식](../match-expressions.md)
