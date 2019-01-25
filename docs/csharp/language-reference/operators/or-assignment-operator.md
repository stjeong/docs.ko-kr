---
title: '|= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '|=_CSharpKeyword'
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
ms.openlocfilehash: f4f7806c8679af400a371decd0c367929b3fb81d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333267"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="92c9b-102">|= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="92c9b-102">|= operator (C# Reference)</span></span>

<span data-ttu-id="92c9b-103">OR 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="92c9b-103">The OR assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c9b-104">주의</span><span class="sxs-lookup"><span data-stu-id="92c9b-104">Remarks</span></span>

<span data-ttu-id="92c9b-105">다음과 같은 `|=` 대입 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="92c9b-105">An expression using the `|=` assignment operator, such as</span></span>

```csharp
x |= y
```

<span data-ttu-id="92c9b-106">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="92c9b-106">is equivalent to</span></span>

```csharp
x = x | y
```

<span data-ttu-id="92c9b-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="92c9b-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="92c9b-108">[&#124; 연산자](or-operator.md)는 정수 피연산자에 대한 비트 논리적 OR 연산과 부울 피연산자에 대한 논리적 OR 연산을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="92c9b-108">The [&#124; operator](or-operator.md) performs a bitwise logical OR operation on integral operands and logical OR on bool operands.</span></span>

<span data-ttu-id="92c9b-109">`|=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [&#124; 연산자](or-operator.md)를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="92c9b-109">The `|=` operator cannot be overloaded directly, but user-defined types can overload the [&#124; operator](or-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="92c9b-110">예제</span><span class="sxs-lookup"><span data-stu-id="92c9b-110">Example</span></span>

[!code-csharp[csRefOperators#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#10)]

## <a name="see-also"></a><span data-ttu-id="92c9b-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="92c9b-111">See also</span></span>

- [<span data-ttu-id="92c9b-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="92c9b-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="92c9b-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="92c9b-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="92c9b-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="92c9b-114">C# operators</span></span>](index.md)