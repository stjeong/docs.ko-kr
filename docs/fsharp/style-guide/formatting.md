---
title: 'F # 코드 서식 지정 지침'
description: 'F # 코드 서식 지정에 대 한 지침을 알아봅니다.'
ms.date: 05/14/2018
ms.openlocfilehash: 0d7d2d1771710db55bf990f3a06079b2aec48fd7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858007"
---
# <a name="f-code-formatting-guidelines"></a><span data-ttu-id="0f439-103">F # 코드 서식 지정 지침</span><span class="sxs-lookup"><span data-stu-id="0f439-103">F# code formatting guidelines</span></span>

<span data-ttu-id="0f439-104">이 문서는 F # 코드 되도록 프로그램 코드의 서식을 지정 하는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-104">This article offers guidelines for how to format your code so that your F# code is:</span></span>

* <span data-ttu-id="0f439-105">일반적으로 보다 쉽게 읽을 것으로 간주</span><span class="sxs-lookup"><span data-stu-id="0f439-105">Generally viewed as more legible</span></span>
* <span data-ttu-id="0f439-106">Visual Studio의 도구 및 다른 편집기를 지정 하 여 적용 되는 규칙에 따라는</span><span class="sxs-lookup"><span data-stu-id="0f439-106">Is in accordance with conventions applied by formatting tools in Visual Studio and other editors</span></span>
* <span data-ttu-id="0f439-107">다른 온라인으로 코드와 유사</span><span class="sxs-lookup"><span data-stu-id="0f439-107">Similar to other code online</span></span>

