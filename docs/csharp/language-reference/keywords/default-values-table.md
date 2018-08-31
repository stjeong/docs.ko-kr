---
title: 기본값 표(C# 참조)
description: C# 값 형식의 기본 값은 무엇인지 알아봅니다.
ms.date: 08/23/2018
helpviewer_keywords:
- constructors [C#], return values
- keywords [C#], new
- default constructor [C#]
- defaults [C#]
- value types [C#], initializing
- variables [C#], value types
- constructors [C#], default constructor
- types [C#], default constructor return values
ms.openlocfilehash: 184a9f42ddd3654a81aef0b7ce35e404de2d4bb9
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935841"
---
# <a name="default-values-table-c-reference"></a><span data-ttu-id="e8614-103">기본값 표(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="e8614-103">Default values table (C# Reference)</span></span>

<span data-ttu-id="e8614-104">다음 표는 [값 형식](value-types.md)의 기본값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-104">The following table shows the default values of [value types](value-types.md).</span></span>

|<span data-ttu-id="e8614-105">값 형식</span><span class="sxs-lookup"><span data-stu-id="e8614-105">Value type</span></span>|<span data-ttu-id="e8614-106">기본값</span><span class="sxs-lookup"><span data-stu-id="e8614-106">Default value</span></span>|
|----------------|-------------------|
|[<span data-ttu-id="e8614-107">bool</span><span class="sxs-lookup"><span data-stu-id="e8614-107">bool</span></span>](bool.md)|`false`|
|[<span data-ttu-id="e8614-108">byte</span><span class="sxs-lookup"><span data-stu-id="e8614-108">byte</span></span>](byte.md)|<span data-ttu-id="e8614-109">0</span><span class="sxs-lookup"><span data-stu-id="e8614-109">0</span></span>|
|[<span data-ttu-id="e8614-110">char</span><span class="sxs-lookup"><span data-stu-id="e8614-110">char</span></span>](char.md)|<span data-ttu-id="e8614-111">'\0'</span><span class="sxs-lookup"><span data-stu-id="e8614-111">'\0'</span></span>|
|[<span data-ttu-id="e8614-112">decimal</span><span class="sxs-lookup"><span data-stu-id="e8614-112">decimal</span></span>](decimal.md)|<span data-ttu-id="e8614-113">0M</span><span class="sxs-lookup"><span data-stu-id="e8614-113">0M</span></span>|
|[<span data-ttu-id="e8614-114">double</span><span class="sxs-lookup"><span data-stu-id="e8614-114">double</span></span>](double.md)|<span data-ttu-id="e8614-115">0.0D</span><span class="sxs-lookup"><span data-stu-id="e8614-115">0.0D</span></span>|
|[<span data-ttu-id="e8614-116">enum</span><span class="sxs-lookup"><span data-stu-id="e8614-116">enum</span></span>](enum.md)|<span data-ttu-id="e8614-117">식 `(E)0`로 생성한 값이며 여기서 `E`는 열거형 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-117">The value produced by the expression `(E)0`, where `E` is the enum identifier.</span></span>|
|[<span data-ttu-id="e8614-118">float</span><span class="sxs-lookup"><span data-stu-id="e8614-118">float</span></span>](float.md)|<span data-ttu-id="e8614-119">0.0F</span><span class="sxs-lookup"><span data-stu-id="e8614-119">0.0F</span></span>|
|[<span data-ttu-id="e8614-120">int</span><span class="sxs-lookup"><span data-stu-id="e8614-120">int</span></span>](int.md)|<span data-ttu-id="e8614-121">0</span><span class="sxs-lookup"><span data-stu-id="e8614-121">0</span></span>|
|[<span data-ttu-id="e8614-122">long</span><span class="sxs-lookup"><span data-stu-id="e8614-122">long</span></span>](long.md)|<span data-ttu-id="e8614-123">0L</span><span class="sxs-lookup"><span data-stu-id="e8614-123">0L</span></span>|
|[<span data-ttu-id="e8614-124">sbyte</span><span class="sxs-lookup"><span data-stu-id="e8614-124">sbyte</span></span>](sbyte.md)|<span data-ttu-id="e8614-125">0</span><span class="sxs-lookup"><span data-stu-id="e8614-125">0</span></span>|
|[<span data-ttu-id="e8614-126">short</span><span class="sxs-lookup"><span data-stu-id="e8614-126">short</span></span>](short.md)|<span data-ttu-id="e8614-127">0</span><span class="sxs-lookup"><span data-stu-id="e8614-127">0</span></span>|
|[<span data-ttu-id="e8614-128">struct</span><span class="sxs-lookup"><span data-stu-id="e8614-128">struct</span></span>](struct.md)|<span data-ttu-id="e8614-129">모든 값 형식 필드를 기본값으로 설정하고 모든 참조 형식 필드를 `null`로 설정하여 생성한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-129">The value produced by setting all value-type fields to their default values and all reference-type fields to `null`.</span></span>|
|[<span data-ttu-id="e8614-130">uint</span><span class="sxs-lookup"><span data-stu-id="e8614-130">uint</span></span>](uint.md)|<span data-ttu-id="e8614-131">0</span><span class="sxs-lookup"><span data-stu-id="e8614-131">0</span></span>|
|[<span data-ttu-id="e8614-132">ulong</span><span class="sxs-lookup"><span data-stu-id="e8614-132">ulong</span></span>](ulong.md)|<span data-ttu-id="e8614-133">0</span><span class="sxs-lookup"><span data-stu-id="e8614-133">0</span></span>|
|[<span data-ttu-id="e8614-134">ushort</span><span class="sxs-lookup"><span data-stu-id="e8614-134">ushort</span></span>](ushort.md)|<span data-ttu-id="e8614-135">0</span><span class="sxs-lookup"><span data-stu-id="e8614-135">0</span></span>|

## <a name="remarks"></a><span data-ttu-id="e8614-136">설명</span><span class="sxs-lookup"><span data-stu-id="e8614-136">Remarks</span></span>

<span data-ttu-id="e8614-137">C#에서 초기화되지 않은 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-137">You cannot use uninitialized variables in C#.</span></span> <span data-ttu-id="e8614-138">해당 형식의 기본값을 사용하여 변수를 초기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-138">You can initialize a variable with the default value of its type.</span></span> <span data-ttu-id="e8614-139">또한 형식의 기본 값을 사용하여 메서드의 [선택적 인수](../../programming-guide/classes-and-structs/named-and-optional-arguments.md#optional-arguments)의 기본값을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-139">You also can use the default value of a type to specify the default value of a method's [optional argument](../../programming-guide/classes-and-structs/named-and-optional-arguments.md#optional-arguments).</span></span>

<span data-ttu-id="e8614-140">[기본값 식](../../programming-guide/statements-expressions-operators/default-value-expressions.md)을 사용하여 다음 예제와 같이 형식의 기본값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-140">Use the [default value expression](../../programming-guide/statements-expressions-operators/default-value-expressions.md) to produce the default value of a type, as the following example shows:</span></span>

```csharp
int a = default(int);
```

<span data-ttu-id="e8614-141">C# 7.1부터 [`default` 리터럴](../../programming-guide/statements-expressions-operators/default-value-expressions.md#default-literal-and-type-inference)을 사용하여 해당 형식의 기본값으로 변수를 초기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-141">Beginning with C# 7.1, you can use the [`default` literal](../../programming-guide/statements-expressions-operators/default-value-expressions.md#default-literal-and-type-inference) to initialize a variable with the default value of its type:</span></span>

```csharp
int a = default;
```

<span data-ttu-id="e8614-142">기본 생성자 또는 암시적 기본 생성자를 사용하여 다음 예제와 같이 값 형식의 기본값을 생성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-142">You also can use the default constructor or the implicit default constructor to produce the default value of a value type, as the following example shows.</span></span> <span data-ttu-id="e8614-143">생성자에 대한 자세한 내용은 [생성자](../../programming-guide/classes-and-structs/constructors.md) 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8614-143">For more information about constructors, see the [Constructors](../../programming-guide/classes-and-structs/constructors.md) article.</span></span>

```csharp
int a = new int();
```

<span data-ttu-id="e8614-144">모든 [참조 형식](reference-types.md)의 기본값은 `null`입니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-144">The default value of any [reference type](reference-types.md) is `null`.</span></span> <span data-ttu-id="e8614-145">[nullable 형식](../../programming-guide/nullable-types/index.md)의 기본값은 <xref:System.Nullable%601.HasValue%2A> 속성은 `false`이고 <xref:System.Nullable%601.Value%2A> 속성은 정의되지 않은 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="e8614-145">The default value of a [nullable type](../../programming-guide/nullable-types/index.md) is an instance for which the <xref:System.Nullable%601.HasValue%2A> property is `false` and the <xref:System.Nullable%601.Value%2A> property is undefined.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8614-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e8614-146">See also</span></span>

- [<span data-ttu-id="e8614-147">C# 참조</span><span class="sxs-lookup"><span data-stu-id="e8614-147">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="e8614-148">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="e8614-148">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="e8614-149">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="e8614-149">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="e8614-150">형식 참조 테이블</span><span class="sxs-lookup"><span data-stu-id="e8614-150">Reference tables for types</span></span>](reference-tables-for-types.md)
- [<span data-ttu-id="e8614-151">값 형식</span><span class="sxs-lookup"><span data-stu-id="e8614-151">Value types</span></span>](value-types.md)
- [<span data-ttu-id="e8614-152">값 형식 표</span><span class="sxs-lookup"><span data-stu-id="e8614-152">Value types table</span></span>](value-types-table.md)
- [<span data-ttu-id="e8614-153">기본 제공 형식 표</span><span class="sxs-lookup"><span data-stu-id="e8614-153">Built-in types table</span></span>](built-in-types-table.md)
