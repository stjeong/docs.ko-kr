---
title: 연산자 키워드(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- operator_CSharpKeyword
- operator
helpviewer_keywords:
- operator keyword [C#]
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
ms.openlocfilehash: c3bfada235993670bf158fe9803a09707b2b3251
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929874"
---
# <a name="operator-c-reference"></a><span data-ttu-id="5cfda-102">연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="5cfda-102">operator (C# Reference)</span></span>

<span data-ttu-id="5cfda-103">`operator` 키워드를 사용하여 기본 제공 연산자를 오버로드하거나 클래스 또는 구조체 선언에서 사용자 정의 변환을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5cfda-103">Use the `operator` keyword to overload a built-in operator or to provide a user-defined conversion in a class or struct declaration.</span></span>

## <a name="example"></a><span data-ttu-id="5cfda-104">예</span><span class="sxs-lookup"><span data-stu-id="5cfda-104">Example</span></span>

<span data-ttu-id="5cfda-105">다음은 소수에 대한 매우 간단한 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="5cfda-105">The following is a very simplified class for fractional numbers.</span></span> <span data-ttu-id="5cfda-106">`+` 및 `*` 연산자를 오버로드하여 소수 더하기 및 곱하기를 수행하고 `Fraction` 형식을 `double` 형식으로 변환하는 변환 연산자도 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5cfda-106">It overloads the `+` and `*` operators to perform fractional addition and multiplication, and also provides a conversion operator that converts a `Fraction` type to a `double` type.</span></span>

[!code-csharp[csrefKeywordsConversion#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#6)]

## <a name="c-language-specification"></a><span data-ttu-id="5cfda-107">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="5cfda-107">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="5cfda-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5cfda-108">See also</span></span>

- [<span data-ttu-id="5cfda-109">C# 참조</span><span class="sxs-lookup"><span data-stu-id="5cfda-109">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="5cfda-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="5cfda-110">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="5cfda-111">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="5cfda-111">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="5cfda-112">implicit</span><span class="sxs-lookup"><span data-stu-id="5cfda-112">implicit</span></span>](implicit.md)
- [<span data-ttu-id="5cfda-113">explicit</span><span class="sxs-lookup"><span data-stu-id="5cfda-113">explicit</span></span>](explicit.md)
- [<span data-ttu-id="5cfda-114">방법: 구조체 간의 사용자 정의 변환 구현</span><span class="sxs-lookup"><span data-stu-id="5cfda-114">How to: Implement User-Defined Conversions Between Structs</span></span>](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
