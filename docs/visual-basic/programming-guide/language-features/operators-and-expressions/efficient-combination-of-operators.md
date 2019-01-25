---
title: 연산자의 효율적 결합(Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- expressions [Visual Basic], parentheses
- operators [Visual Basic], associativity
- expressions [Visual Basic], operators
- operators [Visual Basic], precedence
- Visual Basic code, operators
- Visual Basic code, expressions
- operators [Visual Basic], complex expressions
- expressions [Visual Basic], complex
- parentheses [Visual Basic], complex expressions
- numeric expressions
ms.assetid: bd22340e-b5be-458b-8772-3916c02309a4
ms.openlocfilehash: daaf75256b3449209b4e3c030cc6b54692c6a172
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54620431"
---
# <a name="efficient-combination-of-operators-visual-basic"></a><span data-ttu-id="76c74-102">연산자의 효율적 결합(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="76c74-102">Efficient Combination of Operators (Visual Basic)</span></span>
<span data-ttu-id="76c74-103">복잡 한 식은 여러 다른 연산자를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-103">Complex expressions can contain many different operators.</span></span> <span data-ttu-id="76c74-104">다음은 이에 대한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-104">The following example illustrates this.</span></span>  
  
 `x = (45 * (y + z)) ^ (2 / 85) * 5 + z`  
  
 <span data-ttu-id="76c74-105">앞의 예제에서와 같은 복잡 한 식 작성 연산자 우선 순위 규칙을 파악을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-105">Creating complex expressions such as the one in the preceding example requires a thorough understanding of the rules of operator precedence.</span></span> <span data-ttu-id="76c74-106">자세한 내용은 [Visual Basic의 연산자 우선 순위](../../../../visual-basic/language-reference/operators/operator-precedence.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-106">For more information, see [Operator Precedence in Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md).</span></span>  
  
## <a name="parenthetical-expressions"></a><span data-ttu-id="76c74-107">괄호 식</span><span class="sxs-lookup"><span data-stu-id="76c74-107">Parenthetical Expressions</span></span>  
 <span data-ttu-id="76c74-108">작업을 진행할 연산자 우선 순위에 의해 결정 된 것과 다른 순서로 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-108">Often you want operations to proceed in a different order from that determined by operator precedence.</span></span> <span data-ttu-id="76c74-109">다음 예제를 살펴보십시오.</span><span class="sxs-lookup"><span data-stu-id="76c74-109">Consider the following example.</span></span>  
  
 `x = z * y + 4`  
  
 <span data-ttu-id="76c74-110">앞의 예제를 곱합니다 `z` 하 여 `y`에 추가한 다음 결과를 `4`입니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-110">The preceding example multiplies `z` by `y`, then adds the result to `4`.</span></span> <span data-ttu-id="76c74-111">추가 하려는 경우 `y` 하 고 `4` 결과 곱하기 전에 `z`, 괄호를 사용 하 여 일반 연산자 우선 순위를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-111">But if you want to add `y` and `4` before multiplying the result by `z`, you can override normal operator precedence by using parentheses.</span></span> <span data-ttu-id="76c74-112">식을 괄호로 묶어 해당 식 연산자 우선 순위에 관계 없이 먼저 계산 하도록 강제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-112">By enclosing an expression in parentheses, you force that expression to be evaluated first, regardless of operator precedence.</span></span> <span data-ttu-id="76c74-113">먼저 추가 위해 앞의 예제를 강제 적용 하려면 다음 예제와 같이 다시를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-113">To force the preceding example to do the addition first, you could rewrite it as in the following example.</span></span>  
  
 `x = z * (y + 4)`  
  
 <span data-ttu-id="76c74-114">위의 예제에서는 `y` 하 고 `4`를 더한 값에 더한 후 `z`합니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-114">The preceding example adds `y` and `4`, then multiplies that sum by `z`.</span></span>  
  
### <a name="nested-parenthetical-expressions"></a><span data-ttu-id="76c74-115">중첩 된 괄호 식</span><span class="sxs-lookup"><span data-stu-id="76c74-115">Nested Parenthetical Expressions</span></span>  
 <span data-ttu-id="76c74-116">식에 여러 수준의 우선 순위를 추가로 재정의 하려면 괄호를 중첩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-116">You can nest expressions in multiple levels of parentheses to override precedence even further.</span></span> <span data-ttu-id="76c74-117">가장 깊게 중첩 등을 가장 깊이 중첩 된 마지막 괄호 외부의 식이 다음 가장 깊이 중첩 된 괄호 안에 식은 먼저 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-117">The expressions most deeply nested in parentheses are evaluated first, followed by the next most deeply nested, and so on to the least deeply nested, and finally the expressions outside parentheses.</span></span> <span data-ttu-id="76c74-118">다음은 이에 대한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-118">The following example illustrates this.</span></span>  
  
 `x = (z * 4) ^ (y * (z + 2))`  
  
 <span data-ttu-id="76c74-119">앞의 예제에서 `z + 2` 먼저 계산된 된 다음 다른 괄호 식이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-119">In the preceding example, `z + 2` is evaluated first, then the other parenthetical expressions.</span></span> <span data-ttu-id="76c74-120">일반적으로 더하기 또는 곱하기 보다 높은 우선 순위에는 지 수가 고, 다른 식을 괄호로 묶여 있기 때문에이 예제의 마지막으로 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76c74-120">Exponentiation, which normally has higher precedence than addition or multiplication, is evaluated last in this example because the other expressions are enclosed in parentheses.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76c74-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="76c74-121">See also</span></span>
- [<span data-ttu-id="76c74-122">Visual Basic의 산술 연산자</span><span class="sxs-lookup"><span data-stu-id="76c74-122">Arithmetic Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
- [<span data-ttu-id="76c74-123">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="76c74-123">Comparison Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [<span data-ttu-id="76c74-124">Visual Basic의 논리 및 비트 연산자</span><span class="sxs-lookup"><span data-stu-id="76c74-124">Logical and Bitwise Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
- [<span data-ttu-id="76c74-125">논리/비트 연산자 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="76c74-125">Logical/Bitwise Operators (Visual Basic)</span></span>](../../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [<span data-ttu-id="76c74-126">부울 식</span><span class="sxs-lookup"><span data-stu-id="76c74-126">Boolean Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md)
- [<span data-ttu-id="76c74-127">값 비교</span><span class="sxs-lookup"><span data-stu-id="76c74-127">Value Comparisons</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md)
- [<span data-ttu-id="76c74-128">방법: 숫자 값 계산</span><span class="sxs-lookup"><span data-stu-id="76c74-128">How to: Calculate Numeric Values</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-calculate-numeric-values.md)
- [<span data-ttu-id="76c74-129">Visual Basic에서의 연산자 우선 순위</span><span class="sxs-lookup"><span data-stu-id="76c74-129">Operator Precedence in Visual Basic</span></span>](../../../../visual-basic/language-reference/operators/operator-precedence.md)
