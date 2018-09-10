---
title: '&lt;&lt;= 연산자(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: c689aeccdf3ad6cc6c672cc101a4f0aa92f19791
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517206"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="453a3-102">&lt;&lt;= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="453a3-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="453a3-103">왼쪽 시프트 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="453a3-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="453a3-104">설명</span><span class="sxs-lookup"><span data-stu-id="453a3-104">Remarks</span></span>  
 <span data-ttu-id="453a3-105">다음 형태의 식이 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="453a3-105">An expression of the form</span></span>  
  
```csharp  
x <<= y  
```  
  
 <span data-ttu-id="453a3-106">이 식은 다음과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="453a3-106">is evaluated as</span></span>  
  
```csharp  
x = x << y  
```  
  
 <span data-ttu-id="453a3-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="453a3-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="453a3-108">[<< 연산자](../../../csharp/language-reference/operators/left-shift-operator.md)는 `y`로 지정된 비트 수만큼 `x`를 왼쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="453a3-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="453a3-109">`<<=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [<< 연산자](../../../csharp/language-reference/operators/left-shift-operator.md)를 오버로드할 수 있습니다([operator](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="453a3-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="453a3-110">예</span><span class="sxs-lookup"><span data-stu-id="453a3-110">Example</span></span>  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="453a3-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="453a3-111">See Also</span></span>

- [<span data-ttu-id="453a3-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="453a3-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="453a3-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="453a3-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="453a3-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="453a3-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
