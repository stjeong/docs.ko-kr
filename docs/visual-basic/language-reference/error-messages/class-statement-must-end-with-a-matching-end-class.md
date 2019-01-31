---
title: "'Class' 문은 짝이 되는 'End Class'로 끝나야 합니다."
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 572e1d74810aad6d24e6eefc8d37729f5dc950c9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286951"
---
# <a name="class-statement-must-end-with-a-matching-end-class"></a><span data-ttu-id="50515-102">'Class' 문은 짝이 되는 'End Class'로 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50515-102">'Class' statement must end with a matching 'End Class'</span></span>
<span data-ttu-id="50515-103">`Class` 시작 하는 데 사용 되는 `Class` ; 되므로 일치 하는 블록의 시작 부분에만 사용할 수 있습니다 `End Class` 문 블록을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="50515-103">`Class` is used to initiate a `Class` block; hence it can only appear at the beginning of the block, with a matching `End Class` statement ending the block.</span></span> <span data-ttu-id="50515-104">중복 된 `Class` 문이 종료 하지 하 `Class` 블록 `End Class`합니다.</span><span class="sxs-lookup"><span data-stu-id="50515-104">Either you have a redundant `Class` statement, or you have not ended your `Class` block with `End Class`.</span></span>  
  
 <span data-ttu-id="50515-105">**오류 ID:** BC30481</span><span class="sxs-lookup"><span data-stu-id="50515-105">**Error ID:** BC30481</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="50515-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="50515-106">To correct this error</span></span>  
  
-   <span data-ttu-id="50515-107">불필요한 `Class` 문을 찾아서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50515-107">Locate and remove the unnecessary `Class` statement.</span></span>  
  
-   <span data-ttu-id="50515-108">종료 합니다 `Class` 일치 하는 블록 `End Class`합니다.</span><span class="sxs-lookup"><span data-stu-id="50515-108">Conclude the `Class` block with a matching `End Class`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50515-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="50515-109">See also</span></span>
- [<span data-ttu-id="50515-110">최종 \<키워드 > 문</span><span class="sxs-lookup"><span data-stu-id="50515-110">End \<keyword> Statement</span></span>](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [<span data-ttu-id="50515-111">Class 문</span><span class="sxs-lookup"><span data-stu-id="50515-111">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
