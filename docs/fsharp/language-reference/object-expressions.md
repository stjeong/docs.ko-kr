---
title: 개체 식
description: 사용 하는 방법을 알아봅니다 F# 명명 된 형식을 새 만들려면 개체 식 추가 코드와 오버 헤드를 방지 하려는 경우 필요 합니다.
ms.date: 05/16/2016
ms.openlocfilehash: cb15983543fde2459c589b3de2554575d73db686
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53613923"
---
# <a name="object-expressions"></a>개체 식

*식을 개체* 동적으로 생성 하는 익명 개체 형식의 새 인스턴스를 만드는 식입니다 되는 기존의 기본 형식, 인터페이스 또는 인터페이스의 집합 기반 합니다.

## <a name="syntax"></a>구문

```fsharp
// When typename is a class:
{ new typename [type-params]arguments with
    member-definitions
    [ additional-interface-definitions ]
}
// When typename is not a class:
{ new typename [generic-type-args] with
    member-definitions
    [ additional-interface-definitions ]
}
```

## <a name="remarks"></a>설명

위 구문에는 *typename* 은 기존 클래스 유형 또는 인터페이스 형식입니다. *형식-params* 선택적 제네릭 형식 매개 변수를 설명 합니다. 합니다 *인수* 생성자 매개 변수를 필요로 하는 클래스 형식에만 사용 됩니다. 합니다 *멤버 정의* 기본 클래스 또는 인터페이스에서 추상 메서드의 구현 또는 기본 클래스 메서드를 재정의 합니다.

다음 예제에서는 여러 다른 유형의 개체 식 보여 줍니다.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4301.fs)]

## <a name="using-object-expressions"></a>개체 식 사용

추가 코드와 명명 된 형식을 새로 만드는 데 필요한는 오버 헤드를 방지 하려면 개체 식을 사용 합니다. 개체 식을 사용 하 여 프로그램에서 생성 하는 형식의 수를 최소화 하는 경우 코드 줄의 수를 줄일 수 있으며 형식의 불필요 한 확산을 방지할 수 있습니다. 다양 한 형식을 특정 상황을 처리할 수만 만드는 대신 기존 형식을 사용자 지정 하거나 특정 사례에 대 한 인터페이스의 적절 한 구현을 제공 하는 개체 식을 사용할 수 있습니다.

## <a name="see-also"></a>참고 항목

- [F# 언어 참조](index.md)