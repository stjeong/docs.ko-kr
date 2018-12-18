---
title: '#endif - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#endif'
helpviewer_keywords:
- '#endif directive [C#]'
ms.assetid: 6a5fca55-5aee-441f-86f6-1c99fbe9ec05
ms.openlocfilehash: 13b43919b666dcc8c5adfc3490eaad73960547ae
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243907"
---
# <a name="endif-c-reference"></a><span data-ttu-id="12352-102">#endif(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="12352-102">#endif (C# Reference)</span></span>
<span data-ttu-id="12352-103">`#endif`는 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) 지시문으로 시작한 조건부 지시문의 끝을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12352-103">`#endif` specifies the end of a conditional directive, which began with the [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive.</span></span> <span data-ttu-id="12352-104">예를 들어 개체에 적용된</span><span class="sxs-lookup"><span data-stu-id="12352-104">For example,</span></span>  
  
```csharp
#define DEBUG  
// ...  
#if DEBUG  
    Console.WriteLine("Debug version");  
#endif  
```  
  
## <a name="remarks"></a><span data-ttu-id="12352-105">설명</span><span class="sxs-lookup"><span data-stu-id="12352-105">Remarks</span></span>  
 <span data-ttu-id="12352-106">`#if` 지시문으로 시작되는 조건부 지시문은 `#endif` 지시문을 사용하여 명시적으로 종료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12352-106">A conditional directive, beginning with a `#if` directive, must explicitly be terminated with a `#endif` directive.</span></span> <span data-ttu-id="12352-107">`#endif`를 사용하는 방법에 대한 예제는 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12352-107">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#endif`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12352-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="12352-108">See Also</span></span>

- [<span data-ttu-id="12352-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="12352-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="12352-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="12352-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="12352-111">C# 전처리기 지시문</span><span class="sxs-lookup"><span data-stu-id="12352-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
