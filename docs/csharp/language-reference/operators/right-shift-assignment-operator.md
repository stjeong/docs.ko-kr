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
ms.openlocfilehash: 02a9559a5c4086eeed09094c15c3620366ffad8c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333693"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="bd995-102">&gt;&gt;= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="bd995-102">&gt;&gt;= operator (C# Reference)</span></span>

<span data-ttu-id="bd995-103">오른쪽 시프트 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="bd995-103">The right-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd995-104">주의</span><span class="sxs-lookup"><span data-stu-id="bd995-104">Remarks</span></span>

<span data-ttu-id="bd995-105">다음 형태의 식이 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd995-105">An expression of the form</span></span>

```csharp
x >>= y
```

<span data-ttu-id="bd995-106">이 식은 다음과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd995-106">is evaluated as</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="bd995-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd995-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="bd995-108">[>> 연산자](right-shift-operator.md)는 `y`로 지정된 양만큼 `x`를 오른쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="bd995-108">The [>> operator](right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>

<span data-ttu-id="bd995-109">>>= 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [>> 연산자](right-shift-operator.md)를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="bd995-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](right-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="bd995-110">예제</span><span class="sxs-lookup"><span data-stu-id="bd995-110">Example</span></span>

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a><span data-ttu-id="bd995-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bd995-111">See also</span></span>

- [<span data-ttu-id="bd995-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="bd995-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="bd995-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="bd995-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="bd995-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="bd995-114">C# operators</span></span>](index.md)