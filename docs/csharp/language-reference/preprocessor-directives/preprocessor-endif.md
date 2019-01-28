---
title: '#endif - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#endif'
helpviewer_keywords:
- '#endif directive [C#]'
ms.assetid: 6a5fca55-5aee-441f-86f6-1c99fbe9ec05
ms.openlocfilehash: 58e29363ca1298966ecf88e6b456f33f43a176b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573048"
---
# <a name="endif-c-reference"></a><span data-ttu-id="c8e49-102">#endif(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="c8e49-102">#endif (C# Reference)</span></span>
<span data-ttu-id="c8e49-103">`#endif`는 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) 지시문으로 시작한 조건부 지시문의 끝을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e49-103">`#endif` specifies the end of a conditional directive, which began with the [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive.</span></span> <span data-ttu-id="c8e49-104">예를 들어 개체에 적용된</span><span class="sxs-lookup"><span data-stu-id="c8e49-104">For example,</span></span>  
  
```csharp
#define DEBUG  
// ...  
#if DEBUG  
    Console.WriteLine("Debug version");  
#endif  
```  
  
## <a name="remarks"></a><span data-ttu-id="c8e49-105">주의</span><span class="sxs-lookup"><span data-stu-id="c8e49-105">Remarks</span></span>  
 <span data-ttu-id="c8e49-106">`#if` 지시문으로 시작되는 조건부 지시문은 `#endif` 지시문을 사용하여 명시적으로 종료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e49-106">A conditional directive, beginning with a `#if` directive, must explicitly be terminated with a `#endif` directive.</span></span> <span data-ttu-id="c8e49-107">`#endif`를 사용하는 방법에 대한 예제는 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8e49-107">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#endif`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8e49-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c8e49-108">See also</span></span>

- [<span data-ttu-id="c8e49-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="c8e49-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="c8e49-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="c8e49-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="c8e49-111">C# 전처리기 지시문</span><span class="sxs-lookup"><span data-stu-id="c8e49-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
