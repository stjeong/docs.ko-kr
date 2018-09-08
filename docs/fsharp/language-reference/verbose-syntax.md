---
title: 자세한 구문(F#)
description: 'F # 프로그래밍 언어에서 자세한 정보 및 간단한 구문 간의 차이점에 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: b4f2354738da4692cb444e5e7dd9531d80d26664
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44193162"
---
# <a name="verbose-syntax"></a><span data-ttu-id="2d410-103">자세한 구문</span><span class="sxs-lookup"><span data-stu-id="2d410-103">Verbose Syntax</span></span>

<span data-ttu-id="2d410-104">F # 언어의 많은 구문을 사용할 수 있는 두 가지 형태의 구문이 있습니다: *자세한 구문* 하 고 *간단한 구문을*합니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-104">There are two forms of syntax available for many constructs in the F# language: *verbose syntax* and *lightweight syntax*.</span></span> <span data-ttu-id="2d410-105">자세한 구문 일반적으로 사용 되지 않지만 되 들여쓰기로 덜 중요 한 장점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-105">The verbose syntax is not as commonly used, but has the advantage of being less sensitive to indentation.</span></span> <span data-ttu-id="2d410-106">같은 추가 키워드 보다는 간단한 구문은 짧은 및 들여쓰기를 사용 하 여 구문의 시작과 끝을 알리기 위해 `begin`, `end`, `in`등입니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-106">The lightweight syntax is shorter and uses indentation to signal the beginning and end of constructs, rather than additional keywords like `begin`, `end`, `in`, and so on.</span></span> <span data-ttu-id="2d410-107">기본 구문은 간단한 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-107">The default syntax is the lightweight syntax.</span></span> <span data-ttu-id="2d410-108">이 항목에서는 간단한 구문을 사용 하지 않는 경우 F # 구문에 대 한 구문을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-108">This topic describes the syntax for F# constructs when lightweight syntax is not enabled.</span></span> <span data-ttu-id="2d410-109">간단한 구문을 사용 하도록 설정한 경우에 사용할 수 있도록 계속 자세한 구문 일부 구문에 대 한 자세한 구문은 항상 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-109">Verbose syntax is always enabled, so even if you enable lightweight syntax, you can still use verbose syntax for some constructs.</span></span> <span data-ttu-id="2d410-110">사용 하 여 간단한 구문을 사용 하지 않도록 설정할 수는 `#light "off"` 지시문입니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-110">You can disable lightweight syntax by using the `#light "off"` directive.</span></span>

## <a name="table-of-constructs"></a><span data-ttu-id="2d410-111">구문 표</span><span class="sxs-lookup"><span data-stu-id="2d410-111">Table of Constructs</span></span>

<span data-ttu-id="2d410-112">다음 표에서 상황에서 F # 언어 구문에 대 한 간단 하 고 자세한 구문을 보여 줍니다. 여기서 두 가지 형식 사이 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-112">The following table shows the lightweight and verbose syntax for F# language constructs in contexts where there is a difference between the two forms.</span></span> <span data-ttu-id="2d410-113">이 테이블에서 꺾쇠 괄호 (&lt;&gt;) 사용자가 제공한 구문 요소를 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="2d410-113">In this table, angle brackets (&lt;&gt;) enclose user-supplied syntax elements.</span></span> <span data-ttu-id="2d410-114">이러한 구문 내에서 사용 된 구문에 대 한 자세한 정보에 대 한 각 언어 구문에 대 한 설명서를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="2d410-114">Refer to the documentation for each language construct for more detailed information about the syntax used within these constructs.</span></span>

<table>
<tr>
<th><span data-ttu-id="2d410-115">언어 구문</span><span class="sxs-lookup"><span data-stu-id="2d410-115">Language construct</span></span></th>
<th><span data-ttu-id="2d410-116">간단한 구문</span><span class="sxs-lookup"><span data-stu-id="2d410-116">Lightweight syntax</span></span></th>
<th><span data-ttu-id="2d410-117">자세한 구문</span><span class="sxs-lookup"><span data-stu-id="2d410-117">Verbose syntax</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="2d410-118">복합 식</span><span class="sxs-lookup"><span data-stu-id="2d410-118">compound expressions</span></span>
</td>
<td>

```xml
<expression1>
<expression2>
```
</td><td>

```
<expression1>; <expression2>
```

</td>
</tr>
<tr><td>


<span data-ttu-id="2d410-119">중첩 된 `let` 바인딩</span><span class="sxs-lookup"><span data-stu-id="2d410-119">nested `let` bindings</span></span>

</td><td>
```
let f x =
    let a = 1
    let b = 2
    x + a + b
```

</td><td>

```
let f x =
    let a = 1 in
    let b = 2 in
    x + a + b
```

</td>
</tr>
<tr><td>
<span data-ttu-id="2d410-120">코드 블록</span><span class="sxs-lookup"><span data-stu-id="2d410-120">code block</span></span>
</td><td>

```
(
    <expression1>
    <expression2>
)
```

</td><td>

```
begin
    <expression1>;
    <expression2>;
end
```
</td>
</tr>
<tr><td>
`for...do`
</td><td>

```
for counter = start to finish do
    ...
```

</td><td>

```
for counter = start to finish do
    ...
done
```

</td>
</tr>
<tr><td>
`while...do`
</td><td>

```
while <condition> do
    ...
```

</td><td>

```
while <condition> do
    ...
done
```

</td>
</tr>
<tr><td>
`for...in`
</td><td>

```
for var in start .. finish do
    ...
```

</td><td>

```
for var in start .. finish do
    ...
done
```

</td>
</tr>
<tr><td>
`do`
</td><td>

```
do
    ...
```

</td><td>

```
do
    ...
in
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-121">레코드</span><span class="sxs-lookup"><span data-stu-id="2d410-121">record</span></span>
</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    <value-or-member-definitions>
```

</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-122">클래스</span><span class="sxs-lookup"><span data-stu-id="2d410-122">class</span></span>
</td><td><span data-ttu-id="2d410-123">
```
type <class-name>(<params>) = ... ```

</span><span class="sxs-lookup"><span data-stu-id="2d410-123">
```
type <class-name>(<params>) = ... ```

</span></span></td><td>

```
type <class-name>(<params>) =
    class
        ...
    end
```
</td>
</tr>
<tr><td><span data-ttu-id="2d410-124">구조체(structure)</span><span class="sxs-lookup"><span data-stu-id="2d410-124">structure</span></span></td><td>

```
[<StructAttribute>]
type <structure-name> =
    ...
```
</td><td>

```
type <structure-name> =
    struct
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-125">구별 된 공용 구조체</span><span class="sxs-lookup"><span data-stu-id="2d410-125">discriminated union</span></span></td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    <value-or-member definitions>
```
</td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    with
        <value-or-member-definitions>
    end    
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-126">interface(인터페이스)</span><span class="sxs-lookup"><span data-stu-id="2d410-126">interface</span></span></td><td>

```
type <interface-name> =
    ...
```
</td><td>

```
type <interface-name> =
    interface
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-127">개체 식</span><span class="sxs-lookup"><span data-stu-id="2d410-127">object expression</span></span></td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
        <interface-implementations>
}
```

</td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
    end
    <interface-implementations>
}
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-128">인터페이스 구현</span><span class="sxs-lookup"><span data-stu-id="2d410-128">interface implementation</span></span></td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-129">형식 확장</span><span class="sxs-lookup"><span data-stu-id="2d410-129">type extension</span></span></td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="2d410-130">name</span><span class="sxs-lookup"><span data-stu-id="2d410-130">module</span></span></td><td>

```
module <module-name> =
    ...
```

</td><td>

```
module <module-name> =
    begin
        ...
    end
```

</td>
</tr>
</table>

## <a name="see-also"></a><span data-ttu-id="2d410-131">참고자료</span><span class="sxs-lookup"><span data-stu-id="2d410-131">See also</span></span>

- [<span data-ttu-id="2d410-132">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="2d410-132">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="2d410-133">컴파일러 지시문</span><span class="sxs-lookup"><span data-stu-id="2d410-133">Compiler Directives</span></span>](compiler-directives.md)
- [<span data-ttu-id="2d410-134">코드 서식 지정 지침</span><span class="sxs-lookup"><span data-stu-id="2d410-134">Code Formatting Guidelines</span></span>](code-formatting-guidelines.md)
