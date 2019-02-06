---
title: -> 연산자 - C# 참조
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: be74f02a85aa05cdab32768ed38222fc4d9289b1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255369"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="7a0ce-102">-> 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="7a0ce-102">-> Operator (C# Reference)</span></span>

<span data-ttu-id="7a0ce-103">포인터 멤버 액세스 연산자 `->`는 포인터 간접 참조 및 멤버 액세스를 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-103">The pointer member access operator `->` combines pointer indirection and member access.</span></span>

<span data-ttu-id="7a0ce-104">`x`가 `T*` 형식의 포인터이고 `y`가 `T`의 액세스 가능한 멤버인 경우 다음 형식의 식을 가정해 보세요.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-104">If `x` is a pointer of the type `T*` and `y` is an accessible member of `T`, an expression of the form</span></span>

```csharp
x->y
```

<span data-ttu-id="7a0ce-105">위의 식은 아래의 식과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-105">is equivalent to</span></span>

```csharp
(*x).y
```

<span data-ttu-id="7a0ce-106">`->` 연산자에 [안전하지 않은](../keywords/unsafe.md) 컨텍스트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-106">The `->` operator requires [unsafe](../keywords/unsafe.md) context.</span></span>

<span data-ttu-id="7a0ce-107">자세한 내용은 [방법: 포인터를 사용하여 멤버 액세스](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-107">For more information, see [How to: access a member with a pointer](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="7a0ce-108">연산자 오버로드 가능성</span><span class="sxs-lookup"><span data-stu-id="7a0ce-108">Operator overloadability</span></span>

<span data-ttu-id="7a0ce-109">`->` 연산자를 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-109">The `->` operator cannot be overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="7a0ce-110">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="7a0ce-110">C# language specification</span></span>

<span data-ttu-id="7a0ce-111">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [포인터 멤버 액세스](~/_csharplang/spec/unsafe-code.md#pointer-member-access) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a0ce-111">For more information, see the [Pointer member access](~/_csharplang/spec/unsafe-code.md#pointer-member-access) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7a0ce-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7a0ce-112">See also</span></span>

- [<span data-ttu-id="7a0ce-113">C# 참조</span><span class="sxs-lookup"><span data-stu-id="7a0ce-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7a0ce-114">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="7a0ce-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7a0ce-115">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="7a0ce-115">C# Operators</span></span>](index.md)
- [<span data-ttu-id="7a0ce-116">포인터 형식</span><span class="sxs-lookup"><span data-stu-id="7a0ce-116">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
