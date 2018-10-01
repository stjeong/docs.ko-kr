---
title: float 키워드(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- float
- float_CSharpKeyword
helpviewer_keywords:
- float keyword [C#]
- floating-point numbers [C#], float keyword
ms.assetid: 1e77db7b-dedb-48b7-8dd1-b055e96a9258
ms.openlocfilehash: 98f89ba3d79f7679b69ce10fd875b3caf69c5257
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47157706"
---
# <a name="float-c-reference"></a><span data-ttu-id="0d739-102">float(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="0d739-102">float (C# Reference)</span></span>

<span data-ttu-id="0d739-103">`float` 키워드는 32비트 부동 소수점 값을 저장하는 단순 형식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-103">The `float` keyword signifies a simple type that stores 32-bit floating-point values.</span></span> <span data-ttu-id="0d739-104">다음 표에서는 `float` 형식의 전체 자릿수와 근사 범위를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-104">The following table shows the precision and approximate range for the `float` type.</span></span>

|<span data-ttu-id="0d739-105">형식</span><span class="sxs-lookup"><span data-stu-id="0d739-105">Type</span></span>|<span data-ttu-id="0d739-106">근사 범위</span><span class="sxs-lookup"><span data-stu-id="0d739-106">Approximate range</span></span>|<span data-ttu-id="0d739-107">전체 자릿수</span><span class="sxs-lookup"><span data-stu-id="0d739-107">Precision</span></span>|<span data-ttu-id="0d739-108">.NET 형식</span><span class="sxs-lookup"><span data-stu-id="0d739-108">.NET type</span></span>|  
|----------|-----------------------|---------------|-------------------------|  
|`float`|<span data-ttu-id="0d739-109">±1.5 x 10<sup>−45</sup> ~ ±3.4 x 10<sup>38</sup></span><span class="sxs-lookup"><span data-stu-id="0d739-109">±1.5 x 10<sup>−45</sup> to ±3.4 x 10<sup>38</sup></span></span>|<span data-ttu-id="0d739-110">7개의 자릿수</span><span class="sxs-lookup"><span data-stu-id="0d739-110">7 digits</span></span>|<xref:System.Single?displayProperty=nameWithType>|  

## <a name="literals"></a><span data-ttu-id="0d739-111">리터럴</span><span class="sxs-lookup"><span data-stu-id="0d739-111">Literals</span></span>

<span data-ttu-id="0d739-112">기본적으로 대입 연산자 오른쪽의 실수 리터럴은 [double](double.md)로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-112">By default, a real numeric literal on the right side of the assignment operator is treated as [double](double.md).</span></span> <span data-ttu-id="0d739-113">따라서 부동 변수를 초기화하려면 다음 예제와 같이 접미사 `f` 또는 `F`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-113">Therefore, to initialize a float variable, use the suffix `f` or `F`, as in the following example:</span></span>

```csharp
float x = 3.5F;
```

<span data-ttu-id="0d739-114">이전 선언에서 접미사를 사용하지 않은 경우 [double](double.md) 값을 `float` 변수에 저장하려고 하기 때문에 컴파일 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-114">If you do not use the suffix in the previous declaration, you will get a compilation error because you are trying to store a [double](double.md) value into a `float` variable.</span></span>

## <a name="conversions"></a><span data-ttu-id="0d739-115">변환</span><span class="sxs-lookup"><span data-stu-id="0d739-115">Conversions</span></span>

<span data-ttu-id="0d739-116">식에서 숫자 정수 형식과 부동 소수점 형식을 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-116">You can mix numeric integral types and floating-point types in an expression.</span></span> <span data-ttu-id="0d739-117">이 경우 정수 형식이 부동 소수점 형식으로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-117">In this case, the integral types are converted to floating-point types.</span></span> <span data-ttu-id="0d739-118">식의 계산은 다음 규칙에 따라 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-118">The evaluation of the expression is performed according to the following rules:</span></span>

- <span data-ttu-id="0d739-119">부동 소수점 형식 중 하나가 [double](double.md)이면 식은 같음에 대한 관계형 비교 또는 비교에서 [double](double.md) 또는 [bool](bool.md)로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-119">If one of the floating-point types is [double](double.md), the expression evaluates to [double](double.md), or to [bool](bool.md) in relational comparisons or comparisons for equality.</span></span>

- <span data-ttu-id="0d739-120">식에 [double](double.md) 형식이 없는 경우 식은 같음에 대한 관계형 비교 또는 비교에서 `float` 또는 [bool](bool.md)로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-120">If there is no [double](double.md) type in the expression, the expression evaluates to `float`, or to [bool](bool.md) in relational comparisons or comparisons for equality.</span></span>

<span data-ttu-id="0d739-121">부동 소수점 식에는 다음과 같은 값 집합이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-121">A floating-point expression can contain the following sets of values:</span></span>

- <span data-ttu-id="0d739-122">양수 및 음수 0</span><span class="sxs-lookup"><span data-stu-id="0d739-122">Positive and negative zero</span></span>

- <span data-ttu-id="0d739-123">양수 및 음수 무한대</span><span class="sxs-lookup"><span data-stu-id="0d739-123">Positive and negative infinity</span></span>

- <span data-ttu-id="0d739-124">NaN(Not-a-Number) 값</span><span class="sxs-lookup"><span data-stu-id="0d739-124">Not-a-Number value (NaN)</span></span>

- <span data-ttu-id="0d739-125">한정된 0이 아닌 값의 집합</span><span class="sxs-lookup"><span data-stu-id="0d739-125">The finite set of nonzero values</span></span>

<span data-ttu-id="0d739-126">이러한 값에 대한 자세한 내용은 [IEEE](http://www.ieee.org) 웹 사이트에서 제공되는 이진 부동 소수점 연산에 대한 IEEE 표준을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0d739-126">For more information about these values, see IEEE Standard for Binary Floating-Point Arithmetic, available on the [IEEE](http://www.ieee.org) website.</span></span>

## <a name="example"></a><span data-ttu-id="0d739-127">예</span><span class="sxs-lookup"><span data-stu-id="0d739-127">Example</span></span>

<span data-ttu-id="0d739-128">다음 예제에서는 [int](int.md), [short](short.md) 및 `float`가 수학 식에 포함되어 `float` 결과를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-128">In the following example, an [int](int.md), a [short](short.md), and a `float` are included in a mathematical expression giving a `float` result.</span></span> <span data-ttu-id="0d739-129">(`float`는 <xref:System.Single?displayProperty=nameWithType> 형식의 별칭입니다.) 식에 [double](double.md)이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0d739-129">(Remember that `float` is an alias for the <xref:System.Single?displayProperty=nameWithType> type.) Notice that there is no [double](double.md) in the expression.</span></span>

[!code-csharp[csrefKeywordsTypes#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#13)]

## <a name="c-language-specification"></a><span data-ttu-id="0d739-130">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="0d739-130">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="0d739-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0d739-131">See also</span></span>

- <xref:System.Single>  
- [<span data-ttu-id="0d739-132">C# 참조</span><span class="sxs-lookup"><span data-stu-id="0d739-132">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="0d739-133">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="0d739-133">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="0d739-134">캐스팅 및 형식 변환</span><span class="sxs-lookup"><span data-stu-id="0d739-134">Casting and Type Conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)  
- [<span data-ttu-id="0d739-135">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="0d739-135">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="0d739-136">정수 계열 형식 표</span><span class="sxs-lookup"><span data-stu-id="0d739-136">Integral Types Table</span></span>](integral-types-table.md)  
- [<span data-ttu-id="0d739-137">기본 제공 형식 표</span><span class="sxs-lookup"><span data-stu-id="0d739-137">Built-In Types Table</span></span>](built-in-types-table.md)  
- [<span data-ttu-id="0d739-138">암시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="0d739-138">Implicit Numeric Conversions Table</span></span>](implicit-numeric-conversions-table.md)  
- [<span data-ttu-id="0d739-139">명시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="0d739-139">Explicit Numeric Conversions Table</span></span>](explicit-numeric-conversions-table.md)  