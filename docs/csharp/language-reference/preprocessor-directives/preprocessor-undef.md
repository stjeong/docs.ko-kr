---
title: '#undef(C# 참조)'
ms.date: 06/30/2018
f1_keywords:
- '#undef'
helpviewer_keywords:
- '#undef directive [C#]'
ms.assetid: 686c92d2-7194-4be4-b2f4-80091712d513
ms.openlocfilehash: 3957d58f61e51fab01618f5e1146be9cd0da58fd
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45590756"
---
# <a name="undef-c-reference"></a><span data-ttu-id="ddbee-102">#undef(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="ddbee-102">#undef (C# Reference)</span></span>
<span data-ttu-id="ddbee-103">`#undef`를 사용하면 기호의 정의를 해제할 수 있습니다. 그러면 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) 지시문에서 해당 기호를 식으로 사용하여 식이 `false`로 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="ddbee-103">`#undef` lets you undefine a symbol, such that, by using the symbol as the expression in a [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive, the expression will evaluate to `false`.</span></span>  
  
 <span data-ttu-id="ddbee-104">[#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) 지시문 또는 [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md) 컴파일러 옵션을 사용하여 기호를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddbee-104">A symbol can be defined either with the [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) directive or the [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md) compiler option.</span></span> <span data-ttu-id="ddbee-105">`#undef` 지시문은 지시문이 아닌 문을 사용하기 전에 파일에 나와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddbee-105">The `#undef` directive must appear in the file before you use any statements that are not also directives.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ddbee-106">예</span><span class="sxs-lookup"><span data-stu-id="ddbee-106">Example</span></span>  

```csharp
// preprocessor_undef.cs  
// compile with: /d:DEBUG  
#undef DEBUG  
using System;  
class MyClass
{  
    static void Main()
    {  
#if DEBUG  
        Console.WriteLine("DEBUG is defined");  
#else  
        Console.WriteLine("DEBUG is not defined");  
#endif  
    }  
}  
```

<span data-ttu-id="ddbee-107">**디버그가 정의되어 있지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="ddbee-107">**DEBUG is not defined**</span></span>

## <a name="see-also"></a><span data-ttu-id="ddbee-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ddbee-108">See Also</span></span>

- [<span data-ttu-id="ddbee-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="ddbee-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="ddbee-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="ddbee-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="ddbee-111">C# 전처리기 지시문</span><span class="sxs-lookup"><span data-stu-id="ddbee-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
