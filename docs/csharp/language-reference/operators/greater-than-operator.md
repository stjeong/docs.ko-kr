---
title: '&gt; 연산자(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- '>_CSharpKeyword'
helpviewer_keywords:
- '> operator [C#]'
- greater than operator (>) [C#]
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
ms.openlocfilehash: 08fe174c7e4351edc1d1c8cdb13d736b98242795
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510128"
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="9579d-102">&gt; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="9579d-102">&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="9579d-103">모든 숫자 형식과 열거형은 첫 번째 피연산자가 두 번째 피연산자보다 크면 `true`를 반환하고 그렇지 않으면 `false`를 반환하는 “보다 큼” 관계 연산자(`>`)를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="9579d-103">All numeric and enumeration types define a "greater than" relational operator (`>`) that returns `true` if the first operand is greater than the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9579d-104">설명</span><span class="sxs-lookup"><span data-stu-id="9579d-104">Remarks</span></span>  
 <span data-ttu-id="9579d-105">사용자 정의 형식은 `>` 연산자를 오버로드할 수 있습니다([operator](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="9579d-105">User-defined types can overload the `>` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="9579d-106">`>` 연산자가 오버로드되면 [<](../../../csharp/language-reference/operators/less-than-operator.md) 또한 오버로드되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9579d-106">If `>` is overloaded, [<](../../../csharp/language-reference/operators/less-than-operator.md) must also be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="9579d-107">예</span><span class="sxs-lookup"><span data-stu-id="9579d-107">Example</span></span>  
 [!code-csharp[csRefOperators#29](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="9579d-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9579d-108">See Also</span></span>

- [<span data-ttu-id="9579d-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="9579d-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="9579d-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="9579d-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9579d-111">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="9579d-111">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="9579d-112">explicit</span><span class="sxs-lookup"><span data-stu-id="9579d-112">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)
