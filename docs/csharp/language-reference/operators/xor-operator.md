---
title: ^ 연산자 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: 16419342fec9d6c9845e19e434787c5e4f5a5b12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632254"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="8f7c4-102">^ 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="8f7c4-102">^ operator (C# Reference)</span></span>

<span data-ttu-id="8f7c4-103">이항 `^` 연산자는 정수 형식 및 `bool`에 대해 미리 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-103">Binary `^` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="8f7c4-104">정수 형식의 경우 `^` 연산자는 해당 피연산자의 배타적 비트 OR 연산자를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-104">For integral types, `^` computes the bitwise exclusive-OR of its operands.</span></span> <span data-ttu-id="8f7c4-105">`bool` 피연산자의 경우 `^` 연산자는 피연산자의 배타적 논리 OR 연산을 계산합니다. 즉 피연산자 중 정확히 하나가 `true`일 경우에만 결과가 `true`입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-105">For `bool` operands, `^` computes the logical exclusive-or of its operands; that is, the result is `true` if and only if exactly one of its operands is `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f7c4-106">주의</span><span class="sxs-lookup"><span data-stu-id="8f7c4-106">Remarks</span></span>

<span data-ttu-id="8f7c4-107">사용자 정의 형식은 `^` 연산자를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="8f7c4-107">User-defined types can overload the `^` operator (see [operator](../keywords/operator.md)).</span></span> <span data-ttu-id="8f7c4-108">정수 계열 형식에 대한 연산은 일반적으로 열거형에서 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-108">Operations on integral types are generally allowed on enumeration.</span></span>

## <a name="example"></a><span data-ttu-id="8f7c4-109">예제</span><span class="sxs-lookup"><span data-stu-id="8f7c4-109">Example</span></span>

[!code-csharp[csRefOperators#30](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#30)]

<span data-ttu-id="8f7c4-110">이전 예제에서의 `0xf8 ^ 0x3f` 계산은 16진수 값 F8 및 3F에 해당하는 다음 두 이진 값에 대하여 배타적 비트 OR 연산을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-110">The computation of `0xf8 ^ 0x3f` in the previous example performs a bitwise exclusive-OR of the following two binary values, which correspond to the hexadecimal values F8 and 3F:</span></span>

`1111 1000`

`0011 1111`

<span data-ttu-id="8f7c4-111">배타적 OR 연산 결과는 `1100 0111`이며 16진수로 나타내면 C7입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-111">The result of the exclusive-OR is `1100 0111`, which is C7 in hexadecimal.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f7c4-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8f7c4-112">See also</span></span>

- [<span data-ttu-id="8f7c4-113">C# 참조</span><span class="sxs-lookup"><span data-stu-id="8f7c4-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="8f7c4-114">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="8f7c4-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="8f7c4-115">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="8f7c4-115">C# operators</span></span>](index.md)
