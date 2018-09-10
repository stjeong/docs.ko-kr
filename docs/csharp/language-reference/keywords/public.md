---
title: public 키워드(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 84a3bc49b6eea047d518edc01dab7f2301854b6a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43484159"
---
# <a name="public-c-reference"></a><span data-ttu-id="33ca1-102">public(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="33ca1-102">public (C# Reference)</span></span>

<span data-ttu-id="33ca1-103">`public` 키워드는 형식 및 형식 멤버에 대한 액세스 한정자입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-103">The `public` keyword is an access modifier for types and type members.</span></span> <span data-ttu-id="33ca1-104">공용 액세스는 허용 범위가 가장 큰 액세스 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-104">Public access is the most permissive access level.</span></span> <span data-ttu-id="33ca1-105">다음 예제와 같이, 공용 멤버 액세스에 대한 제한은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-105">There are no restrictions on accessing public members, as in this example:</span></span>

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

<span data-ttu-id="33ca1-106">자세한 내용은 [액세스 한정자](../../programming-guide/classes-and-structs/access-modifiers.md) 및 [액세스 가능성 수준](accessibility-levels.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33ca1-106">See [Access Modifiers](../../programming-guide/classes-and-structs/access-modifiers.md) and [Accessibility Levels](accessibility-levels.md) for more information.</span></span>

## <a name="example"></a><span data-ttu-id="33ca1-107">예</span><span class="sxs-lookup"><span data-stu-id="33ca1-107">Example</span></span>

<span data-ttu-id="33ca1-108">다음 예제에서는 두 개의 클래스, `PointTest` 및 `MainClass`를 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-108">In the following example, two classes are declared, `PointTest` and `MainClass`.</span></span> <span data-ttu-id="33ca1-109">`PointTest`의 공용 멤버 `x` 및 `y`는 `MainClass`에서 직접 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-109">The public members `x` and `y` of `PointTest` are accessed directly from `MainClass`.</span></span>

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

<span data-ttu-id="33ca1-110">`public` 액세스 수준을 [private](private.md) 또는 [protected](protected.md)로 변경하면 오류 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-110">If you change the `public` access level to [private](private.md) or [protected](protected.md), you will get the error message:</span></span>

<span data-ttu-id="33ca1-111">보호 수준 때문에 'PointTest.y'에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33ca1-111">'PointTest.y' is inaccessible due to its protection level.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="33ca1-112">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="33ca1-112">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="33ca1-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="33ca1-113">See also</span></span>

- [<span data-ttu-id="33ca1-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="33ca1-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="33ca1-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="33ca1-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="33ca1-116">액세스 한정자</span><span class="sxs-lookup"><span data-stu-id="33ca1-116">Access Modifiers</span></span>](../../programming-guide/classes-and-structs/access-modifiers.md)
- [<span data-ttu-id="33ca1-117">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="33ca1-117">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="33ca1-118">액세스 한정자</span><span class="sxs-lookup"><span data-stu-id="33ca1-118">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="33ca1-119">액세스 수준</span><span class="sxs-lookup"><span data-stu-id="33ca1-119">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="33ca1-120">한정자</span><span class="sxs-lookup"><span data-stu-id="33ca1-120">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="33ca1-121">private</span><span class="sxs-lookup"><span data-stu-id="33ca1-121">private</span></span>](private.md)
- [<span data-ttu-id="33ca1-122">protected</span><span class="sxs-lookup"><span data-stu-id="33ca1-122">protected</span></span>](protected.md)
- [<span data-ttu-id="33ca1-123">internal</span><span class="sxs-lookup"><span data-stu-id="33ca1-123">internal</span></span>](internal.md)