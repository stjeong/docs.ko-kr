---
title: 파생 클래스는 기본 클래스 이벤트를 발생시킬 수 없습니다.
ms.date: 07/20/2015
f1_keywords:
- vbc30029
- bc30029
helpviewer_keywords:
- BC30029
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
ms.openlocfilehash: 3cb61a40e4522695b876d85f67dac1a109d3c3e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595866"
---
# <a name="derived-classes-cannot-raise-base-class-events"></a><span data-ttu-id="ca7b4-102">파생 클래스는 기본 클래스 이벤트를 발생시킬 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-102">Derived classes cannot raise base class events</span></span>
<span data-ttu-id="ca7b4-103">이벤트 선언 되는 선언 공간 에서만에서 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-103">An event can be raised only from the declaration space in which it is declared.</span></span> <span data-ttu-id="ca7b4-104">따라서 클래스 다른 클래스와 파생 된 하나에서 이벤트를 발생 시킬 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-104">Therefore, a class cannot raise events from any other class, even one from which it is derived.</span></span>  
  
 <span data-ttu-id="ca7b4-105">**오류 ID:** BC30029</span><span class="sxs-lookup"><span data-stu-id="ca7b4-105">**Error ID:** BC30029</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ca7b4-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="ca7b4-106">To correct this error</span></span>  
  
-   <span data-ttu-id="ca7b4-107">이동 합니다 `Event` 문 또는 `RaiseEvent` 문을 동일한 클래스에서.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-107">Move the `Event` statement or the `RaiseEvent` statement so they are in the same class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca7b4-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="ca7b4-108">See also</span></span>
- [<span data-ttu-id="ca7b4-109">Event 문</span><span class="sxs-lookup"><span data-stu-id="ca7b4-109">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="ca7b4-110">RaiseEvent 문</span><span class="sxs-lookup"><span data-stu-id="ca7b4-110">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
