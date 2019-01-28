---
title: '#else - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#else'
helpviewer_keywords:
- '#else directive [C#]'
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
ms.openlocfilehash: 67d3e6b8fc136e16fb0e307a9f8ceca494169bfc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696141"
---
# <a name="else-c-reference"></a><span data-ttu-id="15276-102">#else(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="15276-102">#else (C# Reference)</span></span>
<span data-ttu-id="15276-103">`#else`를 사용하면 복합 조건부 지시문을 만들 수 있습니다. 이 경우 앞의 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) 또는 (선택 사항)[#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) 지시문에 `true`로 평가하는 식이 없으면 컴파일러는 `#else`와 후속 `#endif` 사이에 있는 모든 코드를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="15276-103">`#else` lets you create a compound conditional directive, so that, if none of the expressions in the preceding [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) or (optional) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) directives evaluate to `true`, the compiler will evaluate all code between `#else` and the subsequent `#endif`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="15276-104">주의</span><span class="sxs-lookup"><span data-stu-id="15276-104">Remarks</span></span>  
 <span data-ttu-id="15276-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md)는 `#else` 이후의 다음 전처리기 지시문이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="15276-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) must be the next preprocessor directive after `#else`.</span></span> <span data-ttu-id="15276-106">`#else`를 사용하는 방법에 대한 예제는 [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="15276-106">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#else`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15276-107">참고 항목</span><span class="sxs-lookup"><span data-stu-id="15276-107">See also</span></span>

- [<span data-ttu-id="15276-108">C# 참조</span><span class="sxs-lookup"><span data-stu-id="15276-108">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="15276-109">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="15276-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="15276-110">C# 전처리기 지시문</span><span class="sxs-lookup"><span data-stu-id="15276-110">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