<span data-ttu-id="0f439-108">다음이 지침에 기반한 [F # 서식 지정 규칙에 대 한 포괄적인 지침](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) 하 여 [Anh 똥 Phan](https://github.com/dungpa)합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-108">These guidelines are based on [A comprehensive guide to F# Formatting Conventions](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) by [Anh-Dung Phan](https://github.com/dungpa).</span></span>

## <a name="general-rules-for-indentation"></a><span data-ttu-id="0f439-109">들여쓰기에 대 한 일반 규칙</span><span class="sxs-lookup"><span data-stu-id="0f439-109">General rules for indentation</span></span>

<span data-ttu-id="0f439-110">F # 기본적으로 유효 공백 문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-110">F# uses significant white space by default.</span></span> <span data-ttu-id="0f439-111">다음 지침을 적용할 수이 하는 몇 가지 과제를 다루어야 하는 방법에 대 한 지침을 제공 하려는.</span><span class="sxs-lookup"><span data-stu-id="0f439-111">The following guidelines are intended to provide guidance as to how to juggle some challenges this can impose.</span></span>

### <a name="using-spaces"></a><span data-ttu-id="0f439-112">공간 사용</span><span class="sxs-lookup"><span data-stu-id="0f439-112">Using spaces</span></span>

<span data-ttu-id="0f439-113">들여쓰기가 필요한 경우 공백, 탭 하지 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-113">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="0f439-114">하나 이상의 공간이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-114">At least one space is required.</span></span> <span data-ttu-id="0f439-115">조직에 들여쓰기;에 사용할 공백 수를 지정 하는 코딩 표준을 만들 수 있습니다. 2, 3 또는 4 개의 공백 들여쓰기 발생 하는 각 수준에서 들여쓰기 하는 것이 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-115">Your organization can create coding standards to specify the number of spaces to use for indentation; two, three or four spaces of indentation at each level where indentation occurs is typical.</span></span>

<span data-ttu-id="0f439-116">**들여쓰기 당 4 개의 공백을 사용 하는 것이 좋습니다.**</span><span class="sxs-lookup"><span data-stu-id="0f439-116">**We recommend 4 spaces per indentation.**</span></span>

<span data-ttu-id="0f439-117">즉, 프로그램의 들여쓰기는 주관적입니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-117">That said, indentation of programs is a subjective matter.</span></span> <span data-ttu-id="0f439-118">변형 좋은지 이지만 첫 번째 규칙을 따라야 *들여쓰기 일관성*합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-118">Variations are OK, but the first rule you should follow is *consistency of indentation*.</span></span> <span data-ttu-id="0f439-119">들여쓰기의 일반적으로 허용 되는 스타일을 선택 하 고 코드 베이스 전체에서 체계적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-119">Choose a generally accepted style of indentation and use it systematically throughout your codebase.</span></span>

## <a name="formatting-blank-lines"></a><span data-ttu-id="0f439-120">빈 줄을 서식 지정</span><span class="sxs-lookup"><span data-stu-id="0f439-120">Formatting blank lines</span></span>

* <span data-ttu-id="0f439-121">별도 최상위 함수 및 클래스 정의 두 개의 빈 줄을 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-121">Separate top-level function and class definitions with two blank lines.</span></span>
* <span data-ttu-id="0f439-122">클래스 내의 메서드 정의 비어 있는 단일 선으로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-122">Method definitions inside a class are separated by a single blank line.</span></span>
* <span data-ttu-id="0f439-123">빈 줄을 별도의 관련 된 기능 그룹 (제한적) 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-123">Extra blank lines may be used (sparingly) to separate groups of related functions.</span></span> <span data-ttu-id="0f439-124">다양 한 관련된 one-liner (예를 들어, 구현 집합을 더미) 사이의 빈 줄을 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-124">Blank lines may be omitted between a bunch of related one-liners (for example, a set of dummy implementations).</span></span>
* <span data-ttu-id="0f439-125">논리적 섹션을 나타내기 위해 함수에서 빈 줄을 제한적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-125">Use blank lines in functions, sparingly, to indicate logical sections.</span></span>

## <a name="formatting-comments"></a><span data-ttu-id="0f439-126">주석 형식</span><span class="sxs-lookup"><span data-stu-id="0f439-126">Formatting comments</span></span>

<span data-ttu-id="0f439-127">일반적으로 기계 학습 스타일 블록 주석 통해 여러 이중 슬래시 주석을 선호 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-127">Generally prefer multiple double-slash comments over ML-style block comments.</span></span>

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

<span data-ttu-id="0f439-128">인라인 주석을 첫 번째 글자를 대문자로 표시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-128">Inline comments should capitalize the first letter.</span></span>

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a><span data-ttu-id="0f439-129">명명 규칙</span><span class="sxs-lookup"><span data-stu-id="0f439-129">Naming conventions</span></span>

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a><span data-ttu-id="0f439-130">CamelCase를 사용 하 여 클래스 바인딩, 바인딩 식 및 패턴 바인딩된 값 및 함수에 대 한</span><span class="sxs-lookup"><span data-stu-id="0f439-130">Use camelCase for class-bound, expression-bound and pattern-bound values and functions</span></span>

<span data-ttu-id="0f439-131">일반적인 되며 모든 이름에 대 한 camelCase를 사용 하도록 허용 된 F # 스타일 바인딩된 지역 변수 또는 패턴 일치에 함수 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-131">It is common and accepted F# style to use camelCase for all names bound as local variables or in pattern matches and function definitions.</span></span>

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

<span data-ttu-id="0f439-132">클래스에 바인딩된 로컬로 함수도 camelCase를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-132">Locally-bound functions in classes should also use camelCase.</span></span>

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a><span data-ttu-id="0f439-133">CamelCase를 사용 하 여 모듈 바인딩된 공용 함수에 대 한</span><span class="sxs-lookup"><span data-stu-id="0f439-133">Use camelCase for module-bound public functions</span></span>

<span data-ttu-id="0f439-134">모듈 바인딩된 함수는 공용 API의 일부 이면 camelCase 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-134">When a module-bound function is part of a public API, it should use camelCase:</span></span>

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a><span data-ttu-id="0f439-135">CamelCase를 사용 하 여 내부 및 개인 모듈 바인딩된 값 및 함수에 대 한</span><span class="sxs-lookup"><span data-stu-id="0f439-135">Use camelCase for internal and private module-bound values and functions</span></span>

<span data-ttu-id="0f439-136">다음을 포함 하 여 개인 모듈 바인딩된 값에 대 한 camelCase를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-136">Use camelCase for private module-bound values, including the following:</span></span>

* <span data-ttu-id="0f439-137">스크립트의 임시 함수</span><span class="sxs-lookup"><span data-stu-id="0f439-137">Ad hoc functions in scripts</span></span>

* <span data-ttu-id="0f439-138">값 형식 또는 모듈의 내부 구현을 구성</span><span class="sxs-lookup"><span data-stu-id="0f439-138">Values making up the internal implementation of a module or type</span></span>

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a><span data-ttu-id="0f439-139">CamelCase를 사용 하 여 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f439-139">Use camelCase for parameters</span></span>

<span data-ttu-id="0f439-140">모든 매개 변수는.NET 명명 규칙에 따라 camelCase를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-140">All parameters should use camelCase in accordance with .NET naming conventions.</span></span>

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a><span data-ttu-id="0f439-141">PascalCase를 사용 하 여 모듈에 대 한</span><span class="sxs-lookup"><span data-stu-id="0f439-141">Use PascalCase for modules</span></span>

<span data-ttu-id="0f439-142">모든 모듈 (예: 최상위, 내부, 개인, 중첩 된) PascalCase를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-142">All modules (top-level, internal, private, nested) should use PascalCase.</span></span>

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a><span data-ttu-id="0f439-143">형식 선언, 멤버 및 레이블을 사용 하 여 PascalCase</span><span class="sxs-lookup"><span data-stu-id="0f439-143">Use PascalCase for type declarations, members, and labels</span></span>

<span data-ttu-id="0f439-144">클래스, 인터페이스, 구조체, 열거형, 대리자, 레코드 및 구분 된 공용 구조체 모든 PascalCase로 명명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-144">Classes, interfaces, structs, enumerations, delegates, records, and discriminated unions should all be named with PascalCase.</span></span> <span data-ttu-id="0f439-145">형식 및 레코드 및 구분 된 공용 구조체에 대 한 레이블 내에서 멤버 PascalCase 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-145">Members within types and labels for records and discriminated unions should also use PascalCase.</span></span>

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a><span data-ttu-id="0f439-146">PascalCase를 사용 하 여.NET으로 내장 되는 구문에 대 한</span><span class="sxs-lookup"><span data-stu-id="0f439-146">Use PascalCase for constructs intrinsic to .NET</span></span>

<span data-ttu-id="0f439-147">네임 스페이스, 예외, 이벤트 및 프로젝트 /`.dll` 이름을 PascalCase에도 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-147">Namespaces, exceptions, events, and project/`.dll` names should also use PascalCase.</span></span> <span data-ttu-id="0f439-148">뿐만 아니라 소비자에 게 자연스럽 게 느낄 다른.NET 언어에서 소비 되셨나요, 그리고 발생할 가능성이 있는.NET 명명 규칙에 부합 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-148">Not only does this make consumption from other .NET languages feel more natural to consumers, it's also consistent with .NET naming conventions that you are likely to encounter.</span></span>

### <a name="avoid-underscores-in-names"></a><span data-ttu-id="0f439-149">이름에 밑줄을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-149">Avoid underscores in names</span></span>

<span data-ttu-id="0f439-150">지금까지 일부 F # 라이브러리 이름에 밑줄을 사용 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-150">Historically, some F# libraries have used underscores in names.</span></span> <span data-ttu-id="0f439-151">그러나이 더 이상 광범위 하 게 수락 되 면.NET 명명 규칙을 사용 하 여 충돌 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-151">However, this is no longer widely accepted, partly because it clashes with .NET naming conventions.</span></span> <span data-ttu-id="0f439-152">즉, 일부 F # 프로그래머가 사용 하 여 밑줄 많이, 부분적으로 기록 상의 용도로 허용 오차 존경 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-152">That said, some F# programmers use underscores heavily, partly for historical reasons, and tolerance and respect is important.</span></span> <span data-ttu-id="0f439-153">그러나 사용할 것인지 선택할 수 있는 다른 사용자가 스타일은 종종 싫는 주의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-153">However, be aware that the style is often disliked by others who have a choice about whether to use it.</span></span>

<span data-ttu-id="0f439-154">밑줄을 매우 자주 네이티브 구성 요소와의 상호 운용 하는 몇 가지 예외 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-154">Some exceptions includes interoperating with native components, where underscores are very common.</span></span>

### <a name="use-standard-f-operators"></a><span data-ttu-id="0f439-155">표준 F # 연산자를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-155">Use standard F# operators</span></span>

<span data-ttu-id="0f439-156">다음 연산자를 F # 표준 라이브러리에 정의 되어 있고 해당 항목을 정의 하는 대신 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-156">The following operators are defined in the F# standard library and should be used instead of defining equivalents.</span></span> <span data-ttu-id="0f439-157">더 읽기 쉽고 자연 스러운 코드를 확인 하는 경향이 있습니다 이러한 연산자를 사용 하 여 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-157">Using these operators is recommended as it tends to make code more readable and idiomatic.</span></span> <span data-ttu-id="0f439-158">OCaml 또는 다른 함수형 프로그래밍 언어에서 배경의 개발자가 익숙한 다른 관용구를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-158">Developers with a background in OCaml or other functional programming language may be accustomed to different idioms.</span></span> <span data-ttu-id="0f439-159">다음 목록에는 권장 되는 F # 연산자 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-159">The following list summarizes the recommended F# operators.</span></span>

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a><span data-ttu-id="0f439-160">제네릭에 대 한 접두사 구문을 사용 하 여 (`Foo<T>`) 후 위 구문 보다 우선적으로 (`T Foo`)</span><span class="sxs-lookup"><span data-stu-id="0f439-160">Use prefix syntax for generics (`Foo<T>`) in preference to postfix syntax (`T Foo`)</span></span>

<span data-ttu-id="0f439-161">F # 제네릭 형식 명명 모두는 후 위 ML 스타일을 상속 합니다. (예를 들어 `int list`)와.NET 스타일 접두사 (예를 들어, `list<int>`).</span><span class="sxs-lookup"><span data-stu-id="0f439-161">F# inherits both the postfix ML style of naming generic types (for example, `int list`) as well as the prefix .NET style (for example, `list<int>`).</span></span> <span data-ttu-id="0f439-162">네 개의 특정 형식 제외 하 고.NET 스타일을 선호 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-162">Prefer the .NET style, except for four specific types:</span></span>

1. <span data-ttu-id="0f439-163">F # 목록에서는, 후 위 형식 사용: `int list` 대신 `list<int>`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-163">For F# Lists, use the postfix form: `int list` rather than `list<int>`.</span></span>
2. <span data-ttu-id="0f439-164">F # 옵션에 대해 후 위 형식 사용: `int option` 대신 `option<int>`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-164">For F# Options, use the postfix form: `int option` rather than `option<int>`.</span></span>
3. <span data-ttu-id="0f439-165">F # 배열의 경우 구문 이름을 사용 하 여 `int[]` 대신 `int array` 또는 `array<int>`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-165">For F# arrays, use the syntactic name `int[]` rather than `int array` or `array<int>`.</span></span>
4. <span data-ttu-id="0f439-166">참조 셀에 대 한 사용 `int ref` 대신 `ref<int>` 또는 `Ref<int>`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-166">For Reference Cells, use `int ref` rather than `ref<int>` or `Ref<int>`.</span></span>

<span data-ttu-id="0f439-167">다른 모든 형식에 대 한 접두사 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-167">For all other types, use the prefix form.</span></span>

## <a name="formatting-tuples"></a><span data-ttu-id="0f439-168">튜플 형식</span><span class="sxs-lookup"><span data-stu-id="0f439-168">Formatting tuples</span></span>

<span data-ttu-id="0f439-169">튜플 인스턴스화를 괄호로 묶고 고 내의 구분 쉼표 뒤에 야 공백, 예: `(1, 2)`, `(x, y, z)`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-169">A tuple instantiation should be parenthesized, and the delimiting commas within should be followed by a single space, for example: `(1, 2)`, `(x, y, z)`.</span></span>

<span data-ttu-id="0f439-170">튜플 패턴 일치에서 괄호를 생략 하려면 일반적으로 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-170">It is commonly accepted to omit parentheses in pattern matching of tuples:</span></span>

```fsharp
let (x, y) = z // Destructuring
let x, y = z // OK

// OK
match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-discriminated-union-declarations"></a><span data-ttu-id="0f439-171">구별 된 공용 구조체 선언 서식 지정</span><span class="sxs-lookup"><span data-stu-id="0f439-171">Formatting discriminated union declarations</span></span>

<span data-ttu-id="0f439-172">들여쓰기 `|` 4 개의 공백 사용 하 여 형식 정의에서:</span><span class="sxs-lookup"><span data-stu-id="0f439-172">Indent `|` in type definition by 4 spaces:</span></span>

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

## <a name="formatting-discriminated-unions"></a><span data-ttu-id="0f439-173">구별 된 공용 구조체 형식</span><span class="sxs-lookup"><span data-stu-id="0f439-173">Formatting discriminated unions</span></span>

<span data-ttu-id="0f439-174">여러 줄에 분할 된 인스턴스화된 구별 된 공용 구조체 들여쓰기를 사용 하 여 새 범위를 포함 된 데이터를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-174">Instantiated Discriminated Unions that split across multiple lines should give contained data a new scope with indentation:</span></span>

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

<span data-ttu-id="0f439-175">닫는 괄호를 새 줄 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-175">The closing parenthesis can also be on a new line:</span></span>

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-record-declarations"></a><span data-ttu-id="0f439-176">서식 레코드 선언</span><span class="sxs-lookup"><span data-stu-id="0f439-176">Formatting record declarations</span></span>

<span data-ttu-id="0f439-177">들여쓰기 `{` 형식에서 4로 정의 공백 및 필드 목록 같은 줄에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-177">Indent `{` in type definition by 4 spaces and start the field list on the same line:</span></span>

```fsharp
// OK
type PostalAddress =
    { Address: string
      City: string
      Zip: string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City

// Not OK
type PostalAddress =
  { Address: string
    City: string
    Zip: string }
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
    
// Unusual in F#
type PostalAddress =
    { 
        Address: string
        City: string
        Zip: string
    }
```

<span data-ttu-id="0f439-178">열기 토큰을 새 줄에 닫는 토큰과 같은 줄 배치도 정상 이지만 사용 해야 합니다 [자세한 구문](../language-reference/verbose-syntax.md) 멤버를 정의 (의 `with` 키워드):</span><span class="sxs-lookup"><span data-stu-id="0f439-178">Placing the opening token on the same line and the closing token on a new line is also fine, but be aware that you need to use the [verbose syntax](../language-reference/verbose-syntax.md) to define members (the `with` keyword):</span></span>

```fsharp
//  OK, but verbose syntax required
type PostalAddress = { 
    Address: string
    City: string
    Zip: string
} with
    member x.ZipAndCity = sprintf "%s %s" x.Zip x.City
```

## <a name="formatting-records"></a><span data-ttu-id="0f439-179">레코드 형식</span><span class="sxs-lookup"><span data-stu-id="0f439-179">Formatting records</span></span>

<span data-ttu-id="0f439-180">짧은 레코드는 한 줄에 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-180">Short records can be written in one line:</span></span>

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

<span data-ttu-id="0f439-181">오래 된 레코드는 레이블에 대 한 새 줄을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-181">Records that are longer should use new lines for labels:</span></span>

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

<span data-ttu-id="0f439-182">새 줄에 닫는 토큰과 같은 줄에 여 토큰을 배치 해도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-182">Placing the opening token on the same line and the closing token on a new line is also fine:</span></span>

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

<span data-ttu-id="0f439-183">목록 및 배열 요소에 대 한 동일한 규칙이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-183">The same rules apply for list and array elements.</span></span>

## <a name="formatting-lists-and-arrays"></a><span data-ttu-id="0f439-184">서식 지정 목록 및 배열</span><span class="sxs-lookup"><span data-stu-id="0f439-184">Formatting lists and arrays</span></span>

<span data-ttu-id="0f439-185">쓰기 `x :: l` 주위에 공백을 사용 하 여는 `::` 연산자 (`::` 는 공백으로 둘러싸인 따라서 중 위 연산자,) 및 `[1; 2; 3]` (`;` 는 구분 기호, 공백 뒤에 있으므로).</span><span class="sxs-lookup"><span data-stu-id="0f439-185">Write `x :: l` with spaces around the `::` operator (`::` is an infix operator, hence surrounded by spaces) and `[1; 2; 3]` (`;` is a delimiter, hence followed by a space).</span></span>

<span data-ttu-id="0f439-186">항상 두 명의 고유 중괄호 같은 연산자 사이 하나 이상의 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-186">Always use at least one space between two distinct brace-like operators.</span></span> <span data-ttu-id="0f439-187">예를 들어 사이 공백을 둡니다를 `[` 및 `{`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-187">For example, leave a space between a `[` and a `{`.</span></span>

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

<span data-ttu-id="0f439-188">목록 및 여러 줄 분할 되는 배열 레코드와 마찬가지로 비슷한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-188">Lists and arrays that split across multiple lines follow a similar rule as records do:</span></span>

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a><span data-ttu-id="0f439-189">경우에 형식 지정 식</span><span class="sxs-lookup"><span data-stu-id="0f439-189">Formatting if expressions</span></span>

<span data-ttu-id="0f439-190">조건문의 들여쓰기 구성 하는 식의 크기에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-190">Indentation of conditionals depends on the sizes of the expressions that make them up.</span></span> <span data-ttu-id="0f439-191">하는 경우 `cond`, `e1` 및 `e2` 짧은, 한 줄에 작성 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-191">If `cond`, `e1` and `e2` are short, simply write them on one line:</span></span>

```fsharp
if cond then e1 else e2
```

<span data-ttu-id="0f439-192">경우 `cond`, `e1` 또는 `e2` 더 있지만 여러 줄 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-192">If either `cond`, `e1` or `e2` are longer, but not multi-line:</span></span>

```fsharp
if cond
then e1
else e2
```

<span data-ttu-id="0f439-193">식이 있는 경우 여러 줄:</span><span class="sxs-lookup"><span data-stu-id="0f439-193">If any of the expressions are multi-line:</span></span>

```fsharp
if cond then
    e1
else
    e2
```

<span data-ttu-id="0f439-194">사용 하 여 여러 가지 조건을 `elif` 하 고 `else` 와 동일한 범위에서 들여쓰기가 적용 되는 `if`:</span><span class="sxs-lookup"><span data-stu-id="0f439-194">Multiple conditionals with `elif` and `else` are indented at the same scope as the `if`:</span></span>

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a><span data-ttu-id="0f439-195">패턴 일치 하는 구문</span><span class="sxs-lookup"><span data-stu-id="0f439-195">Pattern matching constructs</span></span>

<span data-ttu-id="0f439-196">사용 된 `|` 없습니다 들여쓰기를 사용 하 여 일치 하는 각 절에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-196">Use a `|` for each clause of a match with no indentation.</span></span> <span data-ttu-id="0f439-197">식 짧은 경우 각 하위 식에 간단한 이기도 한 경우는 단일 선을 사용을 고려할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-197">If the expression is short, you can consider using a single line if each subexpression is also simple.</span></span>

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"
```

<span data-ttu-id="0f439-198">패턴 일치 화살표 오른쪽의 식이 너무 큰 경우 들여쓰기 한 단계에서 다음 줄으로 이동 합니다 `match` / `|`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-198">If the expression on the right of the pattern matching arrow is too large, move it to the following line, indented one step from the `match`/`|`.</span></span>

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

<span data-ttu-id="0f439-199">패턴 일치 익명 함수에 의해 시작 `function`을 해야 일반적으로 들여쓰지 멀리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-199">Pattern matching of anonymous functions, starting by `function`, should generally not indent too far.</span></span> <span data-ttu-id="0f439-200">예를 들어, 한 범위를 다음과 같이 들여쓰기 괜찮습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-200">For example, indenting one scope as follows is fine:</span></span>

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

<span data-ttu-id="0f439-201">패턴에서 정의 된 함수에서 일치 `let` 또는 `let rec` 시작 후 들여쓰기 4 공간을 사용 해야 `let`경우에 `function` 키워드가 사용:</span><span class="sxs-lookup"><span data-stu-id="0f439-201">Pattern matching in functions defined by `let` or `let rec` should be indented 4 spaces after starting of `let`, even if `function` keyword is used:</span></span>

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

<span data-ttu-id="0f439-202">화살표를 정렬 하는 것은 좋지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-202">We do not recommend aligning arrows.</span></span>

## <a name="formatting-trywith-expressions"></a><span data-ttu-id="0f439-203">서식 지정 시도 / 식을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="0f439-203">Formatting try/with expressions</span></span>

<span data-ttu-id="0f439-204">예외 형식에 패턴 일치와 같은 수준에서 써야 `with`합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-204">Pattern matching on the exception type should be indented at the same level as `with`.</span></span>

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a><span data-ttu-id="0f439-205">서식 지정 함수에 대 한 매개 변수 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="0f439-205">Formatting function parameter application</span></span>

<span data-ttu-id="0f439-206">일반적으로 대부분의 함수 매개 변수 응용 프로그램 같은 줄에서 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-206">In general, most function parameter application is done on the same line.</span></span>

<span data-ttu-id="0f439-207">새 줄에 함수에 매개 변수를 적용 하려는 경우 하나의 범위로 들여씁니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-207">If you wish to apply parameters to a function on a new line, indent them by one scope.</span></span>

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

<span data-ttu-id="0f439-208">동일한 지침이 함수 인수로 람다 식에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-208">The same guidelines apply for lambda expressions as function arguments.</span></span> <span data-ttu-id="0f439-209">범위를 하나 만큼 들여씁니다 본문 람다 식의 본문에서 다른 줄에 넣을 수 있는 경우</span><span class="sxs-lookup"><span data-stu-id="0f439-209">If the body of a lambda expression, the body can have another line, indented by one scope</span></span>

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

<span data-ttu-id="0f439-210">그러나 둘 이상의 줄 람다 식의 본문을 사용 하는 경우 별도 함수에 팩터링 하는 것이 좋습니다 보다 단일 인수로 함수에 적용 하는 여러 줄 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-210">However, if the body of a lambda expression is more than one line, consider factoring it out into a separate function rather than have a multi-line construct applied as a single argument to a function.</span></span>

### <a name="formatting-infix-operators"></a><span data-ttu-id="0f439-211">서식 지정 중 위 연산자</span><span class="sxs-lookup"><span data-stu-id="0f439-211">Formatting infix operators</span></span>

<span data-ttu-id="0f439-212">공백 사용 하 여 별도 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-212">Separate operators by spaces.</span></span> <span data-ttu-id="0f439-213">이 규칙에 확실 한 예외는 `!` 고 `.` 연산자.</span><span class="sxs-lookup"><span data-stu-id="0f439-213">Obvious exceptions to this rule are the `!` and `.` operators.</span></span>

<span data-ttu-id="0f439-214">중 위 식은 다음과 같습니다. 확인에 동일한 열 목록</span><span class="sxs-lookup"><span data-stu-id="0f439-214">Infix expressions are OK to lineup on same column:</span></span>

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a><span data-ttu-id="0f439-215">파이프라인 연산자를 서식 지정</span><span class="sxs-lookup"><span data-stu-id="0f439-215">Formatting pipeline operators</span></span>

<span data-ttu-id="0f439-216">파이프라인 `|>` 연산자에서 작동 하는 식 아래에 있는 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-216">Pipeline `|>` operators should go underneath the expressions they operate on.</span></span>

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a><span data-ttu-id="0f439-217">모듈을 서식 지정</span><span class="sxs-lookup"><span data-stu-id="0f439-217">Formatting modules</span></span>

<span data-ttu-id="0f439-218">로컬 모듈의 코드 모듈을 기준으로 써야 하지만 최상위 모듈에는 코드를 들여쓰지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-218">Code in a local module must be indented relative to the module, but code in a top-level module should not be indented.</span></span> <span data-ttu-id="0f439-219">Namespace 요소 들여쓰기 될 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-219">Namespace elements do not have to be indented.</span></span>

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a><span data-ttu-id="0f439-220">서식 개체 식 및 인터페이스</span><span class="sxs-lookup"><span data-stu-id="0f439-220">Formatting object expressions and interfaces</span></span>

<span data-ttu-id="0f439-221">개체 식 및 인터페이스는 동일한 방식으로 정렬 해야 합니다 `member` 4 개의 공백을 후 들여쓰기 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-221">Object expressions and interfaces should be aligned in the same way with `member` being indented after 4 spaces.</span></span>

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-white-space-in-expressions"></a><span data-ttu-id="0f439-222">식에서 공백 서식 지정</span><span class="sxs-lookup"><span data-stu-id="0f439-222">Formatting white space in expressions</span></span>

<span data-ttu-id="0f439-223">F # 식에 불필요 한 공백을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f439-223">Avoid extraneous white space in F# expressions.</span></span>

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

<span data-ttu-id="0f439-224">명명 된 인수도 없어야 공간 관련 된 `=`:</span><span class="sxs-lookup"><span data-stu-id="0f439-224">Named arguments should also not have space surrounding the `=`:</span></span>

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```
