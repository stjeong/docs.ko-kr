---
title: '*= 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 2038f3b55d46f3503496275b3d25b17663b8c1db
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333436"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="13c5b-102">\*= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="13c5b-102">\*= Operator (C# Reference)</span></span>

<span data-ttu-id="13c5b-103">이항 곱하기 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="13c5b-103">The binary multiplication assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c5b-104">주의</span><span class="sxs-lookup"><span data-stu-id="13c5b-104">Remarks</span></span>

<span data-ttu-id="13c5b-105">다음과 같은 `*=` 대입 연산자를 사용하는 식의 경우</span><span class="sxs-lookup"><span data-stu-id="13c5b-105">An expression using the `*=` assignment operator, such as</span></span>

```csharp
x *= y
```

<span data-ttu-id="13c5b-106">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="13c5b-106">is equivalent to</span></span>

```csharp
x = x * y
```

<span data-ttu-id="13c5b-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="13c5b-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="13c5b-108">[\* 연산자](multiplication-operator.md)는 곱하기를 수행할 숫자 형식에 대해 미리 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13c5b-108">The [\* operator](multiplication-operator.md) is predefined for numeric types to perform multiplication.</span></span>

<span data-ttu-id="13c5b-109">`*=` 연산자를 직접 오버로드할 수는 없지만 사용자 정의 형식은 [\* 연산자](multiplication-operator.md)를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="13c5b-109">The `*=` operator cannot be overloaded directly, but user-defined types can overload the [\* operator](multiplication-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="13c5b-110">예제</span><span class="sxs-lookup"><span data-stu-id="13c5b-110">Example</span></span>

[!code-csharp[csRefOperators#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#13)]

## <a name="see-also"></a><span data-ttu-id="13c5b-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="13c5b-111">See also</span></span>

- [<span data-ttu-id="13c5b-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="13c5b-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="13c5b-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="13c5b-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="13c5b-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="13c5b-114">C# Operators</span></span>](index.md)
