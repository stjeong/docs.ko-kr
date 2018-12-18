---
title: '&gt;&gt;= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: aebc92ffb007db7b4950313874ebc2bf3c40615f
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239448"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="04e7f-102">&gt;&gt;= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="04e7f-102">&gt;&gt;= Operator (C# Reference)</span></span>
<span data-ttu-id="04e7f-103">오른쪽 시프트 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="04e7f-103">The right-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="04e7f-104">설명</span><span class="sxs-lookup"><span data-stu-id="04e7f-104">Remarks</span></span>  
 <span data-ttu-id="04e7f-105">다음 형태의 식이 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="04e7f-105">An expression of the form</span></span>  
  
```csharp  
x >>= y  
```  
  
 <span data-ttu-id="04e7f-106">이 식은 다음과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="04e7f-106">is evaluated as</span></span>  
  
```csharp  
x = x >> y  
```  
  
 <span data-ttu-id="04e7f-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="04e7f-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="04e7f-108">[>> 연산자](../../../csharp/language-reference/operators/right-shift-operator.md)는 `y`로 지정된 양만큼 `x`를 오른쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="04e7f-108">The [>> operator](../../../csharp/language-reference/operators/right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>  
  
 <span data-ttu-id="04e7f-109">>>= 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [>> 연산자](../../../csharp/language-reference/operators/right-shift-operator.md)를 오버로드할 수 있습니다([operator](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="04e7f-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](../../../csharp/language-reference/operators/right-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="04e7f-110">예</span><span class="sxs-lookup"><span data-stu-id="04e7f-110">Example</span></span>  
 [!code-csharp[csRefOperators#11](../../../csharp/language-reference/operators/codesnippet/CSharp/right-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="04e7f-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="04e7f-111">See Also</span></span>

- [<span data-ttu-id="04e7f-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="04e7f-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="04e7f-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="04e7f-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="04e7f-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="04e7f-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
