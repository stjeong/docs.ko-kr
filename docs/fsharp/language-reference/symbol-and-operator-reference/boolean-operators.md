---
title: 부울 연산자(F#)
description: 'F # 프로그래밍 언어에서 사용할 수 있는 부울 연산자에 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: faa181090efa7c4064a30b42d83afa4888e98b82
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45638482"
---
# <a name="boolean-operators"></a>부울 연산자

이 항목에서는 F # 언어의 부울 연산자에 대 한 지원을 설명합니다.

## <a name="summary-of-boolean-operators"></a>부울 연산자 요약

다음 표에서 F # 언어에서 사용할 수 있는 부울 연산자를 보여 줍니다. 이러한 연산자에서 지 원하는 유일한 형식이 `bool` 형식입니다.

|연산자|설명|
|--------|-----------|
|`not`|부정 부울|
|<code>&#124;&#124;</code>|부울 OR|
|`&&`|부울 AND|

부울 AND 및 OR 연산자를 수행 *평가 단락 (short-circuit)*, 식의 전체 결과 확인 하는 데 필요한 경우에 연산자의 오른쪽에 있는 식 평가, 합니다. 두 번째 식의 `&&` 연산자는 첫 번째 식이 계산 되는 경우에 계산 됩니다 `true`;의 두 번째 식의 `||` 연산자는 첫 번째 식이 계산 되는 경우에 계산 됩니다 `false`합니다.

## <a name="see-also"></a>참고자료

- [비트 연산자](bitwise-operators.md)
- [산술 연산자](arithmetic-operators.md)
- [기호 및 연산자 참조](index.md)
