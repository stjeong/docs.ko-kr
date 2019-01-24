---
title: '&#39;&lt;eventname&gt; &#39; 은 (는) 이벤트 및 직접 호출할 수 없습니다.'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 3efd8c18497ce288e16659db4ca4693d5a3e6acc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54581998"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="f3218-102">&#39;&lt;eventname&gt; &#39; 은 (는) 이벤트 및 직접 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-102">&#39;&lt;eventname&gt;&#39; is an event, and cannot be called directly</span></span>
<span data-ttu-id="f3218-103">' <`eventname`>'은 (는) 이벤트 및 이므로 직접 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-103">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="f3218-104">사용 된 `RaiseEvent` 이벤트를 발생 시키는 문입니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-104">Use a `RaiseEvent` statement to raise an event.</span></span>  
  
 <span data-ttu-id="f3218-105">프로시저 호출이 프로시저 이름에 대 한 이벤트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-105">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="f3218-106">이벤트 처리기 프로시저 되었지만 이벤트 자체는 일종의 신호 발생 하 고 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-106">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>  
  
 <span data-ttu-id="f3218-107">**오류 ID:** BC32022</span><span class="sxs-lookup"><span data-stu-id="f3218-107">**Error ID:** BC32022</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f3218-108">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="f3218-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="f3218-109">사용 하 여를 `RaiseEvent` 문을 이벤트 신호를 보내고 처리 하는 프로시저를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-109">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3218-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="f3218-110">See also</span></span>
- [<span data-ttu-id="f3218-111">RaiseEvent 문</span><span class="sxs-lookup"><span data-stu-id="f3218-111">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
