---
title: '&#39;클래스&#39; 문은 일치 하는 끝나야 합니다. &#39;End 클래스&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 4e80ce58048bfa7f2fecc65e7167479df07bf57c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715090"
---
# <a name="39class39-statement-must-end-with-a-matching-39end-class39"></a><span data-ttu-id="047e2-102">&#39;클래스&#39; 문은 일치 하는 끝나야 합니다. &#39;End 클래스&#39;</span><span class="sxs-lookup"><span data-stu-id="047e2-102">&#39;Class&#39; statement must end with a matching &#39;End Class&#39;</span></span>
<span data-ttu-id="047e2-103">`Class` 시작 하는 데 사용 되는 `Class` ; 되므로 일치 하는 블록의 시작 부분에만 사용할 수 있습니다 `End Class` 문 블록을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="047e2-103">`Class` is used to initiate a `Class` block; hence it can only appear at the beginning of the block, with a matching `End Class` statement ending the block.</span></span> <span data-ttu-id="047e2-104">중복 된 `Class` 문이 종료 하지 하 `Class` 블록 `End Class`합니다.</span><span class="sxs-lookup"><span data-stu-id="047e2-104">Either you have a redundant `Class` statement, or you have not ended your `Class` block with `End Class`.</span></span>  
  
 <span data-ttu-id="047e2-105">**오류 ID:** BC30481</span><span class="sxs-lookup"><span data-stu-id="047e2-105">**Error ID:** BC30481</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="047e2-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="047e2-106">To correct this error</span></span>  
  
-   <span data-ttu-id="047e2-107">불필요한 `Class` 문을 찾아서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="047e2-107">Locate and remove the unnecessary `Class` statement.</span></span>  
  
-   <span data-ttu-id="047e2-108">종료 합니다 `Class` 일치 하는 블록 `End Class`합니다.</span><span class="sxs-lookup"><span data-stu-id="047e2-108">Conclude the `Class` block with a matching `End Class`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="047e2-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="047e2-109">See also</span></span>
- [<span data-ttu-id="047e2-110">최종 \<키워드 > 문</span><span class="sxs-lookup"><span data-stu-id="047e2-110">End \<keyword> Statement</span></span>](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [<span data-ttu-id="047e2-111">Class 문</span><span class="sxs-lookup"><span data-stu-id="047e2-111">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
