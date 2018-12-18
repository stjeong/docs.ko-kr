---
title: char 키워드 - C# 참조
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- char
- char_CSharpKeyword
helpviewer_keywords:
- char data type [C#]
ms.assetid: b51cf4fb-124c-4067-af48-afbac122b228
ms.openlocfilehash: 6acb40117c4f59deb084965cb3db9e4a96f7f61a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53242349"
---
# <a name="char-c-reference"></a><span data-ttu-id="31961-102">char(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="31961-102">char (C# Reference)</span></span>

<span data-ttu-id="31961-103">`char` 키워드는 .NET Framework에서 유니코드 문자를 표현하는 데 사용하는 <xref:System.Char?displayProperty=nameWithType> 구조체의 인스턴스를 선언하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="31961-103">The `char` keyword is used to declare an instance of the <xref:System.Char?displayProperty=nameWithType> structure that the .NET Framework uses to represent a Unicode character.</span></span> <span data-ttu-id="31961-104">`Char` 개체의 값은 16비트 숫자(서수) 값입니다.</span><span class="sxs-lookup"><span data-stu-id="31961-104">The value of a `Char` object is a 16-bit numeric (ordinal) value.</span></span>

 <span data-ttu-id="31961-105">유니코드 문자는 전 세계에서 대부분의 문자 체계를 표현하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="31961-105">Unicode characters are used to represent most of the written languages throughout the world.</span></span>

|<span data-ttu-id="31961-106">형식</span><span class="sxs-lookup"><span data-stu-id="31961-106">Type</span></span>|<span data-ttu-id="31961-107">범위</span><span class="sxs-lookup"><span data-stu-id="31961-107">Range</span></span>|<span data-ttu-id="31961-108">크기</span><span class="sxs-lookup"><span data-stu-id="31961-108">Size</span></span>|<span data-ttu-id="31961-109">.NET 형식</span><span class="sxs-lookup"><span data-stu-id="31961-109">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`char`|<span data-ttu-id="31961-110">U+0000~U+FFFF</span><span class="sxs-lookup"><span data-stu-id="31961-110">U+0000 to U+FFFF</span></span>|<span data-ttu-id="31961-111">유니코드 16비트 문자</span><span class="sxs-lookup"><span data-stu-id="31961-111">Unicode 16-bit character</span></span>|<xref:System.Char?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="31961-112">리터럴</span><span class="sxs-lookup"><span data-stu-id="31961-112">Literals</span></span>

<span data-ttu-id="31961-113">`char` 형식의 상수는 문자 리터럴, 16진수 이스케이프 시퀀스 또는 유니코드 표현으로 기록될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31961-113">Constants of the `char` type can be written as character literals, hexadecimal escape sequence, or Unicode representation.</span></span> <span data-ttu-id="31961-114">정수 문자 코드를 캐스트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31961-114">You can also cast the integral character codes.</span></span> <span data-ttu-id="31961-115">다음 예제에서 `char` 변수 4개는 동일 문자 `X`를 사용하여 초기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="31961-115">In the following example four `char` variables are initialized with the same character `X`:</span></span>

[!code-csharp[csrefKeywordsTypes#19](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#19)]

## <a name="conversions"></a><span data-ttu-id="31961-116">변환</span><span class="sxs-lookup"><span data-stu-id="31961-116">Conversions</span></span>

<span data-ttu-id="31961-117">`char`는 [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), [ulong](../../../csharp/language-reference/keywords/ulong.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md) 또는 [decimal](../../../csharp/language-reference/keywords/decimal.md)로 암시적으로 변환될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31961-117">A `char` can be implicitly converted to [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), [ulong](../../../csharp/language-reference/keywords/ulong.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span> <span data-ttu-id="31961-118">그러나 기타 형식에서 `char` 형식으로의 암시적 변환은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="31961-118">However, there are no implicit conversions from other types to the `char` type.</span></span>

<span data-ttu-id="31961-119"><xref:System.Char?displayProperty=nameWithType> 형식은 `char` 값 작업을 위한 몇 가지 정적 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="31961-119">The <xref:System.Char?displayProperty=nameWithType> type provides several static methods for working with `char` values.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="31961-120">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="31961-120">C# language specification</span></span>  

<span data-ttu-id="31961-121">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [정수 형식](~/_csharplang/spec/types.md#integral-types)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31961-121">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="31961-122">C# 언어 사양은 C# 구문 및 사용법에 대한 신뢰할 수 있는 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="31961-122">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="31961-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="31961-123">See also</span></span>

- <xref:System.Char>  
- [<span data-ttu-id="31961-124">C# 참조</span><span class="sxs-lookup"><span data-stu-id="31961-124">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="31961-125">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="31961-125">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="31961-126">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="31961-126">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="31961-127">정수 계열 형식 표</span><span class="sxs-lookup"><span data-stu-id="31961-127">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
- [<span data-ttu-id="31961-128">기본 제공 형식 표</span><span class="sxs-lookup"><span data-stu-id="31961-128">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
- [<span data-ttu-id="31961-129">암시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="31961-129">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
- [<span data-ttu-id="31961-130">명시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="31961-130">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  
- [<span data-ttu-id="31961-131">Nullable 형식</span><span class="sxs-lookup"><span data-stu-id="31961-131">Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/index.md)  
- [<span data-ttu-id="31961-132">문자열</span><span class="sxs-lookup"><span data-stu-id="31961-132">Strings</span></span>](../../../csharp/programming-guide/strings/index.md)