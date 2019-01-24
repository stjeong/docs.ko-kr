---
title: DLL 호출 규칙이 잘못되었습니다.
ms.date: 07/20/2015
f1_keywords:
- vbrID49
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
ms.openlocfilehash: 70200b38ea3d1497daa091fa407accabaf3c4eda
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715779"
---
# <a name="bad-dll-calling-convention"></a><span data-ttu-id="a86c6-102">DLL 호출 규칙이 잘못되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-102">Bad DLL calling convention</span></span>
<span data-ttu-id="a86c6-103">인수는 동적 연결 라이브러리 (DLL)에 전달 된 루틴에서 예상 되 정확히 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-103">Arguments passed to a dynamic-link library (DLL) must exactly match those expected by the routine.</span></span> <span data-ttu-id="a86c6-104">호출 규칙 수, 형식 및 인수 순서를 사용 하 여 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-104">Calling conventions deal with number, type, and order of arguments.</span></span> <span data-ttu-id="a86c6-105">프로그램 루틴을 인수 번호 또는 잘못 된 형식이 전달 되는 DLL에서 호출 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-105">Your program may be calling a routine in a DLL that is being passed the wrong type or number of arguments.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a86c6-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="a86c6-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="a86c6-107">모든 인수 형식을 호출 하는 루틴의 선언에 지정 된 인수와 일치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-107">Make sure all argument types agree with those specified in the declaration of the routine that you are calling.</span></span>  
  
2.  <span data-ttu-id="a86c6-108">동일한 호출 하는 루틴의 선언에 지정 된 인수 개수를 전달 하는 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-108">Make sure you are passing the same number of arguments indicated in the declaration of the routine that you are calling.</span></span>  
  
3.  <span data-ttu-id="a86c6-109">DLL 루틴에서 인수 값으로 예상 하는 경우 `ByVal` 루틴의 선언에 해당 인수에 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86c6-109">If the DLL routine expects arguments by value, make sure `ByVal` is specified for those arguments in the declaration for the routine.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a86c6-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="a86c6-110">See also</span></span>
- [<span data-ttu-id="a86c6-111">오류 형식</span><span class="sxs-lookup"><span data-stu-id="a86c6-111">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="a86c6-112">Call 문</span><span class="sxs-lookup"><span data-stu-id="a86c6-112">Call Statement</span></span>](../../../visual-basic/language-reference/statements/call-statement.md)
- [<span data-ttu-id="a86c6-113">Declare 문</span><span class="sxs-lookup"><span data-stu-id="a86c6-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
