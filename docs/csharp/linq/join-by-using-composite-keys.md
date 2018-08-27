---
title: 복합 키를 사용하여 조인(C#의 LINQ)
description: LINQ에서 복합 키를 사용하여 조인하는 방법을 알아봅니다.
ms.date: 12/1/2016
ms.assetid: da70b54d-3213-45eb-8437-fbe75cbcf935
ms.openlocfilehash: ae37d03f996f0b0cc184a86663f16d62e6c29c69
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932336"
---
# <a name="join-by-using-composite-keys"></a><span data-ttu-id="79336-103">복합 키를 사용하여 조인</span><span class="sxs-lookup"><span data-stu-id="79336-103">Join by using composite keys</span></span>

<span data-ttu-id="79336-104">이 예제에서는 둘 이상의 키를 사용하여 일치를 정의하려는 조인 작업을 수행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79336-104">This example shows how to perform join operations in which you want to use more than one key to define a match.</span></span> <span data-ttu-id="79336-105">이 작업은 복합 키를 사용하여 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="79336-105">This is accomplished by using a composite key.</span></span> <span data-ttu-id="79336-106">무명 형식이나 비교할 값이 포함된 명명된 형식으로 복합 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79336-106">You create a composite key as an anonymous type or named typed with the values that you want to compare.</span></span> <span data-ttu-id="79336-107">쿼리 변수가 메서드 경계를 넘어 전달되는 경우 키의 <xref:System.Object.Equals%2A> 및 <xref:System.Object.GetHashCode%2A>를 재정의하는 명명된 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="79336-107">If the query variable will be passed across method boundaries, use a named type that overrides <xref:System.Object.Equals%2A> and <xref:System.Object.GetHashCode%2A> for the key.</span></span> <span data-ttu-id="79336-108">속성의 이름과 속성이 나타나는 순서는 각 키에서 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79336-108">The names of the properties, and the order in which they occur, must be identical in each key.</span></span>

## <a name="example"></a><span data-ttu-id="79336-109">예</span><span class="sxs-lookup"><span data-stu-id="79336-109">Example</span></span>

<span data-ttu-id="79336-110">다음 예제에서는 복합 키를 사용하여 세 테이블의 데이터를 조인하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79336-110">The following example demonstrates how to use a composite key to join data from three tables:</span></span>

```csharp
var query = from o in db.Orders
    from p in db.Products
    join d in db.OrderDetails
        on new {o.OrderID, p.ProductID} equals new {d.OrderID, d.ProductID} into details
        from d in details
        select new {o.OrderID, p.ProductID, d.UnitPrice};
```

<span data-ttu-id="79336-111">복합 키에 대한 형식 유추는 키에 있는 속성의 이름 및 속성이 나타나는 순서에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="79336-111">Type inference on composite keys depends on the names of the properties in the keys, and the order in which they occur.</span></span> <span data-ttu-id="79336-112">소스 시퀀스에 있는 속성에 동일한 이름이 없는 경우 키에서 새 이름을 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79336-112">If the properties in the source sequences don't have the same names, you must assign new names in the keys.</span></span> <span data-ttu-id="79336-113">예를 들어 `Orders` 테이블과 `OrderDetails` 테이블이 각각 해당 열에 다른 이름을 사용한 경우 무명 형식에서 동일한 이름을 지정하여 복합 키를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79336-113">For example, if the `Orders` table and `OrderDetails` table each used different names for their columns, you could create composite keys by assigning identical names in the anonymous types:</span></span>

```csharp
join...on new {Name = o.CustomerName, ID = o.CustID} equals
    new {Name = d.CustName, ID = d.CustID }
```

<span data-ttu-id="79336-114">복합 키는 `group` 절에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79336-114">Composite keys can be also used in a `group` clause.</span></span>

## <a name="see-also"></a><span data-ttu-id="79336-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="79336-115">See also</span></span>

- [<span data-ttu-id="79336-116">LINQ(Language-Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="79336-116">Language Integrated Query (LINQ)</span></span>](index.md)  
- [<span data-ttu-id="79336-117">join 절</span><span class="sxs-lookup"><span data-stu-id="79336-117">join clause</span></span>](../language-reference/keywords/join-clause.md)  
- [<span data-ttu-id="79336-118">group 절</span><span class="sxs-lookup"><span data-stu-id="79336-118">group clause</span></span>](../language-reference/keywords/group-clause.md)  