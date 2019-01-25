---
title: '&lt;&lt; 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: 79a48d88e2c83b5ad78804367ee3c07f78622c08
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333527"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="f6672-102">&lt;&lt; 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="f6672-102">&lt;&lt; operator (C# Reference)</span></span>

<span data-ttu-id="f6672-103">왼쪽 시프트 연산자(`<<`)는 첫 번째 피연산자를 두 번째 피연산자로 지정된 비트 수만큼 왼쪽으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-103">The left-shift operator (`<<`) shifts its first operand left by the number of bits specified by its second operand.</span></span> <span data-ttu-id="f6672-104">두 번째 피연산자의 형식은 [int](../keywords/int.md) 또는 `int`로의 미리 정의된 암시적 숫자 변환이 있는 형식이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-104">The type of the second operand must be an [int](../keywords/int.md) or a type that has a predefined implicit numeric conversion to `int`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6672-105">주의</span><span class="sxs-lookup"><span data-stu-id="f6672-105">Remarks</span></span>

<span data-ttu-id="f6672-106">첫 번째 피연산자가 [int](../keywords/int.md) 또는 [uint](../keywords/uint.md)(32비트 수량)이면 두 번째 피연산자의 하위 5비트로 시프트 수가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-106">If the first operand is an [int](../keywords/int.md) or [uint](../keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand.</span></span> <span data-ttu-id="f6672-107">즉, 실제 시프트 수는 0~31비트입니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-107">That is, the actual shift count is 0 to 31 bits.</span></span>

<span data-ttu-id="f6672-108">첫 번째 피연산자가 [long](../keywords/long.md) 또는 [ulong](../keywords/ulong.md)(64비트 수량)이면 두 번째 피연산자의 하위 6비트로 시프트 수가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-108">If the first operand is a [long](../keywords/long.md) or [ulong](../keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand.</span></span> <span data-ttu-id="f6672-109">즉, 실제 시프트 수는 0~63비트입니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-109">That is, the actual shift count is 0 to 63 bits.</span></span>

<span data-ttu-id="f6672-110">시프트 후 첫 번째 피연산자의 형식 범위 내에 없는 상위 비트는 삭제되고, 비어 있는 하위 비트는 0으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-110">Any high-order bits that are not within the range of the type of the first operand after the shift are discarded, and the low-order empty bits are zero-filled.</span></span> <span data-ttu-id="f6672-111">시프트 작업은 오버플로를 일으키지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-111">Shift operations never cause overflows.</span></span>

<span data-ttu-id="f6672-112">사용자 정의 형식은 `<<` 연산자를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조). 첫 번째 피연산자의 형식은 사용자 정의 형식이어야 하고 두 번째 피연산자의 형식은 `int`여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-112">User-defined types can overload the `<<` operator (see [operator](../keywords/operator.md)); the type of the first operand must be the user-defined type, and the type of the second operand must be `int`.</span></span> <span data-ttu-id="f6672-113">이항 연산자가 오버로드되면 해당 대입 연산자도 암시적으로 오버로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-113">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>

## <a name="example"></a><span data-ttu-id="f6672-114">예제</span><span class="sxs-lookup"><span data-stu-id="f6672-114">Example</span></span>

[!code-csharp[csRefOperators#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#14)]

## <a name="comments"></a><span data-ttu-id="f6672-115">설명</span><span class="sxs-lookup"><span data-stu-id="f6672-115">Comments</span></span>

<span data-ttu-id="f6672-116">`i<<1` 및 `i<<33`은 1과 33의 하위 5비트가 같기 때문에 동일한 결과를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f6672-116">Note that `i<<1` and `i<<33` give the same result, because 1 and 33 have the same low-order five bits.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6672-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f6672-117">See also</span></span>

- [<span data-ttu-id="f6672-118">C# 참조</span><span class="sxs-lookup"><span data-stu-id="f6672-118">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="f6672-119">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="f6672-119">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="f6672-120">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="f6672-120">C# Operators</span></span>](index.md)
