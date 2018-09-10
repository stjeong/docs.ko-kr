---
title: '&amp;&amp; 연산자(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 459b791fde3e4d3940dbd3d916f940e81f365da6
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43529237"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="4796b-102">&amp;&amp; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="4796b-102">&amp;&amp; Operator (C# Reference)</span></span>
<span data-ttu-id="4796b-103">조건부 AND 연산자(`&&`)는 `bool` 피연산자의 논리적 AND를 수행하지만 필요할 경우 두 번째 피연산자만 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="4796b-103">The conditional-AND operator (`&&`) performs a logical-AND of its `bool` operands, but only evaluates its second operand if necessary.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4796b-104">설명</span><span class="sxs-lookup"><span data-stu-id="4796b-104">Remarks</span></span>  
 <span data-ttu-id="4796b-105">이 작업은</span><span class="sxs-lookup"><span data-stu-id="4796b-105">The operation</span></span>  
  
```csharp  
x && y  
```  
  
 <span data-ttu-id="4796b-106">연산에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="4796b-106">corresponds to the operation</span></span>  
  
```csharp  
x & y  
```  
  
 <span data-ttu-id="4796b-107">단, `x`가 `false`일 경우 `y`는 계산되지 않습니다. `y` 값이 무엇이든지 AND 연산의 결과는 `false`이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="4796b-107">except that if `x` is `false`, `y` is not evaluated, because the result of the AND operation is `false` no matter what the value of `y`  is.</span></span> <span data-ttu-id="4796b-108">이것을 "단락" 계산이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="4796b-108">This is known as "short-circuit" evaluation.</span></span>  
  
 <span data-ttu-id="4796b-109">조건부 AND 연산자는 오버로드될 수 없지만 일반 논리 연산자와 [true](../../../csharp/language-reference/keywords/true.md) 및 [false](../../../csharp/language-reference/keywords/false.md) 연산자의 오버로드는 조건부 논리 연산자의 오버로드로 간주합니다(특정 제한 사항 있음).</span><span class="sxs-lookup"><span data-stu-id="4796b-109">The conditional-AND operator cannot be overloaded, but overloads of the regular logical operators and operators [true](../../../csharp/language-reference/keywords/true.md) and [false](../../../csharp/language-reference/keywords/false.md) are, with certain restrictions, also considered overloads of the conditional logical operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4796b-110">예</span><span class="sxs-lookup"><span data-stu-id="4796b-110">Example</span></span>  
 <span data-ttu-id="4796b-111">다음 예제에서는 피연산자가 `false`를 반환하므로 두 번째 `if` 문의 조건식은 첫 번째 피연산자만 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="4796b-111">In the following example, the conditional expression in the second `if` statement evaluates only the first operand because the operand returns `false`.</span></span>  
  
 [!code-csharp[csRefOperators#48](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-and-operator_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="4796b-112">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="4796b-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4796b-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4796b-113">See Also</span></span>

- [<span data-ttu-id="4796b-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="4796b-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4796b-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="4796b-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4796b-116">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="4796b-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
