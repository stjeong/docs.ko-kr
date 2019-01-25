---
title: -= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- -=_CSharpKeyword
helpviewer_keywords:
- subtraction assignment operator (-=) [C#]
- -= operator (subtraction assignment ) [C#]
ms.assetid: 05c7d68a-423f-4de8-891b-cf24e8fb6ed7
ms.openlocfilehash: 3b6890be4460a599a5d2f5f5f6ee1627be933f0b
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333332"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="e2ae4-102">-= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="e2ae4-102">-= operator (C# Reference)</span></span>

<span data-ttu-id="e2ae4-103">빼기 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae4-103">The subtraction assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ae4-104">주의</span><span class="sxs-lookup"><span data-stu-id="e2ae4-104">Remarks</span></span>

<span data-ttu-id="e2ae4-105">다음과 같은 `-=` 대입 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="e2ae4-105">An expression using the `-=` assignment operator, such as</span></span>

```csharp
x -= y
```

 <span data-ttu-id="e2ae4-106">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae4-106">is equivalent to</span></span>

```csharp
x = x - y
```

<span data-ttu-id="e2ae4-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae4-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="e2ae4-108">[- 연산자](subtraction-operator.md)의 의미는 `x` 및 `y`에 따라 달라집니다(숫자 피연산자의 경우 빼기, 대리자 피연산자의 경우 대리자 제거 등).</span><span class="sxs-lookup"><span data-stu-id="e2ae4-108">The meaning of the [- operator](subtraction-operator.md) is dependent on the types of `x` and `y` (subtraction for numeric operands, delegate removal for delegate operands, and so forth).</span></span>

<span data-ttu-id="e2ae4-109">`-=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [- 연산자](subtraction-operator.md)를 오버로드할 수 있습니다([연산자](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="e2ae4-109">The `-=` operator cannot be overloaded directly, but user-defined types can overload the [- operator](subtraction-operator.md) (see [operator](../keywords/operator.md)).</span></span>

<span data-ttu-id="e2ae4-110">또한 -= 연산자는 C#에서 이벤트 구독을 취소하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae4-110">The -= operator is also used in C# to unsubscribe from an event.</span></span> <span data-ttu-id="e2ae4-111">자세한 내용은 [방법: 이벤트 구독 및 구독 취소](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2ae4-111">For more information, see [How to: Subscribe to and Unsubscribe from Events](../../programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).</span></span>

## <a name="example"></a><span data-ttu-id="e2ae4-112">예제</span><span class="sxs-lookup"><span data-stu-id="e2ae4-112">Example</span></span>

[!code-csharp[csRefOperators#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#6)]

## <a name="see-also"></a><span data-ttu-id="e2ae4-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e2ae4-113">See also</span></span>

- [<span data-ttu-id="e2ae4-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="e2ae4-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="e2ae4-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="e2ae4-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="e2ae4-116">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="e2ae4-116">C# operators</span></span>](index.md)
