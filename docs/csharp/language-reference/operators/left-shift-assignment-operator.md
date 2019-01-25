---
title: '&lt;&lt;= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: 4513c4b78dea3e8102c72a43249b4a44ffa2421d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333254"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="83c94-102">&lt;&lt;= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="83c94-102">&lt;&lt;= operator (C# Reference)</span></span>

<span data-ttu-id="83c94-103">왼쪽 시프트 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="83c94-103">The left-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="83c94-104">주의</span><span class="sxs-lookup"><span data-stu-id="83c94-104">Remarks</span></span>

<span data-ttu-id="83c94-105">다음 형태의 식이 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="83c94-105">An expression of the form</span></span>

```csharp
x <<= y
```

<span data-ttu-id="83c94-106">이 식은 다음과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c94-106">is evaluated as</span></span>

```csharp
x = x << y
```

<span data-ttu-id="83c94-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="83c94-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="83c94-108">[<< 연산자](left-shift-operator.md)는 `y`로 지정된 비트 수만큼 `x`를 왼쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="83c94-108">The [<< operator](left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>

<span data-ttu-id="83c94-109">`<<=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [<< 연산자](left-shift-operator.md)를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="83c94-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](left-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="83c94-110">예제</span><span class="sxs-lookup"><span data-stu-id="83c94-110">Example</span></span>

[!code-csharp[csRefOperators#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#12)]

## <a name="see-also"></a><span data-ttu-id="83c94-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="83c94-111">See also</span></span>

- [<span data-ttu-id="83c94-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="83c94-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="83c94-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="83c94-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="83c94-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="83c94-114">C# Operators</span></span>](index.md)
