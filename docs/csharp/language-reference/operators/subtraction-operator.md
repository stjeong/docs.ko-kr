---
title: '- 연산자(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- -_CSharpKeyword
helpviewer_keywords:
- '- operator [C#]'
- subtraction operator (-) [C#]
ms.assetid: 4de7a4fa-c69d-48e6-aff1-3130af970b2d
ms.openlocfilehash: bd852f96ece9c8d5d5e2ec42e802596e795ce04a
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44210106"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="abac4-102">- 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="abac4-102">- Operator (C# Reference)</span></span>
<span data-ttu-id="abac4-103">`-` 연산자는 단항 또는 이항 연산자로 작동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abac4-103">The `-` operator can function as either a unary or a binary operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="abac4-104">설명</span><span class="sxs-lookup"><span data-stu-id="abac4-104">Remarks</span></span>  
 <span data-ttu-id="abac4-105">단항 `-` 연산자는 모든 숫자 형식에 대해 미리 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="abac4-105">Unary `-` operators are predefined for all numeric types.</span></span> <span data-ttu-id="abac4-106">숫자 형식에 대한 단항 `-` 연산의 결과는 피연산자의 숫자 부정입니다.</span><span class="sxs-lookup"><span data-stu-id="abac4-106">The result of a unary `-` operation on a numeric type is the numeric negation of the operand.</span></span>  
  
 <span data-ttu-id="abac4-107">이항 `-` 연산자는 첫 번째 피연산자에서 두 번째 피연산자를 빼도록 모든 숫자 및 열거형 형식에 대해 미리 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abac4-107">Binary `-` operators are predefined for all numeric and enumeration types to subtract the second operand from the first.</span></span>  
  
 <span data-ttu-id="abac4-108">대리자 형식도 대리자 제거를 수행하는 이항 `-` 연산자를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="abac4-108">Delegate types also provide a binary `-` operator, which performs delegate removal.</span></span>  
  
 <span data-ttu-id="abac4-109">사용자 정의 형식은 단항 `-` 및 이항 `-` 연산자를 오버로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abac4-109">User-defined types can overload the unary `-` and binary `-` operators.</span></span> <span data-ttu-id="abac4-110">자세한 내용은 [연산자(C# 참조)](../../../csharp/language-reference/keywords/operator.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="abac4-110">For more information, see [operator (C# Reference)](../../../csharp/language-reference/keywords/operator.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="abac4-111">예</span><span class="sxs-lookup"><span data-stu-id="abac4-111">Example</span></span>  
 [!code-csharp[csRefOperators#40](../../../csharp/language-reference/operators/codesnippet/CSharp/subtraction-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="abac4-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="abac4-112">See Also</span></span>

- [<span data-ttu-id="abac4-113">C# 참조</span><span class="sxs-lookup"><span data-stu-id="abac4-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="abac4-114">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="abac4-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="abac4-115">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="abac4-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
