---
title: '&lt; 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <_CSharpKeyword
helpviewer_keywords:
- less than operator (<) [C#]
- < operator [C#]
ms.assetid: 38cb91e6-79a6-48ec-9c1e-7b71fd8d2b41
ms.openlocfilehash: 3cc125471eee7bf0002e9844c2a1cdc05e8d4a03
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241236"
---
# <a name="lt-operator-c-reference"></a><span data-ttu-id="b7357-102">&lt; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="b7357-102">&lt; Operator (C# Reference)</span></span>
<span data-ttu-id="b7357-103">모든 숫자 형식과 열거형은 첫 번째 피연산자가 두 번째 피연산자보다 작으면 `true`를 반환하고 그렇지 않으면 `false`를 반환하는 “보다 작음” 관계 연산자(`<`)를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b7357-103">All numeric and enumeration types define a "less than" relational operator (`<`) that returns `true` if the first operand is less than the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7357-104">설명</span><span class="sxs-lookup"><span data-stu-id="b7357-104">Remarks</span></span>  
 <span data-ttu-id="b7357-105">사용자 정의 형식은 `<` 연산자를 오버로드할 수 있습니다([operator](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="b7357-105">User-defined types can overload the `<` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="b7357-106">`<` 연산자가 오버로드되면 [>](../../../csharp/language-reference/operators/greater-than-operator.md) 또한 오버로드되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7357-106">If `<` is overloaded, [>](../../../csharp/language-reference/operators/greater-than-operator.md) must also be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="b7357-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7357-107">Example</span></span>  
 [!code-csharp[csRefOperators#24](../../../csharp/language-reference/operators/codesnippet/CSharp/less-than-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b7357-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b7357-108">See Also</span></span>

- [<span data-ttu-id="b7357-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="b7357-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="b7357-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="b7357-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b7357-111">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="b7357-111">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
