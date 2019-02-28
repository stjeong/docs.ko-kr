---
title: Is 연산자(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.is
helpviewer_keywords:
- comparison operators [Visual Basic]
- equivalent objects
- TypeOf...Is expression
- Is operator [Visual Basic]
ms.assetid: 8045a6c8-2a83-45b6-ad47-d09a704c656d
ms.openlocfilehash: c4b23bb2d81d1f5272a5813123681da7406c3368
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56980344"
---
# <a name="is-operator-visual-basic"></a><span data-ttu-id="ad4c2-102">Is 연산자(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ad4c2-102">Is Operator (Visual Basic)</span></span>
<span data-ttu-id="ad4c2-103">두 개체 참조 변수를 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-103">Compares two object reference variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad4c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad4c2-104">Syntax</span></span>  
  
```  
result = object1 Is object2  
```  
  
## <a name="parts"></a><span data-ttu-id="ad4c2-105">요소</span><span class="sxs-lookup"><span data-stu-id="ad4c2-105">Parts</span></span>  
 `result`  
 <span data-ttu-id="ad4c2-106">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-106">Required.</span></span> <span data-ttu-id="ad4c2-107">모든 `Boolean` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-107">Any `Boolean` value.</span></span>  
  
 `object1`  
 <span data-ttu-id="ad4c2-108">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-108">Required.</span></span> <span data-ttu-id="ad4c2-109">모든 `Object` 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-109">Any `Object` name.</span></span>  
  
 `object2`  
 <span data-ttu-id="ad4c2-110">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-110">Required.</span></span> <span data-ttu-id="ad4c2-111">모든 `Object` 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-111">Any `Object` name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ad4c2-112">설명</span><span class="sxs-lookup"><span data-stu-id="ad4c2-112">Remarks</span></span>  
 <span data-ttu-id="ad4c2-113">`Is` 연산자 두 개체 참조가 동일한 개체를 참조 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-113">The `Is` operator determines if two object references refer to the same object.</span></span> <span data-ttu-id="ad4c2-114">그러나 값 비교를 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-114">However, it does not perform value comparisons.</span></span> <span data-ttu-id="ad4c2-115">경우 `object1` 하 고 `object2` 모두 정확히 같은 개체 인스턴스를 참조 `result` 됩니다 `True`가지고 있지 않은 경우 `result` 는 `False`합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-115">If `object1` and `object2` both refer to the exact same object instance, `result` is `True`; if they do not, `result` is `False`.</span></span>  
  
 <span data-ttu-id="ad4c2-116">`Is` 사용 하 여 사용할 수도 있습니다는 `TypeOf` 있도록 키워드는 `TypeOf`... `Is` 개체 변수 데이터 형식과 호환 되는지 테스트 하는 식입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-116">`Is` can also be used with the `TypeOf` keyword to make a `TypeOf`...`Is` expression, which tests whether an object variable is compatible with a data type.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ad4c2-117">합니다 `Is` 키워드에도 사용 되는 [선택... Case 문](../../../visual-basic/language-reference/statements/select-case-statement.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-117">The `Is` keyword is also used in the [Select...Case Statement](../../../visual-basic/language-reference/statements/select-case-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ad4c2-118">예제</span><span class="sxs-lookup"><span data-stu-id="ad4c2-118">Example</span></span>  
 <span data-ttu-id="ad4c2-119">다음 예제에서는 `Is` 개체 참조의 쌍을 비교 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-119">The following example uses the `Is` operator to compare pairs of object references.</span></span> <span data-ttu-id="ad4c2-120">결과에 할당 되는 `Boolean` 두 개체가 동일한 지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-120">The results are assigned to a `Boolean` value representing whether the two objects are identical.</span></span>  
  
 [!code-vb[VbVbalrOperators#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#27)]  
  
 <span data-ttu-id="ad4c2-121">위 예제에 사용할 수 있습니다는 `Is` 연산자 둘 다를 테스트 하려면 초기 바인딩 및 런타임에 바인딩된 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-121">As the preceding example demonstrates, you can use the `Is` operator to test both early bound and late bound objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad4c2-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="ad4c2-122">See also</span></span>
- [<span data-ttu-id="ad4c2-123">TypeOf 연산자</span><span class="sxs-lookup"><span data-stu-id="ad4c2-123">TypeOf Operator</span></span>](../../../visual-basic/language-reference/operators/typeof-operator.md)
- [<span data-ttu-id="ad4c2-124">IsNot 연산자</span><span class="sxs-lookup"><span data-stu-id="ad4c2-124">IsNot Operator</span></span>](../../../visual-basic/language-reference/operators/isnot-operator.md)
- [<span data-ttu-id="ad4c2-125">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ad4c2-125">Comparison Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [<span data-ttu-id="ad4c2-126">Visual Basic에서의 연산자 우선 순위</span><span class="sxs-lookup"><span data-stu-id="ad4c2-126">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="ad4c2-127">기능별 연산자 목록</span><span class="sxs-lookup"><span data-stu-id="ad4c2-127">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="ad4c2-128">연산자 및 식</span><span class="sxs-lookup"><span data-stu-id="ad4c2-128">Operators and Expressions</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
