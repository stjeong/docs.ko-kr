---
title: 암시적 숫자 변환 표(C# 참조)
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: c3c0153a0ae3e07839822c8bb978b1a09277bd53
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188705"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="6e053-102">암시적 숫자 변환 표(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="6e053-102">Implicit numeric conversions table (C# Reference)</span></span>

<span data-ttu-id="6e053-103">다음 표에서는 .NET 숫자 형식 간의 미리 정의된 암시적 숫자 변환을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e053-103">The following table shows the predefined implicit conversions between .NET numeric types.</span></span>
  
|<span data-ttu-id="6e053-104">시작</span><span class="sxs-lookup"><span data-stu-id="6e053-104">From</span></span>|<span data-ttu-id="6e053-105">대상</span><span class="sxs-lookup"><span data-stu-id="6e053-105">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="6e053-106">sbyte</span><span class="sxs-lookup"><span data-stu-id="6e053-106">sbyte</span></span>](sbyte.md)|<span data-ttu-id="6e053-107">`short`, `int`, `long`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-107">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-108">byte</span><span class="sxs-lookup"><span data-stu-id="6e053-108">byte</span></span>](byte.md)|<span data-ttu-id="6e053-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-110">short</span><span class="sxs-lookup"><span data-stu-id="6e053-110">short</span></span>](short.md)|<span data-ttu-id="6e053-111">`int`, `long`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-111">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-112">ushort</span><span class="sxs-lookup"><span data-stu-id="6e053-112">ushort</span></span>](ushort.md)|<span data-ttu-id="6e053-113">`int`, `uint`, `long`, `ulong`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-113">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-114">int</span><span class="sxs-lookup"><span data-stu-id="6e053-114">int</span></span>](int.md)|<span data-ttu-id="6e053-115">`long`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-115">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-116">uint</span><span class="sxs-lookup"><span data-stu-id="6e053-116">uint</span></span>](uint.md)|<span data-ttu-id="6e053-117">`long`, `ulong`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-117">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-118">long</span><span class="sxs-lookup"><span data-stu-id="6e053-118">long</span></span>](long.md)|<span data-ttu-id="6e053-119">`float`, `double`또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-119">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-120">char</span><span class="sxs-lookup"><span data-stu-id="6e053-120">char</span></span>](char.md)|<span data-ttu-id="6e053-121">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` 또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-121">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="6e053-122">float</span><span class="sxs-lookup"><span data-stu-id="6e053-122">float</span></span>](float.md)|`double`|  
|[<span data-ttu-id="6e053-123">ulong</span><span class="sxs-lookup"><span data-stu-id="6e053-123">ulong</span></span>](ulong.md)|<span data-ttu-id="6e053-124">`float`, `double`또는 `decimal`</span><span class="sxs-lookup"><span data-stu-id="6e053-124">`float`, `double`, or `decimal`</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e053-125">설명</span><span class="sxs-lookup"><span data-stu-id="6e053-125">Remarks</span></span>  

- <span data-ttu-id="6e053-126">모든 [정수 형식](integral-types-table.md)은 암시적으로 모든 [부동 소수점 형식](floating-point-types-table.md)으로 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e053-126">Any [integral type](integral-types-table.md) is implicitly convertible to any [floating-point type](floating-point-types-table.md).</span></span>

- <span data-ttu-id="6e053-127">`int`, `uint`, `long` 또는 `ulong`에서 `float`로 변환하고 `long` 또는 `ulong`에서 `double`로 변환하는 동안 전체 자릿수가 손실될 수도 있지만 크기는 손실되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e053-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`, `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
- <span data-ttu-id="6e053-128">`char` 형식으로의 암시적 변환은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e053-128">There are no implicit conversions to the `char` type.</span></span>  
  
- <span data-ttu-id="6e053-129">`float` 및 `double` 형식과 `decimal` 형식 간의 암시적 변환은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e053-129">There are no implicit conversions between the `float` and `double` types and the `decimal` type.</span></span>  
  
- <span data-ttu-id="6e053-130">형식 `int`의 상수 식 값(예: 정수 리터럴로 표시되는 값)은 대상 형식 범위 내에 있는 `sbyte`, `byte`, `short`, `ushort`, `uint` 또는 `ulong`으로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e053-130">A value of a constant expression of type `int` (for example, a value represented by an integral literal) can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided it's within the range of the destination type:</span></span>

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

<span data-ttu-id="6e053-131">암시적 변환에 대한 자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [암시적 변환](~/_csharplang/spec/conversions.md#implicit-conversions) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e053-131">For more information about implicit conversions, see the [Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions) section of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e053-132">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6e053-132">See also</span></span>

- [<span data-ttu-id="6e053-133">C# 참조</span><span class="sxs-lookup"><span data-stu-id="6e053-133">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="6e053-134">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="6e053-134">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="6e053-135">정수 계열 형식 표</span><span class="sxs-lookup"><span data-stu-id="6e053-135">Integral types table</span></span>](integral-types-table.md)
- [<span data-ttu-id="6e053-136">부동 소수점 형식 표</span><span class="sxs-lookup"><span data-stu-id="6e053-136">Floating-point types table</span></span>](floating-point-types-table.md)
- [<span data-ttu-id="6e053-137">기본 제공 형식 표</span><span class="sxs-lookup"><span data-stu-id="6e053-137">Built-in types table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="6e053-138">명시적 숫자 변환 표</span><span class="sxs-lookup"><span data-stu-id="6e053-138">Explicit numeric conversions table</span></span>](explicit-numeric-conversions-table.md)
- [<span data-ttu-id="6e053-139">캐스팅 및 형식 변환</span><span class="sxs-lookup"><span data-stu-id="6e053-139">Casting and type conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
