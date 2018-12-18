---
title: ':: 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 2e456be075f3487676228244e0119ff46ed9a538
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243480"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="fc178-102">:: 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="fc178-102">:: Operator (C# Reference)</span></span>
<span data-ttu-id="fc178-103">네임스페이스 별칭 한정자(`::`)는 식별자를 조회하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc178-103">The namespace alias qualifier (`::`) is used to look up identifiers.</span></span> <span data-ttu-id="fc178-104">다음 예제와 같이 항상 두 식별자 사이에 옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc178-104">It is always positioned between two identifiers, as in this example:</span></span>  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  

<span data-ttu-id="fc178-105">`::` 연산자는 *using 별칭 지시문*과 함께 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc178-105">The `::` operator can also be used with a *using alias directive*:</span></span>

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a><span data-ttu-id="fc178-106">설명</span><span class="sxs-lookup"><span data-stu-id="fc178-106">Remarks</span></span>  
 <span data-ttu-id="fc178-107">네임스페이스 별칭 한정자는 `global`일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc178-107">The namespace alias qualifier can be `global`.</span></span> <span data-ttu-id="fc178-108">별칭이 지정된 네임스페이스가 아니라 전역 네임스페이스에서 조회를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="fc178-108">This invokes a lookup in the global namespace, rather than an aliased namespace.</span></span>  
  
## <a name="for-more-information"></a><span data-ttu-id="fc178-109">자세한 내용</span><span class="sxs-lookup"><span data-stu-id="fc178-109">For More Information</span></span>  
 <span data-ttu-id="fc178-110">`::` 연산자를 사용하는 방법의 예는 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc178-110">For an example of how to use the `::` operator, see the following section:</span></span>  
  
-   [<span data-ttu-id="fc178-111">방법: 전역 네임스페이스 별칭 사용</span><span class="sxs-lookup"><span data-stu-id="fc178-111">How to: Use the Global Namespace Alias</span></span>](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="fc178-112">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="fc178-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fc178-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fc178-113">See Also</span></span>

- [<span data-ttu-id="fc178-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="fc178-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="fc178-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="fc178-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="fc178-116">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="fc178-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="fc178-117">네임스페이스 키워드</span><span class="sxs-lookup"><span data-stu-id="fc178-117">Namespace Keywords</span></span>](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [<span data-ttu-id="fc178-118">. 연산자</span><span class="sxs-lookup"><span data-stu-id="fc178-118">. Operator</span></span>](../../../csharp/language-reference/operators/member-access-operator.md)  
- [<span data-ttu-id="fc178-119">extern alias</span><span class="sxs-lookup"><span data-stu-id="fc178-119">extern alias</span></span>](../../../csharp/language-reference/keywords/extern-alias.md)
