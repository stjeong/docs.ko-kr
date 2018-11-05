---
title: += 연산자(C# 참조)
ms.date: 10/22/2018
f1_keywords:
- +=_CSharpKeyword
helpviewer_keywords:
- += operator [C#]
- addition assignment operator (+=) [C#]
- event subscription [C#]
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
ms.openlocfilehash: ee335e3e2e7d352d4e26b802bad2b08a05c666ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192033"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="b083c-102">+= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="b083c-102">+= Operator (C# Reference)</span></span>

<span data-ttu-id="b083c-103">더하기 대입 연산자.</span><span class="sxs-lookup"><span data-stu-id="b083c-103">The addition assignment operator.</span></span>

<span data-ttu-id="b083c-104">다음과 같은 `+=` 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="b083c-104">An expression using the `+=` operator, such as</span></span>  

```csharp
x += y
```  

<span data-ttu-id="b083c-105">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-105">is equivalent to</span></span>  

```csharp
x = x + y
```  

<span data-ttu-id="b083c-106">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="b083c-107">숫자 형식의 경우 [더하기 연산자](addition-operator.md) `+`는 해당 피연산자의 합계를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-107">For numeric types, the [addition operator](addition-operator.md) `+` computes the sum of its operands.</span></span> <span data-ttu-id="b083c-108">피연산자 중 하나 또는 둘 다가 [문자열](../keywords/string.md) 형식이면 +는 피연산자의 문자열 표현을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-108">If one or both operands is of type [string](../keywords/string.md), it concatenates the string representations of its operands.</span></span> <span data-ttu-id="b083c-109">대리자 형식의 경우 `+` 연산자는 해당 피연산자의 조합인 새 대리자 인스턴스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-109">For delegate types, the `+` operator returns a new delegate instance that is combination of its operands.</span></span>

<span data-ttu-id="b083c-110">사용자 정의 형식이 [더하기 연산자](addition-operator.md) `+`를 [오버로드](../keywords/operator.md)하면 더하기 대입 연산자 `+=`는 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-110">If a user-defined type [overloads](../keywords/operator.md) the [addition operator](addition-operator.md) `+`, the addition assignment operator `+=` is implicitly overloaded.</span></span>

<span data-ttu-id="b083c-111">또한 [이벤트](../keywords/event.md)를 구독할 때 `+=` 연산자를 사용하여 이벤트 처리기 메서드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-111">You also use the `+=` operator to specify an event handler method when you subscribe to an [event](../keywords/event.md).</span></span> <span data-ttu-id="b083c-112">자세한 내용은 [방법: 이벤트 구독 및 구독 취소](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b083c-112">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

<span data-ttu-id="b083c-113">다음 예제에서는 `+=` 연산자의 사용법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b083c-113">The following example demonstrates the usage of the `+=` operator:</span></span>

[!code-csharp-interactive[+= examples](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddAndAssign)]
  
## <a name="see-also"></a><span data-ttu-id="b083c-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b083c-114">See also</span></span>

- [<span data-ttu-id="b083c-115">C# 참조</span><span class="sxs-lookup"><span data-stu-id="b083c-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b083c-116">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="b083c-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b083c-117">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="b083c-117">C# Operators</span></span>](index.md)
- [<span data-ttu-id="b083c-118">이벤트</span><span class="sxs-lookup"><span data-stu-id="b083c-118">Events</span></span>](../../programming-guide/events/index.md)
- [<span data-ttu-id="b083c-119">대리자</span><span class="sxs-lookup"><span data-stu-id="b083c-119">Delegates</span></span>](../../programming-guide/delegates/index.md)
