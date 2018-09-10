---
title: '*= 연산자(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: e47bc5c681c94ac3fc5c345c56b3814350ffa5ec
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517170"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="4ebc1-102">\*= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="4ebc1-102">\*= Operator (C# Reference)</span></span>
<span data-ttu-id="4ebc1-103">이항 곱하기 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="4ebc1-103">The binary multiplication assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4ebc1-104">설명</span><span class="sxs-lookup"><span data-stu-id="4ebc1-104">Remarks</span></span>  
 <span data-ttu-id="4ebc1-105">다음과 같은 `*=` 대입 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="4ebc1-105">An expression using the `*=` assignment operator, such as</span></span>  
  
```csharp  
x *= y  
```  
  
 <span data-ttu-id="4ebc1-106">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="4ebc1-106">is equivalent to</span></span>  
  
```csharp  
x = x * y  
```  
  
 <span data-ttu-id="4ebc1-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ebc1-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="4ebc1-108">[\* 연산자](../../../csharp/language-reference/operators/multiplication-operator.md)는 곱하기를 수행할 숫자 형식에 대해 미리 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ebc1-108">The [\* operator](../../../csharp/language-reference/operators/multiplication-operator.md) is predefined for numeric types to perform multiplication.</span></span>  
  
 <span data-ttu-id="4ebc1-109">`*=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [\* 연산자](../../../csharp/language-reference/operators/multiplication-operator.md)를 오버로드할 수 있습니다([operator](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="4ebc1-109">The `*=` operator cannot be overloaded directly, but user-defined types can overload the [\* operator](../../../csharp/language-reference/operators/multiplication-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="4ebc1-110">예</span><span class="sxs-lookup"><span data-stu-id="4ebc1-110">Example</span></span>  
 [!code-csharp[csRefOperators#13](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="4ebc1-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4ebc1-111">See Also</span></span>

- [<span data-ttu-id="4ebc1-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="4ebc1-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4ebc1-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="4ebc1-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4ebc1-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="4ebc1-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
