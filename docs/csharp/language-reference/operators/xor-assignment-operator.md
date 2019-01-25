---
title: ^= 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
ms.openlocfilehash: 12189d6469a9716d3b7ebcffef23423a75692d1a
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333553"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="caf6c-102">^= 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="caf6c-102">^= operator (C# Reference)</span></span>

<span data-ttu-id="caf6c-103">배타적 OR 대입 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="caf6c-103">The exclusive-OR assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf6c-104">주의</span><span class="sxs-lookup"><span data-stu-id="caf6c-104">Remarks</span></span>

<span data-ttu-id="caf6c-105">다음 형태의 식이 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="caf6c-105">An expression of the form</span></span>

```csharp
x ^= y
```

<span data-ttu-id="caf6c-106">이 식은 다음과 같이 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="caf6c-106">is evaluated as</span></span>

```csharp
x = x ^ y
```

<span data-ttu-id="caf6c-107">단, `x`가 한 번만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="caf6c-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="caf6c-108">[^ 연산자](xor-operator.md)는 정수 피연산자에 대한 배타적 비트 OR 연산과 [bool](../keywords/bool.md) 피연산자에 대한 배타적 논리 OR 연산을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="caf6c-108">The [^ operator](xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../keywords/bool.md) operands.</span></span>

<span data-ttu-id="caf6c-109">^= 연산자는 직접 오버로드할 수 없지만 사용자 정의 형식은 [^ 연산자](xor-operator.md)를 오버로드할 수 있습니다([연산자](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="caf6c-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](xor-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="caf6c-110">예제</span><span class="sxs-lookup"><span data-stu-id="caf6c-110">Example</span></span>

[!code-csharp[csRefOperators#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#23)]

## <a name="see-also"></a><span data-ttu-id="caf6c-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="caf6c-111">See also</span></span>

- [<span data-ttu-id="caf6c-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="caf6c-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="caf6c-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="caf6c-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="caf6c-114">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="caf6c-114">C# operators</span></span>](index.md)