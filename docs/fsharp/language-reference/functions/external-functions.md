---
title: 외부 함수
description: 알아봅니다는 F# 네이티브 코드의 함수를 호출 하는 것에 대 한 언어 지원 합니다.
ms.date: 05/16/2016
ms.openlocfilehash: 86ea78844fb812361233f8360c377465d83be203
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53611733"
---
# <a name="external-functions"></a>외부 함수

설명 F# 네이티브 코드의 함수를 호출 하는 것에 대 한 언어 지원 합니다.

## <a name="syntax"></a>구문

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a>설명

이전 구문에서 *인수* 에 제공 되는 인수를 나타내는 `System.Runtime.InteropServices.DllImportAttribute` 특성입니다. 첫 번째 인수는.dll 확장명 없이이 함수를 포함 하는 DLL의 이름을 나타내는 문자열입니다. 공용 속성에 대 한 추가 인수를 제공할 수 있습니다는 `System.Runtime.InteropServices.DllImportAttribute` 호출 규칙 같은 클래스입니다.

네이티브 다음 내보낸된 함수를 포함 하는 c + + DLL을 있다고 가정 합니다.

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

이 함수를 호출할 수 있습니다 F# 다음 코드를 사용 하 여 합니다.

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

네이티브 코드와의 상호 운용성 이라고 *플랫폼 호출* 이며 CLR의 기능입니다. 자세한 내용은 [비관리 코드 상호 운용](../../../../docs/framework/interop/index.md)을 참조하세요. 이 섹션의 정보에 적용 됩니다 F#입니다.

## <a name="see-also"></a>참고 항목

- [함수](index.md)