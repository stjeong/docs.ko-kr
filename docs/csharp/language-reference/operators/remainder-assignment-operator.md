---
title: '%= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: d0732f9578b64c894ecc1d3bb15cee11a8d5b6a3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245563"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="7a599-102">%= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="7a599-102">%= Operator (C# Reference)</span></span>

<span data-ttu-id="7a599-103">나머지 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-103">The remainder assignment operator.</span></span>

<span data-ttu-id="7a599-104">다음과 같은 `%=` 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="7a599-104">An expression using the `%=` operator, such as</span></span>  

```csharp
x %= y
```  

<span data-ttu-id="7a599-105">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-105">is equivalent to</span></span>  

```csharp
x = x % y
```  

<span data-ttu-id="7a599-106">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="7a599-107">[나머지 연산자](remainder-operator.md)(`%`)는 피연산자를 나눈 후 나머지를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-107">The [remainder operator](remainder-operator.md) `%` computes the remainder after division of its operands.</span></span> <span data-ttu-id="7a599-108">모든 숫자 형식에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="7a599-109">사용자 정의 형식이 [나머지 연산자](remainder-operator.md) `%`에 [오버로드](../keywords/operator.md)되면, 나머지 할당 연산자 `%=`는 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-109">If a user-defined type [overloads](../keywords/operator.md) the [remainder operator](remainder-operator.md) `%`, the remainder assignment operator `%=` is implicitly overloaded.</span></span>
  
<span data-ttu-id="7a599-110">다음 예제에서는 `%=` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a599-110">The following example demonstrates the usage of the `%=` operator:</span></span>

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a><span data-ttu-id="7a599-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7a599-111">See also</span></span>

- [<span data-ttu-id="7a599-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="7a599-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7a599-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="7a599-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7a599-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="7a599-114">C# Operators</span></span>](index.md)
