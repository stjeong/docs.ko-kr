---
title: 람다 식의 첫 번째 식에서는 사용할 수 없습니다는 &#39;Select Case&#39; 문
ms.date: 07/20/2015
f1_keywords:
- bc36635
- vbc36635
helpviewer_keywords:
- BC36635
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
ms.openlocfilehash: afefa821f9695dbbfe2a96aee5afd3171ae5b1db
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700223"
---
# <a name="lambda-expressions-are-not-valid-in-the-first-expression-of-a-39select-case39-statement"></a><span data-ttu-id="61e1d-102">람다 식의 첫 번째 식에서는 사용할 수 없습니다는 &#39;Select Case&#39; 문</span><span class="sxs-lookup"><span data-stu-id="61e1d-102">Lambda expressions are not valid in the first expression of a &#39;Select Case&#39; statement</span></span>
<span data-ttu-id="61e1d-103">테스트 식에 람다 식을 사용할 수 없습니다는 `Select Case` 문입니다.</span><span class="sxs-lookup"><span data-stu-id="61e1d-103">You cannot use a lambda expression for the test expression in a `Select Case` statement.</span></span> <span data-ttu-id="61e1d-104">람다 식 정의는 함수를 테스트 식의 반환을 `Select Case` 문은 기본 데이터 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="61e1d-104">Lambda expression definitions return functions, and the test expression of a `Select Case` statement must be an elementary data type.</span></span>  
  
 <span data-ttu-id="61e1d-105">다음 코드는이 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="61e1d-105">The following code causes this error:</span></span>  
  
```vb  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 <span data-ttu-id="61e1d-106">**오류 ID:** BC36635</span><span class="sxs-lookup"><span data-stu-id="61e1d-106">**Error ID:** BC36635</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="61e1d-107">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="61e1d-107">To correct this error</span></span>  
  
-   <span data-ttu-id="61e1d-108">코드를 검사하여 `If...Then...Else` 문과 같은 다른 조건부 생성이 적합한지 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="61e1d-108">Examine your code to determine whether a different conditional construction, such as an `If...Then...Else` statement, would work for you.</span></span>  
  
-   <span data-ttu-id="61e1d-109">계획 했던 함수를 호출 하려면 다음 코드 에서처럼:</span><span class="sxs-lookup"><span data-stu-id="61e1d-109">You may have intended to call the function, as shown in the following code:</span></span>  
  
```vb  
Dim num? As Integer  
Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
    ' List of the cases  
End Select  
```  
  
## <a name="see-also"></a><span data-ttu-id="61e1d-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="61e1d-110">See also</span></span>
- [<span data-ttu-id="61e1d-111">람다 식</span><span class="sxs-lookup"><span data-stu-id="61e1d-111">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="61e1d-112">If...Then...Else 문</span><span class="sxs-lookup"><span data-stu-id="61e1d-112">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [<span data-ttu-id="61e1d-113">Select...Case 문</span><span class="sxs-lookup"><span data-stu-id="61e1d-113">Select...Case Statement</span></span>](../../../visual-basic/language-reference/statements/select-case-statement.md)
