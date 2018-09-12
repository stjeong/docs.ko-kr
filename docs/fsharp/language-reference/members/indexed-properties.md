---
title: 인덱싱된 속성(F#)
description: 'F # 인덱싱된 속성을 정렬 된 데이터에 대 한 배열 유사 액세스를 제공 하는 속성에 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: e56e4e2ea3f35df4c8ec46012357242cb6ce69f3
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44511044"
---
# <a name="indexed-properties"></a><span data-ttu-id="73e41-103">인덱싱된 속성</span><span class="sxs-lookup"><span data-stu-id="73e41-103">Indexed Properties</span></span>

<span data-ttu-id="73e41-104">*인덱싱된 속성* 속성에 대 한 배열 유사 액세스를 제공 하는 데이터를 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-104">*Indexed properties* are properties that provide array-like access to ordered data.</span></span> <span data-ttu-id="73e41-105">이러한 세 가지 형태로 제공:</span><span class="sxs-lookup"><span data-stu-id="73e41-105">They come in three forms:</span></span>

* `Item`
* `Ordinal`
* `Cardinal`

<span data-ttu-id="73e41-106">F # 멤버에 대 한 배열 유사 액세스를 제공 합니다. 이러한 세 가지 이름 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-106">An F# member must be named one of these three names to provide array-like access.</span></span> <span data-ttu-id="73e41-107">`IndexerName` 아래 세 가지 옵션 중 하나를 나타내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-107">`IndexerName` is used to represent any of the three options below:</span></span>

## <a name="syntax"></a><span data-ttu-id="73e41-108">구문</span><span class="sxs-lookup"><span data-stu-id="73e41-108">Syntax</span></span>

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.IndexerName
    with get(index-variable) =
        get-function-body
    and set index-variablesvalue-variables =
        set-function-body

// Indexed property that has get only.
member self-identifier.IndexerName(index-variable) =
    get-function-body

// Alternative syntax for indexed property with get only
member self-identifier.IndexerName
    with get(index-variables) =
        get-function-body

// Indexed property that has set only.
member self-identifier.IndexerName
    with set index-variablesvalue-variables = 
        set-function-body
```

## <a name="remarks"></a><span data-ttu-id="73e41-109">설명</span><span class="sxs-lookup"><span data-stu-id="73e41-109">Remarks</span></span>

<span data-ttu-id="73e41-110">이전 구문 형식의 둘 다 있는 인덱싱된 속성을 정의 하는 방법을 보여 줍니다는 `get` 및 `set` 메서드를가 `get` 메서드만 있거나는 `set` 방법 으로만 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-110">The forms of the previous syntax show how to define indexed properties that have both a `get` and a `set` method, have a `get` method only, or have a `set` method only.</span></span> <span data-ttu-id="73e41-111">또한만 get 및 set만 나와 있는 구문에 대 한 표시 된 구문은 모두 결합 하 고 get 및 set를 둘 다 있는 속성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-111">You can also combine both the syntax shown for get only and the syntax shown for set only, and produce a property that has both get and set.</span></span> <span data-ttu-id="73e41-112">이 두 번째 형식은 get에 다른 액세스 가능성 한정자 및 특성을 배치 하 고 방법을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-112">This latter form allows you to put different accessibility modifiers and attributes on the get and set methods.</span></span>

<span data-ttu-id="73e41-113">경우는 *IndexerName* 는 `Item`, 컴파일러는 인덱싱된 기본 속성으로 속성을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-113">When the *IndexerName* is `Item`, the compiler treats the property as a default indexed property.</span></span> <span data-ttu-id="73e41-114">A *인덱싱된 기본 속성* 개체 인스턴스에서 배열 유사 구문을 사용 하 여 액세스할 수 있는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-114">A *default indexed property* is a property that you can access by using array-like syntax on the object instance.</span></span> <span data-ttu-id="73e41-115">예를 들어 경우 `obj` 구문은이 속성을 정의 하는 형식의 개체인 `obj.[index]` 속성에 액세스 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-115">For example, if `obj` is an object of the type that defines this property, the syntax `obj.[index]` is used to access the property.</span></span>

<span data-ttu-id="73e41-116">인덱싱된 속성은 속성 및 괄호로 인덱스의 이름을 지정 하는 기본이 아닌 액세스에 대 한 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-116">The syntax for accessing a nondefault indexed property is to provide the name of the property and the index in parentheses.</span></span> <span data-ttu-id="73e41-117">예를 들어 속성이 `Ordinal`에 작성 `obj.Ordinal(index)` 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-117">For example, if the property is `Ordinal`, you write `obj.Ordinal(index)` to access it.</span></span>

<span data-ttu-id="73e41-118">사용 하는 폼에 관계 없이 항상 커리 된 폼을를 사용 해야는 `set` 인덱싱된 속성에는 메서드.</span><span class="sxs-lookup"><span data-stu-id="73e41-118">Regardless of which form you use, you should always use the curried form for the `set` method on an indexed property.</span></span> <span data-ttu-id="73e41-119">커리 된 함수에 대 한 자세한 내용은 [함수](../functions/index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-119">For information about curried functions, see [Functions](../functions/index.md).</span></span>

## <a name="example"></a><span data-ttu-id="73e41-120">예제</span><span class="sxs-lookup"><span data-stu-id="73e41-120">Example</span></span>

<span data-ttu-id="73e41-121">다음 코드 예제에서는 정 및 기본 및 get 및 set 메서드는 기본이 아닌 인덱싱된 속성의 사용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-121">The following code example illustrates the definition and use of default and non-default indexed properties that have get and set methods.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a><span data-ttu-id="73e41-122">출력</span><span class="sxs-lookup"><span data-stu-id="73e41-122">Output</span></span>

```
ONE two three four five six seven eight nine ten
ONE first two second three third four fourth five fifth six 6th
seven seventh eight eighth nine ninth ten tenth
```

## <a name="indexed-properties-with-multiple-index-variables"></a><span data-ttu-id="73e41-123">여러 인덱스 변수를 사용 하 여 인덱싱된 속성</span><span class="sxs-lookup"><span data-stu-id="73e41-123">Indexed Properties with Multiple Index Variables</span></span>

<span data-ttu-id="73e41-124">인덱싱된 속성 둘 이상의 인덱스 변수를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-124">Indexed properties can have more than one index variable.</span></span> <span data-ttu-id="73e41-125">이 경우 변수 속성을 사용 하는 경우 쉼표로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-125">In that case, the variables are separated by commas when the property is used.</span></span> <span data-ttu-id="73e41-126">이러한 속성의 set 메서드에 두 개의 커리 된 인수는 첫 번째 키가 포함 된 튜플을 이며 두 번째는 설정 된 값에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-126">The set method in such a property must have two curried arguments, the first of which is a tuple containing the keys, and the second of which is the value being set.</span></span>

<span data-ttu-id="73e41-127">다음 코드는 여러 인덱스 변수를 사용 하 여 인덱싱된 속성의 사용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73e41-127">The following code demonstrates the use of an indexed property with multiple index variables.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3302.fs)]

## <a name="see-also"></a><span data-ttu-id="73e41-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="73e41-128">See also</span></span>

- [<span data-ttu-id="73e41-129">멤버</span><span class="sxs-lookup"><span data-stu-id="73e41-129">Members</span></span>](index.md)
