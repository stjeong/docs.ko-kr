---
title: 외부 함수(F#)
description: '네이티브 코드의 함수를 호출 하는 것에 대 한 F # 언어 지원에 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: db0d3362d867b07b333951f3380c6735ff471d5e
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45517049"
---
# <a name="external-functions"></a><span data-ttu-id="d11ea-103">외부 함수</span><span class="sxs-lookup"><span data-stu-id="d11ea-103">External Functions</span></span>

<span data-ttu-id="d11ea-104">이 항목에서는 네이티브 코드의 함수를 호출 하는 것에 대 한 F # 언어 지원을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-104">This topic describes F# language support for calling functions in native code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11ea-105">구문</span><span class="sxs-lookup"><span data-stu-id="d11ea-105">Syntax</span></span>

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a><span data-ttu-id="d11ea-106">설명</span><span class="sxs-lookup"><span data-stu-id="d11ea-106">Remarks</span></span>

<span data-ttu-id="d11ea-107">이전 구문에서 *인수* 에 제공 되는 인수를 나타내는 `System.Runtime.InteropServices.DllImportAttribute` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-107">In the previous syntax, *arguments* represents arguments that are supplied to the `System.Runtime.InteropServices.DllImportAttribute` attribute.</span></span> <span data-ttu-id="d11ea-108">첫 번째 인수는.dll 확장명 없이이 함수를 포함 하는 DLL의 이름을 나타내는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-108">The first argument is a string that represents the name of the DLL that contains this function, without the .dll extension.</span></span> <span data-ttu-id="d11ea-109">공용 속성에 대 한 추가 인수를 제공할 수 있습니다는 `System.Runtime.InteropServices.DllImportAttribute` 호출 규칙 같은 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-109">Additional arguments can be supplied for any of the public properties of the `System.Runtime.InteropServices.DllImportAttribute` class, such as the calling convention.</span></span>

<span data-ttu-id="d11ea-110">네이티브 다음 내보낸된 함수를 포함 하는 c + + DLL을 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-110">Assume you have a native C++ DLL that contains the following exported function.</span></span>

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

<span data-ttu-id="d11ea-111">다음 코드를 사용 하 여 F #에서이 함수를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-111">You can call this function from F# by using the following code.</span></span>

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

<span data-ttu-id="d11ea-112">네이티브 코드와의 상호 운용성 이라고 *플랫폼 호출* 이며 CLR의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-112">Interoperability with native code is referred to as *platform invoke* and is a feature of the CLR.</span></span> <span data-ttu-id="d11ea-113">자세한 내용은 [비관리 코드 상호 운용](../../../../docs/framework/interop/index.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d11ea-113">For more information, see [Interoperating with Unmanaged Code](../../../../docs/framework/interop/index.md).</span></span> <span data-ttu-id="d11ea-114">이 섹션의 정보는 F #에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d11ea-114">The information in that section is applicable to F#.</span></span>

## <a name="see-also"></a><span data-ttu-id="d11ea-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="d11ea-115">See also</span></span>

- [<span data-ttu-id="d11ea-116">함수</span><span class="sxs-lookup"><span data-stu-id="d11ea-116">Functions</span></span>](index.md)
