---
title: '&#39;#ElseIf&#39; 일치 하는 뒤에 야 &#39;#If&#39; 또는 &#39;#ElseIf&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 1e63595ee573e9356f6870a02b2131897c725baf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505785"
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a><span data-ttu-id="ff92d-102">&#39;#ElseIf&#39; 일치 하는 뒤에 야 &#39;#If&#39; 또는 &#39;#ElseIf&#39;</span><span class="sxs-lookup"><span data-stu-id="ff92d-102">&#39;#ElseIf&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;</span></span>
<span data-ttu-id="ff92d-103">`#ElseIf` 는 조건부 컴파일 지시문입니다.</span><span class="sxs-lookup"><span data-stu-id="ff92d-103">`#ElseIf` is a conditional compilation directive.</span></span> <span data-ttu-id="ff92d-104">`#ElseIf` 일치 하는 절을 야 `#If` 또는 `#ElseIf` 절.</span><span class="sxs-lookup"><span data-stu-id="ff92d-104">An `#ElseIf` clause must be preceded by a matching `#If` or `#ElseIf` clause.</span></span>  
  
 <span data-ttu-id="ff92d-105">**오류 ID:** BC30014</span><span class="sxs-lookup"><span data-stu-id="ff92d-105">**Error ID:** BC30014</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ff92d-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="ff92d-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="ff92d-107">확인 앞 `#If` 또는 `#ElseIf` 이에서 분리 없습니다 `#ElseIf` 간섭 조건부 컴파일 블록 또는 잘못 배치 된 `#End If`합니다.</span><span class="sxs-lookup"><span data-stu-id="ff92d-107">Check that a preceding `#If` or `#ElseIf` has not been separated from this `#ElseIf` by an intervening conditional compilation block or an incorrectly placed `#End If`.</span></span>  
  
2.  <span data-ttu-id="ff92d-108">경우는 `#ElseIf` 앞에 `#Else` 지시문을 제거 하거나를 `#Else` 로 변경 하거나는 `#ElseIf`합니다.</span><span class="sxs-lookup"><span data-stu-id="ff92d-108">If the `#ElseIf` is preceded by a `#Else` directive, either remove the `#Else` or change it to an `#ElseIf`.</span></span>  
  
3.  <span data-ttu-id="ff92d-109">다른 모든 항목의 순서가 올바른 경우 `#If` 지시문을 조건부 컴파일 블록의 시작 부분에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ff92d-109">If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff92d-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="ff92d-110">See also</span></span>
- [<span data-ttu-id="ff92d-111">#If...Then...#Else 지시문</span><span class="sxs-lookup"><span data-stu-id="ff92d-111">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
