---
title: '&amp; 연산자(C# 참조)'
ms.date: 04/04/2018
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
ms.openlocfilehash: b257c7d41618464e26ab3b54bcfb1f1e2c2e420e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510980"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="b4f07-102">&amp; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="b4f07-102">&amp; Operator (C# Reference)</span></span>
<span data-ttu-id="b4f07-103">`&` 연산자는 단항 또는 이항 연산자로 작동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-103">The `&` operator can function as either a unary or a binary operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b4f07-104">설명</span><span class="sxs-lookup"><span data-stu-id="b4f07-104">Remarks</span></span>  
 <span data-ttu-id="b4f07-105">단항 `&` 연산자는 해당 피연산자의 주소를 반환합니다([안전하지 않은](../../../csharp/language-reference/keywords/unsafe.md) 컨텍스트 필요).</span><span class="sxs-lookup"><span data-stu-id="b4f07-105">The unary `&` operator returns the address of its operand (requires [unsafe](../../../csharp/language-reference/keywords/unsafe.md) context).</span></span>  
  
 <span data-ttu-id="b4f07-106">이항 `&` 연산자는 정수 형식 및 `bool`에 대해 미리 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-106">Binary `&` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="b4f07-107">정수 형식의 경우 & 연산자는 해당 피연산자의 논리적 비트 AND를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-107">For integral types, & computes the logical bitwise AND of its operands.</span></span> <span data-ttu-id="b4f07-108">`bool` 피연산자의 경우 & 연산자는 해당 피연산자의 논리적 AND 연산을 계산합니다. 즉, 피연산자가 둘 다 `true`일 경우에만 결과가 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-108">For `bool` operands, & computes the logical AND of its operands; that is, the result is `true` if and only if both its operands are `true`.</span></span>  
  
 <span data-ttu-id="b4f07-109">이진 `&` 연산자는 [기존 AND 연산자](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`와 달리 첫 번째 연산자의 값에 상관없이 두 피연산자를 모두 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-109">The binary `&` operator evaluates both operands regardless of the first one's value, in contrast to the [conditional AND operator](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`.</span></span> <span data-ttu-id="b4f07-110">예:</span><span class="sxs-lookup"><span data-stu-id="b4f07-110">For example:</span></span>  
  
 [!code-csharp[csRefOperators#37](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_1.cs)]  
  
 <span data-ttu-id="b4f07-111">사용자 정의 형식으로 이항 `&` 연산자를 오버로드할 수 있습니다([operator](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="b4f07-111">User-defined types can overload the binary `&` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="b4f07-112">정수 계열 형식에 대한 연산은 일반적으로 열거형에서 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-112">Operations on integral types are generally allowed on enumeration.</span></span> <span data-ttu-id="b4f07-113">이항 연산자가 오버로드되면 해당 대입 연산자도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4f07-113">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b4f07-114">예</span><span class="sxs-lookup"><span data-stu-id="b4f07-114">Example</span></span>  
 [!code-csharp[csRefOperators#38](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b4f07-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b4f07-115">See Also</span></span>

- [<span data-ttu-id="b4f07-116">C# 참조</span><span class="sxs-lookup"><span data-stu-id="b4f07-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b4f07-117">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="b4f07-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b4f07-118">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="b4f07-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
