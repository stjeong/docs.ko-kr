---
title: ulong 키워드 - C# 참조
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- ulong_CSharpKeyword
- ulong
helpviewer_keywords:
- ulong keyword [C#]
ms.assetid: f2ece624-837a-40cf-92c5-343e7f33397c
ms.openlocfilehash: 97db22612e900658746f40cd117ff941135027a1
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235022"
---
# <a name="ulong-c-reference"></a><span data-ttu-id="d13f4-102">ulong(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="d13f4-102">ulong (C# Reference)</span></span>

<span data-ttu-id="d13f4-103">`ulong` 키워드는 다음 표에 나와 있는 크기와 범위에 따라 값을 저장하는 정수 형식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-103">The `ulong` keyword denotes an integral type that stores values according to the size and range shown in the following table.</span></span>

|<span data-ttu-id="d13f4-104">형식</span><span class="sxs-lookup"><span data-stu-id="d13f4-104">Type</span></span>|<span data-ttu-id="d13f4-105">범위</span><span class="sxs-lookup"><span data-stu-id="d13f4-105">Range</span></span>|<span data-ttu-id="d13f4-106">크기</span><span class="sxs-lookup"><span data-stu-id="d13f4-106">Size</span></span>|<span data-ttu-id="d13f4-107">.NET 형식</span><span class="sxs-lookup"><span data-stu-id="d13f4-107">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`ulong`|<span data-ttu-id="d13f4-108">0 ~ 18,446,744,073,709,551,615</span><span class="sxs-lookup"><span data-stu-id="d13f4-108">0 to 18,446,744,073,709,551,615</span></span>|<span data-ttu-id="d13f4-109">부호 없는 64비트 정수</span><span class="sxs-lookup"><span data-stu-id="d13f4-109">Unsigned 64-bit integer</span></span>|<xref:System.UInt64?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="d13f4-110">리터럴</span><span class="sxs-lookup"><span data-stu-id="d13f4-110">Literals</span></span>

<span data-ttu-id="d13f4-111">10진수 리터럴, 16진수 리터럴 또는 (C# 7.0부터) 이진 리터럴을 할당하여 `ulong` 변수를 선언하고 초기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-111">You can declare and initialize a `ulong` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span>  <span data-ttu-id="d13f4-112">정수 리터럴이 `ulong` 범위를 벗어나는 경우(즉 <xref:System.UInt64.MinValue?displayProperty=nameWithType>보다 작거나 <xref:System.UInt64.MaxValue?displayProperty=nameWithType>보다 큰 경우) 컴파일 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-112">If the integer literal is outside the range of `ulong` (that is, if it is less than <xref:System.UInt64.MinValue?displayProperty=nameWithType> or greater than <xref:System.UInt64.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span>

<span data-ttu-id="d13f4-113">다음 예제에서는 10진수, 16진수 및 이진 리터럴로 표현된 7,934,076,125와 같은 정수가 `ulong` 값에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-113">In the following example, integers equal to 7,934,076,125 that are represented as decimal, hexadecimal, and binary literals are assigned to `ulong` values.</span></span>

[!code-csharp[ulong](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#ULong)]

> [!NOTE]
> <span data-ttu-id="d13f4-114">`0x` 또는 `0X` 접두사를 사용하여 16진수 리터럴을 나타내고, `0b` 또는 `0B` 접두사를 사용하여 이진 리터럴을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-114">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="d13f4-115">10진수 리터럴에는 접두사가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-115">Decimal literals have no prefix.</span></span>

<span data-ttu-id="d13f4-116">C# 7.0부터 가독성 향상을 위해 몇 가지 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-116">Starting with C# 7.0, a couple of features have been added to enhance readability:</span></span>

- <span data-ttu-id="d13f4-117">C# 7.0은 숫자 구분 기호로 밑줄 문자 `_`를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-117">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
- <span data-ttu-id="d13f4-118">C# 7.2는 접두사 뒤에 이진 또는 16진수 리터럴에 대한 자리 구분 기호로 `_`을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-118">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="d13f4-119">10진수 리터럴에 선행 밑줄이 있는 것이 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-119">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="d13f4-120">일부 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-120">Some examples are shown below.</span></span>

[!code-csharp[long](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#LongS)]

<span data-ttu-id="d13f4-121">형식을 나타내는 접미사가 정수 리터럴에 포함되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-121">Integer literals can also include a suffix that denotes the type.</span></span> <span data-ttu-id="d13f4-122">`UL` 또는 `ul` 접미사는 숫자 리터럴을 `ulong` 값으로 명확하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-122">The suffix `UL` or `ul` unambiguously identifies a numeric literal as a `ulong` value.</span></span> <span data-ttu-id="d13f4-123">리터럴 값이 <xref:System.Int64.MaxValue?displayProperty=nameWithType>를 초과할 경우 `L` 접미사는 `ulong`을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-123">The `L` suffix denotes a `ulong` if the literal value exceeds <xref:System.Int64.MaxValue?displayProperty=nameWithType>.</span></span> <span data-ttu-id="d13f4-124">또한 리터럴 값이 <xref:System.UInt32.MaxValue?displayProperty=nameWithType>를 초과할 경우 `U` 또는 `ulong` 접미사는 `u`을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-124">And the `U` or `u` suffix denotes a `ulong` if the literal value exceeds <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span></span> <span data-ttu-id="d13f4-125">다음 예제에서는 `ul` 접미사를 사용하여 정수(long)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-125">The following example uses the `ul` suffix to denote a long integer:</span></span>

[!code-csharp[ulsuffix](~/samples/snippets/csharp/language-reference/keywords/numeric-suffixes.cs#2)]

<span data-ttu-id="d13f4-126">정수 리터럴에 접미사가 없는 경우 해당 형식은 값이 표현될 수 있는 다음 형식 중 첫 번째 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-126">If an integer literal has no suffix, its type is the first of the following types in which its value can be represented:</span></span>

1. [<span data-ttu-id="d13f4-127">int</span><span class="sxs-lookup"><span data-stu-id="d13f4-127">int</span></span>](int.md)
2. [<span data-ttu-id="d13f4-128">uint</span><span class="sxs-lookup"><span data-stu-id="d13f4-128">uint</span></span>](uint.md)
3. [<span data-ttu-id="d13f4-129">long</span><span class="sxs-lookup"><span data-stu-id="d13f4-129">long</span></span>](long.md)
4. `ulong`

## <a name="compiler-overload-resolution"></a><span data-ttu-id="d13f4-130">컴파일러 오버로드 확인</span><span class="sxs-lookup"><span data-stu-id="d13f4-130">Compiler overload resolution</span></span>

<span data-ttu-id="d13f4-131">접미사는 일반적으로 오버로드된 메서드를 호출할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-131">A common use of the suffix is with calling overloaded methods.</span></span> <span data-ttu-id="d13f4-132">예를 들어 `ulong` 및 [int](int.md) 매개 변수를 사용하는 다음의 오버로드된 메서드를 살펴보세요.</span><span class="sxs-lookup"><span data-stu-id="d13f4-132">Consider, for example, the following overloaded methods that use `ulong` and [int](int.md) parameters:</span></span>

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(ulong l) {}
```

<span data-ttu-id="d13f4-133">`ulong` 매개 변수와 함께 접미사를 사용하면 올바른 형식이 호출됩니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-133">Using a suffix with the `ulong` parameter guarantees that the correct type is called, for example:</span></span>

```csharp
SampleMethod(5);    // Calling the method with the int parameter
SampleMethod(5UL);  // Calling the method with the ulong parameter
```

## <a name="conversions"></a><span data-ttu-id="d13f4-134">변환</span><span class="sxs-lookup"><span data-stu-id="d13f4-134">Conversions</span></span>

<span data-ttu-id="d13f4-135">`ulong`에서 [float](float.md), [double](double.md) 또는 [decimal](decimal.md)로 미리 정의된 암시적 변환이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-135">There is a predefined implicit conversion from `ulong` to [float](float.md), [double](double.md), or [decimal](decimal.md).</span></span>

<span data-ttu-id="d13f4-136">`ulong`에서 정수 형식으로의 암시적 변환은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-136">There is no implicit conversion from `ulong` to any integral type.</span></span> <span data-ttu-id="d13f4-137">예를 들어 다음 문은 명시적 캐스트 없이 컴파일 오류를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-137">For example, the following statement will produce a compilation error without an explicit cast:</span></span>

```csharp
long long1 = 8UL;   // Error: no implicit conversion from ulong
```

<span data-ttu-id="d13f4-138">[byte](byte.md), [ushort](ushort.md), [uint](uint.md) 또는 [char](char.md)에서 `ulong`으로 미리 정의된 암시적 변환이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-138">There is a predefined implicit conversion from [byte](byte.md), [ushort](ushort.md), [uint](uint.md), or [char](char.md) to `ulong`.</span></span>

<span data-ttu-id="d13f4-139">또한 부동 소수점 형식에서 `ulong`로의 암시적 변환은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-139">Also, there is no implicit conversion from floating-point types to `ulong`.</span></span> <span data-ttu-id="d13f4-140">예를 들어 명시적 캐스트를 사용하지 않는 경우 다음 문은 컴파일러 오류를 일으킵니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-140">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>

```csharp
// Error -- no implicit conversion from double:
ulong x = 3.0;
// OK -- explicit conversion:
ulong y = (ulong)3.0;
```

<span data-ttu-id="d13f4-141">부동 소수점 형식 및 정수 형식이 혼합된 산술 식에 대한 자세한 내용은 [float](float.md) 및 [double](double.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d13f4-141">For information on arithmetic expressions with mixed floating-point types and integral types, see [float](float.md) and [double](double.md).</span></span>

<span data-ttu-id="d13f4-142">암시적 숫자 변환 규칙에 대한 자세한 내용은 [암시적 숫자 변환 표](implicit-numeric-conversions-table.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d13f4-142">For more information on implicit numeric conversion rules, see the [Implicit Numeric Conversions Table](implicit-numeric-conversions-table.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="d13f4-143">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="d13f4-143">C# language specification</span></span>

<span data-ttu-id="d13f4-144">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [정수 형식](~/_csharplang/spec/types.md#integral-types)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d13f4-144">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="d13f4-145">C# 언어 사양은 C# 구문 및 사용법에 대한 신뢰할 수 있는 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d13f4-145">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="d13f4-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d13f4-146">See also</span></span>

- <xref:System.UInt64>
- [<span data-ttu-id="d13f4-147">C# 참조</span><span class="sxs-lookup"><span data-stu-id="d13f4-147">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d13f4-148">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="d13f4-148">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d13f4-149">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="d13f4-149">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="d13f4-150">정수 계열 형식 표</span><span class="sxs-lookup"><span data-stu-id="d13f4-150">Integral Types Table</span></span>](integral-types-table.md)
- [<span data-ttu-id="d13f4-151">기본 제공 형식 표</span><span class="sxs-lookup"><span data-stu-id="d13f4-151">Built-In Types Table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="d13f4-152">암시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="d13f4-152">Implicit Numeric Conversions Table</span></span>](implicit-numeric-conversions-table.md)
- [<span data-ttu-id="d13f4-153">명시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="d13f4-153">Explicit Numeric Conversions Table</span></span>](explicit-numeric-conversions-table.md)
