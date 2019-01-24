---
title: '&#39;&#39; 의 피연산자는 참조 형식에 없지만이 피연산자의 값 형식은 &#39; &lt;typename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: 0b3f80e98087e455ec730dea8c57478528e9259c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722922"
---
# <a name="39is39-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-39lttypenamegt39"></a><span data-ttu-id="257bd-102">&#39;&#39; 의 피연산자는 참조 형식에 없지만이 피연산자의 값 형식은 &#39; &lt;typename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="257bd-102">&#39;Is&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;</span></span>
<span data-ttu-id="257bd-103">`Is` 비교 연산자는 두 개의 개체 변수가 같은 인스턴스를 참조 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="257bd-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="257bd-104">이 비교 값 형식에 대해 정의 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="257bd-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="257bd-105">**오류 ID:** BC30020</span><span class="sxs-lookup"><span data-stu-id="257bd-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="257bd-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="257bd-106">To correct this error</span></span>  
  
-   <span data-ttu-id="257bd-107">적절 한 산술 비교 연산자를 사용 하 여 또는 `Like` 두 개의 값 형식을 비교 하는 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="257bd-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="257bd-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="257bd-108">See also</span></span>
- [<span data-ttu-id="257bd-109">Is 연산자</span><span class="sxs-lookup"><span data-stu-id="257bd-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="257bd-110">Like 연산자</span><span class="sxs-lookup"><span data-stu-id="257bd-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="257bd-111">비교 연산자</span><span class="sxs-lookup"><span data-stu-id="257bd-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
