---
title: ^= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: cf39c8e8586e9d4f537fe38d8b28f55542db6ab8
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237157"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="4836d-102">^= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="4836d-102">^= Operator (C# Reference)</span></span>
<span data-ttu-id="4836d-103">배타적 OR 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="4836d-103">The exclusive-OR assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4836d-104">설명</span><span class="sxs-lookup"><span data-stu-id="4836d-104">Remarks</span></span>  
 <span data-ttu-id="4836d-105">다음 형태의 식이 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="4836d-105">An expression of the form</span></span>  
  
```csharp  
x ^= y  
```  
  
 <span data-ttu-id="4836d-106">이 식은 다음과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="4836d-106">is evaluated as</span></span>  
  
```csharp  
x = x ^ y  
```  
  
 <span data-ttu-id="4836d-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="4836d-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="4836d-108">[^ 연산자](../../../csharp/language-reference/operators/xor-operator.md)는 정수 피연산자에 대한 배타적 비트 OR 연산과 [bool](../../../csharp/language-reference/keywords/bool.md) 피연산자에 대한 배타적 논리 OR 연산을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4836d-108">The [^ operator](../../../csharp/language-reference/operators/xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../../../csharp/language-reference/keywords/bool.md) operands.</span></span>  
  
 <span data-ttu-id="4836d-109">^= 연산자는 직접 오버로드할 수 없지만 사용자 정의 형식은 [^ 연산자](../../../csharp/language-reference/operators/xor-operator.md)를 오버로드할 수 있습니다([연산자](../../../csharp/language-reference/keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="4836d-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](../../../csharp/language-reference/operators/xor-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="4836d-110">예</span><span class="sxs-lookup"><span data-stu-id="4836d-110">Example</span></span>  
 [!code-csharp[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="4836d-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4836d-111">See Also</span></span>

- [<span data-ttu-id="4836d-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="4836d-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4836d-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="4836d-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4836d-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="4836d-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
