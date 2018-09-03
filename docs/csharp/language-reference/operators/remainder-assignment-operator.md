---
title: '%= 연산자(C# 참조)'
ms.date: 04/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: 009c162b13fab05ba349d0535fe8dfae206502f3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43399493"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="19161-102">%= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="19161-102">%= Operator (C# Reference)</span></span>
<span data-ttu-id="19161-103">나머지 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="19161-103">The remainder assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="19161-104">설명</span><span class="sxs-lookup"><span data-stu-id="19161-104">Remarks</span></span>  
 <span data-ttu-id="19161-105">다음과 같은 `%=` 대입 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="19161-105">An expression using the `%=` assignment operator, such as</span></span>  
  
```csharp  
x %= y  
```  
  
 <span data-ttu-id="19161-106">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="19161-106">is equivalent to</span></span>  
  
```csharp  
x = x % y  
```  
  
 <span data-ttu-id="19161-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="19161-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="19161-108">[% 연산자](../../../csharp/language-reference/operators/remainder-operator.md)는 나누기 후 나머지를 계산하기 위해 숫자 형식에 대해 미리 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19161-108">The [% operator](../../../csharp/language-reference/operators/remainder-operator.md) is predefined for numeric types to compute the remainder after division.</span></span>  
  
 <span data-ttu-id="19161-109">`%=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [% 연산자](../../../csharp/language-reference/operators/remainder-operator.md)를 오버로드할 수 있습니다([연산자(C# 참조)](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="19161-109">The `%=` operator cannot be overloaded directly, but user-defined types can overload the [% operator](../../../csharp/language-reference/operators/remainder-operator.md) (see [operator (C# Reference)](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="19161-110">예</span><span class="sxs-lookup"><span data-stu-id="19161-110">Example</span></span>  
 [!code-csharp[csRefOperators#4](../../../csharp/language-reference/operators/codesnippet/CSharp/modulus-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="19161-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="19161-111">See Also</span></span>

- [<span data-ttu-id="19161-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="19161-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="19161-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="19161-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="19161-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="19161-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
