---
title: WithEvents(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.WithEvents
- WithEvents
helpviewer_keywords:
- WithEvents keyword [Visual Basic]
ms.assetid: 19d461f5-d72f-4de9-8c1d-0a6650316990
ms.openlocfilehash: e1a6cecdf724603b8f4617fe4e8b5ef2c0acdeff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624563"
---
# <a name="withevents-visual-basic"></a><span data-ttu-id="f1ec9-102">WithEvents(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f1ec9-102">WithEvents (Visual Basic)</span></span>
<span data-ttu-id="f1ec9-103">하나 이상의 선언 된 멤버 변수가 이벤트를 발생 시킬 수 있는 클래스의 인스턴스 참조 하는지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-103">Specifies that one or more declared member variables refer to an instance of a class that can raise events.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f1ec9-104">설명</span><span class="sxs-lookup"><span data-stu-id="f1ec9-104">Remarks</span></span>  
 <span data-ttu-id="f1ec9-105">변수를 사용 하 여 정의 되 면 `WithEvents`에 메서드를 사용 하 여 변수의 이벤트를 처리 하는 선언적으로 지정할 수 있습니다는 `Handles` 키워드입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-105">When a variable is defined using `WithEvents`, you can declaratively specify that a method handles the variable's events using the `Handles` keyword.</span></span>  
  
 <span data-ttu-id="f1ec9-106">사용할 수 있습니다 `WithEvents` 클래스 또는 모듈 수준 에서만.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-106">You can use `WithEvents` only at class or module level.</span></span> <span data-ttu-id="f1ec9-107">즉, 선언 컨텍스트는 `WithEvents` 변수 클래스 또는 모듈 이어야 하며 원본 파일, 네임 스페이스, 구조체 또는 프로시저 일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-107">This means the declaration context for a `WithEvents` variable must be a class or module and cannot be a source file, namespace, structure, or procedure.</span></span>  
  
 <span data-ttu-id="f1ec9-108">사용할 수 없습니다 `WithEvents` 구조체 멤버입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-108">You cannot use `WithEvents` on a structure member.</span></span>  
  
 <span data-ttu-id="f1ec9-109">개별 변수만 선언할 수 있습니다-하지 배열-사용 하 여 `WithEvents`입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-109">You can declare only individual variables—not arrays—with `WithEvents`.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="f1ec9-110">규칙</span><span class="sxs-lookup"><span data-stu-id="f1ec9-110">Rules</span></span>  
  
-   <span data-ttu-id="f1ec9-111">**요소 형식입니다.**</span><span class="sxs-lookup"><span data-stu-id="f1ec9-111">**Element Types.**</span></span> <span data-ttu-id="f1ec9-112">선언 해야 `WithEvents` 을 받을 수 있도록 개체 변수를 변수 클래스 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-112">You must declare `WithEvents` variables to be object variables so that they can accept class instances.</span></span> <span data-ttu-id="f1ec9-113">그러나로 선언할 수 없습니다 `Object`합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-113">However, you cannot declare them as `Object`.</span></span> <span data-ttu-id="f1ec9-114">이벤트를 발생 시킬 수 있는 특정 클래스로 선언 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ec9-114">You must declare them as the specific class that can raise the events.</span></span>  
  
 <span data-ttu-id="f1ec9-115">`WithEvents` 한정자는이 컨텍스트에서 사용할 수 있습니다. [Dim 문](../../../visual-basic/language-reference/statements/dim-statement.md)</span><span class="sxs-lookup"><span data-stu-id="f1ec9-115">The `WithEvents` modifier can be used in this context: [Dim Statement](../../../visual-basic/language-reference/statements/dim-statement.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1ec9-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="f1ec9-116">See also</span></span>
- [<span data-ttu-id="f1ec9-117">Handles</span><span class="sxs-lookup"><span data-stu-id="f1ec9-117">Handles</span></span>](../../../visual-basic/language-reference/statements/handles-clause.md)
- [<span data-ttu-id="f1ec9-118">키워드</span><span class="sxs-lookup"><span data-stu-id="f1ec9-118">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="f1ec9-119">이벤트</span><span class="sxs-lookup"><span data-stu-id="f1ec9-119">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
