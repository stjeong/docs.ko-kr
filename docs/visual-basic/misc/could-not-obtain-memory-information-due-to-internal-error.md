---
title: 내부 오류 때문에 메모리 정보를 가져올 수 없습니다.
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_Memory
ms.assetid: 1ba8f774-5858-438e-914e-99fddc9e5e7e
ms.openlocfilehash: 2f1c60ce017173f79665fb2b68e9c355f1c5d167
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595879"
---
# <a name="could-not-obtain-memory-information-due-to-internal-error"></a><span data-ttu-id="a4975-102">내부 오류 때문에 메모리 정보를 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4975-102">Could not obtain memory information due to internal error</span></span>
<span data-ttu-id="a4975-103">`My.Computer.Info` 개체의 메모리 정보 속성 중 하나에 대한 호출이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="a4975-103">A call to one of the memory-information properties of the `My.Computer.Info` object failed.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a4975-104">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="a4975-104">To correct this error</span></span>  
  
-   <span data-ttu-id="a4975-105">`Try...Catch` 개체의 메모리 정보 속성에 대한 호출 주위에 `My.Computer.Info` 블록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a4975-105">Add a `Try...Catch` block around the call to the memory-information property of the `My.Computer.Info` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4975-106">참고자료</span><span class="sxs-lookup"><span data-stu-id="a4975-106">See also</span></span>
- [<span data-ttu-id="a4975-107">My.Computer.Info</span><span class="sxs-lookup"><span data-stu-id="a4975-107">My.Computer.Info</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo)
- [<span data-ttu-id="a4975-108">Try...Catch...Finally 문</span><span class="sxs-lookup"><span data-stu-id="a4975-108">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
