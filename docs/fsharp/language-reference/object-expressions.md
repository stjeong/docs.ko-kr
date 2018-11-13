---
title: 개체 식(F#)
description: 명명 된 형식을 추가 코드와 새로 만드는 데 필요한 오버 헤드를 방지 하려는 경우 F# 식 개체를 사용 하는 방법에 알아봅니다.
ms.date: 05/16/2016
ms.openlocfilehash: 1a971044d680d3bf5a6fff38affdaf001d5403b4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43865464"
---
# <a name="object-expressions"></a><span data-ttu-id="8fd44-103">개체 식</span><span class="sxs-lookup"><span data-stu-id="8fd44-103">Object Expressions</span></span>

<span data-ttu-id="8fd44-104">*식을 개체* 동적으로 생성 하는 익명 개체 형식의 새 인스턴스를 만드는 식입니다 되는 기존의 기본 형식, 인터페이스 또는 인터페이스의 집합 기반 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-104">An *object expression* is an expression that creates a new instance of a dynamically created, anonymous object type that is based on an existing base type, interface, or set of interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd44-105">구문</span><span class="sxs-lookup"><span data-stu-id="8fd44-105">Syntax</span></span>

```fsharp
// When typename is a class:
{ new typename [type-params]arguments with
    member-definitions
    [ additional-interface-definitions ]
}
// When typename is not a class:
{ new typename [generic-type-args] with
    member-definitions
    [ additional-interface-definitions ]
}
```

## <a name="remarks"></a><span data-ttu-id="8fd44-106">설명</span><span class="sxs-lookup"><span data-stu-id="8fd44-106">Remarks</span></span>

<span data-ttu-id="8fd44-107">위 구문에는 *typename* 은 기존 클래스 유형 또는 인터페이스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-107">In the previous syntax, the *typename* represents an existing class type or interface type.</span></span> <span data-ttu-id="8fd44-108">*형식-params* 선택적 제네릭 형식 매개 변수를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-108">*type-params* describes the optional generic type parameters.</span></span> <span data-ttu-id="8fd44-109">합니다 *인수* 생성자 매개 변수를 필요로 하는 클래스 형식에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-109">The *arguments* are used only for class types, which require constructor parameters.</span></span> <span data-ttu-id="8fd44-110">합니다 *멤버 정의* 기본 클래스 또는 인터페이스에서 추상 메서드의 구현 또는 기본 클래스 메서드를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-110">The *member-definitions* are overrides of base class methods, or implementations of abstract methods from either a base class or an interface.</span></span>

<span data-ttu-id="8fd44-111">다음 예제에서는 여러 다른 유형의 개체 식 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-111">The following example illustrates several different types of object expressions.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4301.fs)]

## <a name="using-object-expressions"></a><span data-ttu-id="8fd44-112">개체 식 사용</span><span class="sxs-lookup"><span data-stu-id="8fd44-112">Using Object Expressions</span></span>

<span data-ttu-id="8fd44-113">추가 코드와 명명 된 형식을 새로 만드는 데 필요한는 오버 헤드를 방지 하려면 개체 식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-113">You use object expressions when you want to avoid the extra code and overhead that is required to create a new, named type.</span></span> <span data-ttu-id="8fd44-114">개체 식을 사용 하 여 프로그램에서 생성 하는 형식의 수를 최소화 하는 경우 코드 줄의 수를 줄일 수 있으며 형식의 불필요 한 확산을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-114">If you use object expressions to minimize the number of types created in a program, you can reduce the number of lines of code and prevent the unnecessary proliferation of types.</span></span> <span data-ttu-id="8fd44-115">다양 한 형식을 특정 상황을 처리할 수만 만드는 대신 기존 형식을 사용자 지정 하거나 특정 사례에 대 한 인터페이스의 적절 한 구현을 제공 하는 개체 식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fd44-115">Instead of creating many types just to handle specific situations, you can use an object expression that customizes an existing type or provides an appropriate implementation of an interface for the specific case at hand.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fd44-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="8fd44-116">See also</span></span>

- [<span data-ttu-id="8fd44-117">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="8fd44-117">F# Language Reference</span></span>](index.md)
