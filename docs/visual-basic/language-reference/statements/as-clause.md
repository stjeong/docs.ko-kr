---
title: As 절(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.as
helpviewer_keywords:
- constraints, Visual Basic generic types
- As keyword [Visual Basic], statement syntax
- As keyword [Visual Basic]
ms.assetid: b4281ec8-2be5-49f7-aae8-ae0a96265b0d
ms.openlocfilehash: 893df117ce6ead444ef1da262782cc271102f4d7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672268"
---
# <a name="as-clause-visual-basic"></a><span data-ttu-id="6a460-102">As 절(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6a460-102">As Clause (Visual Basic)</span></span>
<span data-ttu-id="6a460-103">소개는 `As` 선언문 또는 제네릭 형식 매개 변수의 제약 조건 목록에서 데이터 형식을 식별 하는 절.</span><span class="sxs-lookup"><span data-stu-id="6a460-103">Introduces an `As` clause, which identifies a data type in a declaration statement or a constraint list on a generic type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6a460-104">설명</span><span class="sxs-lookup"><span data-stu-id="6a460-104">Remarks</span></span>  
 <span data-ttu-id="6a460-105">`As` 키워드는 다음 컨텍스트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a460-105">The `As` keyword can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="6a460-106">Aggregate 절</span><span class="sxs-lookup"><span data-stu-id="6a460-106">Aggregate Clause</span></span>](../../../visual-basic/language-reference/queries/aggregate-clause.md)  
  
 [<span data-ttu-id="6a460-107">Class 문</span><span class="sxs-lookup"><span data-stu-id="6a460-107">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [<span data-ttu-id="6a460-108">Const 문</span><span class="sxs-lookup"><span data-stu-id="6a460-108">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [<span data-ttu-id="6a460-109">Declare 문</span><span class="sxs-lookup"><span data-stu-id="6a460-109">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="6a460-110">Delegate 문</span><span class="sxs-lookup"><span data-stu-id="6a460-110">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [<span data-ttu-id="6a460-111">Dim 문</span><span class="sxs-lookup"><span data-stu-id="6a460-111">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [<span data-ttu-id="6a460-112">Enum 문</span><span class="sxs-lookup"><span data-stu-id="6a460-112">Enum Statement</span></span>](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [<span data-ttu-id="6a460-113">Event 문</span><span class="sxs-lookup"><span data-stu-id="6a460-113">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [<span data-ttu-id="6a460-114">...에 대 한 다음 문</span><span class="sxs-lookup"><span data-stu-id="6a460-114">For...Next Statements</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)  
  
 [<span data-ttu-id="6a460-115">각각에 대 한 중... 다음 문</span><span class="sxs-lookup"><span data-stu-id="6a460-115">For Each...Next Statements</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)  
  
 [<span data-ttu-id="6a460-116">From 절</span><span class="sxs-lookup"><span data-stu-id="6a460-116">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
  
 [<span data-ttu-id="6a460-117">Function 문</span><span class="sxs-lookup"><span data-stu-id="6a460-117">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="6a460-118">Group Join 절</span><span class="sxs-lookup"><span data-stu-id="6a460-118">Group Join Clause</span></span>](../../../visual-basic/language-reference/queries/group-join-clause.md)  
  
 [<span data-ttu-id="6a460-119">Interface 문</span><span class="sxs-lookup"><span data-stu-id="6a460-119">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [<span data-ttu-id="6a460-120">Operator 문</span><span class="sxs-lookup"><span data-stu-id="6a460-120">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [<span data-ttu-id="6a460-121">Property 문</span><span class="sxs-lookup"><span data-stu-id="6a460-121">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="6a460-122">Structure 문</span><span class="sxs-lookup"><span data-stu-id="6a460-122">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [<span data-ttu-id="6a460-123">Sub 문</span><span class="sxs-lookup"><span data-stu-id="6a460-123">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
 [<span data-ttu-id="6a460-124">시도 중... Catch 하는 중... Finally 문</span><span class="sxs-lookup"><span data-stu-id="6a460-124">Try...Catch...Finally Statements</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="6a460-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="6a460-125">See also</span></span>
- [<span data-ttu-id="6a460-126">방법: 새 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="6a460-126">How to: Create a New Variable</span></span>](../../../visual-basic/programming-guide/language-features/variables/how-to-create-a-new-variable.md)
- [<span data-ttu-id="6a460-127">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6a460-127">Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="6a460-128">변수 선언</span><span class="sxs-lookup"><span data-stu-id="6a460-128">Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="6a460-129">형식 목록</span><span class="sxs-lookup"><span data-stu-id="6a460-129">Type List</span></span>](../../../visual-basic/language-reference/statements/type-list.md)
- [<span data-ttu-id="6a460-130">Visual Basic의 제네릭 형식</span><span class="sxs-lookup"><span data-stu-id="6a460-130">Generic Types in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="6a460-131">키워드</span><span class="sxs-lookup"><span data-stu-id="6a460-131">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
